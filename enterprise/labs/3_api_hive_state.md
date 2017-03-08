*****stop hive
[louisv1@ip-172-31-19-137 ~]$ curl -X POST -u louisv1:cloudera http://34.252.44.118:7180/api/v2/clusters/louisv1%20cluster/services/hive/commands/stop
{
  "id" : 388,
  "name" : "Stop",
  "startTime" : "2017-03-08T10:47:25.072Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }


****status of command  
  curl -u louisv1:cloudera http://34.252.44.118:7180/api/v2/commands/388
{
  "id" : 388,
  "name" : "Stop",
  "startTime" : "2017-03-08T10:47:25.072Z",
  "endTime" : "2017-03-08T10:47:38.704Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully stopped service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 389,
      "name" : "Stop",
      "startTime" : "2017-03-08T10:47:25.074Z",
      "endTime" : "2017-03-08T10:47:38.703Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-45818c070d5d949e31bfc652ea2277d6"
      }
    }, {
      "id" : 390,
      "name" : "Stop",
      "startTime" : "2017-03-08T10:47:25.076Z",
      "endTime" : "2017-03-08T10:47:38.700Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-45818c070d5d949e31bfc652ea2277d6"
      }
    } ]
  }

  
*****start hive 
  curl -X POST -u louisv1:cloudera http://34.252.44.118:7180/api/v2/clusters/louisv1%20cluster/services/hive/commands/start
{
  "id" : 392,
  "name" : "Start",
  "startTime" : "2017-03-08T10:49:10.551Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
