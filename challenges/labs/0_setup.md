# Pre installation checks

## List the cloud provider you are using (AWS, GCE, Azure, other)
AWS
## List the nodes you are using by IP address and name

52.62.49.204  
ec2-52-62-49-204.ap-southeast-2.compute.amazonaws.com  
52.62.21.27  
ec2-52-62-21-27.ap-southeast-2.compute.amazonaws.com  
13.55.208.225  
ec2-13-55-208-225.ap-southeast-2.compute.amazonaws.com  
13.54.190.4  
ec2-13-54-190-4.ap-southeast-2.compute.amazonaws.com  
13.54.139.169  
ec2-13-54-139-169.ap-southeast-2.compute.amazonaws.com  

## List the Linux release you are using
ReHat 7.3

## Demonstrate the disk capacity available on each node is >= 30 GB

I am using 50GB disk size on all nodes.
```
[ec2-user@ip-172-31-11-187 ~]$ sudo fdisk -l
WARNING: fdisk GPT support is currently new, and therefore in an experimental phase. Use at your own discretion.

Disk /dev/xvda: 53.7 GB, 53687091200 bytes, 104857600 sectors
[ec2-user@ip-172-31-13-85 ~]$ sudo fdisk -l
WARNING: fdisk GPT support is currently new, and therefore in an experimental phase. Use at your own discretion.

Disk /dev/xvda: 53.7 GB, 53687091200 bytes, 104857600 sectors
[ec2-user@ip-172-31-1-105 ~]$ sudo fdisk -l                                     WARNING: fdisk GPT support is currently new, and therefore in an experimental phase. Use at your own discretion.

Disk /dev/xvda: 53.7 GB, 53687091200 bytes, 104857600 sectors
[ec2-user@ip-172-31-11-234 ~]$ sudo fdisk -l
WARNING: fdisk GPT support is currently new, and therefore in an experimental phase. Use at your own discretion.

Disk /dev/xvda: 53.7 GB, 53687091200 bytes, 104857600 sectors
[ec2-user@ip-172-31-2-22 ~]$ sudo fdisk -l
WARNING: fdisk GPT support is currently new, and therefore in an experimental phase. Use at your own discretion.

Disk /dev/xvda: 53.7 GB, 53687091200 bytes, 104857600 sectors


```

## List the command and output for yum repolist enabled
```
sudo yum repolist enabled 
[ec2-user@ip-172-31-11-187 ~]$ sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
rhui-REGION-client-config-server-7                       | 2.9 kB     00:00
rhui-REGION-rhel-server-releases                         | 3.5 kB     00:00
rhui-REGION-rhel-server-rh-common                        | 3.8 kB     00:00
(1/7): rhui-REGION-client-config-server-7/x86_64/primary_d | 5.4 kB   00:00
(2/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/gr |  104 B   00:00
(3/7): rhui-REGION-rhel-server-releases/7Server/x86_64/upd | 1.9 MB   00:00
(4/7): rhui-REGION-rhel-server-releases/7Server/x86_64/gro | 701 kB   00:00
(5/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/pr | 118 kB   00:00
(6/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/up |  33 kB   00:00
(7/7): rhui-REGION-rhel-server-releases/7Server/x86_64/pri |  35 MB   00:00
repo id                                          repo name                status
rhui-REGION-client-config-server-7/x86_64        Red Hat Update Infrastru      6
rhui-REGION-rhel-server-releases/7Server/x86_64  Red Hat Enterprise Linux 14,277
rhui-REGION-rhel-server-rh-common/7Server/x86_64 Red Hat Enterprise Linux    228
repolist: 14,511
```

# Adding users

```
useradd -u 2300 cate
useradd -u 2900 jemaine
groupadd kiwis
groupadd aussies
usermod -a -G kiwis jemaine
usermod -a -G aussies cate

```
Listing added users and groups
```
[root@ip-172-31-11-187 ec2-user]# cat /etc/passwd | grep cate
cate:x:2300:2300::/home/cate:/bin/bash
[root@ip-172-31-11-187 ec2-user]# cat /etc/passwd | grep jemaine
jemaine:x:2900:2900::/home/jemaine:/bin/bash
[root@ip-172-31-11-187 ec2-user]# cat /etc/group | grep kiwis
kiwis:x:2901:jemaine
[root@ip-172-31-11-187 ec2-user]# cat /etc/group | grep aussies
aussies:x:2902:cate

```
