# MySQL
---------
* It is datamanagement system that is used to store data in specific format.
* We can store data in two ways.
  1. Temporary Storage
  2. Permanent Storage

## Temporary
-------------
* We can store data during runtime of the program with the help of variable, structure, arrays etc. These type of data exist only when the programming is in execution.

## Permanent Storage
---------------------
* Now to store data permanently we can used specific database like MySQL, Oracle etc.
* MySQL is a RDMBS means Relational Database Management System that is used to store data in specific format.
* In RDBMS database objects like tables, views, indexers etc is used and it is linked to each other.

## Types of Command in MYSQL
----------------------------
# 1. DDL
* It stands for data definition language.
* We will used DDL  for queries related to structure of Database and its object like table,view,etc.
* Create, alter, truncate and drop commands comes under DDL Category.
  
### Table:
* It is the combination of rows and columns.
* Each row of table is called tuple.
* Each column of table is called Attributes.
#### i. show databases
* This command is used to show list of database command to create database.

#### ii. Command to Create database
    create database mydemo;
* We used DDL command to create database.
* Syntax to create tables

      create table <table_Name>(column_name Datatype(size),....);
Example:

    create table Student(id int,sname varchar(250),sage int);
* Create table with primary key

      create table Product(id int primary key,pname varchar(200),pbrand varchar(40));
#### Primary Key
* Primary key is a key that is used to identify the record uniquely.
* Primary key column cann't be null.
* We can used primary to perform searching, deleting and in updation of the record.


Note: Creating table we have to mention the name of our database where table is created.
#### iV. To select database we used below commands
* Syntax :

      use DatabaseName;
* To show structure of table we used below syntax:

      desc TableName;


# 2. DML

#### Insertion of record in all columns of a table
* We used DML to insert any kind of records in a table.
* Syntax to insert record in all columns of a table :

      insert into <Table_Name> values(value1,value2,value3,.....);
  Example

      insert into Product values(1,'Laptop','HP');

* Syntax to insert record in specific columns of a table :

      insert into <table_Name>(Column_Name1,Column_Name2,...) values(Value1,Value2,...);

Example:

    insert into Product(id,pname) values(2,'ASUS');

#### NOT NULL
-----------------
    create table employee(eid,int Not null, ename varchar(250),age int);
    insert into employee(eid,ename,age) values(1,'James',10);

* Not Null is a constraint that is used to check the values of columns can not be null.
* Means if we created any tables and defining not null constraint in any column, then we must insert record on that column.
* MySQL is case insensitive means database and it's related object name can be in upper and lowercase.

* Note: To Store string type value in columns it should be in single or double quotes.

# 5. DCL
# 6. TCL
# 7. DQL

   
