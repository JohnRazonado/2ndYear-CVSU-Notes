> This is from [[09-06-2023 Meeting]] yesterday

## Join
`JOIN` clause is used to combine rows from two or more tables, based on a related column between them.

## INNER JOIN
`INNER JOIN` keyword selects record that have matching values in both tables.

```sql
SELECT column_name 
FROM table1 
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

Sample code
```sql
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomersID;
```


## LEFT JOIN
`LEFT JOIN` keyword returns all records from the let table(table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.

```sql
SELECT column_name
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

Sample code:
```SQL
SELECT Customers.Customername, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
```


## RIGHT JOIN
The `RIGHT JOIN` keyword returns all records from the right table (table2), and the matching record from the left table (table1). The result is 0 records from the left side, if there is no match.

```sql
SELECT column_name
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```

![[Pasted image 20230610152817.png]]


## FULL JOIN
`FULL OUTER JOIN` keyword returns all records when there is a match in left (table1) or right (table2) table records.

Tip: FULL OUTER JOIN and FULL JOIN are the same.

```SQL
SELECT column_name
FROM table1
FULL OUTER JOIN table2
ON table.column_name = table2.column_name
WHERE condition;
```


![[Pasted image 20230610153313.png]]

> Full Outer Join can't be used on MariaDB on XAMPP
> https://gist.github.com/ebta/d3a1c86ca41d885fdefcc75bb440a51b
> https://www.alphacodingskills.com/mariadb/mariadb-full-join.php

## SELF JOIN
> No module information about this one but well look upon this one

## notes
- The activity can't be accomplish unless there's a new table that will connect the authors, editors, and translators.