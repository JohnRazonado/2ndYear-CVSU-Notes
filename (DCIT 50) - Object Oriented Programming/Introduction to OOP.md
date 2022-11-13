>Need to be concise

This part will discuss the fundamentals of OOP, from making everything as an object to different behavior of it.

- OOP as a whole is a paradigm that allows programmers/ developers to code in unison while still having a sense of stacking each other without falling apart.

> This need to have the notes completed today.


## Object
The [[state of an Object|state]] and [[Behavior of an Object|behavior]] of different aspect of a programming language



## Class
The template or blueprint of the object. 

Here's and example of class in Java. It is used every time and needed when just creating the file itself.
```Java
public class Dog{ // This is for the dog examples
	String breed; int age; String color; 
	void barking(){ 
	} 
	void hungry(){ 
	} 
	void sleeping(){
	}
}
```

```Java
public class Pen{// an example for the pen scenario
	String brand, model, serialNo, color;
	int inkLevel = 1000;

	Void write(){
	}
	void decreaseInk(){
	}
}
```


There are different types of variable inside a class:
1. **Local variables** - defined inside methods, constructor or blocks. It will be declared or initialized within the method and will be destroyed when the method is done/completed.
2. **Instance variable** - variables within the class outside of any method but instantiated when the class is loaded. 
3. **Class variables** – Variables declared within the class, outside of any method having a `static` keyword.

---

## Inheritance
Having one object acquires the properties of another (parent-child relationship)
- The child can inherit all parent attributes


### "extends" Keyword
```Java
// Java program to illustrate the
// concept of inheritance

// base class
class Bicycle {
	// the Bicycle class has two fields
	public int gear;
	public int speed;

	// the Bicycle class has one constructor
	public Bicycle(int gear, int speed)
	{
		this.gear = gear;
		this.speed = speed;
	}

	// the Bicycle class has three methods
	public void applyBrake(int decrement)
	{
		speed -= decrement;
	}

	public void speedUp(int increment)
	{
		speed += increment;
	}

	// toString() method to print info of Bicycle
	public String toString()
	{
		return ("No of gears are " + gear + "\n"
				+ "speed of bicycle is " + speed);
	}
}

// derived class
class MountainBike extends Bicycle {

	// the MountainBike subclass adds one more field
	public int seatHeight;

	// the MountainBike subclass has one constructor
	public MountainBike(int gear, int speed,
						int startHeight)
	{
		// invoking base-class(Bicycle) constructor
		super(gear, speed);
		seatHeight = startHeight;
	}

	// the MountainBike subclass adds one more method
	public void setHeight(int newValue)
	{
		seatHeight = newValue;
	}

	// overriding toString() method
	// of Bicycle to print more info
	@Override public String toString()
	{
		return (super.toString() + "\nseat height is "
				+ seatHeight);
	}
}

// driver class
public class Test {
	public static void main(String args[])
	{

		MountainBike mb = new MountainBike(3, 100, 25);
		System.out.println(mb.toString());
	}
}

```

here with a sample of simple inheritance

```Java
// Java program to illustrate the
// concept of single inheritance
import java.io.*;
import java.lang.*;
import java.util.*;

class one {
	public void print_geek()
	{
		System.out.println("Geeks");
	}
}

class two extends one {
	public void print_for() { System.out.println("for"); }
}
// Driver class
public class Main {
	public static void main(String[] args)
	{
		two g = new two();
		g.print_geek();
		g.print_for();
		g.print_geek();
	}
}

```


### "implements" Keyword

```Java
public interface Animal{
}

public class Mammal implements Animal{ 
} 

public class Dog extends Mammal{ 
}

```
> "implements" keyword is used for having an "interface" class




### IS-A Relationship
Making an object a type of that object

```Java
public class Animal{
}

public class Mammal extends Animal{
}

public class Reptile extends Animal{ 
}

public class Dog extends Mammal{ 
}
```
> We can say that
>  - Mammal IS-A Animal
>  - Reptile IS-A Animal


We can also have this relationship on **implements** keyword:

```Java
public interface Animal{
}

public class Mammal implements Animal{ 
} 

public class Dog extends Mammal{ 
}
```

### HAS-A Relationship

```Java
public class Vehicle{

} 

public class Speed{

} 

public class Van extends Vehicle{
	privateS peed sp; 
}
```


## Encapsulation
Hiding objects and classes giving it security as private as possible.

Encapsulation is the technique of making the fields in a class private and providing access to the fields via public methods. If a field is declared private, it cannot be accessed by anyone outside the class, thereby hiding the fields within the class. For this reason, encapsulation is also referred to as data hiding. 

Encapsulation can be described as a protective barrier that prevents the code and data being randomly accessed by other code defined outside the class. Access to the data and code is tightly controlled by an interface.

```Java
/* File name : EncapTest.java */
public class EncapTest{
	private String name;
	private String idNum;
	private int age;
	
	public int getAge(){
		return age;
	}
	public String getName(){
		return name;
	 }
	public String getIdNum(){
	return idNum;
}

public void setAge(int newAge){ 
	age = newAge;
}
public void setName(String newName){

	name = newName; 
	} 

	public void setIdNum(String newId){
	idNum = newId; 
	} 
}

```

```Java
/* File name : RunEncap.java */ 
public class RunEncap{ 
public static void main(String args[]){ 
	EncapTest encap =new EncapTest();
	encap.setName("James");
	encap.setAge(20);
	encap.setIdNum("12343ms");
	System.out.print("Name : "+ encap.getName()+" Age : "+ encap.getAge()); 
	}
}

// The result would be
// Name:JamesAge:20
```

### Using Access Modifiers
The fields of a class can be made read-only or write-only. A class can have total control over what is stored in its fields. 

The users of a class do not know how the class stores its data. A class can change the data type of a field and users of the class do not need to change any of their code.

## Polymorphism
Having different forms in one single class.

- It occurs when parent class reference is used to refer a child class object
- All Java objects are polymorphic.

```Java
public interfaceVegetarian{}
public class Animal{} 
public class Deer extends Animal implements Vegetarian{}
```
> Now the deer is:
> 	- IS-A Animal
> 	- IS-A Vegetarian 
> 	- IS-A Deer
> 	- IS-A Object

### Method overriding


### Method Overloading



## Abstraction
It is the ability to create a class that can't be instantiated. All other functionality as a class exist but without creating an instance of it.
### Abstract class
You can declare an abstract class using the `abstract` keyword

```Java
/* File name : Employee.java */ 
public abstract classEmployee {
	private String name; 
	private String address;
	private int number;
	
	public Employee(String name,String address,int number) { 
		System.out.println("Constructing an Employee");
		this.name = name;
		this.address = address;
		this.number = number;
	} 
	public double computePay() { 
	System.out.println("Inside Employee computePay"); 
	return 0.0; 
	}
	public void mailCheck() {
	System.out.println("Mailing a check to "+this.name +" "+this.address); 
	}
	public String toString() {
	return name +" "+ address +" "+ number;
	}
	public String getName() {
	return name; 
	}
	public String getAddress() {
	return address;
	}
	public void setAddress(String newAddress) {
	address = newAddress;
	}
	public int getNumber() {
	return number;
	} 
}
```


#### Abstract method
If you want a class to contain a particular method but you want the actual implementation of that method to be determined by child classes, you can declare the method in the parent class as abstract. The abstract keyword is also used to declare a method as abstract.

An abstract method consists of a method signature, but no method body.

```Java
public abstract class Employee {
	private String name; 
	private String address;
	private int number;
	public abstract tdouble computePay(); //Remainder of class definition 
}

public class Salary extends Employee { 
	private double salary;// Annual salary
	public double computePay() {
		System.out.println("Computing salary pay for "+ getName()); return salary/52; } 

//Remainder of class definition
}
```

### Interface class
Basically a collection of abstract methods. Like an abstract class but you can't put any normal method on it.

- It is also considered **Not a class**
- An interface can contain any number of methods. 
- An interface is written in a file with a **.java** extension, with the name of the interface matching the name of the file. 
- The bytecode of an interface appears in a **.class** file. 
- Interfaces appear in packages, and their corresponding bytecode file must be in a directory structure that matches the package name.
- Interface can't contain any constructor
- You can't instantiate an interface.
- It can't contain any instance fields. Only declared on `static` and `final`
- An interface is implicitly abstract. You do not need to use the `abstract` keyword when declaring an interface.

```Java
/* File name : Animal.java */
interface Animal{
	public void eat();
	public void travel();
}
```


To use the interface, you need to use the `implements` keyword:

```Java
/* File name : MammalInt.java */
public class MammalInt implements Animal{
	public void eat(){
		System.out.println("Mammal eats");
	}
	public void travel(){
		System.out.println("Mammal travels");
	}
	public int noOfLegs(){
		return 0;
	}
	public static void main(String args[]){
		MammalInt m =new MammalInt();
		m.eat();
		m.travel(); 
	} 
}
```