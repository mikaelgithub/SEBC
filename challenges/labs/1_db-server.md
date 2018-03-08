## A command and output that shows the hostname of your database server
```
MariaDB [(none)]> select @@hostname;
+------------+
| @@hostname |
+------------+
| mel1       |
+------------+
1 row in set (0.00 sec)
```

## A command and output that reports the database server version
```
[root@mel1 mikael_dauzet]# mysql -V
mysql  Ver 15.1 Distrib 5.5.59-MariaDB, for Linux (x86_64) using readline 5.1
```

## A command and output that lists all the databases in the server
```
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
+--------------------+
8 rows in set (0.00 sec)
```