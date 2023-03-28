A class is a group of objects which have common properties. It is a template or blueprint from which objects are created. It is a logical entity. It can't be physical.

It contains:
- Fields
- Methods
- Constructors
- Blocks
- Nested class and interface

### Syntax
```Java
class <className>{
	field;
	method;
}
```

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