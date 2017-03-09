[root@ip-172-31-22-186 ~]# kinit george
Password for george@SEBC.CORP:
[root@ip-172-31-22-186 ~]# beeline -u "jdbc:hive2://172.31.18.222:10000/default;principal=hive/ip-172-31-18-222.eu-west-1.compute.internal@SEBC.CORP"
scan complete in 2ms
Connecting to jdbc:hive2://172.31.18.222:10000/default;principal=hive/ip-172-31-18-222.eu-west-1.compute.internal@SEBC.CORP
Connected to: Apache Hive (version 1.1.0-cdh5.9.1)
Driver: Hive JDBC (version 1.1.0-cdh5.9.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
Beeline version 1.1.0-cdh5.9.1 by Apache Hive
0: jdbc:hive2://172.31.18.222:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170309091414_15300385-e9a7-4a76-b12e-58e163d4a9a7): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170309091414_15300385-e9a7-4a76-b12e-58e163d4a9a7); Time taken: 0.071 seconds
INFO  : Executing command(queryId=hive_20170309091414_15300385-e9a7-4a76-b12e-58e163d4a9a7): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170309091414_15300385-e9a7-4a76-b12e-58e163d4a9a7); Time taken: 0.141 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.316 seconds)
0: jdbc:hive2://172.31.18.222:10000/default>





[root@ip-172-31-22-186 ~]# kdestroy
[root@ip-172-31-22-186 ~]# kinit ferdinand
Password for ferdinand@SEBC.CORP:
[root@ip-172-31-22-186 ~]# beeline -u "jdbc:hive2://172.31.18.222:10000/default;principal=hive/ip-172-31-18-222.eu-west-1.compute.internal@SEBC.CORP"
scan complete in 2ms
Connecting to jdbc:hive2://172.31.18.222:10000/default;principal=hive/ip-172-31-18-222.eu-west-1.compute.internal@SEBC.CORP
Connected to: Apache Hive (version 1.1.0-cdh5.9.1)
Driver: Hive JDBC (version 1.1.0-cdh5.9.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
Beeline version 1.1.0-cdh5.9.1 by Apache Hive
0: jdbc:hive2://172.31.18.222:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170309091616_b253c77a-658c-4d4f-ba1c-37bb8f230372): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170309091616_b253c77a-658c-4d4f-ba1c-37bb8f230372); Time taken: 0.098 seconds
INFO  : Executing command(queryId=hive_20170309091616_b253c77a-658c-4d4f-ba1c-37bb8f230372): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170309091616_b253c77a-658c-4d4f-ba1c-37bb8f230372); Time taken: 0.158 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.365 seconds)

