- The rule to follow what to name **identifiers**
	- Class
	- Package
	- Variable
	- Constant
	- Method

## Advantage
- Make code easier to read for yourself and other programmers.
	- Increases Readability (*Readability 100*)
- Less time spent to figure out what the code does.

## Key rules
> This applies to every identifier
-  Name must not contain any white spaces
	- naming like `wow laki` won't be recognize
		- It should be `wowLaki` for example
- Name shouldn't start with special characters like:
	- & (ampersand)
	- $ (dollar)
	- _ (underscore)

## Naming rules
### Class
- Should start with **uppercase letter**
- Be a **noun** like
	- Color
	- Button
	- System
	- Thread
- Use **appropriate words**, instead of acronyms.
```Java
public class Employee{
	//code here
}
```

### Interface
- Should start with **uppercase letter**
- Should be an **adjective** like
	- Runnable
	- Remote
	- ActionListener
- Use appropriate words, instead of acronyms

```Java
interface Printable{
	//code snippet
}
```


### Method
- Should start with **lowercase letter**
- Should be **verb** like
	- main()
	- print()
	- println()
- If contain with multiple words, *start with lowercase followed by an uppercase*:
	- actionPerformed()

```Java
class Employee{
	//method
	void draw(){
		//put blue ice white dragon
	}
	void actionDeny(){
		//deny spell performed
	}
}
```

### Variable
- should start with **lowercase letter** like
	- id
	- name
- Like method, if it contains multiple words, start with lowercase letter followed by an uppercase:
	- firstName
	- lastName
- **Avoid** using one-character variable like `x`, `y`, `z`. %%I'll kill you if you do this to our code%%

```Java
class Employee{
	//variable
	int id;
	// code snippet
}
```

### [[Packages|Package]]
- Should be **lowercase letter** like
	- java
	- lang
- If contain multiple words, separate it by dots (.) like
	- java.util
	- java.lang

```Java
package com.javatpoint //package
class Employee{
	//code snippet
}
```

### Constant
- Should be **uppercase letters** to all like
	- RED
	- YELLOW
- If name contains multiple words, separate it by an underscore(\_) like `MAX_PRIORITY`
- May contain digits but not as first letter.
```Java
class Employee{
	//constant
	static final int MIN_AGE = 18;
	//code snippet
}
```


## CamelCase convention in Java
- Java follows camel-case syntax for naming the class, interface, method, and variable.
- If the name is combined with two words, the second word will start with uppercase letter always
	- actionPerformed()
	- firstName
	- ActionEvent
	- ActionListener

