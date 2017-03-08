#!/bin/sh
# Confirm the path values given below correspond to your installation

MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
HADOOP=/opt/cloudera/parcels/CDH/bin

# Mark start of the loop
echo Testing loop started on `date`

# Mapper containers
for i in 20    
do
   # Reducer containers
   for j in 1 #1 
   do                 
      # Container memory
      for k in 512 1024 #1536 
      do                         
        echo "**************Logic START***********************"    
	      # Set mapper JVM heap 
        MAP_MB=`echo "($k*0.8)/1" | bc` 

        # Set reducer JVM heap 
        RED_MB=`echo "($k*0.8)/1" | bc` 
        
        # Size of generated files in 100-byte chuncks
        #declare -SIZE number
        SIZE=`echo "($k*100000)" | bc`
         
        echo "i value : ${i} "
        echo "j value : ${j} " 
        echo "k value : ${k} "
        echo "MAP_MB value : ${MAP_MB} "
        echo "RED_MB value : ${RED_MB} "
        echo "SIZE value : ${SIZE} "
        time ${HADOOP}/hadoop jar ${MR}/hadoop-examples.jar teragen \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     51200000 /results/tg-10GB-${i}-${j}-${k} 1>tera_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err
                     #${SIZE} /results/tg-10GB-${i}-${j}-${k} 1>tera_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err
                    
                                            
        echo "Teragen done"
        time ${HADOOP}/hadoop jar $MR/hadoop-examples.jar terasort \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.job.reduces=$j \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
	                   /results/tg-10GB-${i}-${j}-${k}  \
                     /results/ts-10GB-${i}-${j}-${k} 1>>tera_${i}_${j}_${k}.out 2>>tera_${i}_${j}_${k}.err                         
        echo "Terasort done"
        $HADOOP/hadoop fs -rm -r -skipTrash /results/tg-10GB-${i}-${j}-${k}                         
        $HADOOP/hadoop fs -rm -r -skipTrash /results/ts-10GB-${i}-${j}-${k}     
        #echo values

        echo "**************Logic END***********************"             
      done
   done
done

echo Testing loop ended on `date`
