
# PostgreSQL_Brilliant Cloud Research

# Welcome to My Documentation
This Tutorial is part of a  Cloud Research Project By **Brilliant Cloud Research Group** Bangladesh 
* PostgreSQL Official Site: [Link](https://www.postgresql.org/)
 * How To Install PostgreSQL on Windows: [Link](https://bit.ly/30Ev1A7)
 * PSQL Quick Referrence: [Link](http://gpdb.docs.pivotal.io/archive/gs/43/pdf/PSQLQuickRef.pdf)

## What is PostgreSql ?
![Postgresql logo](https://i.ibb.co/pfSDwdt/postgrelogo.png)
**PostgreSQL** is a powerful, open source object-relational database system. PostgreSql uses sql as main query language.
###  *Why Use PostgreSql ?*
* PostgreSQL is a free open source software (OSS) 
* PostgreSQL is scalable, and it gives high performance.
* PostgreSQL is very reliable; it rarely crashes. Also, PostgreSQL is ACID  
compliant, which means that it can tolerate some hardware failure. 
### *Create a User and Role*
**What is a User?**
Every database cluster contains a set of database users.Users own database objects (for example, tables) and can assign privileges on those objects to other users to control who has access to which object.
#### *To know more about users and roles [here](https://www.quora.com/What-is-the-difference-between-PostgreSQL-users-groups-and-roles):* 

#### CREATE USER adds a new user to a PostgreSQL database cluster.

**Example :** ```CREATE USER Rahim WITH PASSWORD 'rahim1234';```

![CREATE USER](https://i.ibb.co/GHX6N6s/CREATE-USER.png)

Must use `;` at the end of the statement otherwise the command not work.

### Create a Database
You can use *CREATE DATABASE* command to Create a Database
**Example:**
```SQL
CREATE DATABASE Student;
```
Must use `;` at the end of the statement otherwise the command not work.

![CREATE DATABASE](https://i.ibb.co/9tz2tQB/CREATE-DATABASE.png)

### Delete a Database
You can use *DROP DATABASE* command to Delete a Database
**Example:**
```SQL
DROP DATABASE Student;
```
Must use `;` at the end of the statement otherwise the command not work.

![DELETE DATABASE](https://i.ibb.co/Z11S0Fg/DELETE-DATABASE.png)
#### What is a Primary Key in PostgreSQL ?

**`PRIMARY KEY`** 
is a column in a **table** which must contain a **unique** value which can be used to identify each and every **row** of a **table** uniquely.*

#### What is a Foreign Key in PostgreSQL?
A **`FOREIGN KEY`** is a **key** used to link two tables together.
### How To Create a Table
*A table consists of rows and columns. Tables allow you to store structured data like customers, products, employees, etc.*

***Steps to Create a Table in PostgreSQ***
First you Have to connect the database which you want to create a table.
To Connect the database you can use : ``\c databasename;``
**Example**: ![databaseconnect](https://i.ibb.co/zV7WtBJ/databaseconnect.png)
1.  First, specify the name of the **table** after the **CREATE TABLE** keywords.
2.  Second, **creating** a **table** that already exists will result in a error. ...
3.  Third, specify a comma-separated list of **table** columns. ...
4.  Finally, specify the **table** constraints including primary key, foreign key, and check constraints.
*To Create a Table in Postgresql Use:* ``CREATE TABLE`` Keyword. 

```SQL
#Example:
CREATE TABLE student_info (
id BIGSERIAL  NOT  NULL  PRIMARY  KEY,
first_name VARCHAR(50) NOT  NULL,
last_name VARCHAR(50) NOT  NULL,
email VARCHAR(150),
gender VARCHAR(7),
date_of_birth DATE  NOT  NULL,
Country_of_birth VARCHAR(50));
```
*Always write your SQL Keyword in **Upper Case**. Later, You can easily findout the keywords and table or column names, etc.*


![CREATE TABLE](https://i.ibb.co/5sGjXdC/TABLE-CREATE.png)
```NOT NULL``` *is use for when the user must have insert a Value.*

### Insert Values into Table
![INSERT VALUES](https://i.ibb.co/2qQGndZ/insert.png)

### Using Help
*To know all available psql commands, you use the* `\?` *command.*
*To get help on specific PostgreSQL statement, you use the* `\h` *command.*
### Clear The Screen In psql
``` 
Use : \! clear or \! cls
```
![Clear Screen](https://i.ibb.co/VMbQfzw/clear-screen.gif)
### Show Current User Information
```
\conninfo
```
### Change User Command
```
\c - username
```
![Change User](https://i.ibb.co/kGBmC2r/change-user.gif)
### Import Table Form sql File
**Command:** `\i '<file path';`
*For example, if your file is named **student_info.sql** and is located in the D drive root, you would run `'\i D:\student_info.sql';`*
 If you are not using Windows you should remove the single quote ```('')``` or `\i /location/filename.sql;` on linux if any error occured.
### Retrive information from Database table
Another simple way to get information about a table is to use a `SELECT` statement to query the `COLUMNS` attribute in a Postgres table.
Now we are use `SELECT` statement to get infromation we just add to our student_info Database. 
```SQL
SELECT * FROM student_info;
```
![getdata](https://i.ibb.co/Z8KVvjT/select-all.gif)
### PostgreSQL `ORDER BY`
The `ORDER BY` command is used to sort the result set in ascending or descending order.
The `ASC` command is used to sort the data returned in ascending order.

The `DESC` command is used to sort the data returned in descending order.
**Example:** 
```SQL
SELECT * FROM student_info ORDER BY ASC or DESC
```

![orderby](https://i.ibb.co/KbgNxBV/order-by.gif)
### `DISTINCT` 
The `DISTINCT` clause is used in the `SELECT`statement to remove duplicate rows from a result set.
**Syntax :**
```sql
SELECT
   DISTINCT column1
FROM
   table_name;
```
![DISTINCT](https://i.ibb.co/vhWsfSb/DISTINCT.gif)
### Comparison Operators
In PostgreSQL you allows to do:
-   Arithmetic operators
-   Comparison operators
-   Logical operators
-   Bitwise operators

To Know more  follow this link: [Link](https://www.tutorialspoint.com/postgresql/postgresql_operators.htm)
### `WHERE` Clause & `AND`
The PostgreSQL WHERE clause is used to filter the results from a SELECT, INSERT, UPDATE, or DELETE statement.
**Syntax:** `WHERE conditions;`
```SQL
//conditions The conditions that must be met for records to be selected.
SELECT *
FROM student_info
WHERE gender = 'Male';
```
![wherecause](https://i.ibb.co/4WVnsYM/WHERE.gif)
### Using `AND` condition
**Syntax:** 
```SQL
SELECT *
FROM student_info
WHERE gender= 'Male'
AND country_of_birth = 'France';
```
![AND](https://i.ibb.co/RDW3Tvn/AND.gif)*Learn more about Logical contions*: [Link](https://www.w3resource.com/PostgreSQL/postgresql-logical-operators.php)
### LIMIT OFFSET and FETCH
**`LIMIT`** is used to specify some numbers of records to display. The `LIMIT` clause is widely used by many relational database management systems such as MySQL, H2, and HSQLDB. However, the `LIMIT` clause is not a SQL-standard.

![LIMIT](https://i.ibb.co/8bqKbGj/LIMIT.gif)

 The **`OFFSET`** clause specifies the number of rows to skip before starting to return rows from the **query**
	**Note:** 
	`OFFSET` value must be greater than or equal to zero. It cannot be negative, else return error.
	**Syntax:**
~~~SQL
SELECT column_name(s)
FROM table_name
WHERE condition
ORDER BY column_name
OFFSET rows_to_skip ROWS;
~~~
![offset](https://i.ibb.co/vLW00Tz/OFFSET.gif)

 ### `FETCH` Keyword

Because the `LIMIT` keyword is not a SQL Standard for set limit the output.The official way to limiting the results comming from the query is by using the **`FETCH`** Keyword.

### `IN` Operator
The `IN` operator is used in a `WHERE` clause. `IN` Keyword take a array of values and then returns the query matching those values.
Syntax : 
```SQL
SELECT FROM table_name WHERE column_name IN (value1,value2,...);
```
![IN](https://i.ibb.co/tq1NdgW/IN.gif)

 ### `BETWEEN` Operator
PostgreSQL `BETWEEN` operator to match a value against a range of values.
**Syntax:** 
```SQL
SELECT *
FROM student_info
WHERE date_of_birth BETWEEN '2020-01-12'AND '2020-05-12' ORDER BY date_of_birth;
```
![Between](https://i.ibb.co/vJBPvvs/BETWEEN.gif)
### Like and ILIKE
The PostgreSQL **LIKE** operator is used to match text values against a pattern using wildcards. If the search expression can be matched to the pattern expression, the ``LIKE ``operator will return true, which is **1**.

There are two wildcards used in conjunction with the LIKE operator −
-   The percent sign (%)
-   The underscore (_) 
#### Syntax:
```SQL
SELECT column_name FROM table_name WHERE column_name LIKE '%value';
```
![like](https://i.ibb.co/NjvY5w7/LIKE.gif)
#### `ILIKE`
*The **keyword ILIKE** can be used instead of **`LIKE`** to make the match case-insensitive according to the active locale. This is not in the **SQL** standard but is a **PostgreSQL** extension.*
#### Syntax:
```SQL
SELECT _column1, column2, 
FROM table_name 
WHERE columnN ILIKE _pattern;
```
![ILIKE](https://i.ibb.co/7kfhhcC/ILIKE.gif)
#### GROUP BY and HAVING
*The _group_ by clause is used to divide the rows in a table into smaller _groups_ that have the same values in the specified columns*
*Syntax:*
```SQL
SELECT column_name(s)  
FROM table_name  
WHERE condition  
GROUP BY column_name(s)  
ORDER BY column_name(s);
```
*Example:* 
```SQL
SELECT gender,COUNT(*) FROM student_info GROUP BY gender ORDER BY gender;
```
![GROUPBY](https://i.ibb.co/0ZRtgRH/GROUP.gif)
### `HAVING`
*The` HAVING` clause allows us to pick out particular rows where the function's result meets some condition.*
**Syntax:**
```SQL
SELECT
FROM
WHERE
GROUP BY
HAVING
ORDER BY
```
![Having](https://i.ibb.co/BLnkY2S/HAVING.gif)
###  Aggregate Functions
### MIN, MAX, AVEGARE


Know More About Aggregate Functions Follow This : [LINK](https://www.postgresql.org/docs/9.5/functions-aggregate.html)
## Extras
Set Enviromental Path on Windows: [Link](https://youtu.be/3GWZUNCDqNo)
 Video Tutorial : [PostgreSQL  For Begineers freecode Camp](https://www.youtube.com/watch?v=qw--VYLpxG4)
 *Free Book: [Relating to the Database](https://leanpub.com/relating-to-the-database)* 
Postgre Support: [Here](https://www.postgresql.org/support/)
Community : [Link](https://www.postgresql.org/community/)
Jobs: [Link](https://www.postgresql.org/list/pgsql-jobs/)

