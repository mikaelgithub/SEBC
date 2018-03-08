## List the cloud provider you are using (AWS, GCE, Azure, CloudCat, other)
Google Cloud

## List your instances by IP address and DNS name (don't use /etc/hosts for this)
```
[root@mel1 mikael_dauzet]# hostname -f && hostname -i
mel1.c.sebc-194321.internal
10.142.0.2
[root@mel2 mikael_dauzet]# hostname -f && hostname -i
mel2.c.sebc-194321.internal
10.142.0.3
[root@mel3 mikael_dauzet]# hostname -f && hostname -i
mel3.c.sebc-194321.internal
10.142.0.4
[root@mel4 mikael_dauzet]# hostname -f && hostname -i
mel4.c.sebc-194321.internal
10.142.0.5
[root@mel5 mikael_dauzet]# hostname -f && hostname -i
mel5.c.sebc-194321.internal
10.142.0.6
```

## List the Linux release you are using
```
[root@mel1 mikael_dauzet]# cat /etc/centos-release
CentOS Linux release 7.4.1708 (Core) 
```

## List the file system capacity for the first node
```
[root@mel1 mikael_dauzet]# fdisk -l
Disk /dev/sda: 53.7 GB, 53687091200 bytes, 104857600 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 4096 bytes
I/O size (minimum/optimal): 4096 bytes / 4096 bytes
Disk label type: dos
Disk identifier: 0x00094189
   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048   104856254    52427103+  83  Linux
```

## List the command and output for yum repolist enabled
```
[root@mel1 mikael_dauzet]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.mojohost.com
 * epel: mirror.vcu.edu
 * extras: packages.oit.ncsu.edu
 * updates: mirror.cogentco.com
repo id                   repo name                                            status
base/7/x86_64             CentOS-7 - Base                                       9,591
epel/x86_64               Extra Packages for Enterprise Linux 7 - x86_64       12,382
extras/7/x86_64           CentOS-7 - Extras                                       392
google-cloud-compute      Google Cloud Compute                                      9
google-cloud-sdk          Google Cloud SDK                                        413
updates/7/x86_64          CentOS-7 - Updates                                    2,398
repolist: 25,185
```

## Add users and groups
```
[root@mel1 mikael_dauzet]# cat /etc/passwd | grep jim
jim:x:2800:2800::/home/jim:/bin/bash
[root@mel1 mikael_dauzet]# cat /etc/passwd | grep jemaine
jemaine:x:2900:2900::/home/jemaine:/bin/bash
[root@mel1 mikael_dauzet]# 
```
```
[root@mel1 mikael_dauzet]# cat /etc/group | grep kiwi
kiwi:x:2901:jemaine
[root@mel1 mikael_dauzet]# cat /etc/group | grep aussie
aussie:x:2902:jim
```