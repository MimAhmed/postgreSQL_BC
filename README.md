
# PostgreSQL_Brilliant Cloud Research

# Welcome to My Documentation
This Tutorial is part of a  Cloud Research Project By **Brilliant Cloud Research Group** Bangladesh 
* PostgreSQL Official Site: [https://www.postgresql.org](https://www.postgresql.org/)
* How To Install PostgreSQL on Windows: [https://bit.ly/30Ev1A7](https://bit.ly/30Ev1A7)
* PSQL Quick Referrence: [http://gpdb.docs.pivotal.io/archive/gs/43/pdf/PSQLQuickRef.pdf](http://gpdb.docs.pivotal.io/archive/gs/43/pdf/PSQLQuickRef.pdf)

# What is PostgreSql ?
**PostgreSQL** is a powerful, open source object-relational database system. PostgreSql uses sql as main query language.
# Why Use PostgreSql ?
* PostgreSQL is a free open source software (OSS) 
* PostgreSQL is scalable, and it gives high performance.
* PostgreSQL is very reliable; it rarely crashes. Also, PostgreSQL is ACID  
compliant, which means that it can tolerate some hardware failure. 

## Create a Database
You can use *CREATE DATABASE* command to Create a Database
**Example:**
```
CREATE DATABASE Student;
```
Must use `;` at the end of the statement otherwise the command not work.

![CREATE DATABASE](https://i.ibb.co/9tz2tQB/CREATE-DATABASE.png)

## Delete a Database
You can use *DROP DATABASE* command to Delete a Database
**Example:**
```
DROP DATABASE Student;
```
Must use `;` at the end of the statement otherwise the command not work.

![DELETE DATABASE](https://i.ibb.co/Z11S0Fg/DELETE-DATABASE.png)
# How To Create a Table
A table consists of rows and columns. Tables allow you to store structured data like customers, products, employees, etc.

***Steps to Create a Table in PostgreSQ***
First you Have to connect the database which you want to create a table.
1.  First, specify the name of the **table** after the **CREATE TABLE** keywords.
2.  Second, **creating** a **table** that already exists will result in a error. ...
3.  Third, specify a comma-separated list of **table** columns. ...
4.  Finally, specify the **table** constraints including primary key, foreign key, and check constraints.
**To Create a Table in Postgresql Use:** ``CREATE TABLE`` Keyword. **Example:**``CREATE TABLE student_info;``

![CREATE TABLE](https://i.ibb.co/5sGjXdC/TABLE-CREATE.png)
# Insert Values into Table
![INSERT VALUES](https://i.ibb.co/2qQGndZ/insert.png)
# Create a User and Role
**What is a User?**
Every database cluster contains a set of database users.Users own database objects (for example, tables) and can assign privileges on those objects to other users to control who has access to which object.

**CREATE USER adds a new user to a PostgreSQL database cluster.**

**Example :** ```CREATE USER Rahim WITH PASSWORD 'rahim1234';```

![CREATE USER](https://i.ibb.co/NYDjQgt/CREATE-USER.png)

Must use `;` at the end of the statement otherwise the command not work.
