# Class 7

## Auto Increment
- স্বয়ংক্রিয়ভাবে বৃদ্ধি পাওয়া

## Queries
```
MariaDB [neuralgem]> CREATE TABLE admin (
    -> name VARCHAR(50),
    -> phone VARCHAR(15),
    -> email VARCHAR(50),
    -> address VARCHAR(100),
    -> created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    -> updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    -> id INT AUTO_INCREMENT);
ERROR 1075 (42000): Incorrect table definition; there can be only one auto column and it must be defined as a key
MariaDB [neuralgem]> 

MariaDB [neuralgem]> CREATE TABLE admin ( name VARCHAR(50), phone VARCHAR(15), email VARCHAR(50), address VARCHAR(100), created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP, updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP, id INT PRIMARY KEY AUTO_INCREMENT);
Query OK, 0 rows affected (0.016 sec)

INSERT INTO admin (name, phone, email, address) VALUES
('Rahman A. Khan', '01712345601', 'rahman.khan@example.com', '12/A, Road 5, Mirpur, Dhaka'),
('Sadia Islam', '01823456702', 'sadia.islam@example.com', 'House 30, Lane 10, Agrabad, Chittagong'),
('Mohammad Hossain', '01934567803', 'mohammad.h@example.com', 'Main Road, Khulna Sadar'),
('Ayesha Begum', '01745678904', 'ayesha.b@example.com', 'Upazila Complex, Boalia, Rajshahi'),
('Jasim Uddin', '01856789005', 'jasim.uddin@example.com', 'Zindabazar, Sylhet'),
('Fahima Akter', '01967890106', 'fahima.a@example.com', 'Cantonment Area, Rangpur'),
('Kazi M. Ali', '01778901207', 'kazi.ali@example.com', 'Station Road, Barisal'),
('Nusrat Jahan', '01889012308', 'nusrat.j@example.com', 'Notredame Road, Mymensingh'),
('Elias Chowdhury', '01990123409', 'elias.ch@example.com', 'Court Hill, Kandirpar, Comilla'),
('Shirin Sultana', '01701234510', 'shirin.s@example.com', 'Kalibari Road, Jessore'),
('Md. Kamal', '01812345611', 'md.kamal@example.com', 'Borobazar, Bogra'),
('Rina Khatun', '01923456712', 'rina.khatun@example.com', 'College Road, Dinajpur'),
('Sagor Ahmed', '01734567813', 'sagor.ahmed@example.com', 'Shahbagh, Dhaka'),
('Tanjina Akter', '01845678914', 'tanjina.a@example.com', 'Oxygen Mor, Chittagong'),
('Ashraf Ali', '01956789015', 'ashraf.ali@example.com', 'Goalpara, Khulna'),
('Laila Rahman', '01767890116', 'laila.r@example.com', 'New Market Area, Rajshahi'),
('Imran Hassan', '01878901217', 'imran.h@example.com', 'Shahjalal Uposhohor, Sylhet'),
('Priya Das', '01989012318', 'priya.das@example.com', 'Zero Point, Rangpur'),
('Hasan Khan', '01790123419', 'hasan.khan@example.com', 'Alekanda, Barisal'),
('Suma Begum', '01801234520', 'suma.b@example.com', 'Muktagacha, Mymensingh'),
('Zahidul Islam', '01912345621', 'zahidul.i@example.com', 'Laksam Road, Comilla'),
('Sonia Akhter', '01723456722', 'sonia.a@example.com', 'Khulna Road, Jessore'),
('Tareq Aziz', '01834567823', 'tareq.aziz@example.com', 'Sutrapur, Dhaka'),
('Rumana Haq', '01945678924', 'rumana.h@example.com', 'GEC Circle, Chittagong'),
('Faruque Mia', '01756789025', 'faruque.m@example.com', 'Shiromoni, Khulna'),
('Mita Devi', '01867890126', 'mita.d@example.com', 'Laxmipur, Rajshahi'),
('Sanaul Alam', '01978901227', 'sanaul.a@example.com', 'Ambarkhana, Sylhet'),
('Bristi Roy', '01789012328', 'bristi.r@example.com', 'Mithapukur, Rangpur'),
('Shafiqul Islam', '01890123429', 'shafiqul.i@example.com', 'Patuakhali Road, Barisal'),
('Jannatul Ferdous', '01901234530', 'jannatul.f@example.com', 'Jamalpur Road, Mymensingh'),
('Ruhul Amin', '01713456731', 'ruhul.a@example.com', 'Chawkbazar, Comilla'),
('Afsana Mimi', '01824567832', 'afsana.m@example.com', 'Monirampur, Jessore'),
('Alif Zaman', '01935678933', 'alif.z@example.com', 'Tejgaon, Dhaka'),
('Shaila Noor', '01746789034', 'shaila.n@example.com', 'Patiya, Chittagong'),
('Rafiqul Bashar', '01857890135', 'rafiqul.b@example.com', 'Bagerhat Road, Khulna'),
('Sumaiya Z. M', '01968901236', 'sumaiya.z@example.com', 'Naogaon Road, Rajshahi'),
('Kamrul Hasan', '01779012337', 'kamrul.h@example.com', 'Habiganj Road, Sylhet'),
('Maliha Tabassum', '01880123438', 'maliha.t@example.com', 'Kurigram Road, Rangpur'),
('Sajib Talukder', '01991234539', 'sajib.t@example.com', 'Bhola Road, Barisal'),
('Nargis Akter', '01702345640', 'nargis.a@example.com', 'Netrokona Sadar, Mymensingh'),
('Abir Khan', '01813456741', 'abir.khan@example.com', 'Brahmanbaria Road, Comilla'),
('Mitu Sarkar', '01924567842', 'mitu.s@example.com', 'Kushtia Road, Jessore'),
('Tawhidul Haque', '01735678943', 'tawhidul.h@example.com', 'Gulshan 1, Dhaka'),
('Dipa Barua', '01846789044', 'dipa.barua@example.com', 'Cox\'s Bazar Road, Chittagong'),
('Akbar Ali', '01957890145', 'akbar.ali@example.com', 'Satkhira Road, Khulna'),
('Nishat Anjum', '01768901246', 'nishat.a@example.com', 'Chapainawabganj Rd, Rajshahi'),
('Shamsul H', '01879012347', 'shamsul.h@example.com', 'Sunamganj Road, Sylhet'),
('Sumi Islam', '01980123448', 'sumi.i@example.com', 'Dinajpur Sadar, Rangpur'),
('Babu Mia', '01791234549', 'babu.mia@example.com', 'Pirojpur Road, Barisal'),
('Roksana Pervin', '01802345650', 'roksana.p@example.com', 'Sherpur Road, Mymensingh');

MariaDB [neuralgem]> ALTER TABLE admin MODIFY COLUMN id INT PRIMARY KEY AUTO_INCREMENT FIRST;
ERROR 1068 (42000): Multiple primary key defined
MariaDB [neuralgem]> ALTER TABLE admin MODIFY COLUMN id AUTO_INCREMENT FIRST;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'FIRST' at line 1
MariaDB [neuralgem]> ALTER TABLE admin MODIFY COLUMN id INT AUTO_INCREMENT FIRST;
Query OK, 0 rows affected (0.020 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [neuralgem]> desc admin;
+------------+--------------+------+-----+---------------------+-------------------------------+
| Field      | Type         | Null | Key | Default             | Extra                         |
+------------+--------------+------+-----+---------------------+-------------------------------+
| id         | int(11)      | NO   | PRI | NULL                | auto_increment                |
| name       | varchar(50)  | NO   |     | NULL                |                               |
| phone      | varchar(15)  | NO   |     | NULL                |                               |
| email      | varchar(50)  | NO   |     | NULL                |                               |
| address    | varchar(100) | YES  |     | NULL                |                               |
| created_at | timestamp    | NO   |     | current_timestamp() |                               |
| updated_at | timestamp    | NO   |     | current_timestamp() | on update current_timestamp() |
+------------+--------------+------+-----+---------------------+-------------------------------+
7 rows in set (0.003 sec)

```