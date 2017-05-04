CM 5.9.2
Java 1.7
CDH 5.9.2

Backup DB

Stop Management Services
mysqldump -uamon -pamon_password amon > /tmp/amon-backup.sql
mysqldump -urman -prman_password rman > /tmp/rman-backup.sql
mysqldump -umetastore -phive_password hive > /tmp/hive-backup.sql
mysqldump -usentry -psentry_password hive > /tmp/sentry-backup.sql
mysqldump -unav -pnav_password nav > /tmp/nav-backup.sql
mysqldump -unavms -pnavms_password navms > /tmp/navms-backup.sql
mysqldump -uhue -phue_password hue > /tmp/hue-backup.sql
mysqldump -uoozie -poozie oozie > /tmp/oozie-backup.sql

Stop Management Services
Stop all running commands
sudo service cloudera-scm-server stop
sudo service cloudera-scm-agent stop
sudo cp -r /etc/cloudera-scm-server /tmp/cloudera-scm-server-old
sudo cp -r /etc/cloudera-scm-agent /tmp/cloudera-scm-agent

Download Cloudera repo
Navigate to https://archive.cloudera.com/cm5/
https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/

wget https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/cloudera-manager.repo

sudo vi /etc/yum.repos.d/cloudera-manager.repo

sudo yum clean all
sudo yum upgrade cloudera-manager-server cloudera-manager-daemons cloudera-manager-agent

Checking:
rpm -qa 'cloudera-manager-*'

Starting Cloudera Manager Server
sudo service cloudera-scm-server start
tail -f /var/log/cloudera-scm-server/cloudera-scm-server.log

Upgrade the Agents through the Wizard in CM

