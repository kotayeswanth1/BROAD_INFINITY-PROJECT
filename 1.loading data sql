[training@localhost ~]$ mysql --user=training--password =training
ERROR 1044 (42000): Access denied for user ''@'localhost' to database '=training'
[training@localhost ~]$ mysql--user=training--password =training
bash: mysql--user=training--password: command not found
[training@localhost ~]$ pwd
/home/training
[training@localhost ~]$ mysql--user=training--password=training
bash: mysql--user=training--password=training: command not found
[training@localhost ~]$ mysql--user=training--password=training
bash: mysql--user=training--password=training: command not found
[training@localhost ~]$ mysql --user=training --password=training
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 9
Server version: 5.1.66 Source distribution

Copyright (c) 2000, 2012, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hue                |
| metastore          |
| movielens          |
| mysql              |
| test               |
| training           |
+--------------------+
7 rows in set (0.05 sec)

mysql> load data infile '/home/training/Downloads'
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '' at line 1
mysql> create database ecommerce;
Query OK, 1 row affected (0.11 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| ecommerce          |
| hue                |
| metastore          |
| movielens          |
| mysql              |
| test               |
| training           |
+--------------------+
8 rows in set (0.03 sec)

mysql> use ecommerces;
ERROR 1049 (42000): Unknown database 'ecommerces'
mysql> use ecommerce;
Database changed
mysql> create table clickstream(userid int,timestamp,page varchar(20));
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'page varchar(20))' at line 1
mysql> create table clickstream(userid int,times TIMESTAMP,page varchar(20));
Query OK, 0 rows affected (0.21 sec)

mysql> SHOW TABLES;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| clickstream         |
+---------------------+
1 row in set (0.11 sec)

mysql> PWS
    -> PWD;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'PWS
PWD' at line 1
mysql> LOAD DATA local INFILE'/home/training/Downloads/clickstream_data.csv'INTO TABLE clickstream fields terminated by","lines terminated by'\n' ignore 1 lines;
ERROR 2 (HY000): File '/home/training/Downloads/clickstream_data.csv' not found (Errcode: 2)
mysql> LOAD DATA local INFILE'/home/training/Downloads/Dataset-clickstream_data.csv.csv'INTO TABLE clickstream fields terminated by","lines terminated by'\n' ignore 1 lines;
ERROR 2 (HY000): File '/home/training/Downloads/Dataset-clickstream_data.csv.csv' not found (Errcode: 2)
mysql> LOAD DATA local INFILE'/home/training/Downloads/'INTO TABLE clickstream fields terminated by","lines terminated by'\n' ignore 1 lines;
ERROR 2 (00000): Error reading file '/home/training/Downloads/' (Errcode: 21)
mysql> LOAD DATA local INFILE'/home/training/Downloads/Dataset-clickstream_data.csv.csv'INTO TABLE clickstream fields terminated by","lines terminated by'\n' ignore 1 lines;
ERROR 2 (HY000): File '/home/training/Downloads/Dataset-clickstream_data.csv.csv' not found (Errcode: 2)
mysql> LOAD DATA local INFILE'/home/training/Downloads/Dataset-clickstream_data.csv.csv'INTO TABLE clickstream fields terminated by','lines terminated by'\n' ignore 1 lines;
ERROR 2 (HY000): File '/home/training/Downloads/Dataset-clickstream_data.csv.csv' not found (Errcode: 2)
mysql> LOAD DATA local INFILE'/home/training/Downloads/Dataset -clickstream_data.csv.csv'INTO TABLE clickstream fields terminated by','lines terminated by'\n' ignore 1 lines;
ERROR 2 (HY000): File '/home/training/Downloads/Dataset -clickstream_data.csv.csv' not found (Errcode: 2)
mysql> LOAD DATA local INFILE'/home/training/Downloads/Dataset - clickstream_data.csv.csv'INTO TABLE clickstream fields terminated by','lines terminated by'\n' ignore 1 lines;
Query OK, 13 rows affected, 13 warnings (0.17 sec)
Records: 13  Deleted: 0  Skipped: 0  Warnings: 0
show tables;
ERROR 1046 (3D000): No database selected
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| ecommerce          |
| hue                |
| metastore          |
| movielens          |
| mysql              |
| test               |
| training           |
+--------------------+
8 rows in set (0.10 sec)

mysql> use ecommerce;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> show tables;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| clickstream         |
+---------------------+
1 row in set (0.00 sec)

mysql> select * from clickstream
    -> ;
+--------+---------------------+-----------------+
| userid | times               | page            |
+--------+---------------------+-----------------+
      |0 | 2023-01-01 10:00:00 | homepage"
  |    0 | 2023-01-01 10:01:00 | product_page"
      |0 | 2023-01-01 10:02:00 | homepage"
     | 0 | 2023-01-01 10:03:00 | cart_page"
      |0 | 2023-01-01 10:05:00 | homepage"
  |    0 | 2023-01-01 10:06:00 | product_page"
     | 0 | 2023-01-01 10:07:00 | cart_page"
      |0 | 2023-01-01 10:09:00 | homepage"
  |    0 | 2023-01-01 10:10:00 | product_page"
     | 0 | 2023-01-01 10:11:00 | cart_page"
 |     0 | 2023-01-01 10:12:00 | checkout_page"
      |0 | 2023-01-01 10:15:00 | homepage"
|      0 | 2023-01-01 10:16:00 | product_page"   |
+--------+---------------------+-----------------+
13 rows in set (0.06 sec)

mysql> create table custermers(userid int,name varchar(20),email varchar(30));
Query OK, 0 rows affected (0.26 sec)

mysql> LOAD DATA local INFILE'/home/training/Downloads/Dataset - customer_data.csv.csv INTO TABLE custermers fields terminated by','lines terminated by '\n' IGNORE 1 lines;
PAGER set to stdout
    '> ;
    '> Ctrl-C -- exit!
Aborted
[training@localhost ~]$ mysql --user=training --password=training
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 9
Server version: 5.1.66 Source distribution

Copyright (c) 2000, 2012, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show tables
    -> ;
ERROR 1046 (3D000): No database selected
mysql> use ecommerce;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> show tables;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| clickstream         |
| custermers          |
+---------------------+
2 rows in set (0.00 sec)

mysql> LOAD DATA local INFILE'/home/training/Downloads/Dataset - customer_data.csv.csv INTO TABLE custermers fields terminated by','lines terminated by '\n' IGNORE 1 lines;
PAGER set to stdout
    '> pager less -SFX
    '> DESCRIBE Alerts;
    '> Ctrl-C -- exit!
Aborted
[training@localhost ~]$ mysql --user=training --password=training
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 10
Server version: 5.1.66 Source distribution

Copyright (c) 2000, 2012, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> use ecommerce;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> show tables;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| clickstream         |
| custermers          |
+---------------------+
2 rows in set (0.00 sec)

mysql> LOAD DATA local INFILE'/home/training/Downloads/ecommerce - customer_data.csv.csv INTO TABLE custermers fields terminated by','lines terminated by '\n' IGNORE 1 lines;
PAGER set to stdout
    '> ^C
    '> Ctrl-C -- exit!
Aborted
[training@localhost ~]$ mysql --user=training --password=training
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 5.1.66 Source distribution

Copyright (c) 2000, 2012, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> use ecommerce;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> show tables;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| clickstream         |
| custermers          |
+---------------------+
2 rows in set (0.00 sec)

mysql> LOAD DATA local INFILE'/home/training/Downloads/ecommerce customer_data.csv INTO TABLE custermers fields terminated by','lines terminated by '\n' IGNORE 1 lines;
PAGER set to stdout
    '> ^CCtrl-C -- exit!
Aborted
[training@localhost ~]$ mysql --user=training --password=training
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 12
Server version: 5.1.66 Source distribution

Copyright (c) 2000, 2012, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> use ecommerce;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> use ecommerce;
Database changed
mysql> show tables;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| clickstream         |
| custermers          |
+---------------------+
2 rows in set (0.00 sec)

mysql> LOAD DATA local INFILE'/home/training/Downloads/customer_data.csv INTO TABLE custermers fields terminated by','lines terminated by '\n' IGNORE 1 lines;
PAGER set to stdout
    '> ^Cc4
    '> Ctrl-C -- exit!
Aborted
[training@localhost ~]$ mysql --user=training --password=training
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 13
Server version: 5.1.66 Source distribution

Copyright (c) 2000, 2012, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> use ecommerce;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> show tables;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| clickstream         |
| custermers          |
+---------------------+
2 rows in set (0.00 sec)

mysql> LOAD DATA local INFILE'/home/training/Downloads/customer_data.csv' INTO TABLE custermers fields terminated by','lines terminated by '\n' IGNORE 1 lines;
ERROR 2 (HY000): File '/home/training/Downloads/customer_data.csv' not found (Errcode: 2)
mysql> LOAD DATA local INFILE'/home/training/Downloads/customer.csv' INTO TABLE custermers fields terminated by','lines terminated by '\n' IGNORE 1 lines;
Query OK, 5 rows affected (0.38 sec)
Records: 5  Deleted: 0  Skipped: 0  Warnings: 0

mysql> select *from customers
    -> ;
ERROR 1146 (42S02): Table 'ecommerce.customers' doesn't exist
mysql> select *from custermers;
+--------+----------------+-----------------------------+
| userid | name           | email                       |
+--------+----------------+-----------------------------+
       | | John Doe       | john.doe@example.com
     | 2 | Jane Smith     | jane.smith@example.com
 |     3 | Robert Johnson | robert.johnson@example.com
     | 4 | Lisa Brown     | lisa.brown@example.com
|      5 | Michael Wilson | michael.wilson@example.com  |
+--------+----------------+-----------------------------+
5 rows in set (0.01 sec)

mysql> select *from clickstream
    -> ;
+--------+---------------------+-----------------+
| userid | times               | page            |
+--------+---------------------+-----------------+
      |0 | 2023-01-01 10:00:00 | homepage"
  |    0 | 2023-01-01 10:01:00 | product_page"
      |0 | 2023-01-01 10:02:00 | homepage"
     | 0 | 2023-01-01 10:03:00 | cart_page"
      |0 | 2023-01-01 10:05:00 | homepage"
  |    0 | 2023-01-01 10:06:00 | product_page"
     | 0 | 2023-01-01 10:07:00 | cart_page"
      |0 | 2023-01-01 10:09:00 | homepage"
  |    0 | 2023-01-01 10:10:00 | product_page"
     | 0 | 2023-01-01 10:11:00 | cart_page"
 |     0 | 2023-01-01 10:12:00 | checkout_page"
      |0 | 2023-01-01 10:15:00 | homepage"
|      0 | 2023-01-01 10:16:00 | product_page"   |
+--------+---------------------+-----------------+
13 rows in set (0.00 sec)

mysql> drop table clickstream
    -> ;
Query OK, 0 rows affected (0.13 sec)

mysql> create table clickstream(userid int,timestamp,page varchar(20));
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'page varchar(20))' at line 1
mysql> create table clickstream(userid int,times TIMESTAMP,page varchar(20));
Query OK, 0 rows affected (0.05 sec)

mysql> LOAD DATA local INFILE'/home/training/Downloads/clickstream.csv'INTO TABLE clickstream fields terminated by','lines terminated by'\n' ignore 1 lines;
Query OK, 13 rows affected (0.10 sec)
Records: 13  Deleted: 0  Skipped: 0  Warnings: 0

mysql> select * from clickstream
    -> ;
+--------+---------------------+----------------+
| userid | times               | page           |
+--------+---------------------+----------------+
      |1 | 2023-01-01 10:00:00 | homepage
  |    1 | 2023-01-01 10:01:00 | product_page
      |2 | 2023-01-01 10:02:00 | homepage
     | 2 | 2023-01-01 10:03:00 | cart_page
      |3 | 2023-01-01 10:05:00 | homepage
  |    3 | 2023-01-01 10:06:00 | product_page
     | 3 | 2023-01-01 10:07:00 | cart_page
      |4 | 2023-01-01 10:09:00 | homepage
  |    4 | 2023-01-01 10:10:00 | product_page
     | 4 | 2023-01-01 10:11:00 | cart_page
 |     4 | 2023-01-01 10:12:00 | checkout_page
      |5 | 2023-01-01 10:15:00 | homepage
|      5 | 2023-01-01 10:16:00 | product_page   |
+--------+---------------------+----------------+
13 rows in set (0.00 sec)

mysql> create table purchase;
ERROR 1113 (42000): A table must have at least 1 column
mysql> create table purchase(userid int,timestamp,amount int);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'amount int)' at line 1
mysql> create table purchase(userid int,timestamp, amount int);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ' amount int)' at line 1
mysql> create table purchase(userid int,timestamp, amount int(10));
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ' amount int(10))' at line 1
mysql> create table purchase(userid int,timestamp, amount varchar(20));
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ' amount varchar(20))' at line 1
mysql> create table purchase(userid int,timestamp TIMESTAMP,amount int);
Query OK, 0 rows affected (0.04 sec)

mysql>  LOAD DATA local INFILE'/home/training/Downloads/clickstream.csv'INTO TABLE clickstream fields terminated by','lines terminated by'\n' ignore 1 lines;
Query OK, 13 rows affected (0.00 sec)
Records: 13  Deleted: 0  Skipped: 0  Warnings: 0

mysql>  LOAD DATA local INFILE'/home/training/Downloads/purchase.csv'INTO TABLE purchase fields terminated by','lines terminated by'\n' ignore 1 lines;
Query OK, 5 rows affected (0.00 sec)
Records: 5  Deleted: 0  Skipped: 0  Warnings: 0

mysql> select * from purchase;
+--------+---------------------+--------+
| userid | timestamp           | amount |
+--------+---------------------+--------+
|      1 | 2023-01-01 10:05:00 |    100 |
|      2 | 2023-01-01 10:08:00 |    150 |
|      3 | 2023-01-01 10:09:00 |    200 |
|      4 | 2023-01-01 10:13:00 |    120 |
|      5 | 2023-01-01 10:17:00 |     80 |
+--------+---------------------+--------+
5 rows in set (0.00 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| ecommerce          |
| hue                |
| metastore          |
| movielens          |
| mysql              |
| test               |
| training           |
+--------------------+
8 rows in set (0.00 sec)

mysql> show table
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '' at line 1
mysql> show tables;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| clickstream         |
| custermers          |
| purchase            |
+---------------------+
3 rows in set (0.00 sec)

mysql> 


