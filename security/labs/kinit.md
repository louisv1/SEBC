[root@ip-172-31-17-175 ~]# kdestroy
[root@ip-172-31-17-175 ~]# kinit cm/admin
Password for cm/admin@SEBC.CORP:
[root@ip-172-31-17-175 ~]# klist -e
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: cm/admin@SEBC.CORP

Valid starting     Expires            Service principal
03/08/17 18:08:07  03/09/17 18:08:07  krbtgt/SEBC.CORP@SEBC.CORP
        renew until 03/15/17 18:08:07, Etype (skey, tkt): arcfour-hmac, arcfour-hmac
