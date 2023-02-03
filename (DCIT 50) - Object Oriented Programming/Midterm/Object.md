- An object is an instance of a class. A class is a template or blueprint
from which objects are created. So, an object is the instance(result) of a
class.
- Object Definitions:
	- is a real-world entity.
	- is a runtime entity.
	- is an *entity which has [[State of an Object|state]] and [[Behavior of an Object|behavior]]*.
	- is an *instance of a class*.

Sample:
```Java
public class Student {
	int id; //field or data member or instance variable
	String name; //creating main method inside the Student class
	public static void main(String args[]) {
		//Creating an object or instance
		Student s1=new Student(); //creating an object of Student
		
		//Printing values of the object
		System.out.println(s1.id);//accessing member through reference variable
		System.out.println(s1.name);
	}
}
```
