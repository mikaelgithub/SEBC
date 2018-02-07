```
kinit mikaelgithub

hadoop fs -mkdir /mikaelgithub
hadoop fs -mkdir /gffernandez
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar pi 10 10000
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 50000000 /mikaelgithub/teragen
```
Update proxy and peer principal

add the following properties to the HDFS service Cluster-wide Advanced Configuration Snippet (Safety Valve) for core-site.xml property on the source cluster:
```
<property>
    <name>hadoop.proxyuser.gffernandez.groups</name>
    <value>*</value>
</property>
<property>
    <name>hadoop.proxyuser.gffernandez.hosts</name>
    <value>*</value>
</property>
```
Add peer in CM - Backup
```
http://54.191.132.13:7180 admin / cloudera
```


