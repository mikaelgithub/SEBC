kinit mikaelgithub

hadoop fs -mkdir /mikaelgithub
hadoop fs -mkdir /gffernandez
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar pi 10 10000
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 500000000 /mikaelgithub/teragen

