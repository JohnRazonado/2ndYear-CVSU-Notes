Having different forms in one single class.
- One task performed in different ways.
- It occurs when parent class reference is used to refer a child class object
- All Java objects are polymorphic.

> Polymorphism is derived from 2 Greek words: *poly* and *morphs*. The word "poly" means **many** and "morphs" means **forms**. So polymorphism means **many forms**.

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

Example:
to convince the customer differently, to draw
something, shape, triangle, rectangle, etc.


#### Method Overriding
- As the name suggests, it overrides the method in the child of the class.
- Means having the same method on different class inherited from the parent class but different outcome.


```Java
class Animal{
	void eat(){System.out.println("eating...");}
}
class Dog extends Animal{
	void eat(){System.out.println("eating bread...");}
}
class Cat extends Animal{
	void eat(){System.out.println("eating rat...");}
}
class Lion extends Animal{
	void eat(){System.out.println("eating meat...");}
}
class TestPolymorphism3{
	public static void main(String[] args){
		Animal a;
		a=new Dog();
		a.eat();
		a=new Cat();
		a.eat();
		a=new Lion();
		a.eat();
}}

// Output
eating bread...
eating rat...
eating meat...

```

You can use the `super` keyword to retain the parent class call inside the child class of the same method

```Java
class ParentClass{
	public void disp(){
		System.out.println("Parent Class is called");
	}
}
class ChildClass extends ParentClass{
	public void disp(){
		super.disp();
		System.out.println("Child Class is called");
	}
}
public class Overriding_Example {
	public static void main(String args[]){
		//ParentClass reference but ChildClass Object.
		ParentClass  obj1 = new ChildClass();

		// Child Class disp () will be called, as it reference to the child class.
		obj1.disp(); 
	}
}
```

#### Method Overloading
- Having more than one method with the same name within the same [[Introduction to OOP#Class|class]] but different parameters.
- JVM detect differences using their parameters.
```Java
class Pattern {

  // method without parameter
  public void display() {
    for (int i = 0; i < 10; i++) {
      System.out.print("*");
    }
  }

  // method with single parameter
  public void display(char symbol) {
    for (int i = 0; i < 10; i++) {
      System.out.print(symbol);
    }
  }
}

class Main {
  public static void main(String[] args) {
    Pattern d1 = new Pattern();

    // call method without any argument
    d1.display();
    System.out.println("\n");

    // call method with a single argument
    d1.display('#');
  }
}


// Output
**********

##########
```

> In this example we have two display method, one don't have any input parameter while the other has a `char` parameter.
> 
> To create a method overload, you must need to have different parameters, either in types, amount, or both so JVM won't get mad at you.