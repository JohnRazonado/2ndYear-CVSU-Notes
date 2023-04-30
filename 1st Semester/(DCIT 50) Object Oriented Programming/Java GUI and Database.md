This is for only on creating java GUI project
> This will only use the NetBeans drag and drop system.

## Needing Softwares
- XAMPP
	- is a PHPMyAdmin GUI controller.
	- We will need if for the phpMyAdmin system of it.
- NetBeans
	- ![[Pasted image 20221207133820.png]]
	- Use Java with Maven
- MySQL connector
	- ![[Pasted image 20221207134704.png]]
	  click "MySQL Community Downloads"
	  - ![[Pasted image 20221207134736.png]]
	  - Then choose "Platform Independent"![[Pasted image 20221207134820.png]]
	  - Then pick the "ZIP Archive" one to be downloaded ![[Pasted image 20221207134848.png]]
	  - Then click "No Thanks, just download" ![[Pasted image 20221207134908.png]]
	  - After downloading, we need to extract the content of the ZIP file by right-clicking on it and selecting "Extract Here" if you're using a WINRar ![[Pasted image 20221207135137.png]]
	  - After opening the extracted folder, you will see this file named "mysql-connector-java-x.xxxx"![[Pasted image 20221207135828.png]]

## Importing MySQL Connector to Java Project
> Note: for some old NetBeans version, instead of the option "Add Dependency..." it is "Add JAR file" of some sort and that's is more easy since all you need is to locate the SQL connector JAR file.

1. On your project window, right-click on the "Dependencies" folder and select "Add Dependency..."![[Pasted image 20221207141335.png]]
2. Then this window will popup:![[Pasted image 20221207141426.png]]
   First thing that you need to look at are the 3 blank text area. Just write these text on it if you have the same connector name: ![[Pasted image 20221207142352.png]]
   The hit "Add"
   > If you have a newer version, just copy and paste the end part of the name of the connector.
   
   There's some JAR files that will appear at your "Dependencies" folder   ![[Pasted image 20221207142507.png]]
3. But the JAR file isn't really that connected, so we need to manually reconnect it: Right-click on the first file then select "Manually install artifact" ![[Pasted image 20221207142705.png]]
   Then browse and locate your file ![[Pasted image 20221207142804.png]] ![[Pasted image 20221207142753.png]]
   After that, click "Install locally" ![[Pasted image 20221207142830.png]]
   It is now connected to your project.
4. Now, you need to import it to your project at the main class by initiating these variables first:
   ```Java
   static final String USERNAME = "root";
   static final String PASSWORD = "";
   static final String DB = "jdbc:mysql://localhost:3306/test";
   
```
> The first two variables are for the username and the password of the database were going to access, the default username is usually "root"
> The last variable is the location of the database, in this example we have the `test` database but you can put whatever the name of the database could be.
> Then the port part which is `3306` can also vary depending what's appearing on your XAMPP control panel at MySQL part ![[Pasted image 20221207145056.png]]

5. Then we will add another 3 variables that will leave it blank or null:
   ```Java
   private static Connection conn = null;
   private static Statement cmd = null;
   private static String sql;
```
The first variable is the `Connection conn` that is used for 
Then the `Statement cmd` is the holder for any command to pass on the database
and the `String sql` is the holder for any SQL commands that we need to throw

6. Since you'll probably getting some error, you need to import:
   ```Java
   import java.sql.*;
```
To avoid red error due to the variables.
7. Add a new method called `openDB`:
   ```Java
   public static void openDB(){
	   try{
		   conn = DriverManager. getConnection(DB, USERNAME, PASSWORD);
	   } catch(Exception e){
		   e.printStackTrace();
	   }
   }
```

## Starting with Java GUI
We will now utilize the drag-and-drop  feature built-in on NetBeans
1. Firstly, it needs to create a file first by right-clicking the main project folder and select "New", then select "jFrame Form"
    ![[Pasted image 20221207151225.png]]
    Then this window will appear: ![[Pasted image 20221207151309.png]]
    Fill in the Class name first, then select the package which is your sampleapplication
    ![[Pasted image 20221207151417.png]]
    Hit "Finish"
    Then a new panel will appear to select different elements: ![[Pasted image 20221207151459.png]]


### Creating a Login panel
![[Pasted image 20221207162304.png]]

This is the result somewhat we want in the end. It needs to also have a fake menu option to which we can enter once we login. But we'll focus first on the login part.

1. After creating the file, it will only have an initial window. Try to add a label, textField, passwordField, and Btn for login
2. The double click the Login button at the GUI panel to go to its `ActionPerformed` method which is the event handler when you click the button. Put this code there:
   ```Java
private void btnLoginActionPerformed(java.awt.event.ActionEvent evt){
	Mainclass main = new MainClass();
	main.openDB();
	if(main.validCredentials(txtUser.getText(), txtPass.getText())){
		JOptionPane.showMessageDialog(null, "Login Successfully");
		frmMenu menu = new frmMenu();
		this.hide();
		menu.show();
	} else{
		JOptionPane.showMessageDialog(null, "Invalid username or password");
	}
}   
```
> Please ignore the method because it is automatically made by NetBeans



   
## Login Credentials
Since the sample GUI is a login window, this will validate on the SQL side if that user is on the database or not.
```Java
public static boolean validCredentials(String user, String pass){
	try{
		cmd = conn.createStatement();
		sql = "SELECT * FROM accounts WHERE user = '" + user + "' AND pass = '" + pass + "'";
		ResultSet rs = cmd.executeQuery(sql);
		return rs.next();
		
	} catch(Exception e){
		e.printStackTrace();
		return false;
	}
}
```