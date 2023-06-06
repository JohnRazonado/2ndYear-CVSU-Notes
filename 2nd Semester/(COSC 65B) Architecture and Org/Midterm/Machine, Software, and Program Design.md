#inProgress 
## Computer Organization
![[Pasted image 20230405085947.png]]

### [[Preliminaries - Architecture and Organization#Central Processing Unit (CPU)|Central Processing Unit (CPU)]]
- **Brains** of the computer
	- ALU or Arithmetic/Logical Unit
		- Perform Arithmetic calculations
		- Calculations are performed using binary numbers
	- Also contains the **Control Unit**
		- The fetch/execute cycle is the steps the CPU takes to execute an instruction
		- Performing the action specified by an instruction is known as executing the instruction
		- The program counter (PC) holds the memory address of the next instruction
- Where decisions are made, computations are performed, and input/output requests are delegated

### [[Preliminaries - Architecture and Organization#Memory|Memory]]
- Stores information being processed by the CPU.

### [[Preliminaries - Architecture and Organization#I/O Devices|Input Devices and Output Devices]]
- **Input Devices** - Allows people supply information to computers
- **Output Devices** - Allows people to receive information from computers
- Accessories that allow computer to perform specific tasks
	- Receive information for processing
	- Return the results of processing
	- Store information
- Common input and output devices
	- Speakers
	- Printer
	- Keyboard
	- Mouse
	- Joystick
	- Microphone
	- Scanner
	- CD-ROM
	- DVD
- Some devices are capable of both input and output
	- Floppy drive
	- Hard Drive
	- Magnetic tape units

#### Monitor
- Display device that operates like a television
	- Also known as CRT (Cathode ray tube)
- Controlled by an output device called a *graphics card*
- Displayable area
	- Measured in dot per inch, dots are often referred to as pixels (short for picture element)
	- Standard resolution is 640 by 480
	- Many cards support resolution of 1280 by 1024 or better
	- Number of colors supported varies from 16 to billions

## Software
### Application Software
- Programs designed to perform specific tasks that are transparent to the user

- Software that has made using computers indispensable and popular
- Common application software
	- Word processors
	- Desktop publishing programs
	- Spreadsheets
	- Presentation managers
	- Drawing programs
- *Learning how to develop application software is our focus*

### System Software
- Programs that support the execution and development of other programs
- Two majors types
	- Operating systems
	- Translation systems
#### Operating System
- Examples
	- Windows
	- Unix
	- Mac OS X
- Control and manages the computing resources
- Important services that an operating system provides
	- File system
		- Directories, folders, files
	- Commands that allow for manipulation of the file system
		- Sort, delete, copy
	- Ability to perform input and output on a variety of devices
	- Management of the running systems
#### Translation System
- Set of programs used to develop software
- A key component of a translation system is a translator
- Some types of translators
	- Compiler
		- Converts from one language to another
	- Linker
		- Combines resources
- Examples
	- Microsoft Visual C++, CBuilder, g++, Code Warrior
		- Performs compilation, linking, and other activities

## Software Development
### Software Development Activities
- Editing
- Compiling
- Linking with precompiled files
	- Object files
	- Library modules
- Loading and executing
- Viewing the behavior of the program

### Cycle
![[Pasted image 20230405132328.png]]

### IDEs
- Integrated Development Environments or IDEs
- Support the entire software development cycle
	- E.g., MS Visual C++, Borland, Code Warrior
- Provides all the capabilities for developing software
	- Editor
	- Compiler
	- Linker
	- Loader
	- Debugger
	- Viewer

## Engineering Software
### Software Engineering
- Area of computer science concerned with building large software systems
### Challenge
- Tremendous advances in hardware have not been accompanied by comparable advances in software.

### Complexity Trade-off
- System complexity tends to grow as the system becomes more user friendly
![[Pasted image 20230405133322.png]]


### Soft Eng Goals
- Reliability
	- An unreliable life-critical system can be fatal
- Understandability
	- Future development is difficult if software is hard to understand
- Cost Effectiveness
	- Cost to develop and maintain should not exceed profit
- Adaptability
	- System that is adaptive is easier to alter and expand
- Reusability
	- Improves reliability, maintainability, and profitability.

### Principles
#### Abstraction
- Extract relevant properties while ignoring inessentials
	- Defines a view of the object
-  Example - car
	- Car dealer views a car from selling features standpoint
		- Price, length of warranty, color, etc.
	- Mechanic views a car from systems maintenance standpoint
		- Size of the oil filter, types of spark plugs, etc.

#### Encapsulation
- Hide and protect essential information through a controlled interface

- Steps
	- Decompose an object into parts
	- Hide and protect essential information
	- Supply interface that allows information to be modified in a controlled and useful manner
- Internal representation can be changed without affecting other system parts
- Example - car radio
	- Interface consists of controls and power and antenna connectors
		- The details of hot it works is hidden
	- To install and use a radio
		- Do not need to know anything about the radio's electronics

#### Modularity
- Dividing an object into smaller modules so that it is easier to understand and manipulate
- Most complex systems are modular
- Example - Automobile can be decomposed into subsystems
	- Cooling system
		- Radiator          Thermostat        Water pump
	- Ignition system
		- Battery            Starter                 Spark plugs

#### Hierarchy
- Ranking or ordering of objects based on some relationship between them.
- Helps us understand complex systems
	- Example - a company hierarchy helps employees understand the company and their positions within it
- For complex systems, a useful way of ordering similar abstractions is a taxonomy from least general to most general.
- Sample
	- ![[Pasted image 20230405140117.png]]

## OO Design and Programming
- Object-oriented design and programming methodology supports good software engineering
	- Promotes thinking in a way that models the way we think and interact with the real world
- Example - Watching television
	- The remote is a physical object with properties
		- Weight, size, can send message to the television
	- The television is also a physical object with a various properties.

### [[Object|Objects]]
- An object is almost anything with the following characteristics
	- Name
	- Properties
	- The ability to act upon receiving a message
		- Basic message types
			- Directive to perform an action
			- Request to change one of its properties