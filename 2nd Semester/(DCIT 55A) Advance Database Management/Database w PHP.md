- Before you can access the data in a database, you must create a connection to the database.
- In PHP, this is done with the `mysql_connect()` function.

Syntax: 
```PHP
mysql_connect(severname, username, password);
```

|Parameter| Description|
|---|---|
|servername| Specifies the server to connect to. Default value is "localhost"|
|username| Specifies username to log in with. Default value is the name of the user owning the sever process|
|password| password connected to the username|

Code connecting to database:
```PHP
<?php
$con = mysql_connect("localhost", "root", "");

if (!$con){
	die('Could not connect:'.mysql_error());
}
//some code

mysql_close($con);
?>
```

#### Creating Database in PHP
```php
<?php
$con = mysql_connect("localhost","root","");
if(!$con){
	die('Could not connect'.mysql_error())
}
if (mysql_query("CREATE DATBASE pmg", $con)) {
	echo "Database created";
} else {
	echo "Error creating database".mysql_error();
}
mysql_close($con);
?>
```
> `mysql_query()` sends an unique query to the currently active database on the server.


#### Insert Data Into a Database table 
**`mysql_select_db`**
- Select a MySQL database
- Sets the current active database on the server
- Every subsequent call to `mysql_query()` will be made on the active database.

Code:
```php
$con = mysql_connect("localhost", "root", "");
if(!$con){
	die('Could not connect:'.mysql_error());
}
mysql_select_db("pmg", $con);

mysql_query("INSERT INTO student (Rollno, Name, Mark)
	VALUES (1, 'Raju', 35)", $con);

mysql_close($con);
```

##### Insert data from HTML
```html
<html>
<body>
	<form action="insert.php" method="post">
		<input type="text" name="rollNo" />
		<input type="text" name="name" />
		<input type="text" name="mark" />
		<input type="submit" />
	</form>
</body>
</html>
```

PHP code:
```PHP
<?php
$con = mysql_connect("localhost", "root", "");
if(!$con){
	die('Could not connect:'.mysql_error());
}
mysql_select_db("pmg", $con);

$sql = "INSERT INTO student (rollno, name, mark) 
	VALUES
		('$_POST[rollno]', '$_POST[name]','$_POST[mark]')";

if(!mysql_query($sql, $con)){
	die('Error:'.mysql_error());
}
print_r($_POST);
?>
```


### NOTES
To run, you need to put the PHP file to the `htdocs` on the main file of XAMPP or based on the link of ma'am, this will be in any part of the directory but needed to click the `admin` of apache.

![[Pasted image 20230623185456.png]]


## Notes: Finals
### Laboratory
- This will be online
- You need to redesign and alter the code
- Max of 3 members in a group
- This will include the manipulation of PHP
- Deadline: First week of July

### Written Exam
- On July 5, Wednesday
- Coverage are all the topics tackled from the semester

