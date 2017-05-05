# Yum repo d
```
[root@ip-172-31-11-187 ec2-user]# ls /etc/yum.repos.d
cloudera-manager.repo        redhat-rhui-client-config.repo
mysql-community.repo         redhat-rhui.repo
mysql-community-source.repo  rhui-load-balancers.conf
redhat.repo
```

# Prepare databases

```
[root@ip-172-31-11-187 ec2-user]# /usr/share/cmf/schema/scm_prepare_database.sh mysql scm scm scm_password
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
```

