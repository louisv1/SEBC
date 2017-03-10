[root@ip-172-31-30-238 ~]# su - ronaldo
[ronaldo@ip-172-31-30-238 ~]$ kinit ronaldo
Password for ronaldo@LOUISV1.ES:
[ronaldo@ip-172-31-30-238 ~]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 10 100
Number of Maps  = 10
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
17/03/10 10:15:45 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-29-188.eu-west-1.compute.internal/172.31.29.188:8032
17/03/10 10:15:46 INFO hdfs.DFSClient: Created token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@LOUISV1.ES, renewer=yarn, realUser=, issueDate=1489140945765, maxDate=1489745745765, sequenceNumber=3, masterKeyId=2 on 172.31.30.102:8020
17/03/10 10:15:46 INFO security.TokenCache: Got dt for hdfs://ip-172-31-30-102.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.30.102:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@LOUISV1.ES, renewer=yarn, realUser=, issueDate=1489140945765, maxDate=1489745745765, sequenceNumber=3, masterKeyId=2)
17/03/10 10:15:46 INFO input.FileInputFormat: Total input paths to process : 10
17/03/10 10:15:46 INFO mapreduce.JobSubmitter: number of splits:10
17/03/10 10:15:46 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489140343635_0003
17/03/10 10:15:46 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.30.102:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@LOUISV1.ES, renewer=yarn, realUser=, issueDate=1489140945765, maxDate=1489745745765, sequenceNumber=3, masterKeyId=2)
17/03/10 10:15:47 INFO impl.YarnClientImpl: Submitted application application_1489140343635_0003
17/03/10 10:15:47 INFO mapreduce.Job: The url to track the job: http://ip-172-31-29-188.eu-west-1.compute.internal:8088/proxy/application_1489140343635_0003/
17/03/10 10:15:47 INFO mapreduce.Job: Running job: job_1489140343635_0003
17/03/10 10:16:00 INFO mapreduce.Job: Job job_1489140343635_0003 running in uber mode : false
17/03/10 10:16:00 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 10:16:12 INFO mapreduce.Job:  map 10% reduce 0%
17/03/10 10:16:15 INFO mapreduce.Job:  map 20% reduce 0%
17/03/10 10:16:17 INFO mapreduce.Job:  map 30% reduce 0%
17/03/10 10:16:18 INFO mapreduce.Job:  map 40% reduce 0%
17/03/10 10:16:19 INFO mapreduce.Job:  map 70% reduce 0%
17/03/10 10:16:25 INFO mapreduce.Job:  map 80% reduce 0%
17/03/10 10:16:28 INFO mapreduce.Job:  map 100% reduce 0%
17/03/10 10:16:35 INFO mapreduce.Job:  map 100% reduce 100%
17/03/10 10:16:35 INFO mapreduce.Job: Job job_1489140343635_0003 completed successfully
17/03/10 10:16:35 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=98
                FILE: Number of bytes written=1368431
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=2990
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=10
                Total time spent by all maps in occupied slots (ms)=87499
                Total time spent by all reduces in occupied slots (ms)=7430
                Total time spent by all map tasks (ms)=87499
                Total time spent by all reduce tasks (ms)=7430
                Total vcore-seconds taken by all map tasks=87499
                Total vcore-seconds taken by all reduce tasks=7430
                Total megabyte-seconds taken by all map tasks=89598976
                Total megabyte-seconds taken by all reduce tasks=7608320
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=340
                Input split bytes=1810
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=340
                Reduce input records=20
                Reduce output records=0
                Spilled Records=40
                Shuffled Maps =10
                Failed Shuffles=0
                Merged Map outputs=10
                GC time elapsed (ms)=452
                CPU time spent (ms)=9990
                Physical memory (bytes) snapshot=4724125696
                Virtual memory (bytes) snapshot=17198653440
                Total committed heap usage (bytes)=5471993856
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1180
        File Output Format Counters
                Bytes Written=97
Job Finished in 49.616 seconds
Estimated value of Pi is 3.14800000000000000000
