# Class 5

## Queries
```
MariaDB [neuralgem]> SELECT * FROM students WHERE phone IS NULL;
+------+------+-------+-------+-------+
| name | roll | phone | email | class |
+------+------+-------+-------+-------+
| b    |   67 | NULL  | NULL  | NULL  |
| c    |   87 | NULL  | NULL  | NULL  |
+------+------+-------+-------+-------+
2 rows in set (0.003 sec)

MariaDB [neuralgem]> SELECT * FROM students WHERE class = '8' AND roll > 200;
+------------------+------+-------------+----------------------------+-------+
| name             | roll | phone       | email                      | class |
+------------------+------+-------------+----------------------------+-------+
| Fahim Ahmed      |  201 | 01712345678 | fahim.ahmed@example.com.bd | 8     |
| Kamaluddin Mia   |  210 | 01799123456 | kamal.mia@bdpost.net       | 8     |
| Badrul Hasan     |  218 | 01788123456 | badrul.h@school.com        | 8     |
| Waliullah Sheikh |  225 | 01666567890 | waliullah.s@schoolnet.co   | 8     |
+------------------+------+-------------+----------------------------+-------+
4 rows in set (0.002 sec)

MariaDB [neuralgem]> SELECT * FROM students WHERE class = '8' AND roll < 200;
Empty set (0.001 sec)

MariaDB [neuralgem]> SELECT * FROM students WHERE class = '8' AND roll > 205;
+------------------+------+-------------+--------------------------+-------+
| name             | roll | phone       | email                    | class |
+------------------+------+-------------+--------------------------+-------+
| Kamaluddin Mia   |  210 | 01799123456 | kamal.mia@bdpost.net     | 8     |
| Badrul Hasan     |  218 | 01788123456 | badrul.h@school.com      | 8     |
| Waliullah Sheikh |  225 | 01666567890 | waliullah.s@schoolnet.co | 8     |
+------------------+------+-------------+--------------------------+-------+
3 rows in set (0.001 sec)

MariaDB [neuralgem]> 

MariaDB [neuralgem]> SELECT * FROM students WHERE class = '8' OR roll < 200;
+------------------+------+-------------+----------------------------+-------+
| name             | roll | phone       | email                      | class |
+------------------+------+-------------+----------------------------+-------+
| Miftah           |    1 | 01742855755 | miftah@miftahcoding.com    | 13    |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| Fahim Ahmed      |  201 | 01712345678 | fahim.ahmed@example.com.bd | 8     |
| Miftah           |    1 | 01742855755 | miftah@miftahcoding.com    | 13    |
| Kamaluddin Mia   |  210 | 01799123456 | kamal.mia@bdpost.net       | 8     |
| Badrul Hasan     |  218 | 01788123456 | badrul.h@school.com        | 8     |
| Waliullah Sheikh |  225 | 01666567890 | waliullah.s@schoolnet.co   | 8     |
| b                |   67 | NULL        | NULL                       | NULL  |
| c                |   87 | NULL        | NULL                       | NULL  |
+------------------+------+-------------+----------------------------+-------+
15 rows in set (0.003 sec)

MariaDB [neuralgem]> SELECT * FROM students WHERE class = '8' AND roll < 200;
Empty set (0.000 sec)

MariaDB [neuralgem]> SELECT * FROM students WHERE class = '8' AND roll < 210;
+-------------+------+-------------+----------------------------+-------+
| name        | roll | phone       | email                      | class |
+-------------+------+-------------+----------------------------+-------+
| Fahim Ahmed |  201 | 01712345678 | fahim.ahmed@example.com.bd | 8     |
+-------------+------+-------------+----------------------------+-------+
1 row in set (0.001 sec)

MariaDB [neuralgem]> SELECT * FROM students ORDER BY name ASC;
+------------------+------+-------------+----------------------------+-------+
| name             | roll | phone       | email                      | class |
+------------------+------+-------------+----------------------------+-------+
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| a                |   12 | 1221        | as@gmail.com               | 5     |
| Alomgir Kabir    |  216 | 01866456789 | alomgir.kabir@example.com  | 6     |
| Ashraful Haque   |  208 | 01877456789 | a.haque@edu.com.bd         | 9     |
| b                |   67 | NULL        | NULL                       | NULL  |
| Badrul Hasan     |  218 | 01788123456 | badrul.h@school.com        | 8     |
| c                |   87 | NULL        | NULL                       | NULL  |
| Dilruba Khan     |  222 | 01733678901 | dilruba.k@netmail.net      | 5     |
| Elias Chowdhury  |  219 | 01999456789 | elias.chowdhury@email.org  | 11    |
| Fahim Ahmed      |  201 | 01712345678 | fahim.ahmed@example.com.bd | 8     |
| Farzana Yeasmin  |  211 | 01911234567 | farzana.y@schoolmail.co    | 11    |
| Jannatul Ferdous |  220 | 01811789012 | jannatul.f@bdwebmail.co    | 7     |
| Kamaluddin Mia   |  210 | 01799123456 | kamal.mia@bdpost.net       | 8     |
| Kazi Alam        |  203 | 01834567890 | kazi.alam@school.org       | 9     |
| Laila Rahman     |  213 | 01633890123 | laila.rahman@myweb.org     | 12    |
| Miftah           |    1 | 01742855755 | miftah@miftahcoding.com    | 13    |
| Miftah           |    1 | 01742855755 | miftah@miftahcoding.com    | 13    |
| Mirza Hafiz      |  223 | 01944901234 | mirza.hafiz@mailserver.com | 9     |
| Mohammad Hossain |  206 | 01755123456 | m.hossain@bdmail.org       | 12    |
| Nasir Uddin      |  212 | 01822567890 | nasir.uddin@mail.com.bd    | 7     |
| Nusrat Jahan     |  202 | 01923456789 | nusrat.jahan@webmail.net   | 10    |
| Rahman Khan      |  205 | 01656789012 | rahman.khan@bdmail.net     | 7     |
| Rumana Sultana   |  215 | 01955789012 | rumana.sultana@mail.bd     | 9     |
| Sadia Afrin      |  217 | 01677901234 | sadia.afrin@bdstudent.net  | 10    |
| Shafiqul Islam   |  214 | 01744123456 | shafiqul.i@test.net        | 5     |
| Shirin Akter     |  209 | 01688901234 | shirin.akter@web.com       | 10    |
| Sonia Reza       |  224 | 01855234567 | sonia.reza@bdinternet.org  | 10    |
| Tanisha Islam    |  204 | 01745678901 | tanisha.islam@mail.com     | 11    |
| Tariqul Islam    |  221 | 01622345678 | tariqul.i@sample.com.bd    | 12    |
| Waliullah Sheikh |  225 | 01666567890 | waliullah.s@schoolnet.co   | 8     |
| Zainab Begum     |  207 | 01966789012 | zainab.b@examplebd.net     | 6     |
+------------------+------+-------------+----------------------------+-------+
36 rows in set (0.003 sec)

```