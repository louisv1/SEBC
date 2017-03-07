*tried distcp between aws instance with azure instance. But the distcp gets confused and uses external and internal and fails with conflict.
*if i add internal and external to host file then doesnt resolve name/ip correctly
*this is more a cloud problem and would work easier if both instances on aws, proceeded with distcp local 


***terasort input
yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen 5242880 /louisv1src/terasort-input
17/03/07 11:58:38 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-23-155.eu-west-1.compute.internal/172.31.23.155:8032
17/03/07 11:58:38 INFO terasort.TeraSort: Generating 5242880 using 2
17/03/07 11:58:38 INFO mapreduce.JobSubmitter: number of splits:2
17/03/07 11:58:39 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1488885244338_0004
17/03/07 11:58:39 INFO impl.YarnClientImpl: Submitted application application_1488885244338_0004
17/03/07 11:58:39 INFO mapreduce.Job: The url to track the job: http://ip-172-31-23-155.eu-west-1.compute.internal:8088/proxy/application_1488885244338_0004/
17/03/07 11:58:39 INFO mapreduce.Job: Running job: job_1488885244338_0004
17/03/07 11:58:45 INFO mapreduce.Job: Job job_1488885244338_0004 running in uber mode : false
17/03/07 11:58:45 INFO mapreduce.Job:  map 0% reduce 0%
17/03/07 11:58:55 INFO mapreduce.Job:  map 50% reduce 0%
17/03/07 11:58:56 INFO mapreduce.Job:  map 100% reduce 0%
17/03/07 11:58:56 INFO mapreduce.Job: Job job_1488885244338_0004 completed successfully
17/03/07 11:58:56 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=244230
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=167
                HDFS: Number of bytes written=524288000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=16519
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=16519
                Total vcore-seconds taken by all map tasks=16519
                Total megabyte-seconds taken by all map tasks=16915456
        Map-Reduce Framework
                Map input records=5242880
                Map output records=5242880
                Input split bytes=167
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=199
                CPU time spent (ms)=14140
                Physical memory (bytes) snapshot=739086336
                Virtual memory (bytes) snapshot=3147243520
                Total committed heap usage (bytes)=855638016
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=11257830824958050
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=524288000

				
****copy from one to another using distcp				
hadoop distcp /louisv1src /louisv1trg
17/03/07 12:00:00 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[/louisv1src], targetPath=/louisv1trg, targetPathExists=true, filtersFile='null'}
17/03/07 12:00:01 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-23-155.eu-west-1.compute.internal/172.31.23.155:8032
17/03/07 12:00:01 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 5; dirCnt = 2
17/03/07 12:00:01 INFO tools.SimpleCopyListing: Build file listing completed.
17/03/07 12:00:01 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
17/03/07 12:00:01 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
17/03/07 12:00:01 INFO tools.DistCp: Number of paths in the copy list: 5
17/03/07 12:00:01 INFO tools.DistCp: Number of paths in the copy list: 5
17/03/07 12:00:01 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-23-155.eu-west-1.compute.internal/172.31.23.155:8032
17/03/07 12:00:02 INFO mapreduce.JobSubmitter: number of splits:3
17/03/07 12:00:02 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1488885244338_0005
17/03/07 12:00:02 INFO impl.YarnClientImpl: Submitted application application_1488885244338_0005
17/03/07 12:00:02 INFO mapreduce.Job: The url to track the job: http://ip-172-31-23-155.eu-west-1.compute.internal:8088/proxy/application_1488885244338_0005/
17/03/07 12:00:02 INFO tools.DistCp: DistCp job-id: job_1488885244338_0005
17/03/07 12:00:02 INFO mapreduce.Job: Running job: job_1488885244338_0005
17/03/07 12:00:08 INFO mapreduce.Job: Job job_1488885244338_0005 running in uber mode : false
17/03/07 12:00:08 INFO mapreduce.Job:  map 0% reduce 0%
17/03/07 12:00:14 INFO mapreduce.Job:  map 33% reduce 0%
17/03/07 12:00:19 INFO mapreduce.Job:  map 100% reduce 0%
17/03/07 12:00:19 INFO mapreduce.Job: Job job_1488885244338_0005 completed successfully
17/03/07 12:00:20 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=375036
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=524290147
                HDFS: Number of bytes written=524288000
                HDFS: Number of read operations=59
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=14
        Job Counters
                Launched map tasks=3
                Other local map tasks=3
                Total time spent by all maps in occupied slots (ms)=20849
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=20849
                Total vcore-seconds taken by all map tasks=20849
                Total megabyte-seconds taken by all map tasks=21349376
        Map-Reduce Framework
                Map input records=5
                Map output records=0
                Input split bytes=357
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=190
                CPU time spent (ms)=12230
                Physical memory (bytes) snapshot=677523456
                Virtual memory (bytes) snapshot=4729229312
                Total committed heap usage (bytes)=1080557568
        File Input Format Counters
                Bytes Read=1790
        File Output Format Counters
                Bytes Written=0
        org.apache.hadoop.tools.mapred.CopyMapper$Counter
                BYTESCOPIED=524288000
                BYTESEXPECTED=524288000
                COPY=5

****check that it copied				
[louisv1@ip-172-31-19-137 ~]$ hdfs dfs -ls /louisv1trg
Found 1 items
drwxr-xr-x   - louisv1 louisv1          0 2017-03-07 12:00 /louisv1trg/louisv1src
[louisv1@ip-172-31-19-137 ~]$ hdfs dfs -ls /louisv1trg/louisv1src
Found 1 items
drwxr-xr-x   - louisv1 louisv1          0 2017-03-07 12:00 /louisv1trg/louisv1src/terasort-input



****fsck on trg dir
hdfs fsck /louisv1trg/louisv1src -files -blocks
Connecting to namenode via http://ip-172-31-23-155.eu-west-1.compute.internal:50070
FSCK started by louisv1 (auth:SIMPLE) from /172.31.19.137 for path /louisv1trg/louisv1src at Tue Mar 07 12:02:46 UTC 2017
/louisv1trg/louisv1src <dir>
/louisv1trg/louisv1src/terasort-input <dir>
/louisv1trg/louisv1src/terasort-input/_SUCCESS 0 bytes, 0 block(s):  OK

/louisv1trg/louisv1src/terasort-input/part-m-00000 262144000 bytes, 2 block(s):  OK
0. BP-2062838230-172.31.23.155-1488829512439:blk_1073743631_2807 len=134217728 Live_repl=3
1. BP-2062838230-172.31.23.155-1488829512439:blk_1073743634_2810 len=127926272 Live_repl=3

/louisv1trg/louisv1src/terasort-input/part-m-00001 262144000 bytes, 2 block(s):  OK
0. BP-2062838230-172.31.23.155-1488829512439:blk_1073743633_2809 len=134217728 Live_repl=3
1. BP-2062838230-172.31.23.155-1488829512439:blk_1073743635_2811 len=127926272 Live_repl=3

Status: HEALTHY
 Total size:    524288000 B
 Total dirs:    2
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 131072000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Tue Mar 07 12:02:46 UTC 2017 in 2 milliseconds


The filesystem under path '/louisv1trg/louisv1src' is HEALTHY

****fsck on src dir
[louisv1@ip-172-31-19-137 ~]$ hdfs fsck /louisv1src -files -blocks
Connecting to namenode via http://ip-172-31-23-155.eu-west-1.compute.internal:50070
FSCK started by louisv1 (auth:SIMPLE) from /172.31.19.137 for path /louisv1src at Tue Mar 07 12:03:04 UTC 2017
/louisv1src <dir>
/louisv1src/terasort-input <dir>
/louisv1src/terasort-input/_SUCCESS 0 bytes, 0 block(s):  OK

/louisv1src/terasort-input/part-m-00000 262144000 bytes, 2 block(s):  OK
0. BP-2062838230-172.31.23.155-1488829512439:blk_1073743612_2788 len=134217728 Live_repl=3
1. BP-2062838230-172.31.23.155-1488829512439:blk_1073743613_2789 len=127926272 Live_repl=3

/louisv1src/terasort-input/part-m-00001 262144000 bytes, 2 block(s):  OK
0. BP-2062838230-172.31.23.155-1488829512439:blk_1073743611_2787 len=134217728 Live_repl=3
1. BP-2062838230-172.31.23.155-1488829512439:blk_1073743614_2790 len=127926272 Live_repl=3

Status: HEALTHY
 Total size:    524288000 B
 Total dirs:    2
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 131072000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Tue Mar 07 12:03:04 UTC 2017 in 1 milliseconds


The filesystem under path '/louisv1src' is HEALTHY

