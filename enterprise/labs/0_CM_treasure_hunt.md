•What is ubertask optimization?
Runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings



•Where in CM is the Kerberos Security Realm value displayed?
go administration->security then kerberos tab, lots of info there. Click on config button will then show you a lot of info. The realm will be shown in field Kerberos Security Realm. Will be nineth field from teh top 
can also just go administration->settings, on Category on left select "kerberos", will get to same place as above
Or you can just search Kerberos Security Realm and you will see paramter



•Which CDH service(s) host a property for enabling Kerberos authentication?
Kerberos i activated for multiple services, when activating principals are created for multiple services



•How do you upgrade the CM agents?
You can use an upgrade wizard that is invoked when you connect to the Admin Console or manually install the Cloudera Manager Agent packages.



•Give the  tsquery  statement used to chart Hue's CPU utilization?
this is cpu cores used SELECT cpu_system_rate + cpu_user_rate WHERE entityName = "hue-HUE_SERVER-3f17bdad9b349c657409db948ee5c52c" AND category = ROLE




•Name all the roles that make up the Hive service
Hiveserver2
Hive Metastore Server
Gateway
can add webhact server



•What steps must be completed before integrating Cloudera Manager with Kerberos?
*according to wizzard
Set up a working KDC.
The KDC should be configured to have non-zero ticket lifetime and renewal lifetime
OpenLdap client libraries should be installed on the Cloudera Manager Server host if you want to use Active Directory. Also, Kerberos client libraries should be installed on ALL hosts.
Cloudera Manager needs an account that has permissions to create other accounts in the KDC.

*in simple english, high level
install krb5-server, two as a min so you hav secondary kdc
install krb5-workstation on all the nodes
configure krb5.conf 
configure kadm5.acl
configure kdc.conf
execute kdb5_util create , creates like the db for kerberos
test it


