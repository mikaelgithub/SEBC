## The full teragen command and output
```
[root@mel2 mikael_dauzet]# time sudo -u jim hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar \
> teragen \
> -Ddfs.blocksize=67108864 \
> -Dmapreduce.job.maps=16 \
> -Dmapreduce.map.memory.mb=768 \
> 65536000 \
> /user/jim/tgen
18/03/09 10:47:17 INFO client.RMProxy: Connecting to ResourceManager at mel1.c.sebc-194321.internal/10.142.0.2:8032
18/03/09 10:47:18 INFO terasort.TeraSort: Generating 65536000 using 16
18/03/09 10:47:18 INFO mapreduce.JobSubmitter: number of splits:16
18/03/09 10:47:18 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1520551211781_0006
18/03/09 10:47:19 INFO impl.YarnClientImpl: Submitted application application_1520551211781_0006
18/03/09 10:47:19 INFO mapreduce.Job: The url to track the job: http://mel1.c.sebc-194321.internal:8088/proxy/application_1520551211781_0006/
18/03/09 10:47:19 INFO mapreduce.Job: Running job: job_1520551211781_0006
18/03/09 10:47:28 INFO mapreduce.Job: Job job_1520551211781_0006 running in uber mode : false
18/03/09 10:47:28 INFO mapreduce.Job:  map 0% reduce 0%
18/03/09 10:47:39 INFO mapreduce.Job:  map 3% reduce 0%
18/03/09 10:47:42 INFO mapreduce.Job:  map 12% reduce 0%
18/03/09 10:47:45 INFO mapreduce.Job:  map 17% reduce 0%
18/03/09 10:47:47 INFO mapreduce.Job:  map 19% reduce 0%
18/03/09 10:47:55 INFO mapreduce.Job:  map 22% reduce 0%
18/03/09 10:47:58 INFO mapreduce.Job:  map 26% reduce 0%
18/03/09 10:48:00 INFO mapreduce.Job:  map 29% reduce 0%
18/03/09 10:48:01 INFO mapreduce.Job:  map 33% reduce 0%
18/03/09 10:48:04 INFO mapreduce.Job:  map 36% reduce 0%
18/03/09 10:48:07 INFO mapreduce.Job:  map 38% reduce 0%
18/03/09 10:48:13 INFO mapreduce.Job:  map 40% reduce 0%
18/03/09 10:48:16 INFO mapreduce.Job:  map 42% reduce 0%
18/03/09 10:48:17 INFO mapreduce.Job:  map 45% reduce 0%
18/03/09 10:48:19 INFO mapreduce.Job:  map 47% reduce 0%
18/03/09 10:48:20 INFO mapreduce.Job:  map 51% reduce 0%
18/03/09 10:48:22 INFO mapreduce.Job:  map 53% reduce 0%
18/03/09 10:48:23 INFO mapreduce.Job:  map 54% reduce 0%
18/03/09 10:48:26 INFO mapreduce.Job:  map 56% reduce 0%
18/03/09 10:48:30 INFO mapreduce.Job:  map 60% reduce 0%
18/03/09 10:48:33 INFO mapreduce.Job:  map 62% reduce 0%
18/03/09 10:48:35 INFO mapreduce.Job:  map 66% reduce 0%
18/03/09 10:48:38 INFO mapreduce.Job:  map 68% reduce 0%
18/03/09 10:48:40 INFO mapreduce.Job:  map 69% reduce 0%
18/03/09 10:48:41 INFO mapreduce.Job:  map 72% reduce 0%
18/03/09 10:48:44 INFO mapreduce.Job:  map 74% reduce 0%
18/03/09 10:48:46 INFO mapreduce.Job:  map 78% reduce 0%
18/03/09 10:48:49 INFO mapreduce.Job:  map 80% reduce 0%
18/03/09 10:48:51 INFO mapreduce.Job:  map 81% reduce 0%
18/03/09 10:48:53 INFO mapreduce.Job:  map 84% reduce 0%
18/03/09 10:48:56 INFO mapreduce.Job:  map 86% reduce 0%
18/03/09 10:48:59 INFO mapreduce.Job:  map 88% reduce 0%
18/03/09 10:49:00 INFO mapreduce.Job:  map 90% reduce 0%
18/03/09 10:49:03 INFO mapreduce.Job:  map 94% reduce 0%
18/03/09 10:49:04 INFO mapreduce.Job:  map 96% reduce 0%
18/03/09 10:49:05 INFO mapreduce.Job:  map 99% reduce 0%
18/03/09 10:49:00 INFO mapreduce.Job:  map 90% reduce 0%
18/03/09 10:49:06 INFO mapreduce.Job:  map 100% reduce 0%
18/03/09 10:49:07 INFO mapreduce.Job: Job job_1520551211781_0006 completed successfully
18/03/09 10:49:07 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1971958
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1368
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=64
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=32
        Job Counters 
                Launched map tasks=16
                Other local map tasks=16
                Total time spent by all maps in occupied slots (ms)=263721
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=263721
                Total vcore-seconds taken by all map tasks=263721
                Total megabyte-seconds taken by all map tasks=270050304
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1368
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=7983
                CPU time spent (ms)=128430
                Physical memory (bytes) snapshot=3406233600
                Virtual memory (bytes) snapshot=21068115968
                Total committed heap usage (bytes)=2144600064
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=6553600000
real    1m52.332s
user    0m6.442s
sys     0m0.343s

```

## The result of the time command
```
real    1m52.332s
user    0m6.442s
sys     0m0.343s
```

## The command and output of hdfs dfs -ls /user/jim/tgen
```
[root@mel2 mikael_dauzet]# hdfs dfs -ls /user/jim/tgen
Found 17 items
-rw-r--r--   3 jim hadoop          0 2018-03-09 10:49 /user/jim/tgen/_SUCCESS
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:47 /user/jim/tgen/part-m-00000
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:47 /user/jim/tgen/part-m-00001
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:47 /user/jim/tgen/part-m-00002
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00003
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00004
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00005
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00006
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00007
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00008
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00009
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00010
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00011
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00012
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:48 /user/jim/tgen/part-m-00013
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:49 /user/jim/tgen/part-m-00014
-rw-r--r--   3 jim hadoop  409600000 2018-03-09 10:49 /user/jim/tgen/part-m-00015
```

## The command and output of hadoop fsck -blocks /user/jim
```
[root@mel2 mikael_dauzet]# sudo -u jim hadoop fsck -blocks /user/jim
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.
Connecting to namenode via http://mel1.c.sebc-194321.internal:50070
FSCK started by jim (auth:SIMPLE) from /10.142.0.3 for path /user/jim at Fri Mar 09 10:51:48 EST 2018
.................Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    3
 Total files:   17
 Total symlinks:                0
 Total blocks (validated):      112 (avg. block size 58514285 B)
 Minimally replicated blocks:   112 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri Mar 09 10:51:48 EST 2018 in 6 milliseconds
The filesystem under path '/user/jim' is HEALTHY
```
