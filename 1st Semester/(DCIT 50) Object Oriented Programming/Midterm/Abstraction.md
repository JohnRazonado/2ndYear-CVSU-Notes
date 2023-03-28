- Ability of <mark style="background: #FFB8EBA6;">hiding internal details and showing functionality</mark>
- It is the ability to create a class that can't be instantiated. 
- All other functionality as a class exist but without creating an instance of it.
> Essentially, we know what an object is but we don't really need to know the inner working of it.

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


### Abstract method
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