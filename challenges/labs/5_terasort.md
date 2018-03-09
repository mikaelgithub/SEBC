## Run the terasort program as user jim with the output target /user/jim/tsort
```
[root@mel2 mikael_dauzet]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar \
> terasort \
> /user/jim/tgen \
> /user/jim/tsort
18/03/09 11:28:59 INFO terasort.TeraSort: starting
18/03/09 11:29:00 INFO hdfs.DFSClient: Created token for jim: HDFS_DELEGATION_TOKEN owner=jim@MIKAELGITHUB.PA, renewer=yarn, realUser=, issueDate=1520555340736, maxDate=1521160140736, sequenceNumber=2, masterKeyId=2 on 10.142.0.2:8020
18/03/09 11:29:00 INFO security.TokenCache: Got dt for hdfs://mel1.c.sebc-194321.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.142.0.2:8020, Ident: (token for jim: HDFS_DELEGATION_TOKEN owner=jim@MIKAELGITHUB.PA, renewer=yarn, realUser=, issueDate=1520555340736, maxDate=1521160140736, sequenceNumber=2, masterKeyId=2)
18/03/09 11:29:00 INFO input.FileInputFormat: Total input paths to process : 16
Spent 361ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 366ms
Sampling 10 splits of 112
Making 2 from 100000 sampled records
Computing parititions took 1144ms
Spent 1512ms computing partitions.
18/03/09 11:29:02 INFO client.RMProxy: Connecting to ResourceManager at mel1.c.sebc-194321.internal/10.142.0.2:8032
18/03/09 11:29:02 INFO mapreduce.JobSubmitter: number of splits:112
18/03/09 11:29:02 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1520554644230_0001
18/03/09 11:29:02 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.142.0.2:8020, Ident: (token for jim: HDFS_DELEGATION_TOKEN owner=jim@MIKAELGITHUB.PA, renewer=yarn, realUser=, issueDate=1520555340736, maxDate=1521160140736, sequenceNumber=2, masterKeyId=2)
18/03/09 11:29:04 INFO impl.YarnClientImpl: Submitted application application_1520554644230_0001
18/03/09 11:29:04 INFO mapreduce.Job: The url to track the job: http://mel1.c.sebc-194321.internal:8088/proxy/application_1520554644230_0001/
18/03/09 11:29:04 INFO mapreduce.Job: Running job: job_1520554644230_0001
18/03/09 11:29:17 INFO mapreduce.Job: Job job_1520554644230_0001 running in uber mode : false
18/03/09 11:29:17 INFO mapreduce.Job:  map 0% reduce 0%
18/03/09 11:29:34 INFO mapreduce.Job:  map 1% reduce 0%
18/03/09 11:29:35 INFO mapreduce.Job:  map 2% reduce 0%
18/03/09 11:29:36 INFO mapreduce.Job:  map 3% reduce 0%
18/03/09 11:29:44 INFO mapreduce.Job:  map 4% reduce 0%
18/03/09 11:29:47 INFO mapreduce.Job:  map 5% reduce 0%
18/03/09 11:29:54 INFO mapreduce.Job:  map 6% reduce 0%
18/03/09 11:29:55 INFO mapreduce.Job:  map 7% reduce 0%
18/03/09 11:29:58 INFO mapreduce.Job:  map 8% reduce 0%
18/03/09 11:30:04 INFO mapreduce.Job:  map 9% reduce 0%
18/03/09 11:30:07 INFO mapreduce.Job:  map 10% reduce 0%
18/03/09 11:30:10 INFO mapreduce.Job:  map 11% reduce 0%
18/03/09 11:30:15 INFO mapreduce.Job:  map 12% reduce 0%
18/03/09 11:30:17 INFO mapreduce.Job:  map 13% reduce 0%
18/03/09 11:30:25 INFO mapreduce.Job:  map 14% reduce 0%
18/03/09 11:30:28 INFO mapreduce.Job:  map 15% reduce 0%
18/03/09 11:30:33 INFO mapreduce.Job:  map 16% reduce 0%
18/03/09 11:30:35 INFO mapreduce.Job:  map 17% reduce 0%
18/03/09 11:30:39 INFO mapreduce.Job:  map 18% reduce 0%
18/03/09 11:30:44 INFO mapreduce.Job:  map 19% reduce 0%
18/03/09 11:30:45 INFO mapreduce.Job:  map 20% reduce 0%
18/03/09 11:30:49 INFO mapreduce.Job:  map 21% reduce 0%
18/03/09 11:30:56 INFO mapreduce.Job:  map 22% reduce 0%
18/03/09 11:31:00 INFO mapreduce.Job:  map 23% reduce 0%
18/03/09 11:31:06 INFO mapreduce.Job:  map 24% reduce 0%
18/03/09 11:31:08 INFO mapreduce.Job:  map 25% reduce 0%
18/03/09 11:31:11 INFO mapreduce.Job:  map 26% reduce 0%
18/03/09 11:31:17 INFO mapreduce.Job:  map 27% reduce 0%
18/03/09 11:31:21 INFO mapreduce.Job:  map 28% reduce 0%
18/03/09 11:31:22 INFO mapreduce.Job:  map 29% reduce 0%
18/03/09 11:31:33 INFO mapreduce.Job:  map 31% reduce 0%
18/03/09 11:31:36 INFO mapreduce.Job:  map 32% reduce 0%
18/03/09 11:31:44 INFO mapreduce.Job:  map 33% reduce 0%
18/03/09 11:31:45 INFO mapreduce.Job:  map 34% reduce 0%
18/03/09 11:31:46 INFO mapreduce.Job:  map 35% reduce 0%
18/03/09 11:31:54 INFO mapreduce.Job:  map 36% reduce 0%
18/03/09 11:31:56 INFO mapreduce.Job:  map 37% reduce 0%
18/03/09 11:31:57 INFO mapreduce.Job:  map 38% reduce 0%
18/03/09 11:32:06 INFO mapreduce.Job:  map 39% reduce 0%
18/03/09 11:32:09 INFO mapreduce.Job:  map 40% reduce 0%
18/03/09 11:32:15 INFO mapreduce.Job:  map 41% reduce 0%
18/03/09 11:32:16 INFO mapreduce.Job:  map 42% reduce 0%
18/03/09 11:32:21 INFO mapreduce.Job:  map 43% reduce 0%
18/03/09 11:32:26 INFO mapreduce.Job:  map 45% reduce 0%
18/03/09 11:32:32 INFO mapreduce.Job:  map 46% reduce 0%
18/03/09 11:32:37 INFO mapreduce.Job:  map 47% reduce 0%
18/03/09 11:32:44 INFO mapreduce.Job:  map 48% reduce 0%
18/03/09 11:32:47 INFO mapreduce.Job:  map 50% reduce 0%
18/03/09 11:32:55 INFO mapreduce.Job:  map 51% reduce 0%
18/03/09 11:32:57 INFO mapreduce.Job:  map 53% reduce 0%
18/03/09 11:33:06 INFO mapreduce.Job:  map 54% reduce 0%
18/03/09 11:33:07 INFO mapreduce.Job:  map 55% reduce 0%
18/03/09 11:33:17 INFO mapreduce.Job:  map 58% reduce 0%
18/03/09 11:33:27 INFO mapreduce.Job:  map 60% reduce 0%
18/03/09 11:33:29 INFO mapreduce.Job:  map 61% reduce 0%
18/03/09 11:33:37 INFO mapreduce.Job:  map 63% reduce 0%
18/03/09 11:33:47 INFO mapreduce.Job:  map 65% reduce 0%
18/03/09 11:33:52 INFO mapreduce.Job:  map 66% reduce 0%
18/03/09 11:33:57 INFO mapreduce.Job:  map 68% reduce 0%
18/03/09 11:34:03 INFO mapreduce.Job:  map 69% reduce 0%
18/03/09 11:34:07 INFO mapreduce.Job:  map 70% reduce 0%
18/03/09 11:34:09 INFO mapreduce.Job:  map 71% reduce 0%
18/03/09 11:34:18 INFO mapreduce.Job:  map 72% reduce 0%
18/03/09 11:34:19 INFO mapreduce.Job:  map 73% reduce 0%
18/03/09 11:34:25 INFO mapreduce.Job:  map 74% reduce 0%
18/03/09 11:34:28 INFO mapreduce.Job:  map 75% reduce 0%
18/03/09 11:34:29 INFO mapreduce.Job:  map 76% reduce 0%
18/03/09 11:34:37 INFO mapreduce.Job:  map 77% reduce 0%
18/03/09 11:34:38 INFO mapreduce.Job:  map 78% reduce 0%
18/03/09 11:34:43 INFO mapreduce.Job:  map 79% reduce 0%
18/03/09 11:34:48 INFO mapreduce.Job:  map 80% reduce 0%
18/03/09 11:34:53 INFO mapreduce.Job:  map 81% reduce 0%
18/03/09 11:34:58 INFO mapreduce.Job:  map 82% reduce 0%
18/03/09 11:34:59 INFO mapreduce.Job:  map 83% reduce 0%
18/03/09 11:35:00 INFO mapreduce.Job:  map 84% reduce 0%
18/03/09 11:35:08 INFO mapreduce.Job:  map 85% reduce 0%
18/03/09 11:35:09 INFO mapreduce.Job:  map 86% reduce 0%
18/03/09 11:35:13 INFO mapreduce.Job:  map 86% reduce 3%
18/03/09 11:35:17 INFO mapreduce.Job:  map 86% reduce 4%
18/03/09 11:35:18 INFO mapreduce.Job:  map 87% reduce 4%
18/03/09 11:35:20 INFO mapreduce.Job:  map 88% reduce 6%
18/03/09 11:35:23 INFO mapreduce.Job:  map 88% reduce 7%
18/03/09 11:35:26 INFO mapreduce.Job:  map 88% reduce 8%
18/03/09 11:35:28 INFO mapreduce.Job:  map 89% reduce 8%
18/03/09 11:35:29 INFO mapreduce.Job:  map 89% reduce 10%
18/03/09 11:35:32 INFO mapreduce.Job:  map 89% reduce 11%
18/03/09 11:35:34 INFO mapreduce.Job:  map 90% reduce 11%
18/03/09 11:35:38 INFO mapreduce.Job:  map 91% reduce 14%
18/03/09 11:35:41 INFO mapreduce.Job:  map 92% reduce 15%
18/03/09 11:35:48 INFO mapreduce.Job:  map 93% reduce 15%
18/03/09 11:35:49 INFO mapreduce.Job:  map 94% reduce 15%
18/03/09 11:35:50 INFO mapreduce.Job:  map 94% reduce 16%
18/03/09 11:35:57 INFO mapreduce.Job:  map 95% reduce 16%
18/03/09 11:35:58 INFO mapreduce.Job:  map 96% reduce 16%
18/03/09 11:36:06 INFO mapreduce.Job:  map 97% reduce 16%
18/03/09 11:36:13 INFO mapreduce.Job:  map 98% reduce 16%
18/03/09 11:36:18 INFO mapreduce.Job:  map 99% reduce 16%
18/03/09 11:36:20 INFO mapreduce.Job:  map 99% reduce 17%
18/03/09 11:36:23 INFO mapreduce.Job:  map 100% reduce 17%
18/03/09 11:36:26 INFO mapreduce.Job:  map 100% reduce 33%
18/03/09 11:36:29 INFO mapreduce.Job:  map 100% reduce 34%
18/03/09 11:36:31 INFO mapreduce.Job:  map 100% reduce 36%
18/03/09 11:36:32 INFO mapreduce.Job:  map 100% reduce 37%
18/03/09 11:36:34 INFO mapreduce.Job:  map 100% reduce 39%
18/03/09 11:36:35 INFO mapreduce.Job:  map 100% reduce 40%
18/03/09 11:36:37 INFO mapreduce.Job:  map 100% reduce 42%
18/03/09 11:36:38 INFO mapreduce.Job:  map 100% reduce 43%
18/03/09 11:36:40 INFO mapreduce.Job:  map 100% reduce 44%
18/03/09 11:36:43 INFO mapreduce.Job:  map 100% reduce 46%
18/03/09 11:36:44 INFO mapreduce.Job:  map 100% reduce 47%
18/03/09 11:36:46 INFO mapreduce.Job:  map 100% reduce 49%
18/03/09 11:36:47 INFO mapreduce.Job:  map 100% reduce 50%
18/03/09 11:36:49 INFO mapreduce.Job:  map 100% reduce 51%
18/03/09 11:36:50 INFO mapreduce.Job:  map 100% reduce 52%
18/03/09 11:36:52 INFO mapreduce.Job:  map 100% reduce 53%
18/03/09 11:36:53 INFO mapreduce.Job:  map 100% reduce 54%
18/03/09 11:36:55 INFO mapreduce.Job:  map 100% reduce 56%
18/03/09 11:36:56 INFO mapreduce.Job:  map 100% reduce 57%
18/03/09 11:36:58 INFO mapreduce.Job:  map 100% reduce 58%
18/03/09 11:36:59 INFO mapreduce.Job:  map 100% reduce 60%
18/03/09 11:37:01 INFO mapreduce.Job:  map 100% reduce 61%
18/03/09 11:37:02 INFO mapreduce.Job:  map 100% reduce 62%
18/03/09 11:37:04 INFO mapreduce.Job:  map 100% reduce 79%
18/03/09 11:37:06 INFO mapreduce.Job:  map 100% reduce 80%
18/03/09 11:37:09 INFO mapreduce.Job:  map 100% reduce 81%
18/03/09 11:37:10 INFO mapreduce.Job:  map 100% reduce 82%
18/03/09 11:37:12 INFO mapreduce.Job:  map 100% reduce 83%
18/03/09 11:37:13 INFO mapreduce.Job:  map 100% reduce 84%
18/03/09 11:37:14 INFO mapreduce.Job:  map 100% reduce 85%
18/03/09 11:37:16 INFO mapreduce.Job:  map 100% reduce 86%
18/03/09 11:37:19 INFO mapreduce.Job:  map 100% reduce 87%
18/03/09 11:37:22 INFO mapreduce.Job:  map 100% reduce 88%
18/03/09 11:37:25 INFO mapreduce.Job:  map 100% reduce 89%
18/03/09 11:37:28 INFO mapreduce.Job:  map 100% reduce 90%
18/03/09 11:37:32 INFO mapreduce.Job:  map 100% reduce 91%
18/03/09 11:37:35 INFO mapreduce.Job:  map 100% reduce 92%
18/03/09 11:37:38 INFO mapreduce.Job:  map 100% reduce 93%
18/03/09 11:37:41 INFO mapreduce.Job:  map 100% reduce 94%
18/03/09 11:37:44 INFO mapreduce.Job:  map 100% reduce 95%
18/03/09 11:37:47 INFO mapreduce.Job:  map 100% reduce 96%
18/03/09 11:37:50 INFO mapreduce.Job:  map 100% reduce 97%
18/03/09 11:37:53 INFO mapreduce.Job:  map 100% reduce 98%
18/03/09 11:37:56 INFO mapreduce.Job:  map 100% reduce 99%
18/03/09 11:37:58 INFO mapreduce.Job:  map 100% reduce 100%
18/03/09 11:37:59 INFO mapreduce.Job: Job job_1520554644230_0001 completed successfully
18/03/09 11:38:00 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2924717017
                FILE: Number of bytes written=5790755394
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553614672
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=342
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters 
                Launched map tasks=112
                Launched reduce tasks=2
                Data-local map tasks=110
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=1063582
                Total time spent by all reduces in occupied slots (ms)=230933
                Total time spent by all map tasks (ms)=1063582
                Total time spent by all reduce tasks (ms)=230933
                Total vcore-seconds taken by all map tasks=1063582
                Total vcore-seconds taken by all reduce tasks=230933
                Total megabyte-seconds taken by all map tasks=1089107968
                Total megabyte-seconds taken by all reduce tasks=236475392
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2851741545
                Input split bytes=14672
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2851741545
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =224
                Failed Shuffles=0
                Merged Map outputs=224
                GC time elapsed (ms)=19589
                CPU time spent (ms)=570150
                Physical memory (bytes) snapshot=45382017024
                Virtual memory (bytes) snapshot=172504715264
                Total committed heap usage (bytes)=38465765376
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
18/03/09 11:38:00 INFO terasort.TeraSort: done
```