***When executing from command line it hangs while running, when I look in cloudera manager or yarn resource manager it is still running. 
***looks like client loses connection and hangs 
***below is commands executed, included screenshots from resource manager of jobs that run and time  


executed for teragen
 time hadoop  jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 107374182 /user/louisv1/terasort-input 

took 2mins, 1sec



executed tersasort
 time hadoop  jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/louisv1/terasort-input /user/louisv1/terasort-output

took 7 mins 18 sec