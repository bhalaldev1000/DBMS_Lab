# DBMS LAB
## Q1) Write a SQL Query to create a  table with specific columns and constraints?
### Sol:
```
CREATE DATABASES employees;
SHOW TABLES;
SHOW DATABASES;
USE employees;
```
Now Create 5 table
```
CREATE TABLE EMPLOYEES(
EMP_ID int primary key auto_increment ,
Name varchar(100),
Department varchar(50),
Designation varchar(100)
);
CREATE TABLE STUDENTS(
STUDENT_ID int primary key auto_increment ,
Name varchar(100),
Department varchar(50),
Designation varchar(100)
);
CREATE TABLE STAFF(
STAFF_ID int primary key auto_increment ,
Name varchar(100),
Department varchar(50),
Designation varchar(100)
);
CREATE TABLE FACULTY(
FACULTY_ID int primary key auto_increment ,
Name varchar(100),
Department varchar(50),
Designation varchar(100)
);
CREATE TABLE PARENTS(
PARENTS_ID int primary key auto_increment ,
Name varchar(100),
Department varchar(50),
Designation varchar(100)
);
CREATE TABLE GAMERS(
GAMERS_ID int primary key auto_increment ,
Name varchar(100),
Department varchar(50),
Designation varchar(100)
);
```
## Q2) Write a SQL Query to add a new column to an existing table?
### Sol:
```
ALTER TABLE EMPLOYEES ADD MobNo int unique;
ALTER TABLE STUDENTS ADD MobNo int unique;
ALTER TABLE STAFF ADD MobNo int unique;
ALTER TABLE FACULTY ADD MobNo int unique;
ALTER TABLE PARENTS ADD MobNo int unique;
ALTER TABLE GAMERS ADD MobNo int unique;
```
Now Check Description of the database
```
desc employees;
```
### Output:
```
+-------------+--------------+------+-----+---------+----------------+
| Field       | Type         | Null | Key | Default | Extra          |
+-------------+--------------+------+-----+---------+----------------+
| EMP_ID      | int          | NO   | PRI | NULL    | auto_increment |
| Name        | varchar(100) | YES  |     | NULL    |                |
| Department  | varchar(50)  | YES  |     | NULL    |                |
| Designation | varchar(100) | YES  |     | NULL    |                |
| MobNo       | int          | YES  | UNI | NULL    |                |
+-------------+--------------+------+-----+---------+----------------+
5 rows in set (0.01 sec)
```
## Q3) Write a SQL Query to change data type of an existing column in a table?
### Sol:
```
ALTER TABLE EMPLOYEES MODIFY MobNo varchar(10) unique;
```
Now Check Description of the database
```
desc employees;
```
### Output:
```
+-------------+--------------+------+-----+---------+----------------+
| Field       | Type         | Null | Key | Default | Extra          |
+-------------+--------------+------+-----+---------+----------------+
| EMP_ID      | int          | NO   | PRI | NULL    | auto_increment |
| Name        | varchar(100) | YES  |     | NULL    |                |
| Department  | varchar(50)  | YES  |     | NULL    |                |
| Designation | varchar(100) | YES  |     | NULL    |                |
| MobNo       | varchar(10)  | YES  | UNI | NULL    |                |
+-------------+--------------+------+-----+---------+----------------+
5 rows in set (0.00 sec)
```

