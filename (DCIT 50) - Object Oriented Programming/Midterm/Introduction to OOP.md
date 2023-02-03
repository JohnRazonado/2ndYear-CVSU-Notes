This part will discuss the fundamentals of OOP, from making everything as an object to different behavior of it.

- OOP as a whole is a paradigm that allows programmers/ developers to code in unison while still having a sense of stacking each other without falling apart.
- A programming **paradigm** that tells everything is an <mark style="background: #BBFABBA6;">object</mark>.
- Some popular OOP languages are Java, C#, PHP, Python, C++, and more.


## Some History
### Simula
- Considered as the <mark style="background: #D2B3FFA6;">first object-oriented programming language</mark>.
- Where the paradigm that everything is an object.

### Smalltalk
- Considered to be the <mark style="background: #D2B3FFA6;">first OOP language</mark>.

## Terms used in OOP design
- **Coupling** - Knowledge or information or dependency of another class. Arises when classes are aware of each other.
	- It mostly refers to how related or dependent two classes/ modules to one another. 
	- Low coupling - major changes in one class won't affect the other.
	- High coupling - major changes will affect another class making it difficult to maintain.
- **Cohesion** - Levels of a component which performs a single well-define task.
	- A highly cohesive method do single well-defined task.
- **Association** - Relationship between objects ^e7dd84
	- One to One
	- One to Many
	- Many to One
	- Many to Many
- **Aggregation** - Way to achieve [[Introduction to OOP#^e7dd84|Association]]. Represents relationship where one object contains other as part of its state. ^96c534
	- It is a pure **has-a** relationship where objects are independent of each other.
	- If we delete the parent class, the child will still exist.
	- A "uses" B = Aggregation : B exists independently (conceptually) from A
- **Composition** - Also a way to achieve [[Introduction to OOP#^e7dd84|Association]]. Represents the relationship where one object contains other objects as a part of its state. ^08727e
	- Specific type of aggregation where objects are dependent to one another
	- Child objects have a lifetime where if we delete the parent class, child also gets cease to exist.
	- Also referred as "[death](https://www.infoworld.com/article/3029325/exploring-association-aggregation-and-composition-in-oop.html)" relationship
	- A "owns" B = Composition : B has no meaning or purpose in the system without A

Example of [[Introduction to OOP#^96c534|Aggregation]] vs. [[Introduction to OOP#^08727e|Composition]]:
> A Text Editor owns a Buffer (composition). A Text Editor uses a File (aggregation). When the Text Editor is closed, the Buffer is destroyed but the File itself is not destroyed.
>- [Curtis Batt](https://softwareengineering.stackexchange.com/questions/61376/aggregation-vs-composition)

Good software design has **high cohesion** and **low coupling**.
> - See this [stackoverflow query](https://stackoverflow.com/questions/3085285/difference-between-cohesion-and-coupling)

## Concepts
OOP is created to really simplifies software development and maintenance by having the following concepts:
- [[Object]]
- [[Class]]
- [[Inheritance]]
- [[Polymorphism]]
- [[Abstraction]]
- [[Encapsulation]]

### [[Object]]
The **[[State of an Object|state]]**, **[[Behavior of an Object|behavior]]**, and **[[Identity]]** of different aspect of a programming language
- For Example, Pen is an object. Its name is Reynolds; color is white, known as its state. It is used to write, so writing is its behavior.

### [[Class]]
- The template or blueprint of the object.
- The *Collection of objects*.
- A logical entity.

---

### [[Inheritance]]
- The child can inherit all parent attributes
- Used to achieve runtime polymorphism
- Need to use the **[[Inheritance#"extends" Keyword|extend]]** keyword to inherit the attributes

> object acquires all the properties and behaviors of a parent object,

### [[Encapsulation]]
**Hiding objects and data** giving it security as private as possible.

- _process of wrapping code and data together into a single unit_,
- Using setter and getter classes
- The **[Java Bean](https://www.javatpoint.com/java-bean)** class is the example of a fully encapsulated class.

### [[Polymorphism]]
Having different forms in one single class.
- One task performed in different ways.
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

Example:
to convince the customer differently, to draw
something, shape, triangle, rectangle, etc.

#### [[Polymorphism#Method Overriding|Method Overriding]]
- Having the same method on different class inherited from the parent class but different outcome.

#### [[Polymorphism#Method Overloading|Method Overloading]]
- Having more than one method with the same name within the same [[Introduction to OOP#Class|class]] but different parameters.

### [[Abstraction]]
- Ability of <mark style="background: #FFB8EBA6;">hiding internal details and showing functionality</mark>
- It is the ability to create a class that can't be instantiated. 
- All other functionality as a class exist but without creating an instance of it.
> Essentially, we know what an object is but we don't really need to know the inner working of it.

In order to use the abstract functionality, you need to use an [[Abstraction#Abstract class|abstract class]] and [[Abstraction#Interface class|interface]] to achieve it. Also using an [[Abstraction#Abstract method|abstract method]] using the `abstract` keyword if you want a method needed in every inherit of the [[Abstraction#Abstract class|abstract class]].
