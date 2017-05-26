#HDFS
```
[ec2-user@ip-172-31-11-187 yum.repos.d]$ hdfs dfs -ls /user
Found 7 items
drwxr-xr-x   - hdfs         supergroup            0 2017-05-04 21:44 /user/hdfs
drwxrwxrwx   - mapred       hadoop                0 2017-05-04 21:40 /user/history
drwxrwxr-t   - hive         hive                  0 2017-05-04 21:41 /user/hive
drwxrwxr-x   - hue          hue                   0 2017-05-04 21:41 /user/hue
drwxrwxr-x   - impala       impala                0 2017-05-04 21:41 /user/impala
drwxr-xr-x   - mikaelgithub mikaelgithub          0 2017-05-04 21:44 /user/mikaelgithub
drwxrwxr-x   - oozie        oozie                 0 2017-05-04 21:41 /user/oozie
```
## API Version
```
http://52.62.49.204:7180/api/version
v16
```
## Hosts
http://52.62.49.204:7180/api/v16/hosts
```
{
  "items" : [ {
    "hostId" : "99566c29-85c7-42a8-85c6-60bb93eda794",
    "ipAddress" : "172.31.1.105",
    "hostname" : "ip-172-31-1-105.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/hostRedirect/99566c29-85c7-42a8-85c6-60bb93eda794",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  }, {
    "hostId" : "b19b5d6f-becf-4c41-a967-a075d99fc816",
    "ipAddress" : "172.31.11.187",
    "hostname" : "ip-172-31-11-187.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/hostRedirect/b19b5d6f-becf-4c41-a967-a075d99fc816",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  }, {
    "hostId" : "4c094802-5ad2-43d1-8854-a7c5b498850a",
    "ipAddress" : "172.31.11.234",
    "hostname" : "ip-172-31-11-234.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/hostRedirect/4c094802-5ad2-43d1-8854-a7c5b498850a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  }, {
    "hostId" : "7a41fd82-38c7-473b-adaa-ea496e93f66d",
    "ipAddress" : "172.31.13.85",
    "hostname" : "ip-172-31-13-85.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/hostRedirect/7a41fd82-38c7-473b-adaa-ea496e93f66d",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  }, {
    "hostId" : "052fb716-f5a4-45d7-b851-6baaa16ce98f",
    "ipAddress" : "172.31.2.22",
    "hostname" : "ip-172-31-2-22.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/hostRedirect/052fb716-f5a4-45d7-b851-6baaa16ce98f",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  } ]
}
```
```
http://52.62.49.204:7180/api/v16/clusters/mikaelgithub/services
```
```
{
  "items" : [ {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hive",
    "roleInstancesUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hive/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "roleInstancesUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/zookeeper/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hue",
    "roleInstancesUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hue/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/oozie",
    "roleInstancesUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/oozie/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "impala",
    "type" : "IMPALA",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/impala",
    "roleInstancesUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/impala/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "IMPALA_ASSIGNMENT_LOCALITY",
      "summary" : "DISABLED",
      "suppressed" : false
    }, {
      "name" : "IMPALA_CATALOGSERVER_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "IMPALA_IMPALADS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "IMPALA_STATESTORE_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Impala",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/yarn",
    "roleInstancesUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/yarn/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "roleInstancesUrl" : "http://ip-172-31-11-187.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hdfs/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS",
    "entityStatus" : "GOOD_HEALTH"
  } ]
}
```
