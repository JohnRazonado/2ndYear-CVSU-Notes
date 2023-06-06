> Every command syntax in SQL isn't case-sensitive, so Alter and ALTER is similar to the parser's eyes.

## Basic Syntax
### Others

### USE statement
- Allows you to select database you want to utilize

```SQL
USE database_name
```

### SHOW statement
- Provides information about the databases, columns, or status information

```SQL
SHOW databases;
```
>This shows all of the database in your localhost.


### DESCRIBE statement
- Provides information about the columns in a table

```SQL
DESC table_name;

DESCRIBE table_name;
```

### [[Structured Query Language#DDL - Data Definition Language|DDL - Data Definition Language]]
#### CREATE
- Create new table, view of table, database, or other object in database

```SQL
CREATE DATABASE database_name;

CREATE TABLE table_name(
	colname1 datatype,
	colname2 datatype,
	etc
);
```

#### [[Structured Query Language#^57592b|ALTER]]
- Modify existing database and other objects like table

```SQL
ALTER TABLE table_name {ADD|DROP|MODIFY} column_name {data_type};

ALTER TABLE table_name RENAME TO new_table_name
```

#### DROP
- Deletes table, view of table, database, or other objects in the database

```SQL
DROP DATABASE database_name;

DROP TABLE table_name;
```

### [[Structured Query Language#DML - Data Manipulation Language|DML - Data Manipulation Language]]
#### INSERT
- Creates a record
```SQL
INSERT INTO table_name( column1, column2....columnN) VALUES ( value1, value2....valueN);


INSERT INTO table_name  VALUES ( value1, value2....valueN);
```

If inserting multiple rows:
```SQL
INSERT INTO table_name (column1, column2, column3,etc)
VALUES 
	(value1, value2, value3, etc),
    (value1, value2, value3, etc),
    (value1, value2, value3, etc);
```

#### UPDATE
- Modifies a record
```SQL
UPDATE table_name   SET column1 = value1, column2 = value2……..
     column N=valueN   WHERE  (CONDITION);
```

#### DELETE
- Deletes records
```SQL
DELETE FROM table_name  WHERE (CONDITION);
```

### [[Structured Query Language#DCL – Data Control Language|DCL - Data Control Language]]
#### [GRANT](https://mariadb.com/kb/en/grant/)
- Give privilege to user
```SQL
GRANT
    _priv_type_ [(_column_list_)]
      [, _priv_type_ [(_column_list_)]] ...
    ON [_object_type_] _priv_level_
    TO _user_specification_ [ _user_options_ ...]
```

#### [REVOKE](https://mariadb.com/kb/en/revoke/)
- Takes back privileges granted from user
```SQL
REVOKE ALL PRIVILEGES, GRANT OPTION
    FROM user [, user] ...
```

### [[Structured Query Language#DQL - Data Query Language|DQL - Data Query Language]]
#### [[Other SQL Functions#SELECT functions|SELECT]]
- Retrieves certain record from tables.
```SQL
SELECT column1, column2....columnN   FROM table_name;

SELECT * FROM table_name
```

##### WHERE
```SQL
SELECT column1, column2....columnN FROM table_name WHERE CONDITION;

SELECT * FROM fruits WHERE season = "summer";

SELECT name, price FROM fruits WHERE season = "winter" 
```

###### w/ AND/OR clause
```SQL
SELECT column1, column2....columnN FROM table_name
WHERE CONDITION-1 {AND|OR} CONDITION-2;
```


##### LIKE
used to compare a value to similar values using wildcard operators. There are two wildcards used in conjunction with the `LIKE` operator.

**Wildcards** - `%` (percentage) and `_`(underscore)
>Underscore represent a single number or character while percent represents many or multiple characters

```SQL
SELECT FROM table_name WHERE column LIKE 'XXX%'

SELECT FROM table_name WHERE column LIKE 'XXX_'
```


##### SUM
Returns total sum of a numeric column

```SQL
SELECT SUM(column_name) FROM table_name WHERE condition;
```

##### MIN/MAX
Min returns the smallest value on the selected table

```SQL
SELECT MIN(column_name) FROM table_name WHERE condition;
```

Max returns the largest value 
```SQL
SELECT MAX(column_name) FROM table_name WHERE condition;
```

##### AVG
Returns average value of a numeric column
```SQL
SELECT AVG(column_name) FROM table_name WHERE condition;
```

##### COUNT
Returns the number of rows matching the condition
```SQL
SELECT COUNT(column_name) FROM table_name WHERE condition;
```

##### ORDER BY
Sort result-set in ascending or descending order.

```SQL
SELECT column1, column2, ....
FROM table_name
ORDER BY column1, coloumn2 .... ASC|DESC;
```

## [[Other SQL Functions#Keys|Key and Unique Identifiers]]
#### PRIMARY
- Constraints as unique identifier of each record in a table
- Must needs to be **UNIQUE** value and **NOT NULL**
```SQL
CREATE TABLE Persons (
	ID int NOT NULL,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int,
	PRIMARY KEY (ID)
);
```
>Primary key here is the "`ID`" when the `Persons` table is created

You can also put a PRIMARY KEY later on using `ALTER`
```SQL
ALTER TABLE Persons ADD PRIMARY KEY (ID);
```

You can also drop the PRIMARY KEY
```SQL
ALTER TABLE Persons DROP PRIMARY KEY;
```

#### FOREIGN
- Constraint use to have relationship between tables using PRIMARY KEY
- Prevent actions that would destroy links between tables.

```SQL
CREATE TABLE Orders (
	OrderID int NOT NULL,
	OrderNumber int NOT NULL,
	PersonID int,
	PRIMARY KEY (OrderID),
	FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
```
> A `FOREIGN KEY` was created on `PersonID` in `Orders` table that connect it to the `Persons` table.

You can use `ALTER` statement to add a FOREIGN KEY down the line
```SQL
ALTER TABLE customer  
ADD FOREIGN KEY (salesman_id) REFERENCES salesman(salesman_id);
```

You can also remove it
```SQL
ALTER TABLE customer  
DROP FOREIGN KEY salesman_id;
```

#### AUTO_INCREMENT
- Allows unique number to generate automatically when new record is inserted

```SQL
CREATE TABLE Persons (
	Personid int NOT NULL AUTO_INCREMENT,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int,
	PRIMARY KEY (Personid)
);
```
> "Personid" in this sample is `AUTO-INCREMENT PRIMARY KEY` field on "Persons" table.


## [[Conditional Statements]]
Helps to define different logic and actions for different conditions

### If statements
If-else is known as a conditional statement. Similarly in SQL, it is known as the conditional SQL statement. if & else control structure used mostly in the procedures & methods.

Basic syntax
```SQL
IF(condition, true, false)
```

Sample statement
```SQL
SELECT *, if(CourseCode="BSIT", "BS Information Technology", "BS Computer Science") as "Course Description" FROM student_record;
```

If you need a nested If-else statement
```SQL
SELECT *, 
	if(YearCode=1, "Freshmen", 
		if(YearCode=2, "Sophomore", 
			if(YearCode=3, "Junior", "Senior")
		)
	) as "Year Description" 
FROM student_record;
```

### Case statements
Similar on how other programming languages on how they use CASE statement.

```SQL
CASE  
    WHEN condition1 THEN result1  
    WHEN condition2 THEN result2  
    WHEN conditionN THEN resultN  
    ELSE result_ 
END;
```
>keyword `CASE` signals the beginning of a case statement, and the keyword `END` signals its end.

Sample use case is interpreting numerical grades to its letter grade value
```SQL
SELECT *,
  CASE
    WHEN score >= 94 THEN "A"
    WHEN score >= 90 THEN "A-"
    WHEN score >= 87 THEN "B+"
    WHEN score >= 83 THEN "B"
    WHEN score >= 80 THEN "B-"
    WHEN score >= 77 THEN "C+"
    WHEN score >= 73 THEN "C"
    WHEN score >= 70 THEN "C-"
    WHEN score >= 67 THEN "D+"
    WHEN score >= 60 THEN "D"
    ELSE "F"
  END AS grade
FROM students_grades;
```