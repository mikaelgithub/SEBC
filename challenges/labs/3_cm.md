## The command and output for hdfs dfs -ls /user
```
[root@mel2 mikael_dauzet]# sudo -u hdfs hdfs dfs -ls /user
Found 7 items
drwxrwxrwx   - mapred  hadoop          0 2018-03-09 10:20 /user/history
drwxrwxr-t   - hive    hive            0 2018-03-09 10:20 /user/hive
drwxrwxr-x   - hue     hue             0 2018-03-09 10:21 /user/hue
drwxrwxr-x   - impala  impala          0 2018-03-09 10:21 /user/impala
drwxr-xr-x   - jemaine hadoop          0 2018-03-09 10:23 /user/jemaine
drwxr-xr-x   - jim     hadoop          0 2018-03-09 10:23 /user/jim
drwxrwxr-x   - oozie   oozie           0 2018-03-09 10:21 /user/oozie
```

## The command and output from the CM API call ../api/v14/hosts
```
http://35.196.120.94:7180/api/v14/hosts
```
```
{
  "items" : [ {
    "hostId" : "79c9ee4c-347c-4fa7-bdbc-316138039276",
    "ipAddress" : "10.142.0.2",
    "hostname" : "mel1.c.sebc-194321.internal",
    "rackId" : "/default",
    "hostUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/hostRedirect/79c9ee4c-347c-4fa7-bdbc-316138039276",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 2,
    "numPhysicalCores" : 1,
    "totalPhysMemBytes" : 8202735616
  }, {
    "hostId" : "9d79466c-a8b6-4be2-a73f-b382f277ce40",
    "ipAddress" : "10.142.0.3",
    "hostname" : "mel2.c.sebc-194321.internal",
    "rackId" : "/default",
    "hostUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/hostRedirect/9d79466c-a8b6-4be2-a73f-b382f277ce40",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 2,
    "numPhysicalCores" : 1,
    "totalPhysMemBytes" : 8202735616
  }, {
    "hostId" : "25f9180c-ee15-418b-9d1b-885d957a9c21",
    "ipAddress" : "10.142.0.4",
    "hostname" : "mel3.c.sebc-194321.internal",
    "rackId" : "/default",
    "hostUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/hostRedirect/25f9180c-ee15-418b-9d1b-885d957a9c21",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 1,
    "numPhysicalCores" : 1,
    "totalPhysMemBytes" : 3975020544
  }, {
    "hostId" : "ac5b79b2-d911-46c0-a08d-e54b34666a44",
    "ipAddress" : "10.142.0.5",
    "hostname" : "mel4.c.sebc-194321.internal",
    "rackId" : "/default",
    "hostUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/hostRedirect/ac5b79b2-d911-46c0-a08d-e54b34666a44",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 1,
    "numPhysicalCores" : 1,
    "totalPhysMemBytes" : 3975020544
  }, {
    "hostId" : "e9f1bebc-e242-4535-a7f0-4537c8b5c2f3",
    "ipAddress" : "10.142.0.6",
    "hostname" : "mel5.c.sebc-194321.internal",
    "rackId" : "/default",
    "hostUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/hostRedirect/e9f1bebc-e242-4535-a7f0-4537c8b5c2f3",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 1,
    "numPhysicalCores" : 1,
    "totalPhysMemBytes" : 3975020544
  } ]
}
```

## The command and output from the CM API call ../api/v8/clusters/<githubName>/services
```
http://35.196.120.94:7180/api/v8/clusters/MIKAELGITHUB/services
```
```
{
  "items" : [ {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "impala",
    "type" : "IMPALA",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/serviceRedirect/impala",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "IMPALA_ASSIGNMENT_LOCALITY",
      "summary" : "DISABLED"
    }, {
      "name" : "IMPALA_CATALOGSERVER_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_IMPALADS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_STATESTORE_HEALTH",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Impala"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://mel2.c.sebc-194321.internal:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  } ]
}
```