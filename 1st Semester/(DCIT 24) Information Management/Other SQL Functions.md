> 	We'll use this table named **customer** with the following data:

|customer_id|cust_name|	city|	grade|	salesman_id|
|---|---|---|---|---|
|3002|Nick Rimando|New York|100	|5001|	
|3007|Brad Davis|New York|200	|5001|	
|3005|	Graham Zusi|	California|	200|5002|	
|3008|	Julian Green|	London	|300|5002|	
|3004|	Fabian Johnson|	Paris|	300|	5006|	
|3009|	Geoff Cameron|	Berlin|	100|	5003|	
|3003|	Jozy Altidor|	Moscow	|200|	5007|	
|3001|	Brad Guzan|	London||	5005|	
> The BLANK part in the end is `NULL`

## SELECT functions
These are functions that need to use the `SELECT` in the data query language and so on.

### LIKE
the `LIKE` clause is used to compare a value to similar values using wildcard operators. There are two wildcards used in conjunction with the `LIKE` operator.
#### Wildcards
- % (percentage)
- \_ (underscore)
> Percent sigh represents zero, one or multiple characters
> Underscore represent a single number or character.
> Can both be used in combination.

```SQL
SELECT FROM table_name WHERE column LIKE 'XXX%'
```

Example
```SQL
SELECT * FROM customer WHERE cust_name LIKE 'J%';
```

Output
|customer_id|	cust_name|	city|	grade|	salesman_id|	
|---|---|---|---|---|
|3008|	Julian Green|	London	|300|	5002|	
|3003|	Jozy Altidor|	Moscow|	200|	5007|

### ORDER BY
- A keyword used to sort the result-set in ascending or descending order.
- Sorts the records in ascending order by default. Use `DESC` keyword to sort it descending order.
```sql
SELECT column1, column2, ....
FROM table_name
ORDER BY column1, coloumn2 .... ASC|DESC;
```

Example:
```sql
SELECT cust_name, city FROM customer ORDER BY cust_name, city ASC;
```
|cust_name|	city|
|---|---|
|Brad Davis|New York|
|	Brad Guzan|	London|
|	Fabian Johnson|	Paris|	
|	Geoff Cameron|	Berlin|	
|	Graham Zusi|	California|	
|	Jozy Altidor|	Moscow	|
|	Julian Green|	London	|		
|Nick Rimando|New York|	

```sql
SELECT * FROM customer ORDER BY city DESC;
```

|customer_id|cust_name|	city|	grade|	salesman_id|
|---|---|---|---|---|
|3004|	Fabian Johnson|	Paris|	300|	5006|	
|3002|Nick Rimando|New York|100	|5001|	
|3007|Brad Davis|New York|200	|5001|
|3003|	Jozy Altidor|	Moscow	|200|	5007|
|3001|	Brad Guzan|	London||	5005|	
|3008|	Julian Green|	London	|300|5002|
|3005|	Graham Zusi|	California|	200|5002|		
|3009|	Geoff Cameron|	Berlin|	100|	5003|	


### SUM
Function that returns the total sum of a numeric column.

```SQL
SELECT SUM(column_name) FROM table_name WHERE condition;
```

Example
```SQL
SELECT SUM(grade) FROM customer WHERE grade<=200;
```

Output
|SUM(grade)| |
|---|---|
|800||



### COUNT
Function that returns the number of rows that matches a specified criterion.

```SQL
SELECT COUNT(column_name) FROM table_name WHERE condition;
```

Example
```SQL
SELECT COUNT(grade) FROM customer;

SELECT COUNT(grade) FROM customer WHERE grade=200;
```

Output
|Count(grade)| |
|---|---|
|7||

|Count(grade)| |
|---|---|
|3||

### AVG
Function returns the average value on a numeric column.

```SQL
SELECT AVG(column_name) FROM table_name WHERE condition;
```

Example
```SQL
SELECT AVG(grade) FROM customer;
```

Output
|AVG(grade)| |
|---|---|
|200.0000||


### MAX
Function that returns the largest value of the selected column

```SQL
SELECT MAX(column_name) FROM table_name WHERE condition;
```

Example
```SQL
SELECT MAX(grade) FROM customer WHERE 1;
```
or
```SQL
SELECT MAX(grade) FROM customer;
```

Output
|MAX(grade)| |
|---|---|
|300||


### MIN
Function that returns the smallest value of the selected column

```SQL
SELECT MIN(column_name) FROM table_name WHERE condition;
```

Example
```SQL
SELECT MIN(grade) FROM customer WHERE 1;
```
or
```SQL
SELECT MIN(grade) FROM customer;
```

Output
|MIN(grade)| |
|---|---|
|100||



## Keys
### PRIMARY KEY
- PRIMARY KEY constraint uniquely identifies each record in a table.
- It must contain UNIQUE values, and cannot contain NULL values.
- A table can have only ONE primary key; and in the table, this primary key can consist of single or multiple columns (fields).

```SQL
CREATE TABLE Persons (
	ID int NOT NULL,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int,
	PRIMARY KEY (ID)
);
```

Note: the primary key is on the "ID" column when the "Persons" table is created.

You can edit a table to have a PRIMARY KEY later on:
```SQL
ALTER TABLE Persons ADD PRIMARY KEY (ID);
```

You can also `DROP` it:
```SQL
ALTER TABLE Persons DROP PRIMARY KEY;
```

Example:
```SQL
ALTER TABLE customer ADD PRIMARY KEY (customer_id);
```

![[Pasted image 20221231000847.png]]



### FOREIGN KEY
- `FOREIGN KEY` constraint is used to prevent actions that would destroy links between tables.
- It is a field (or collection of fields) in one table, that refers to the `PRIMARY KEY` in another table.
- table with `FOREIGN KEY` is called the child table, and the table with the primary key is called the referenced or parent table.

```SQL
CREATE TABLE Orders (
	OrderID int NOT NULL,
	OrderNumber int NOT NULL,
	PersonID int,
	PRIMARY KEY (OrderID),
	FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
```
Note: This sample create `FOREIGN KEY` on "PersonsID" column of "Orders" table when created.

Example if `ALTER`
```SQL
ALTER TABLE customer  
ADD FOREIGN KEY (salesman_id) REFERENCES salesman(salesman_id);
```
> Note: The references needs to be a PRIMARY KEY to have the link be a FOREIGN KEY

or 

```SQL
ALTER TABLE favorite_food
    ADD CONSTRAINT fk_fav_food_person_id FOREIGN KEY (person_id)
          REFERENCES person (person_id);
```
>to also managed the name of the foreign key

If you need to [remove](https://stackoverflow.com/questions/13606469/cannot-change-column-used-in-a-foreign-key-constraint)
```SQL
ALTER TABLE customer  
DROP FOREIGN KEY salesman_id;
```


## Auto Increment Field
- `AUTO_INCREMENT` allows a unique number to be generated automatically when a new record is inserted into a table, often this is the `PRIMARY KEY` field that we would like to be created automatically every time a new record is inserted.

```SQL
CREATE TABLE Persons (
	Personid int NOT NULL AUTO_INCREMENT,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int,
	PRIMARY KEY (Personid)
);
```

Note: "Personid" in this sample is `AUTO-INCREMENT PRIMARY KEY` field on "Persons" table.

