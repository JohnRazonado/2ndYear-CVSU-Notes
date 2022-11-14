A Package can be defined as a grouping of related types(classes, interfaces, enumerations and annotations) providing access protection and name space management. 

- Some of the existing packages in Java are: 
	- java.lang - bundles the fundamental classes
	- java.io - classes for input, output functions are bundled in this package
> Programmers can also define their own packages. Use to group classes/interfaces

## Import
If a class wants to use another class in the same package, the package name does not need to be used. Classes in the same package find each other without any special syntax.

Example:
> This part is the main class
```Java
package payroll; 
public class Boss {
	public void payEmployee(Employee e){
		e.mailCheck();
	}
}
```

To use this as to another class without using the payroll prefix (`payroll.Employee`)
```Java
import payroll.*; //using a wildcard "*" to import
import payroll.Employee; //using the class itself

```

## Structure of Packages
Two major results occur when a class is placed in a package:
- The name of the package becomes a part of the name of the class, as we just discussed in the previous section. 
- The name of the package must match the directory structure where the corresponding bytecode resides. 

Here is simple way of managing your files in Java: 
>Put the source code for a class, interface, enumeration, or annotation type in a text file whose name is the simple name of the type and whose extension is .java. For example:

```Java
// File Name : Car.java
package vehicle; public class Car{ 
	// Class implementation. 
}
```
The class name and pathname could be
- Class name -> vehicle.Car
- Path name -> vehicle\\Car.java (in Windows)