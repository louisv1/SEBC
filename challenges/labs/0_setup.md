-List the cloud provider you are using 
AWS

List the nodes you are using by IP address and name
172.31.30.102  ip-172-31-30-102
172.31.29.188  ip-172-31-29-188  
172.31.30.238  ip-172-31-30-238
172.31.16.175  ip-172-31-16-175
172.31.18.189  ip-172-31-18-189

List the Linux release you are using 
Centos 6.5


Demonstrate the disk capacity available on each node is >= 30 GB
[root@ip-172-31-30-102 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  707M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm


[root@ip-172-31-29-188 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  708M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm


[root@ip-172-31-30-238 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  709M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm


[root@ip-172-31-16-175 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  708M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm


[root@ip-172-31-18-189 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  707M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm



List the command and output for  yum repolist enabled  
[root@ip-172-31-30-102 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: mirror.vorboss.net
 * extras: centos.serverspace.co.uk
 * updates: centos.serverspace.co.uk
base                                                                        | 3.7 kB     00:00
extras                                                                      | 3.4 kB     00:00
updates                                                                     | 3.4 kB     00:00
repo id                                  repo name                                           status
base                                     CentOS-6 - Base                                     6,696
extras                                   CentOS-6 - Extras                                      64
updates                                  CentOS-6 - Updates                                    959
repolist: 7,719







[root@ip-172-31-18-189 ~]# grep 'merengues' /etc/group
merengues:x:501:
[root@ip-172-31-18-189 ~]# grep 'barca' /etc/group
barca:x:500:


[root@ip-172-31-18-189 ~]# grep '2010' /etc/passwd
naymar:x:2010:501::/home/naymar:/bin/bash
[root@ip-172-31-18-189 ~]# grep '2016' /etc/passwd
ronaldo:x:2016:500::/home/ronaldo:/bin/bash