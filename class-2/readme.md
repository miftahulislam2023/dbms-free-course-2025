# Class 2

## Project Based Learning
- E-commerce Website এর Database Design করব
  - Variant manually ইনপুট দিতে হচ্ছে
  - Date manually ইনপুট দিতে হচ্ছে
  - Customer table এ প্রোডাক্ট ইনফর্মেশন কেন থাকবে?
- Solution হল রিলেশন ইউজ করা

## Sheets/Excel
- Row, Column, Cell

## ১ম কাজ - Database তৈরি করা - Done
- SHOW databases; -> Database যেগুলো আছে অলরেডি সেগুলো দেখানো
- CREATE database e-commerce;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near '-commerce' at line 1
- CREATE database ecommerce;
Query OK, 1 row affected (0.004 sec)


## ২য় কাজ - Database এ প্রবেশ করা
- SELECT database ecommerce;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'ecommerce' at line 1
- USE ecommerce; -> Database এ প্রবেশ করার কমান্ড

## Database এর কমান্ড শিখতে হবে
- ভিন্ন ভিন্ন ল্যাঙ্গুয়েজে কমান্ড ভিন্ন ভিন্ন হয়ে থাকে
- MySQL, MongoDB

## ৩য় কাজ - Database এ Table বানানো
- CREATE TABLE product(
    name VARCHAR(100),
    description VARCHAR(100),
    price INT,
    variant VARCHAR(100));
- SHOW tables;
+---------------------+
| Tables_in_ecommerce |
+---------------------+
| product             |
+---------------------+
1 row in set (0.000 sec)