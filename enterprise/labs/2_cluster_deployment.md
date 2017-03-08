curl -u louisv1:cloudera http://34.252.44.118:7180/api/v2/cm/deployment
{
  "timestamp" : "2017-03-08T10:37:57.144Z",
  "clusters" : [ {
    "name" : "louisv1 cluster",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "1077936128"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "1077936128"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "1190762905"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "200"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-21-180.eu-west-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "IluvSQL1!"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-3f17bdad9b349c657409db948ee5c52c",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-08869a89515c0c416"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-45818c070d5d949e31bfc652ea2277d6",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c7a0j67etojnl5hhnqoge494z"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-45818c070d5d949e31bfc652ea2277d6",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4nzq20f41dezmrr12e5qmn10q"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-45818c070d5d949e31bfc652ea2277d6",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "842tor4qltafy9vf9pp3cn9h4"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-89fed64aa471235d253dbf7172b61633",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "6e58e567-7e2c-4f12-a878-b9046003e475"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c4fvqwnqjjtkp64jb913sdrkn"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ca7fedb18975b1e3b505ccc741c08d3a",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-09b09f060336a9078"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6plvz6kzjssij8c020tn2hb7j"
          }, {
            "name" : "serverId",
            "value" : "2"
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
          "value" : "ip-172-31-21-180.eu-west-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "IluvSQL1!"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-45818c070d5d949e31bfc652ea2277d6"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-3f17bdad9b349c657409db948ee5c52c",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-08869a89515c0c416"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2hz4rcdfn7xsidbdzd1z1iyj3"
          }, {
            "name" : "secret_key",
            "value" : "CKmzwORSFZtJtSaytzBN2MNsPIPdCX"
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
            "value" : "ip-172-31-21-180.eu-west-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "IluvSQL1!"
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
        "name" : "oozie-OOZIE_SERVER-3f17bdad9b349c657409db948ee5c52c",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-08869a89515c0c416"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "92jl46jcr6bdjwfac0bfv2by3"
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
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
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
            "value" : "1024"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5250"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "FRvzY3OLP2jM2C3k5dumUCICVqjnug"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-45818c070d5d949e31bfc652ea2277d6",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "amo5hbj3oc1qjqufayj6lzfhl"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-0960c87ac036ce79d828dfec3a417514",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "27a47c1a-090f-4bb2-89fd-9e08e862a668"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7qh60y5vpe0v2mzbw7wnuc2j7"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-45818c070d5d949e31bfc652ea2277d6",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8tdzvv6djvw0yj09nf1f40vzo"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-89fed64aa471235d253dbf7172b61633",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "6e58e567-7e2c-4f12-a878-b9046003e475"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4221fbkdcva4pddnqptodpd6y"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-ca7fedb18975b1e3b505ccc741c08d3a",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-09b09f060336a9078"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4c6spizj2nzuzhu6tqvrz74t3"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-ca7fedb18975b1e3b505ccc741c08d3a",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-09b09f060336a9078"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "47"
          }, {
            "name" : "role_jceks_password",
            "value" : "2q2majpf9798n4fl5opk76i07"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "1077936128"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "1077936128"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "NevMr7Dv8m4Vjq6eXcXM5NOtk1WB86"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "NKDMwARtW73x9Um5XN3EXhJ9wn9XDo"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "rrHTELi7h8XbgtqpmFJ7BvXmxRBpcT"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-89fed64aa471235d253dbf7172b61633",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "6e58e567-7e2c-4f12-a878-b9046003e475"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-0960c87ac036ce79d828dfec3a417514",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "27a47c1a-090f-4bb2-89fd-9e08e862a668"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "pltn5fo791s8b9bg9n8al4at"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-45818c070d5d949e31bfc652ea2277d6",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4vg1n3hxeb23h771jl2ru32br"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-89fed64aa471235d253dbf7172b61633",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "6e58e567-7e2c-4f12-a878-b9046003e475"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aicd937qlbx0r4jcypd6dzs7p"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-ca7fedb18975b1e3b505ccc741c08d3a",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-09b09f060336a9078"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "54mkibl5jvny2lo2q61ev87vl"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-45818c070d5d949e31bfc652ea2277d6",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c4cg6o3u8j5zzi96iolwukybn"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-ca7fedb18975b1e3b505ccc741c08d3a",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-09b09f060336a9078"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "35pww5rl3gjpc7g3b6hufvau7"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-45818c070d5d949e31bfc652ea2277d6",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5w9i4nt4vq8wz5xq8isxr569c"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-45818c070d5d949e31bfc652ea2277d6",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "egcd7rs9xnd784j2wkafox8bd"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-89fed64aa471235d253dbf7172b61633",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "6e58e567-7e2c-4f12-a878-b9046003e475"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3w8bwtbok0j50lbygwyc6ezme"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-ca7fedb18975b1e3b505ccc741c08d3a",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-09b09f060336a9078"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "rvi3bnb2scu878vvy2wb3gqg"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-45818c070d5d949e31bfc652ea2277d6",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "hdfsha1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "hdfsha1"
          }, {
            "name" : "namenode_id",
            "value" : "55"
          }, {
            "name" : "role_jceks_password",
            "value" : "6xelp2iprnoaoxxamffyx7ezt"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-ca7fedb18975b1e3b505ccc741c08d3a",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-09b09f060336a9078"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "hdfsha1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "hdfsha1"
          }, {
            "name" : "namenode_id",
            "value" : "49"
          }, {
            "name" : "role_jceks_password",
            "value" : "9fgo7dqf905ycbsrsrzg8p6x0"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "6e58e567-7e2c-4f12-a878-b9046003e475",
    "ipAddress" : "172.31.16.81",
    "hostname" : "ip-172-31-16-81.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "27a47c1a-090f-4bb2-89fd-9e08e862a668",
    "ipAddress" : "172.31.19.137",
    "hostname" : "ip-172-31-19-137.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "b92ef81a-1730-4368-a4c6-8eb11d3b069d",
    "ipAddress" : "172.31.20.196",
    "hostname" : "ip-172-31-20-196.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-08869a89515c0c416",
    "ipAddress" : "172.31.21.180",
    "hostname" : "ip-172-31-21-180.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-09b09f060336a9078",
    "ipAddress" : "172.31.23.155",
    "hostname" : "ip-172-31-23-155.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : " minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "524165acc9163cd708d095f59e5c46c3073a007e5774bc356ec78cd04f048773",
    "pwSalt" : -5456336709850760670,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-3f17bdad9b349c657409db948ee5c52c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c68ef76e3ce981bd7228999c1caef6e8e51b21582803016911aabf0571c91fca",
    "pwSalt" : 8096782958141540514,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-3f17bdad9b349c657409db948ee5c52c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e10d4f7464b95b607f6c95af1c0f608109a756a1b4ea08c87cb6d2d18b594686",
    "pwSalt" : 4075914545661023131,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-3f17bdad9b349c657409db948ee5c52c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f9e5207077e3197ed2a8a0dbda3a4c0487620d27c7bf7db4d4afeb92c0d47479",
    "pwSalt" : -5974289647389404670,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-3f17bdad9b349c657409db948ee5c52c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b8cf4280276b942e015313b5c862e8857f8c214bf9c2cf3127389d9a87d49723",
    "pwSalt" : -1243688525703352241,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-3f17bdad9b349c657409db948ee5c52c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e2774d9fa8154cedc2054299611c3c0df3f149f8615e67ab03703327ee90d408",
    "pwSalt" : -5618339238765665329,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "a723518b1081b9c792a4c5250a4e15bf97c971562ae6d21aa890a5f4d27bd489",
    "pwSalt" : 2063166045027854006,
    "pwLogin" : true
  }, {
    "name" : "louisv1",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "5a15a8dcb2472691df4ad74a2a5a209f419b02d4cc0499383e71d9f3a9f8600e",
    "pwSalt" : -8666921518005227372,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "f7d867c39933472c31d5d6b5a93a5516ccdc25e9288c0934686786dca9e0ae03",
    "pwSalt" : 1601680903713663698,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1014",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
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
          "value" : "ip-172-31-21-180.eu-west-1.compute.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "activity"
        }, {
          "name" : "firehose_database_password",
          "value" : "IluvSQL1!"
        }, {
          "name" : "firehose_database_user",
          "value" : "activity"
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
          "value" : "ip-172-31-21-180.eu-west-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "IluvSQL1!"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
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
      "name" : "mgmt-ACTIVITYMONITOR-3f17bdad9b349c657409db948ee5c52c",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "i-08869a89515c0c416"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6a5hvof1t1j36mvg2x0zqd22k"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-3f17bdad9b349c657409db948ee5c52c",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-08869a89515c0c416"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2kgnozjv1levillly22fd1vvh"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-3f17bdad9b349c657409db948ee5c52c",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-08869a89515c0c416"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "ws5ve16galvhghok5c18tah3"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-3f17bdad9b349c657409db948ee5c52c",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-08869a89515c0c416"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7maq1vvq076626mxwqjs41snn"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-3f17bdad9b349c657409db948ee5c52c",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-08869a89515c0c416"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eju73c38ptwxurwq1t7l7bm6y"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-3f17bdad9b349c657409db948ee5c52c",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-08869a89515c0c416"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "9oncnq11wb68xjj75amjy3g3d"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 10:20"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://ip-172-31-21-180/cdh5.8.3/parcels/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
