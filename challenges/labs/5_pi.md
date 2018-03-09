## Run the Hadoop pi program as user jemaine
```
[root@mel2 mikael_dauzet]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar \
> pi 50 100
Number of Maps  = 50
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
Wrote input for Map #10
Wrote input for Map #11
Wrote input for Map #12
Wrote input for Map #13
Wrote input for Map #14
Wrote input for Map #15
Wrote input for Map #16
Wrote input for Map #17
Wrote input for Map #18
Wrote input for Map #19
Wrote input for Map #20
Wrote input for Map #26
Wrote input for Map #21
Wrote input for Map #22
Wrote input for Map #23
Wrote input for Map #24
Wrote input for Map #25
Wrote input for Map #26
Wrote input for Map #27
Wrote input for Map #28
Wrote input for Map #29
Wrote input for Map #30
Wrote input for Map #31
Wrote input for Map #32
Wrote input for Map #33
Wrote input for Map #34
Wrote input for Map #35
Wrote input for Map #36
Wrote input for Map #37
Wrote input for Map #38
Wrote input for Map #39
Wrote input for Map #40
Wrote input for Map #41
Wrote input for Map #42
Wrote input for Map #43
Wrote input for Map #44
Wrote input for Map #45
Wrote input for Map #46
Wrote input for Map #47
Wrote input for Map #48
Wrote input for Map #49
Starting Job
18/03/09 11:38:51 INFO client.RMProxy: Connecting to ResourceManager at mel1.c.sebc-194321.internal/10.142.0.2:8032
18/03/09 11:38:52 INFO hdfs.DFSClient: Created token for jemaine: HDFS_DELEGATION_TOKEN owner=jemaine@MIKAELGITHUB.PA, renewer=yarn, realUser=, issueDate=1520555932218, maxDate=1521160732218, sequenceNumber=3, masterKeyId=2 on 10.142.0.2:8020
18/03/09 11:38:52 INFO security.TokenCache: Got dt for hdfs://mel1.c.sebc-194321.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.142.0.2:8020, Ident: (token for jemaine: HDFS_DELEGATION_TOKEN owner=jemaine@MIKAELGITHUB.PA, renewer=yarn, realUser=, issueDate=1520555932218, maxDate=1521160732218, sequenceNumber=3, masterKeyId=2)
18/03/09 11:38:52 INFO input.FileInputFormat: Total input paths to process : 50
18/03/09 11:38:52 INFO mapreduce.JobSubmitter: number of splits:50
18/03/09 11:38:52 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1520554644230_0002
18/03/09 11:38:52 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.142.0.2:8020, Ident: (token for jemaine: HDFS_DELEGATION_TOKEN owner=jemaine@MIKAELGITHUB.PA, renewer=yarn, realUser=, issueDate=1520555932218, maxDate=1521160732218, sequenceNumber=3, masterKeyId=2)
18/03/09 11:38:53 INFO impl.YarnClientImpl: Submitted application application_1520554644230_0002
18/03/09 11:38:53 INFO mapreduce.Job: The url to track the job: http://mel1.c.sebc-194321.internal:8088/proxy/application_1520554644230_0002/
18/03/09 11:38:53 INFO mapreduce.Job: Running job: job_1520554644230_0002
18/03/09 11:39:06 INFO mapreduce.Job: Job job_1520554644230_0002 running in uber mode : false
18/03/09 11:39:06 INFO mapreduce.Job:  map 0% reduce 0%
18/03/09 11:39:14 INFO mapreduce.Job:  map 2% reduce 0%
18/03/09 11:39:20 INFO mapreduce.Job:  map 4% reduce 0%
18/03/09 11:39:22 INFO mapreduce.Job:  map 6% reduce 0%
18/03/09 11:39:23 INFO mapreduce.Job:  map 8% reduce 0%
18/03/09 11:39:25 INFO mapreduce.Job:  map 10% reduce 0%
18/03/09 11:39:29 INFO mapreduce.Job:  map 12% reduce 0%
18/03/09 11:39:30 INFO mapreduce.Job:  map 14% reduce 0%
18/03/09 11:39:32 INFO mapreduce.Job:  map 16% reduce 0%
18/03/09 11:39:35 INFO mapreduce.Job:  map 18% reduce 0%
18/03/09 11:39:37 INFO mapreduce.Job:  map 22% reduce 0%
18/03/09 11:39:42 INFO mapreduce.Job:  map 26% reduce 0%
18/03/09 11:39:44 INFO mapreduce.Job:  map 28% reduce 0%
18/03/09 11:39:47 INFO mapreduce.Job:  map 30% reduce 0%
18/03/09 11:39:49 INFO mapreduce.Job:  map 32% reduce 0%
18/03/09 11:39:51 INFO mapreduce.Job:  map 34% reduce 0%
18/03/09 11:39:52 INFO mapreduce.Job:  map 36% reduce 0%
18/03/09 11:39:56 INFO mapreduce.Job:  map 38% reduce 0%
18/03/09 11:39:57 INFO mapreduce.Job:  map 40% reduce 0%
18/03/09 11:39:59 INFO mapreduce.Job:  map 42% reduce 0%
18/03/09 11:40:02 INFO mapreduce.Job:  map 44% reduce 0%
18/03/09 11:40:03 INFO mapreduce.Job:  map 46% reduce 0%
18/03/09 11:40:07 INFO mapreduce.Job:  map 50% reduce 0%
18/03/09 11:40:11 INFO mapreduce.Job:  map 52% reduce 0%
18/03/09 11:40:13 INFO mapreduce.Job:  map 54% reduce 0%
18/03/09 11:40:14 INFO mapreduce.Job:  map 56% reduce 0%
18/03/09 11:40:17 INFO mapreduce.Job:  map 58% reduce 0%
18/03/09 11:40:18 INFO mapreduce.Job:  map 60% reduce 0%
18/03/09 11:40:21 INFO mapreduce.Job:  map 62% reduce 0%
18/03/09 11:40:22 INFO mapreduce.Job:  map 64% reduce 0%
18/03/09 11:40:25 INFO mapreduce.Job:  map 66% reduce 0%
18/03/09 11:40:27 INFO mapreduce.Job:  map 68% reduce 0%
18/03/09 11:40:29 INFO mapreduce.Job:  map 70% reduce 0%
18/03/09 11:40:31 INFO mapreduce.Job:  map 72% reduce 0%
18/03/09 11:40:32 INFO mapreduce.Job:  map 74% reduce 0%
18/03/09 11:40:36 INFO mapreduce.Job:  map 76% reduce 0%
18/03/09 11:40:37 INFO mapreduce.Job:  map 78% reduce 0%
18/03/09 11:40:38 INFO mapreduce.Job:  map 80% reduce 0%
18/03/09 11:40:43 INFO mapreduce.Job:  map 84% reduce 0%
18/03/09 11:40:44 INFO mapreduce.Job:  map 86% reduce 0%
18/03/09 11:40:48 INFO mapreduce.Job:  map 88% reduce 0%
18/03/09 11:40:51 INFO mapreduce.Job:  map 90% reduce 0%
18/03/09 11:40:52 INFO mapreduce.Job:  map 92% reduce 0%
18/03/09 11:40:58 INFO mapreduce.Job:  map 94% reduce 0%
18/03/09 11:40:59 INFO mapreduce.Job:  map 96% reduce 31%
18/03/09 11:41:02 INFO mapreduce.Job:  map 96% reduce 32%
18/03/09 11:41:06 INFO mapreduce.Job:  map 100% reduce 32%
18/03/09 11:41:07 INFO mapreduce.Job:  map 100% reduce 100%
18/03/09 11:41:07 INFO mapreduce.Job: Job job_1520554644230_0002 completed successfully
18/03/09 11:41:07 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=261
                FILE: Number of bytes written=6362615
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=14240
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=203
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters 
                Launched map tasks=50
                Launched reduce tasks=1
                Data-local map tasks=49
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=283520
                Total time spent by all reduces in occupied slots (ms)=17389
                Total time spent by all map tasks (ms)=283520
                Total time spent by all reduce tasks (ms)=17389
                Total vcore-seconds taken by all map tasks=283520
                Total vcore-seconds taken by all reduce tasks=17389
                Total megabyte-seconds taken by all map tasks=290324480
                Total megabyte-seconds taken by all reduce tasks=17806336
        Map-Reduce Framework
                Map input records=50
                Map output records=100
                Map output bytes=900
                Map output materialized bytes=1700
                Input split bytes=8340
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=1700
                Reduce input records=100
                Reduce output records=0
                Spilled Records=200
                Shuffled Maps =50
                Failed Shuffles=0
                Merged Map outputs=50
                GC time elapsed (ms)=4674
                CPU time spent (ms)=31240
                Physical memory (bytes) snapshot=20879544320
                Virtual memory (bytes) snapshot=78409453568
                Total committed heap usage (bytes)=19711389696
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters 
                Bytes Read=5900
        File Output Format Counters 
                Bytes Written=97
Job Finished in 135.377 seconds
Estimated value of Pi is 3.14160000000000000000
```