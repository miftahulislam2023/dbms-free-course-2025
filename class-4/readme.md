# Class 4
## Convention
- Command বড় হাতে লেখা
- SHOW, CREATE, TABLE, DATABASE, USE

## CRUD
- Create
- Read
- Update
- Delete

## Queries
```
MariaDB [(none)]> quit
Bye
MariaDB [(none)]> exit
Bye
MariaDB [(none)]> \q
Bye
MariaDB [(none)]> CREATE DATABASE asd;
Query OK, 1 row affected (0.001 sec)

MariaDB [(none)]> DROP DATABASE asd;
Query OK, 0 rows affected, 2 warnings (0.002 sec)

MariaDB [neuralgem]> RENAME TABLE students TO student;
Query OK, 0 rows affected (0.011 sec)


MariaDB [neuralgem]> SELECT * FROM student;
ERROR 1146 (42S02): Table 'neuralgem.student' doesn't exist
MariaDB [neuralgem]> SELECT * FROM students;
+---------------+-------------+----------------------------+------+-------+
| name          | phone       | email                      | roll | class |
+---------------+-------------+----------------------------+------+-------+
| Miftah        | 01742855755 | miftah@miftahcoding.com    | 1    | 13    |
| a             | 1221        | as@gmail.com               | 12   | 5     |
| a             | 1221        | as@gmail.com               | 12   | 5     |
| a             | 1221        | as@gmail.com               | 12   | 5     |
| a             | 1221        | as@gmail.com               | 12   | 5     |
| a             | 1221        | as@gmail.com               | 12   | 5     |
| a             | 1221        | as@gmail.com               | 12   | 5     |
| a             | 1221        | as@gmail.com               | 12   | 5     |
| Fahim Ahmed   | 01712345678 | fahim.ahmed@example.com.bd | 201  | 8     |
| Nusrat Jahan  | 01923456789 | nusrat.jahan@webmail.net   | 202  | 10    |
| Kazi Alam     | 01834567890 | kazi.alam@school.org       | 203  | 9     |
| Tanisha Islam | 01745678901 | tanisha.islam@mail.com     | 204  | 11    |
| Rahman Khan   | 01656789012 | rahman.khan@bdmail.net     | 205  | 7     |
| Miftah        | 01742855755 | miftah@miftahcoding.com    | 1    | 13    |
+---------------+-------------+----------------------------+------+-------+
14 rows in set (0.002 sec)

MariaDB [neuralgem]> ALTER TABLE students ADD COLUMN fathername VARCHAR(100);
Query OK, 0 rows affected (0.021 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [neuralgem]> SELECT * FROM students;
+---------------+-------------+----------------------------+------+-------+------------+
| name          | phone       | email                      | roll | class | fathername |
+---------------+-------------+----------------------------+------+-------+------------+
| Miftah        | 01742855755 | miftah@miftahcoding.com    | 1    | 13    | NULL       |
| a             | 1221        | as@gmail.com               | 12   | 5     | NULL       |
| a             | 1221        | as@gmail.com               | 12   | 5     | NULL       |
| a             | 1221        | as@gmail.com               | 12   | 5     | NULL       |
| a             | 1221        | as@gmail.com               | 12   | 5     | NULL       |
| a             | 1221        | as@gmail.com               | 12   | 5     | NULL       |
| a             | 1221        | as@gmail.com               | 12   | 5     | NULL       |
| a             | 1221        | as@gmail.com               | 12   | 5     | NULL       |
| Fahim Ahmed   | 01712345678 | fahim.ahmed@example.com.bd | 201  | 8     | NULL       |
| Nusrat Jahan  | 01923456789 | nusrat.jahan@webmail.net   | 202  | 10    | NULL       |
| Kazi Alam     | 01834567890 | kazi.alam@school.org       | 203  | 9     | NULL       |
| Tanisha Islam | 01745678901 | tanisha.islam@mail.com     | 204  | 11    | NULL       |
| Rahman Khan   | 01656789012 | rahman.khan@bdmail.net     | 205  | 7     | NULL       |
| Miftah        | 01742855755 | miftah@miftahcoding.com    | 1    | 13    | NULL       |
+---------------+-------------+----------------------------+------+-------+------------+
14 rows in set (0.001 sec)

MariaDB [neuralgem]> DESC students;
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| Field      | Type                                                          | Null | Key | Default | Extra |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| name       | varchar(100)                                                  | YES  |     | NULL    |       |
| phone      | varchar(15)                                                   | YES  |     | NULL    |       |
| email      | varchar(100)                                                  | YES  |     | NULL    |       |
| roll       | varchar(10)                                                   | YES  |     | NULL    |       |
| class      | enum('1','2','3','4','5','6','7','8','9','10','11','12','13') | YES  |     | NULL    |       |
| fathername | varchar(100)                                                  | YES  |     | NULL    |       |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
6 rows in set (0.004 sec)

MariaDB [neuralgem]> ALTER TABLE students MODIFY COLUMN name VARCHAR(50);
Query OK, 14 rows affected (0.035 sec)             
Records: 14  Duplicates: 0  Warnings: 0

MariaDB [neuralgem]> DESC students;
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| Field      | Type                                                          | Null | Key | Default | Extra |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| name       | varchar(50)                                                   | YES  |     | NULL    |       |
| phone      | varchar(15)                                                   | YES  |     | NULL    |       |
| email      | varchar(100)                                                  | YES  |     | NULL    |       |
| roll       | varchar(10)                                                   | YES  |     | NULL    |       |
| class      | enum('1','2','3','4','5','6','7','8','9','10','11','12','13') | YES  |     | NULL    |       |
| fathername | varchar(100)                                                  | YES  |     | NULL    |       |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
6 rows in set (0.003 sec)

MariaDB [neuralgem]> DESC students;
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| Field      | Type                                                          | Null | Key | Default | Extra |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| name       | varchar(50)                                                   | YES  |     | NULL    |       |
| phone      | varchar(15)                                                   | YES  |     | NULL    |       |
| email      | varchar(100)                                                  | YES  |     | NULL    |       |
| roll       | varchar(10)                                                   | YES  |     | NULL    |       |
| class      | enum('1','2','3','4','5','6','7','8','9','10','11','12','13') | YES  |     | NULL    |       |
| fathername | varchar(100)                                                  | YES  |     | NULL    |       |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
6 rows in set (0.003 sec)

MariaDB [neuralgem]> ALTER TABLE students MODIFY COLUMN fathername VARCHAR(100) FIRST;
Query OK, 0 rows affected (0.010 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [neuralgem]> DESC students;
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| Field      | Type                                                          | Null | Key | Default | Extra |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| fathername | varchar(100)                                                  | YES  |     | NULL    |       |
| name       | varchar(50)                                                   | YES  |     | NULL    |       |
| phone      | varchar(15)                                                   | YES  |     | NULL    |       |
| email      | varchar(100)                                                  | YES  |     | NULL    |       |
| roll       | varchar(10)                                                   | YES  |     | NULL    |       |
| class      | enum('1','2','3','4','5','6','7','8','9','10','11','12','13') | YES  |     | NULL    |       |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
6 rows in set (0.003 sec)

MariaDB [neuralgem]> ALTER TABLE students MODIFY COLUMN roll VARCHAR(10) AFTER name;
Query OK, 0 rows affected (0.009 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [neuralgem]> DESC students;
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| Field      | Type                                                          | Null | Key | Default | Extra |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
| fathername | varchar(100)                                                  | YES  |     | NULL    |       |
| name       | varchar(50)                                                   | YES  |     | NULL    |       |
| roll       | varchar(10)                                                   | YES  |     | NULL    |       |
| phone      | varchar(15)                                                   | YES  |     | NULL    |       |
| email      | varchar(100)                                                  | YES  |     | NULL    |       |
| class      | enum('1','2','3','4','5','6','7','8','9','10','11','12','13') | YES  |     | NULL    |       |
+------------+---------------------------------------------------------------+------+-----+---------+-------+
6 rows in set (0.002 sec)

MariaDB [neuralgem]> SELECT * FROM students WHERE class = '10';
+--------------+------+-------------+---------------------------+-------+
| name         | roll | phone       | email                     | class |
+--------------+------+-------------+---------------------------+-------+
| Nusrat Jahan | 202  | 01923456789 | nusrat.jahan@webmail.net  | 10    |
| Shirin Akter | 209  | 01688901234 | shirin.akter@web.com      | 10    |
| Sadia Afrin  | 217  | 01677901234 | sadia.afrin@bdstudent.net | 10    |
| Sonia Reza   | 224  | 01855234567 | sonia.reza@bdinternet.org | 10    |
+--------------+------+-------------+---------------------------+-------+
4 rows in set (0.001 sec)

MariaDB [neuralgem]> SELECT * FROM students WHERE roll < 205;
+---------------+------+-------------+----------------------------+-------+
| name          | roll | phone       | email                      | class |
+---------------+------+-------------+----------------------------+-------+
| Miftah        |    1 | 01742855755 | miftah@miftahcoding.com    | 13    |
| a             |   12 | 1221        | as@gmail.com               | 5     |
| a             |   12 | 1221        | as@gmail.com               | 5     |
| a             |   12 | 1221        | as@gmail.com               | 5     |
| a             |   12 | 1221        | as@gmail.com               | 5     |
| a             |   12 | 1221        | as@gmail.com               | 5     |
| a             |   12 | 1221        | as@gmail.com               | 5     |
| a             |   12 | 1221        | as@gmail.com               | 5     |
| Fahim Ahmed   |  201 | 01712345678 | fahim.ahmed@example.com.bd | 8     |
| Nusrat Jahan  |  202 | 01923456789 | nusrat.jahan@webmail.net   | 10    |
| Kazi Alam     |  203 | 01834567890 | kazi.alam@school.org       | 9     |
| Tanisha Islam |  204 | 01745678901 | tanisha.islam@mail.com     | 11    |
| Miftah        |    1 | 01742855755 | miftah@miftahcoding.com    | 13    |
+---------------+------+-------------+----------------------------+-------+
13 rows in set (0.001 sec)

```