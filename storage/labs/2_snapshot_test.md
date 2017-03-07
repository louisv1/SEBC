Did the below
 [root@ip-172-31-19-137 ~]# su - hdfs
 [hdfs@ip-172-31-19-137 ~]$ hdfs dfs -mkdir /precious
 [hdfs@ip-172-31-19-137 ~]$ hdfs dfs -put /SEBC.zip /precious
 [hdfs@ip-172-31-19-137 ~]$ hdfs dfsadmin -allowSnapshot /precious
 Allowing snaphot on /precious succeeded
 [hdfs@ip-172-31-19-137 ~]$ hdfs dfs -createSnapshot /precious sebc-hdfs-test
 Created snapshot /precious/.snapshot/sebc-hdfs-test
 [hdfs@ip-172-31-19-137 ~]$ hdfs dfs -rm -r /precious/SEBC.zip
 [hdfs@ip-172-31-19-137 ~]$ hdfs dfs -cp /precious/.snapshot/sebc-hdfs-test/SEBC.zip /precious
 [hdfs@ip-172-31-19-137 ~]$ hdfs dfs -ls /precious/
 Found 1 items
 -rw-r--r-- 3 hdfs supergroup 415069 2017-03-07 15:21 /precious/SEBC.zip

worked. Used hdfs user cause normal user cant do snapshots
