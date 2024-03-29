 
 **SQL** is a programming language was first developed in the 1970's.
- By IBM researchers **Raymond Boyce** and **Donald Chamberlin**.
- The programming language called "SEQUEL", was published in the book of Edgar Frank Codd's paper "**A Relational Model of Data for Large Shared Data Banks**" in 1970
### History
- **1970** - Dr. E. F. "Ted" of IBM is known as the father of relational databases. He described a relational model for databases.
- **1974** - Structured Query Language appeared
- **1978** - IBM worked to develop Codd's ideas and released a product named **System R**
- **1986** - IBM developed the first prototype of relational database and standardized by ANSI.
- First relational database was release by **Relational Software** later becoming **Oracle**.

## What really is it?
- SQL is Structured Query Language, which is a computer language for storing, manipulating and retrieving data stored in relational database.
- SQL is the standard language for Relation Database System.
	- All relational database management systems like MySQL, MS Access, Oracle, Sybase, Informix, postgres and SQL Server use SQL as standard database language.

## Why SQL?
It allows users to
- Access data in relational database management systems (RDMS).
- Describe the [[2nd Year/(DCIT 24) Information Management/Introduction#Data|data]].
- [[Structured Query Language#DML - Data Manipulation Language|Define the data in database and manipulate]] it.
- Embed within other languages using SQL modules, libraries & pre-compilers.
	- Used to be manipulated by other languages like Java or Python.
- [[Structured Query Language#DDL - Data Definition Language|Create and drop databases and tables]].
- Create view, stored procedure, functions in a database.
- [[Structured Query Language#DCL – Data Control Language| Set permissions]] on tables, procedures, and views.

## Process

```mermaid
flowchart TD;
SQL["SQL Query"] --> Query["Query Language Processor"]
Parser["Parser + Optimizer"] --> Query
DBMS["DBMS Engine"] --> Database[("Physical Database")]
Query --> DBMS
File["File Manager \n+\nTransaction manager"] --> DBMS
```




## Commands
### DDL - Data Definition Language
|Command| Description|
|---|---|
|CREATE | Create new table, a view of a table, or other object in database.|
|ALTER | Modifies an existing database object, such as a table.|
|DROP| Deletes an entire table, a view of a table or other object in the database.|

### DML - Data Manipulation Language
|Command | Description|
|---|---|
|INSERT| Creates a record|
|UPDATE| Modifies records|
|DELETE | Deletes records|

### DCL – Data Control Language
|Command | Description|
|---|---|
| GRANT | Gives a privilege to user|
| REVOKE | Takes back privileges granted from user.|

### DQL - Data Query Language
|Command | Description|
|---| ---|
|SELECT | Retrieves certain records from one or more tables|


## Syntax Commands
> Keywords in SQL aren't case-sensitive so `create` will be the same as `CREATE`

CREATE DATABASE:
```SQL
CREATE  DATABASE database_name ;
```

USE STATEMENT:
```SQL
USE database-name;
```


SHOW STATEMENT:
```SQL
SHOW databases;
```


CREATE TABLE:
```SQL
CREATE TABLE table_name(

       column-name1 datatype, 

       column –name2 datatype;

      etc,)
```

Example:
```SQL
CREATE TABLE salesman(
	salesman_id int,
    name varchar(255),
    city varchar(255),
    commission float
);
```

SQL DESC Statement:
```SQL
DESC table_name;
```
```SQL
DESCRIBE  table-name;
```


DROP DATABASE  STATEMENT:
```SQL
DROP DATABASE database_name;
```

DROP TABLE STATEMENT:
```SQL
DROP  TABLE  table_name;
```

**ALTER TABLE RENAME:**
```SQL
RENAME TABLE activity4_razonado TO activity3_razonado;
```
> This is a new syntax according to [javatpoint](https://www.javatpoint.com/sql-rename-database)
> Renaming database isn't as direct as it should be according to [stackoverflow](https://stackoverflow.com/questions/67093/how-do-i-rename-a-mysql-database-change-schema-name)


**ALTER TABLE STATEMENT:** ^57592b
```SQL
ALTER TABLE table_name {ADD|DROP|MODIFY} column_name {data_type};
```
```SQL
ALTER TABLE table_name RENAME TO new_table_name
```

Alter to modify column data type
```SQL
ALTER TABLE table_name  
MODIFY COLUMN column_name datatype;
```
Alter rename column
```SQL
ALTER TABLE table_name
RENAME COLUMN old_name to new_name;
```
Alter add|drop column
```SQL
ALTER TABLE table_name
DROP COLUMN column_name;

ALTER TABLE table_name
ADD column_name datatype;
```

**ALTER Database**
```SQL
ALTER {DATABASE | SCHEMA} [db_name]
    alter_specification ...
    
ALTER {DATABASE | SCHEMA} db_name
    UPGRADE DATA DIRECTORY NAME
```
>Enables you to change the overall characteristics of a database. These characteristics are stored in the `db.opt` file in the database directory. To use `ALTER DATABASE`, you need the `ALTER` privilege on the database. `ALTER SCHEMA` is a synonym for ALTER DATABASE.

**DELETE STATEMENT:**
```SQL
DELETE FROM table_name  WHERE (CONDITION);
```

**SQL UPDATE STATEMENT:**
```SQL
UPDATE table_name   SET column1 = value1, column2 = value2……..
     column N=valueN   WHERE  (CONDITION);
```

    
**SQL INSERT INTO Statement:**
```SQL
INSERT INTO table_name( column1, column2....columnN) VALUES ( value1, value2....valueN);
```
```SQL
INSERT INTO table_name  VALUES ( value1, value2....valueN);
```

[Insert multiple rows](https://www.freecodecamp.org/news/insert-into-sql-how-to-insert-into-a-table-query-example-statement/)
```SQL
INSERT INTO table_name (column1, column2, column3,etc)
VALUES 
	(value1, value2, value3, etc),
    (value1, value2, value3, etc),
    (value1, value2, value3, etc);
```


Example:
```SQL
INSERT INTO us_states VALUES (1, "California", "California Poppy");
```

```SQL
INSERT INTO salesman(salesman_id, name, city, commission)
VALUES
	(5001, "James Hoog", "New York", 0.15),
    (5002, "Nail Knite", "Paris", 0.13),
    (5005, "Pit Alex", "London", 0.11),
    (5006, "Mc Lyon", "Paris", 0.14),
    (5007, "Paul Adam", "Rome", 0.13),
    (5003, "Lauson Hen", "San Jose", 0.12);
```

**SQL SELECT Statement:**
```SQL
SELECT column1, column2....columnN   FROM table_name;
```
```SQL
SELECT * FROM table_name
```

**SQL WHERE Clause:**
```SQL
SELECT column1, column2....columnN FROM table_name WHERE CONDITION;
```

**SQL UPDATE STATEMENT:**
```SQL
UPDATE table_name   SET column1 = value1, column2 = value2……..

INSERT INTO table_name( column1, column2....columnN) VALUES ( value1, value2....valueN);column N=valueN   WHERE  (CONDITION) ;
```

Example
```SQL
UPDATE Customers  
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'  
WHERE CustomerID = 1;
```

**SQL INSERT INTO Statement:**
```SQL
INSERT INTO table_name( column1, column2....columnN) VALUES ( value1, value2....valueN);
```
```SQL
INSERT INTO table_name  VALUES ( value1, value2....valueN);
```

Example
```SQL
INSERT INTO us_states (name, flower) VALUES ("Alaska", "Forget-me-not");
INSERT INTO us_states (name) VALUES ("Hawaii");
```

**SQL SELECT Statement:**
```SQL
SELECT column1, column2....columnN   FROM table_name;
```
```SQL
SELECT * FROM table_name
```

**SQL WHERE Clause:**
```SQL
SELECT column1, column2....columnN FROM table_name WHERE CONDITION;
```
Example
```SQL
SELECT * FROM fruits WHERE season = "summer";

SELECT name, price FROM fruits WHERE season = "winter" 
```


**SQL AND/OR Clause:**
```SQL
SELECT column1, column2....columnN FROM table_name
WHERE CONDITION-1 {AND|OR} CONDITION-2;
```
Example
```SQL
SELECT * FROM fruits WHERE price < 4 AND season = "summer";

SELECT name, price FROM fruits WHERE season = "summer" OR season="winter";
```

#### SQL Command Connections
|**SYNTAX USE**| **Database and Other Database related objects**| **Data and Records**|
|---|---|---|
|Create New| **CREATE**| **INSERT**|
|Modify/ Change| **ALTER**| **UPDATE**|
|Delete/ Remove|**DROP**|**DELETE**|
|Retrieves information|**DESCRIBE**|**SELECT**|
|Displays Errors, Lists, View, etc.|**SHOW**|---|
|Select object to USE |**USE**|---|



