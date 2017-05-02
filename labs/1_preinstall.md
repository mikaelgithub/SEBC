## <center> <a name="pre_install"/> Day 1 - 01/05/2017

1. Swapiness
```
sudo cat /proc/sys/vm/swappiness
$ sudo sysctl vm.swappiness=1
```
<center> <img src="png/1_preinstall-swapiness.PNG"> </center>

2. Show Mount 
```
$ mount
$ mount -t ext
```
3. 
* This step is not required

4. Disable transparent hugepage support
```
$ sudo su
$ echo never > /sys/kernel/mm/transparent_hugepage/enabled
$ cat /sys/kernel/mm/transparent_hugepage/enabled
always madvise [never]
```
---
<div style="page-break-after: always;"></div>

## <center> <a name="aa"/> Day 2 - 02/05/2017

5. List your network interface configuration
```
$ netstat -i
Kernel Interface table
Iface      MTU    RX-OK RX-ERR RX-DRP RX-OVR    TX-OK TX-ERR TX-DRP TX-OVR Flg
eth0      9001      702      0      0 0           699      0      0      0 BMRU
lo       65536        4      0      0 0             4      0      0      0 LRU
```

6. Forward and reverse lookup
```
$ getent hosts localhost
::1             localhost localhost.localdomain localhost6 localhost6.localdomain6
$ nslookup 35.162.188.199
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
199.188.162.35.in-addr.arpa     name = ec2-35-162-188-199.us-west-2.compute.amazonaws.com.

Authoritative answers can be found from:

```

7. NSCD
```
yum install nscd
yum install ntp
service nscd start
$ service nscd status
Redirecting to /bin/systemctl status  nscd.service
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-05-01 22:16:46 EDT; 3min 21s ago
 Main PID: 9716 (nscd)
```

 8. NTPD
```
service ntpd start
$ service ntpd status
Redirecting to /bin/systemctl status  ntpd.service
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-05-01 22:18:19 EDT; 2min 27s ago
```   

---
<div style="page-break-after: always;"></div>

## <center> <a name="aa"/> MySQL installation 

```
sudo yum install wget
$ sudo wget http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm
$ sudo rpm -ivh mysql-community-release-el7-5.noarch.rpm
```
Enabling Mysql 5.5
```
$ sudo vi /etc/yum.repos.d/mysql-community.repo
or 
$ sudo yum repolist enabled | grep mysql
mysql-connectors-community/x86_64                MySQL Connectors Communi     36
mysql-tools-community/x86_64                     MySQL Tools Community        47
mysql56-community/x86_64                         MySQL 5.6 Community Serv    327
$ sudo yum-config-manager --disable mysql56-community
$ sudo yum-config-manager --enable mysql55-community
$ sudo yum repolist enabled | grep mysql
mysql-connectors-community/x86_64                MySQL Connectors Communi     36
mysql-tools-community/x86_64                     MySQL Tools Community        47
mysql55-community/x86_64                         MySQL 5.5 Community Serv    308
$ yum update

```
Installation
```
$ sudo yum install mysql-community-server
$ wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.0.8.tar.gz
$ sudo service mysqld start
Redirecting to /bin/systemctl start  mysqld.service
mkdir mysql_bkp
$ sudo mv /var/lib/mysql/ib_logfile0 mysql_bkp/
$ sudo mv /var/lib/mysql/ib_logfile1 mysql_bkp/
$ sudo cp /etc/my.cnf /etc/my.cnf.old
$ sudo vi /etc/my.cnf2

```
update my.cnf file 
```
[mysqld]
transaction-isolation = READ-COMMITTED
# Disabling symbolic-links is recommended to prevent assorted security risks;
# to do so, uncomment this line:
# symbolic-links = 0

key_buffer_size = 32M
max_allowed_packet = 32M
thread_stack = 256K
thread_cache_size = 64
query_cache_limit = 8M
query_cache_size = 64M
query_cache_type = 1

max_connections = 550
#expire_logs_days = 10
#max_binlog_size = 100M

#log_bin should be on a disk with enough free space. Replace '/var/lib/mysql/mysql_binary_log' with an appropriate path for your system
#and chown the specified folder to the mysql user.
log_bin=/var/lib/mysql/mysql_binary_log

# For MySQL version 5.1.8 or later. For older versions, reference MySQL documentation for configuration help.
binlog_format = mixed

read_buffer_size = 2M
read_rnd_buffer_size = 16M
sort_buffer_size = 8M
join_buffer_size = 8M

# InnoDB settings
innodb_file_per_table = 1
innodb_flush_log_at_trx_commit  = 2
innodb_log_buffer_size = 64M
innodb_buffer_pool_size = 4G
innodb_thread_concurrency = 8
innodb_flush_method = O_DIRECT
innodb_log_file_size = 512M

[mysqld_safe]
log-error=/var/log/mysqld.log
pid-file=/var/run/mysqld/mysqld.pid

sql_mode=STRICT_ALL_TABLES
```
Then
```
$ sudo cp /etc/my.cnf2 /etc/my.cnf

$ sudo /sbin/chkconfig mysqld on
$ sudo service mysql start

$ sudo /usr/bin/mysql_secure_installation
	
NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MySQL
      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

In order to log into MySQL to secure it, we'll need the current
password for the root user.  If you've just installed MySQL, and
you haven't set the root password yet, the password will be blank,
so you should just press enter here.

Enter current password for root (enter for none):
ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: YES)
Enter current password for root (enter for none):
OK, successfully used password, moving on...

Setting the root password ensures that nobody can log into the MySQL
root user without the proper authorisation.

Set root password? [Y/n] Y
New password: cloudera
Remove anonymous users? [Y/n] y
Disallow root login remotely? [Y/n] n
Remove test database and access to it? [Y/n] y
Reload privilege tables now? [Y/n] y

$ sudo service mysql stop
```

Installing JDBC connector
```
$ wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.42.tar.gz
$ tar zxvf mysql-connector-java-5.1.42.tar.gz
$ sudo mkdir -p /usr/share/java/
$ sudo chmod -R 777 /usr/share/java
$ sudo cp mysql-connector-java-5.1.42/mysql-connector-java-5.1.42-bin.jar /usr/share/java/mysql-connector-java.jar

```
Creating Databases for Activity Monitor, Reports Manager, Hive Metastore Server, Sentry Server, Cloudera Navigator Audit Server, and Cloudera Navigator Metadata Server
```
$ mysql -u root -p
Enter password:
create database amon DEFAULT CHARACTER SET utf8;
grant all on amon.* TO 'amon'@'%' IDENTIFIED BY 'amon_password';
create database rman DEFAULT CHARACTER SET utf8;
grant all on rman.* TO 'rman'@'%' IDENTIFIED BY 'rman_password';
create database metastore DEFAULT CHARACTER SET utf8;
grant all on metastore.* TO 'hive'@'%' IDENTIFIED BY 'hive_password';
create database sentry DEFAULT CHARACTER SET utf8;
grant all on sentry.* TO 'sentry'@'%' IDENTIFIED BY 'sentry_password';
create database nav DEFAULT CHARACTER SET utf8;
grant all on nav.* TO 'nav'@'%' IDENTIFIED BY 'nav_password';
create database navms DEFAULT CHARACTER SET utf8;
grant all on navms.* TO 'navms'@'%' IDENTIFIED BY 'navms_password';

```
Configuring MySQL for Oozie
```

create database oozie;
grant all privileges on oozie.* to 'oozie'@'localhost' identified by 'oozie';
grant all privileges on oozie.* to 'oozie'@'%' identified by 'oozie';

```
Add the MySQL JDBC Driver JAR to Oozie
```
$ sudo mkdir /var/lib/oozie
$ sudo cp /usr/share/java/mysql-connector-java.jar /var/lib/oozie/
```

CM Installation
```
$ python --version
Python 2.7.5
$ sudo easy_install pip
$ sudo pip install psycopg2

$ wget https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/cloudera-manager.repo
$ sudo cp cloudera-manager.repo /etc/yum.repos.d/
$ sudo vi /etc/yum.repos.d/cloudera-manager.repo
# baseurl=https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5/
baseurl=https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.9.2/

$ sudo yum install oracle-j2sdk1.7
$ sudo yum install cloudera-manager-daemons cloudera-manager-server

```
Prepare database
```
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql rman rman rman_password
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql metastore hive hive_password
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql sentry sentry sentry_password
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql metastore hive hive_password
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql sentry sentry sentry_password
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql nav nav nav_password
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql navms navms navms_password
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql amon amon amon_password
sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql oozie oozie oozie
```
Start
```
$ sudo service cloudera-scm-server start
$ sudo tail -f /var/log/cloudera-scm-server/cloudera-scm-server.log

```
* Preparing the cluster:
	* on all nodes: 
	* Set vm.swappiness
	* Disable transparent hugepage support
	* Install the mysql package
```
$ sudo yum install mysql
```
	* Download and copy the JDBC connector

Preparing replica
on server and replica nodes
Install mysql-server

```
$ mysql -u root -p
GRANT REPLICATION SLAVE ON *.* TO 'root'@'ec2-34-208-235-6.us-west-2.compute.amazonaws.com' IDENTIFIED BY 'cloudera';
SET GLOBAL binlog_format = 'ROW';
FLUSH TABLES WITH READ LOCK;
SHOW MASTER STATUS;
+-------------------------+----------+--------------+------------------+-------------------+
| File                    | Position | Binlog_Do_DB | Binlog_Ignore_DB | Executed_Gtid_Set |
+-------------------------+----------+--------------+------------------+-------------------+
| mysql_binary_log.000003 | 45695855 |              |                  |                   |
+-------------------------+----------+--------------+------------------+-------------------+
UNLOCK TABLES;

On the replica:
CHANGE MASTER TO MASTER_HOST='ec2-34-209-76-165.us-west-2.compute.amazonaws.com', MASTER_USER='root', MASTER_PASSWORD='cloudera', MASTER_LOG_FILE='mysql_binary_log.000003', MASTER_LOG_POS=45695855;
START SLAVE;
SHOW SLAVE STATUS \G

```
Configuration of CM and CDH

```
List of hosts:
NN1 172.31.17.69 ec2-34-209-76-165.us-west-2.compute.amazonaws.com,
NN2 172.31.8.123 ec2-34-208-235-6.us-west-2.compute.amazonaws.com
DN1 172.31.20.125 ec2-52-36-135-147.us-west-2.compute.amazonaws.com,
DN2 172.31.25.62 ec2-52-10-91-94.us-west-2.compute.amazonaws.com,
DN3 172.31.30.207 ec2-54-70-80-229.us-west-2.compute.amazonaws.com,

