# Class 3
## Data Types
- Numeric -> সংখ্যাজাতীয়
  - Integer Types (Exact Value) - INTEGER, INT, SMALLINT, TINYINT, MEDIUMINT, BIGINT
  - Fixed-Point Types (Exact Value) - DECIMAL, NUMERIC
  - Floating-Point Types (Approximate Value) - FLOAT, DOUBLE
    - দশমিক সংখ্যা -> দশমিকের পর কিছু থাকে -> 10.1, 2.5, 3.333
  - Bit-Value Type - BIT
- Date and Time -> তারিখ এবং সময় সংক্রান্ত
  - DATE -> 'YYYY-MM-DD'
  - TIME -> 'hhh:mm:ss'
  - DATETIME -> 'YYYY-MM-DD hh:mm:ss'
  - TIMESTAMP -> 'YYYY-MM-DD hh:mm:ss'
- String -> অক্ষর, শব্দ ইত্যাদি
  - The CHAR and VARCHAR Types
  - The BINARY and VARBINARY Types
  - The BLOB and TEXT Types
  - The VECTOR Type
  - The ENUM Type
  - The SET Type

## Binary
- 0, 1
- 0 1 10 11 100 101 110 111
- 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10

## Inserting Data Into A Table
- INSERT INTO students (name, phone, email, roll, class) VALUES ('Miftah', '01742855755', 'miftah@miftahcoding.com', '1', '13');

## Show Data in A Table
- 

## Today's Queries
```
MariaDB [(none)]> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| ecommerce          |
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| test               |
+--------------------+
6 rows in set (0.008 sec)

MariaDB [(none)]> CREATE DATABASE neuralgem;
Query OK, 1 row affected (0.003 sec)

MariaDB [(none)]> USE neuralgem;
Database changed
MariaDB [neuralgem]> SHOW tables;
Empty set (0.001 sec)

MariaDB [neuralgem]> CREATE TABLE students(
    -> name VARCHAR(100),
    -> phone VARCHAR(15),
    -> email VARCHAR(100),
    -> roll VARCHAR(10),
    -> class ENUM('1', '2', '3', '4', '5', '6','7','8','9','10','11','12','13'));
Query OK, 0 rows affected (0.028 sec)
MariaDB [neuralgem]> DESC students;
+-------+---------------------------------------------------------------+------+-----+---------+-------+
| Field | Type                                                          | Null | Key | Default | Extra |
+-------+---------------------------------------------------------------+------+-----+---------+-------+
| name  | varchar(100)                                                  | YES  |     | NULL    |       |
| phone | varchar(15)                                                   | YES  |     | NULL    |       |
| email | varchar(100)                                                  | YES  |     | NULL    |       |
| roll  | varchar(10)                                                   | YES  |     | NULL    |       |
| class | enum('1','2','3','4','5','6','7','8','9','10','11','12','13') | YES  |     | NULL    |       |
+-------+---------------------------------------------------------------+------+-----+---------+-------+
5 rows in set (0.014 sec)

MariaDB [neuralgem]> DESCRIBE students;
+-------+---------------------------------------------------------------+------+-----+---------+-------+
| Field | Type                                                          | Null | Key | Default | Extra |
+-------+---------------------------------------------------------------+------+-----+---------+-------+
| name  | varchar(100)                                                  | YES  |     | NULL    |       |
| phone | varchar(15)                                                   | YES  |     | NULL    |       |
| email | varchar(100)                                                  | YES  |     | NULL    |       |
| roll  | varchar(10)                                                   | YES  |     | NULL    |       |
| class | enum('1','2','3','4','5','6','7','8','9','10','11','12','13') | YES  |     | NULL    |       |
+-------+---------------------------------------------------------------+------+-----+---------+-------+
5 rows in set (0.002 sec)
MariaDB [neuralgem]> INSERT INTO students (name, phone, email, roll, class) VALUES ('Miftah', '01742855755', 'miftah@miftahcoding.com', '1', '13');
Query OK, 1 row affected (0.010 sec)

MariaDB [neuralgem]> SELECT * FROM students;
+--------+-------------+-------------------------+------+-------+
| name   | phone       | email                   | roll | class |
+--------+-------------+-------------------------+------+-------+
| Miftah | 01742855755 | miftah@miftahcoding.com | 1    | 13    |
+--------+-------------+-------------------------+------+-------+
1 row in set (0.004 sec)


```