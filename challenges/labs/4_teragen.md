time hadoop  jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Dmapred.map.tasks=8 -Ddfs.block.size=16000000  65536000 /user/neymar/tgen640



real    1m21.784s
user    0m6.006s
sys     0m0.815s




[neymar@ip-172-31-29-188 ~]$ hdfs dfs -ls /user/neymar/tgen640
Found 9 items
-rw-r--r--   3 neymar neymar          0 2017-03-10 09:38 /user/neymar/tgen640/_SUCCESS
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:38 /user/neymar/tgen640/part-m-00000
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:38 /user/neymar/tgen640/part-m-00001
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:37 /user/neymar/tgen640/part-m-00002
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:37 /user/neymar/tgen640/part-m-00003
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:37 /user/neymar/tgen640/part-m-00004
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:37 /user/neymar/tgen640/part-m-00005
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:37 /user/neymar/tgen640/part-m-00006
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:38 /user/neymar/tgen640/part-m-00007





[neymar@ip-172-31-29-188 ~]$ hdfs fsck /user/neymar/tgen640 -blocks
Connecting to namenode via http://ip-172-31-30-102.eu-west-1.compute.internal:50070
FSCK started by neymar (auth:SIMPLE) from /172.31.29.188 for path /user/neymar/tgen640 at Fri Mar 10 09:41:38 UTC 2017
.........Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    1
 Total files:   9
 Total symlinks:                0
 Total blocks (validated):      416 (avg. block size 15753846 B)
 Minimally replicated blocks:   416 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri Mar 10 09:41:38 UTC 2017 in 24 milliseconds


The filesystem under path '/user/neymar/tgen640' is HEALTHY
