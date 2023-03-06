Having one object acquires the properties of another (parent-child relationship)
- The child can inherit all parent attributes

> object acquires all the properties and behaviors of a parent object,

#### "extends" Keyword
```Java
// Java program to illustrate the concept of inheritance
// base class
class Bicycle {
	// the Bicycle class has two fields
	public int gear;
	public int speed;

	// the Bicycle class has one constructor
	public Bicycle(int gear, int speed){
		this.gear = gear;
		this.speed = speed;
	}
	// the Bicycle class has three methods
	public void applyBrake(int decrement){
		speed -= decrement;
	}
	public void speedUp(int increment){
		speed += increment;
	}
	// toString() method to print info of Bicycle
	public String toString(){
		return ("No of gears are " + gear + "\n"
				+ "speed of bicycle is " + speed);
	}
}

// derived class
class MountainBike extends Bicycle {
	// the MountainBike subclass adds one more field
	public int seatHeight;
	// the MountainBike subclass has one constructor
	public MountainBike(int gear, int speed, int startHeight){
		// invoking base-class(Bicycle) constructor
		super(gear, speed);
		seatHeight = startHeight;
	}
	// the MountainBike subclass adds one more method
	public void setHeight(int newValue){
		seatHeight = newValue;
	}
	// overriding toString() method
	// of Bicycle to print more info
	@Override public String toString(){
		return (super.toString() + "\nseat height is "
				+ seatHeight);
	}
}

// driver class
public class Test {
	public static void main(String args[]){
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


#### "implements" Keyword

```Java
public interface Animal{
}

public class Mammal implements Animal{ 
} 

public class Dog extends Mammal{ 
}

```
> "implements" keyword is used for having an "interface" class




#### IS-A Relationship
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

#### HAS-A Relationship

```Java
public class Vehicle{

} 

public class Speed{

} 

public class Van extends Vehicle{
	privateS peed sp; 
}
```

