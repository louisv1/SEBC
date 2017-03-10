[root@ip-172-31-29-188 ~]# su - neymar
[neymar@ip-172-31-29-188 ~]$ kinit neymar
Password for neymar@LOUISV1.ES:
[neymar@ip-172-31-29-188 ~]$ hadoop  jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort -Dmapreduce.job.maps=12 -Dmapreduce.job.reduces=2 -Dmapreduce.map.memory.mb=819 /user/neymar/tgen640  /user/neymar/tsort640m >tera_sort.out
17/03/10 10:32:06 INFO terasort.TeraSort: starting
17/03/10 10:32:08 INFO hdfs.DFSClient: Created token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@LOUISV1.ES, renewer=yarn, realUser=, issueDate=1489141928453, maxDate=1489746728453, sequenceNumber=5, masterKeyId=2 on 172.31.30.102:8020
17/03/10 10:32:08 INFO security.TokenCache: Got dt for hdfs://ip-172-31-30-102.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.30.102:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@LOUISV1.ES, renewer=yarn, realUser=, issueDate=1489141928453, maxDate=1489746728453, sequenceNumber=5, masterKeyId=2)
17/03/10 10:32:08 INFO input.FileInputFormat: Total input paths to process : 8
17/03/10 10:32:09 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-29-188.eu-west-1.compute.internal/172.31.29.188:8032
17/03/10 10:32:10 INFO mapreduce.JobSubmitter: number of splits:416
17/03/10 10:32:10 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489140343635_0005
17/03/10 10:32:10 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.30.102:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@LOUISV1.ES, renewer=yarn, realUser=, issueDate=1489141928453, maxDate=1489746728453, sequenceNumber=5, masterKeyId=2)
17/03/10 10:32:10 INFO impl.YarnClientImpl: Submitted application application_1489140343635_0005
17/03/10 10:32:10 INFO mapreduce.Job: The url to track the job: http://ip-172-31-29-188.eu-west-1.compute.internal:8088/proxy/application_1489140343635_0005/
17/03/10 10:32:10 INFO mapreduce.Job: Running job: job_1489140343635_0005
17/03/10 10:32:21 INFO mapreduce.Job: Job job_1489140343635_0005 running in uber mode : false
17/03/10 10:32:21 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 10:32:37 INFO mapreduce.Job:  map 1% reduce 0%
17/03/10 10:32:41 INFO mapreduce.Job:  map 2% reduce 0%
17/03/10 10:32:46 INFO mapreduce.Job:  map 3% reduce 0%
17/03/10 10:32:47 INFO mapreduce.Job:  map 4% reduce 0%
17/03/10 10:32:53 INFO mapreduce.Job:  map 5% reduce 0%
17/03/10 10:32:57 INFO mapreduce.Job:  map 6% reduce 0%
17/03/10 10:33:05 INFO mapreduce.Job:  map 7% reduce 0%
17/03/10 10:33:07 INFO mapreduce.Job:  map 9% reduce 0%
17/03/10 10:33:17 INFO mapreduce.Job:  map 11% reduce 0%
17/03/10 10:33:27 INFO mapreduce.Job:  map 13% reduce 0%
17/03/10 10:33:36 INFO mapreduce.Job:  map 14% reduce 0%
17/03/10 10:33:37 INFO mapreduce.Job:  map 15% reduce 0%
17/03/10 10:33:42 INFO mapreduce.Job:  map 16% reduce 0%
17/03/10 10:33:46 INFO mapreduce.Job:  map 17% reduce 0%
17/03/10 10:33:51 INFO mapreduce.Job:  map 18% reduce 0%
17/03/10 10:33:54 INFO mapreduce.Job:  map 19% reduce 0%
17/03/10 10:33:57 INFO mapreduce.Job:  map 20% reduce 0%
17/03/10 10:34:06 INFO mapreduce.Job:  map 21% reduce 0%
17/03/10 10:34:08 INFO mapreduce.Job:  map 22% reduce 0%
17/03/10 10:34:14 INFO mapreduce.Job:  map 23% reduce 0%
17/03/10 10:34:18 INFO mapreduce.Job:  map 24% reduce 0%
17/03/10 10:34:19 INFO mapreduce.Job:  map 25% reduce 0%
17/03/10 10:34:27 INFO mapreduce.Job:  map 26% reduce 0%
17/03/10 10:34:30 INFO mapreduce.Job:  map 27% reduce 0%
17/03/10 10:34:33 INFO mapreduce.Job:  map 28% reduce 0%
17/03/10 10:34:38 INFO mapreduce.Job:  map 29% reduce 0%
17/03/10 10:34:43 INFO mapreduce.Job:  map 30% reduce 0%
17/03/10 10:34:47 INFO mapreduce.Job:  map 31% reduce 0%
17/03/10 10:34:52 INFO mapreduce.Job:  map 32% reduce 0%
17/03/10 10:34:56 INFO mapreduce.Job:  map 33% reduce 0%
17/03/10 10:35:00 INFO mapreduce.Job:  map 34% reduce 0%
17/03/10 10:35:06 INFO mapreduce.Job:  map 35% reduce 0%
17/03/10 10:35:07 INFO mapreduce.Job:  map 36% reduce 0%
17/03/10 10:35:12 INFO mapreduce.Job:  map 37% reduce 0%
17/03/10 10:35:19 INFO mapreduce.Job:  map 38% reduce 0%
17/03/10 10:35:20 INFO mapreduce.Job:  map 39% reduce 0%
17/03/10 10:35:25 INFO mapreduce.Job:  map 40% reduce 0%
17/03/10 10:35:31 INFO mapreduce.Job:  map 41% reduce 0%
17/03/10 10:35:33 INFO mapreduce.Job:  map 42% reduce 0%
17/03/10 10:35:38 INFO mapreduce.Job:  map 43% reduce 0%
17/03/10 10:35:43 INFO mapreduce.Job:  map 44% reduce 0%
17/03/10 10:35:47 INFO mapreduce.Job:  map 45% reduce 0%
17/03/10 10:35:52 INFO mapreduce.Job:  map 46% reduce 0%
17/03/10 10:35:55 INFO mapreduce.Job:  map 47% reduce 0%
17/03/10 10:35:57 INFO mapreduce.Job:  map 48% reduce 0%
17/03/10 10:36:04 INFO mapreduce.Job:  map 49% reduce 0%
17/03/10 10:36:07 INFO mapreduce.Job:  map 50% reduce 0%
17/03/10 10:36:11 INFO mapreduce.Job:  map 51% reduce 0%
17/03/10 10:36:16 INFO mapreduce.Job:  map 52% reduce 0%
17/03/10 10:36:19 INFO mapreduce.Job:  map 53% reduce 0%
17/03/10 10:36:24 INFO mapreduce.Job:  map 54% reduce 0%
17/03/10 10:36:29 INFO mapreduce.Job:  map 55% reduce 0%
17/03/10 10:36:32 INFO mapreduce.Job:  map 56% reduce 0%
17/03/10 10:36:36 INFO mapreduce.Job:  map 57% reduce 0%
17/03/10 10:36:43 INFO mapreduce.Job:  map 58% reduce 0%
17/03/10 10:36:44 INFO mapreduce.Job:  map 59% reduce 0%
17/03/10 10:36:53 INFO mapreduce.Job:  map 60% reduce 0%
17/03/10 10:36:54 INFO mapreduce.Job:  map 61% reduce 0%
17/03/10 10:36:55 INFO mapreduce.Job:  map 62% reduce 0%
17/03/10 10:37:03 INFO mapreduce.Job:  map 63% reduce 0%
17/03/10 10:37:07 INFO mapreduce.Job:  map 64% reduce 0%
17/03/10 10:37:13 INFO mapreduce.Job:  map 65% reduce 0%
17/03/10 10:37:15 INFO mapreduce.Job:  map 66% reduce 0%
17/03/10 10:37:20 INFO mapreduce.Job:  map 67% reduce 0%
17/03/10 10:37:23 INFO mapreduce.Job:  map 68% reduce 0%
17/03/10 10:37:30 INFO mapreduce.Job:  map 69% reduce 0%
17/03/10 10:37:32 INFO mapreduce.Job:  map 70% reduce 0%
17/03/10 10:37:37 INFO mapreduce.Job:  map 71% reduce 0%
17/03/10 10:37:43 INFO mapreduce.Job:  map 72% reduce 0%
17/03/10 10:37:44 INFO mapreduce.Job:  map 73% reduce 0%
17/03/10 10:37:51 INFO mapreduce.Job:  map 74% reduce 0%
17/03/10 10:37:55 INFO mapreduce.Job:  map 75% reduce 0%
17/03/10 10:37:58 INFO mapreduce.Job:  map 76% reduce 0%
17/03/10 10:38:04 INFO mapreduce.Job:  map 77% reduce 0%
17/03/10 10:38:08 INFO mapreduce.Job:  map 78% reduce 0%
17/03/10 10:38:14 INFO mapreduce.Job:  map 79% reduce 0%
17/03/10 10:38:16 INFO mapreduce.Job:  map 80% reduce 0%
17/03/10 10:38:20 INFO mapreduce.Job:  map 81% reduce 0%
17/03/10 10:38:24 INFO mapreduce.Job:  map 82% reduce 0%
17/03/10 10:38:32 INFO mapreduce.Job:  map 83% reduce 0%
17/03/10 10:38:34 INFO mapreduce.Job:  map 84% reduce 0%
17/03/10 10:38:36 INFO mapreduce.Job:  map 84% reduce 5%
17/03/10 10:38:42 INFO mapreduce.Job:  map 84% reduce 9%
17/03/10 10:38:43 INFO mapreduce.Job:  map 85% reduce 9%
17/03/10 10:38:44 INFO mapreduce.Job:  map 86% reduce 9%
17/03/10 10:38:48 INFO mapreduce.Job:  map 86% reduce 12%
17/03/10 10:38:52 INFO mapreduce.Job:  map 87% reduce 12%
17/03/10 10:38:54 INFO mapreduce.Job:  map 88% reduce 16%
17/03/10 10:39:00 INFO mapreduce.Job:  map 88% reduce 19%
17/03/10 10:39:04 INFO mapreduce.Job:  map 89% reduce 19%
17/03/10 10:39:06 INFO mapreduce.Job:  map 90% reduce 21%
17/03/10 10:39:07 INFO mapreduce.Job:  map 90% reduce 22%
17/03/10 10:39:12 INFO mapreduce.Job:  map 90% reduce 24%
17/03/10 10:39:13 INFO mapreduce.Job:  map 91% reduce 26%
17/03/10 10:39:17 INFO mapreduce.Job:  map 92% reduce 26%
17/03/10 10:39:18 INFO mapreduce.Job:  map 92% reduce 27%
17/03/10 10:39:19 INFO mapreduce.Job:  map 92% reduce 29%
17/03/10 10:39:22 INFO mapreduce.Job:  map 93% reduce 29%
17/03/10 10:39:24 INFO mapreduce.Job:  map 93% reduce 30%
17/03/10 10:39:25 INFO mapreduce.Job:  map 93% reduce 31%
17/03/10 10:39:26 INFO mapreduce.Job:  map 94% reduce 31%
17/03/10 10:39:34 INFO mapreduce.Job:  map 95% reduce 31%
17/03/10 10:39:35 INFO mapreduce.Job:  map 96% reduce 31%
17/03/10 10:39:36 INFO mapreduce.Job:  map 96% reduce 32%
17/03/10 10:39:43 INFO mapreduce.Job:  map 97% reduce 32%
17/03/10 10:39:44 INFO mapreduce.Job:  map 98% reduce 32%
17/03/10 10:39:46 INFO mapreduce.Job:  map 98% reduce 33%
17/03/10 10:39:50 INFO mapreduce.Job:  map 99% reduce 33%
17/03/10 10:39:53 INFO mapreduce.Job:  map 100% reduce 33%
17/03/10 10:39:57 INFO mapreduce.Job:  map 100% reduce 50%
17/03/10 10:39:58 INFO mapreduce.Job:  map 100% reduce 67%
17/03/10 10:40:00 INFO mapreduce.Job:  map 100% reduce 68%
17/03/10 10:40:03 INFO mapreduce.Job:  map 100% reduce 69%
17/03/10 10:40:04 INFO mapreduce.Job:  map 100% reduce 70%
17/03/10 10:40:07 INFO mapreduce.Job:  map 100% reduce 72%
17/03/10 10:40:10 INFO mapreduce.Job:  map 100% reduce 74%
17/03/10 10:40:13 INFO mapreduce.Job:  map 100% reduce 76%
17/03/10 10:40:16 INFO mapreduce.Job:  map 100% reduce 77%
17/03/10 10:40:19 INFO mapreduce.Job:  map 100% reduce 79%
17/03/10 10:40:22 INFO mapreduce.Job:  map 100% reduce 82%
17/03/10 10:40:25 INFO mapreduce.Job:  map 100% reduce 84%
17/03/10 10:40:28 INFO mapreduce.Job:  map 100% reduce 86%
17/03/10 10:40:31 INFO mapreduce.Job:  map 100% reduce 88%
17/03/10 10:40:34 INFO mapreduce.Job:  map 100% reduce 90%
17/03/10 10:40:37 INFO mapreduce.Job:  map 100% reduce 92%
17/03/10 10:40:40 INFO mapreduce.Job:  map 100% reduce 94%
17/03/10 10:40:43 INFO mapreduce.Job:  map 100% reduce 96%
17/03/10 10:40:46 INFO mapreduce.Job:  map 100% reduce 98%
17/03/10 10:40:49 INFO mapreduce.Job:  map 100% reduce 100%
17/03/10 10:40:51 INFO mapreduce.Job: Job job_1489140343635_0005 completed successfully
17/03/10 10:40:51 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2945334091
                FILE: Number of bytes written=5861676000
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553663648
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=1254
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=416
                Launched reduce tasks=2
                Data-local map tasks=414
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=3853903
                Total time spent by all reduces in occupied slots (ms)=297449
                Total time spent by all map tasks (ms)=3853903
                Total time spent by all reduce tasks (ms)=297449
                Total vcore-seconds taken by all map tasks=3853903
                Total vcore-seconds taken by all reduce tasks=297449
                Total megabyte-seconds taken by all map tasks=3946396672
                Total megabyte-seconds taken by all reduce tasks=304587776
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2864044507
                Input split bytes=63648
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2864044507
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =832
                Failed Shuffles=0
                Merged Map outputs=832
                GC time elapsed (ms)=42183
                CPU time spent (ms)=1552740
                Physical memory (bytes) snapshot=196382371840
                Virtual memory (bytes) snapshot=581883449344
                Total committed heap usage (bytes)=236456509440
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
17/03/10 10:40:51 INFO terasort.TeraSort: done
