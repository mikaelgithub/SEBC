Curl on the end point 
```
curl -u admin:admin 'http://localhost:7180/api/v2/cm/deployment'
```

```
[ec2-user@ip-172-31-2-22 ~]$ curl -u admin:admin 'http://localhost:7180/api/v2/cm/deployment'?pretty
{
  "timestamp" : "2017-05-04T07:01:00.536Z",
  "clusters" : [ {
    "name" : "MIKAELGITHUB",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "3144679424"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "314467942"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "3144679424"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2839648665"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "477"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-2-22.ap-southeast-2.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-18ce19a908ecd6217947092601af37c5",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0ff1740811ea07331"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-4895e05c7522f32189f10cb572d30bdd",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-067848b670dc99225"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-4f7d729b30370ef91c3add7461eed593",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-034e8a5bb7787de42"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-51451df441e9f319ab6de0470ddd9490",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-07fafa8ec0f63a5a3"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-64adb9cd8d76372656c80c445130fcdb",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0531596b61f169ed1"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-51451df441e9f319ab6de0470ddd9490",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-07fafa8ec0f63a5a3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5j4qmxz9g4gnnedth9gu71qoi"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-51451df441e9f319ab6de0470ddd9490",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-07fafa8ec0f63a5a3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "g0294tt5xwaqdenrnop9w13d"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-4f7d729b30370ef91c3add7461eed593",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-034e8a5bb7787de42"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ajrv3kvhbocaxuilm1qqmzorm"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-51451df441e9f319ab6de0470ddd9490",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-07fafa8ec0f63a5a3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a38oqcpknoo65tm531sv9i5ru"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-64adb9cd8d76372656c80c445130fcdb",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0531596b61f169ed1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5k2e7z58iscsw6wpn3fvf89d3"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-2-22.ap-southeast-2.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue_password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-18ce19a908ecd6217947092601af37c5"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-4f7d729b30370ef91c3add7461eed593",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-034e8a5bb7787de42"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4yq8u8xgepozul5g2vk3l3wbf"
          }, {
            "name" : "secret_key",
            "value" : "9hSzM8QdYs4ikRi5N1a4wFU3jTFj75"
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-4f7d729b30370ef91c3add7461eed593",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "i-034e8a5bb7787de42"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2o3z8rwmrd5glpj31c8v50x15"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-2-22.ap-southeast-2.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-4895e05c7522f32189f10cb572d30bdd",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-067848b670dc99225"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "239oda2ei4plz6gg7ovkrokcg"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3186"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3851"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "lF17UTiDSrSNxdYrrXrav1j59k2hP0"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-64adb9cd8d76372656c80c445130fcdb",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-0531596b61f169ed1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9ljw4p2iiexpymjp1sieitiji"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-4895e05c7522f32189f10cb572d30bdd",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-067848b670dc99225"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "erui0dzku7kf8be738jsfpj5f"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-4f7d729b30370ef91c3add7461eed593",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-034e8a5bb7787de42"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7ir6dkd71zj11pmjdk3dmxvro"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-64adb9cd8d76372656c80c445130fcdb",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0531596b61f169ed1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4v9utqztc5n0e2dx0cx3wbh7q"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-64adb9cd8d76372656c80c445130fcdb",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-0531596b61f169ed1"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "79"
          }, {
            "name" : "role_jceks_password",
            "value" : "9a9n62z6xa5il904yahmt497k"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "958398464"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "5367448780"
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "3903848448"
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          } ]
        } ],
        "items" : [ {
          "name" : "core_site_safety_valve",
          "value" : "<property>\n    <name>hadoop.proxyuser.gffernandez.groups</name>\n    <value>*</value>\n</property>\n<property>\n    <name>hadoop.proxyuser.gffernandez.hosts</name>\n    <value>*</value>\n</property>"
        }, {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "7hjv0IzKmji6fVqfm5BfiH3zJaeXLL"
        }, {
          "name" : "dfs_permissions_supergroup",
          "value" : "mikaelgithub"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "Awjg3B3iUIs9HR8UHyNQbtQAV2ALbl"
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos"
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "RCz0MSWGP9SQpCbUynJ2nAna0R9SWt"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-18ce19a908ecd6217947092601af37c5",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-0ff1740811ea07331"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-4895e05c7522f32189f10cb572d30bdd",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-067848b670dc99225"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5h3t9szct61aznl9ips5t4kke"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-4f7d729b30370ef91c3add7461eed593",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-034e8a5bb7787de42"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9ta3uu3tlpfvnbl5i9wgvbgsa"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-64adb9cd8d76372656c80c445130fcdb",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0531596b61f169ed1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4ebx8f2uz95iwr49xsa3ovqdk"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-18ce19a908ecd6217947092601af37c5",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-0ff1740811ea07331"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dcp6r4mamt8laofefoojgzbu0"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-18ce19a908ecd6217947092601af37c5",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0ff1740811ea07331"
        },
        "config" : {
          "items" : [ {
            "name" : "namenode_id",
            "value" : "83"
          }, {
            "name" : "role_jceks_password",
            "value" : "bafxke1pykec1l2z3njshow3f"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-18ce19a908ecd6217947092601af37c5",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "i-0ff1740811ea07331"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1l8a653m94ah6vygttbe95jmy"
          } ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-51451df441e9f319ab6de0470ddd9490",
        "type" : "SECONDARYNAMENODE",
        "hostRef" : {
          "hostId" : "i-07fafa8ec0f63a5a3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "55pu4k1f31z78pw41c8rilgfz"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0ff1740811ea07331",
    "ipAddress" : "172.31.0.29",
    "hostname" : "ip-172-31-0-29.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-07fafa8ec0f63a5a3",
    "ipAddress" : "172.31.11.233",
    "hostname" : "ip-172-31-11-233.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-034e8a5bb7787de42",
    "ipAddress" : "172.31.12.35",
    "hostname" : "ip-172-31-12-35.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-067848b670dc99225",
    "ipAddress" : "172.31.2.22",
    "hostname" : "ip-172-31-2-22.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0531596b61f169ed1",
    "ipAddress" : "172.31.3.38",
    "hostname" : "ip-172-31-3-38.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-18ce19a908ecd6217947092601af37c5",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f57ced6bc007cd7d0ec9076aa1bdc507f9feaf875a9763631b41e82d6e7a8190",
    "pwSalt" : -3972953550512907201,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-18ce19a908ecd6217947092601af37c5",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e2f145fc6d0f3d2613647b5b063bbff17daba5d63bb8b254675450018c838278",
    "pwSalt" : -2513525821773890181,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-18ce19a908ecd6217947092601af37c5",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "73dd9a917959c36bef4e0db449d4439d9fdf9389878406e88c0038eeb7c73ff1",
    "pwSalt" : 3423298823637022118,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-18ce19a908ecd6217947092601af37c5",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "d113dfbe8b4bc8535b35e6ab4ed17cbd6e573bda14ba9c24b6f534c8dc31b5e1",
    "pwSalt" : 4992704825597719373,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-18ce19a908ecd6217947092601af37c5",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "55441b5d9e34f43d663051da555587abecc8bd6aa18b9b021ba6a78128efabba",
    "pwSalt" : 4617185454590153847,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "b0f7ef6e7ae1b5d12f139c12db6b4fd944c52e7bfef139d92b4126052bda9002",
    "pwSalt" : 8318331334432049418,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "941b4e5655037057814c6b7617f0f8d2a2c24335887539dd1a5ea3e8974647c7",
    "pwSalt" : 3124090909479426215,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170330-1814",
    "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-172-31-2-22.ap-southeast-2.compute.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "amon_password"
        }, {
          "name" : "firehose_database_user",
          "value" : "amon"
        }, {
          "name" : "firehose_heapsize",
          "value" : "958398464"
        } ]
      }, {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "958398464"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-2-22.ap-southeast-2.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "958398464"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-18ce19a908ecd6217947092601af37c5",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "i-0ff1740811ea07331"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2qf072xxrennwny2zfcgtmjxc"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-18ce19a908ecd6217947092601af37c5",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-0ff1740811ea07331"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "c247u546liehr5ywidz9jbreu"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-18ce19a908ecd6217947092601af37c5",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-0ff1740811ea07331"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "37fvfhjruf3rv86z01utwy9e5"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-18ce19a908ecd6217947092601af37c5",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-0ff1740811ea07331"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "80xqyiii58re46du7tc2qxzam"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-18ce19a908ecd6217947092601af37c5",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-0ff1740811ea07331"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "e3z0ijokz7uhhauwzj0gjy87u"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-18ce19a908ecd6217947092601af37c5",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-0ff1740811ea07331"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "twbikkg3c8j55yfzfqxo6fxh"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false"
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/24/2012 18:30"
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAABBAAIAD01JS0FFTEdJVEhVQi5NRQAEcm9vdAAFYWRtaW4AAAABWQo6EwEAFwAQ6Jf8GFkO8iQ3Th9kv9hVtQAAAAE="
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "root/admin@MIKAELGITHUB.ME"
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-2-22.ap-southeast-2.compute.internal"
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    }, {
      "name" : "SECURITY_REALM",
      "value" : "MIKAELGITHUB.ME"
    } ]
  }
```
