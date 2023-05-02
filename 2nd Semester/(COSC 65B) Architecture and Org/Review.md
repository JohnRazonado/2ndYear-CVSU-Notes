> Need to remove the preliminaries and program design. The new topics that needs to review are:
> - Boolean Algebra
> - Logic Gates


## [[Boolean Algebra]]
- Branch of algebra dealing with two value:
	- 1 and 0
- Deals with **logic and truth values**.
	- True and False
	- High and Low
- Known to be used on digital circuitry in digital computers and other digital systems.
- Name in honor of English Mathematician **George Boole**,
	- Proposed basic principle in **1854** in his treatise
	- **An Investigation of the Laws of Thought on Which to Found the Mathematical Theories of Logic and Probabilities.**
- First utilized by Claude Shannon in 1938
	- In 1938, Claude Shannon, a research assistant in the Electrical Engineering Department at M.I.T., suggested that Boolean algebra could be used to solve problems in relay-switching circuit design.
- Convenient in two areas
	- **Analysis** - economical way of describing function of digital circuitry.
	- **Design** -  applied to develop a simplified implementation of that function.
### Logic Operations
#### AND
- Yields true (1) if and only if both of its operands are true
- 
#### OR
-  yields true if either or both of its operands are true. 
#### NOT
- inverts the value of its operand.

##### Precedence
1. NOT
2. AND
3. OR


### Advance Operators
#### XOR
- exclusive-or (XOR)
-  1 if and only if exactly one of the operands has the value 1
#### NAND
 - Complement (NOT) of the AND function
#### NOR
- Complement of OR

![[Pasted image 20230405145053.png]]

![[Pasted image 20230405145101.png]]

### [[2nd Year/2nd Semester/(COSC 65B) Architecture and Org/Boolean Algebra#Postulate and Rules|Postulates and Rules]]
#### Identity law
- This states that if we OR a variable with 0 or AND a variable with 1, the result is the original variable.
- ![[Pasted image 20230430205208.png]]
#### Commutative law
-  order in which variables are ORed or ANDed does not affect the result.
- ![[Pasted image 20230430205222.png]]
#### Associative law
-  Grouping of variables when ORed or ANDed does not affect the result.
- ![[Pasted image 20230430205253.png]]
#### Distributive law
- ORing or ANDing a variable with a group of variables that are ORed or ANDed together is equivalent to ORing or ANDing the variable with each individual variable in the group.
- ![[Pasted image 20230430205317.png]]
#### Complement law
- Every variable has a complement, which is the value that makes the OR or AND operation with the original variable equal to 1 or 0
- (A')' = A 
#### DeMorgan's laws
- Have two states
	-  Complement of a group of variables ORed together is equivalent to the AND of the complements of each individual variable in the group.
		- ![[Pasted image 20230430205540.png]]
	-  Complement of a group of variables ANDed together is equivalent to the OR of the complements of each individual variable in the group.
		- ![[Pasted image 20230430205600.png]]



## [[Binary Arithmetic]]
### [[Number System]]
|Number System| Base n|
|---|---|
|Decimal| Base 10|
|Octal| Base 8|
|Hexadecimal| Base 16|
|Binary| Base 2|

#### Binary
- Individual digits of a binary number are referred to as bits
- Can be represented as **True** or **False** (**T** or **F**), **High** or **Low** (**H** or **L**), and **On** or **Off**

01011 = 0 \* 2<sup>4</sup>  \* 1 \* 2<sup>3</sup> + 0 \* 2<sup>2</sup> + 1 \* 2<sup>1</sup> + 1 \** 2<sup>0</sup> = 11
00010 = 0 \* 2<sup>4</sup> + 0 \* 2<sup>3</sup> + 0 \* 2<sup>2</sup> + 1 \* 2<sup>1</sup> + 0 \* 2<sup>0</sup> = 2


### Binary Addition
|Binary Addition| Equivalent Decimal Addition|
|---|---|
|![[Pasted image 20230405142344.png]]|![[Pasted image 20230405142400.png]]|

#### Binary Multiplication
|Binary Multiplication| Equivalent Decimal Multiplication|
|---|---|
|![[Pasted image 20230405142811.png]]|![[Pasted image 20230405142821.png]]|

#### Binary Division
- Mga BIG BOI na kayo

#### One's Complement
- Binary subtraction that inverses
#### Two's Complement
- Representation of signed binary numbers
- Leading bit is a sign bit
	- Binary number with leading 0 is positive
	- Binary number with leading 1 is negative
- Magnitude of positive numbers is just the binary representation
- Magnitude o negative numbers is found by
	- Complement the bits
	- Replace all the 1's with 0's, and all the 0's with 1's
	- Add one to the complemented number
- The carry in the most significant bit position is thrown away when performing arithmetic



## [[Logic Gates#Gates|Gates]]
- A gate is a basic building block that performs a specific logical operation on one or more binary inputs to produce a binary output.
- Logical functions are implemented by the interconnection of gates.
- A gate is an electronic circuit that produces an output signal that is a simple Boolean operation on its input signals.
- Gates are used to construct more complex digital circuits, such as adders, multiplexers, and memory units.

---
> Beyond this line are outlines that isn't scoped by the midterm examination
---


## [[Preliminaries - Architecture and Organization|Architecture and Organization]]
Way of computer systems designed and how its component works to perform tasks and instructions.

**Architecture** - Overall design and structure of a computer system. Includes [[Preliminaries - Architecture and Organization#ISA|ISA]], processor org, mem hierarchy, and I/O systems.

**Organization** - Diff components way and works together interconnected to implement comp struc. Includes a typical Von Neumann Architecture.

### Types of Computer Architecture
#### Von Neumann Architecture
- Mathematician **John Vonn Neumann** in **1940**
- Four Main Components:
	- **CPU**
	- **Memory**
	- **I/O Devices**
	- **Control Unit**
- Widely used today for general computers
- **Fundamental concept in computer science**

#### Harvard Architecture
- Instruction and data stored in separate memories
	- Faster access to instructions and data
- Commonly in embedded systems.

#### SIMD (Single Instruction, Multiple Data) Architecture
- Perform same operation on multiple data simultaneously
- Commonly used in GPUs

#### MIMD (Multiple Instructions, Multiple Data) Architecture
- Execute multiple instructions on multiple data elements simultaneously
- Common in clusters computers and distributed computing system.

#### [[Preliminaries - Architecture and Organization#CISC|CISC (Complex Instruction Set Computing) Architecture]]
- Used on older desktop and server processors

#### [[Preliminaries - Architecture and Organization#RISC|RISC (Reduced Instruction Set Computing) Architecture]]
- Commonly used in modern desktop and server processors
	- As well as on mobile devices and embedded systems


### Components of Computer Systems
#### CPU
- Central Processing Unit
- Brain of Computer
-  Executing instructions and performing calculations
- Composition
	- **Arithmetic Logic Unit (ALU)**
		- Perform arithmetic and logical operations
			- Addition, subtraction, comparison
	- **Control Unit (CU)**
		- Instruction executed bit by bit
		- Fetches instruction from memory
		- The fetch/execute cycle is the steps the CPU takes to execute an instruction.
		- Performing the action specified by an instruction is known as executing the instruction.
	- **Register**
		- Fast memory, small capacity to hold data and instruction.

#### Memory
- Stores information being processed by the CPU.
- Critical component of computer systems
- Stores both data and instructions

#### RAM
- Random Access Memory
- **Volatile memory**
- Contents lost when computer is turned off

#### ROM
- Read-only Memory
- **Non-volatile memory** - retains content even in power loss.
	- **HDD** - Movable disk inside and has moving parts
	- **SSD/Flash Drive** - Store on flash storage chip

#### I/O Devices
- Input/Output Devices
- Responsible for communicating outside world
-  Includes buses, which are communication pathways allow to transfer between different components
- **Input Devices** - Allows people supply information to computers
- **Output Devices** - Allows people to receive information from computers

##### Monitor
- Display device that operates like a television
	- Also known as CRT (Cathode ray tube)
- Controlled by an output device called a *graphics card*
- Displayable area
	- Measured in dot per inch, dots are often referred to as pixels (short for picture element)

### Evolution of Computers
#### First Generation
-   Vacuum Tube
-   Famous compute are known as IAS computer like Alan Turing EDVAC (Electronic Discrete Variable Computer) of 1946
#### Second Generation
-   Big Transistors - Smaller than vacuum, cheaper, and generates less heat.
-   IBM 7094 [BELL71] introduced in 1952
#### Third Generation
-   Began to used integrated circuit (IC)
-   IBM System/360 and the DEC PDP-8 in 1958.
#### Fourth Generation
-   Based on advancement of Integrated Circuits
-   Introduction of Larger-scale Integration (LSI), VLSI, and ULSI chips.

### Intel x86 Architecture
- Used in a large parts of computers
	- decades of design effort on complex instruction set
- Incorporates sophisticated design principles from mainframes and supercomputers
- Ranked 1st maker of micropocessors
- Evolution of its flagship microprocessor = Good indicator of evolution of computer tech.

#### Evolution of Intel products
-   **8080**: 8-bit machine
    -   **First personal computer**, Altair.
-   **8086**: More powerful than previous one, 16-Bit Machine
-   **80286**: Extension of 8086, have 16 MB addressing memory instead of 1 MB
-   **80386**: First 32-bit machine
-   **80486**: Introduced sophisticated cache tech and sophisticated instruction pipelining.  
    - Offered built-in math processor, offloading complex math operations complex math operations from main CPU.
-   **Pentium**: use of superscalar techniques
    -   Multiple instructions in parallel.
-   **Pentium Pro**: Continued move into superscalar organization
    -   Aggressive use of register renaming, branch prediction, data flow analysis, and speculative execution.
-   **Pentium II**: Intel MMX technology
    -   Process video, audio, and graphics data efficiently.
-   **Pentium III**: Additional floating point instructions
    -   Increase performance on multiple data objects.
        -   Digital signal processing and graphics processing.
-   **Pentium IV**: Additional floating-point
    -   Other enhancement for multimedia
-   **Core**: First x86 with dual core
    -   Implementation of two cores on single chip.
-   **Core 2**: Extends to 64 bits, with Core 2 Quad.
    -   Four cores on a single chip
    -   256-bit Advanced Vector Extensions instructions.
        -   "256 bits" means how many bits can be executed in a clock cycle (CPU time).
        -   Then 512-bit instructions.

### Instruction Sets
- Collection of instructions/commands that a processor can understand and executed.

##### [[Preliminaries - Architecture and Organization#ISA|ISA]]
- **Instruction Set Architecture**
- Defines instruction of a processor can execute

##### x86
- Most known in personal computer and servers
- Large and complex instruction set


##### [[ARM Architecture|ARM]]
- Family of RISC design in embedded systems
- Design by **ARM Holdings**, Cambridge England
	- They don't make processor but the designs microprocessors and multicore instead license it.
- Types of licensable products:
	- **Processors**
	- **Processor architectures**
- High-speed processors known for small die size and low powered
- Widely used in smartphones and other handheld devices, including game systems.

###### Cortex Architectures (A, R, M)
- **CORTEX-A/CORTEX-A50**
	- **Application processors**
	- Intended for mobile devices
-  **CORTEX-R** 
	- Support **real-time applications**, in which the timing of events needs with rapid response to events.
	- automotive braking systems, mass storage controllers, and networking and printing devices.
- **CORTEX-M**
	- Primarily for **microcontroller domain** that needs fast and lowest possible power consumption.
	- Market includes IoT devices, wireless sensor/actuator networks used in factories and other enterprises, automotive body electronics, and so on.

##### MIPS
- Known for **simplicity and efficiency**
- Embedded systems and network equipment
- Calculators use it

#### Types of Instruction Sets
##### RISC
-   **Reduced Instruction Set Computing**
-   Fewer instructions and simple operations

##### CISC
-   **Complex Instruction Set Computing**
-   One time big time execution of instruction
-   Multiple operations in one instruction

##### [[Preliminaries - Architecture and Organization#RISC vs. CISC|RISC vs. CISC]]
There is no best architecture since different architectures can simply be better in some scenarios but less ideal in others.

-   RISC-based machines execute one instruction per clock cycle.
-   CISC machines can have special instructions as well as instructions that take more than one cycle to execute.
-   This means that the same instruction executed on a CISC architecture might take several instructions to execute on a RISC machine.
-   The RISC architecture will need more working (RAM) memory than CISC to hold values as it loads each instruction, acts upon it, then loads the next one.

|CISC| RISC|
|---|---|
|The original microprocessor ISA| Redesigned ISA emerged in the early 1980s|
|Instruction can take several clock cycles| Single-cycle instructions|
|**Hardware-centric design** - ISA does as much as possible using hardware circuitry| **Software-centric design** - High-level compilers take on most of the burden of coding many software steps from the programmer|
|Efficient use of RAM than RISC| Heavy use of RAM (can caused bottlenecks if RAM is limited)|
|Complex and variable length instructions| Simple, standardized instructions|
|May support microcode (micro-programming which instructions = small programs)| Only one layer of instructions|
|Large number of instructions| Small number of fixed-length instructions|
|Compound addressing modes| Limited addressing modes|

### [[Preliminaries - Architecture and Organization#Embedded Systems|Embedded Systems]]
- Fixed OS and functions, use of electronics and software within a product unlike to a general-purpose computer
- Can't reprogram and can't have any viruses at all.

#### Internet of Things (IoT)
- Major driver of proliferation of embedded system
- Primarily driven by deeply embedded devices:
	- low-bandwidth
	- low-repetition data-capture
	- low-bandwidth data-usage appliances
	- communicate and provide data via UI

##### Generations of IoT
1. **Information technology (IT)**
2. **Operational technology (OT)**
3. **Personal technology**
4. **Sensor/actuator technology**

### Cloud Computing
- A model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources that can rapidly provisioned and released with minimal effort.
- Concept of cloud computing is dated back 1950s, became available in early 2000s.
-  you get economies of scale, professional network management, and professional security management.

#### Cloud Networking
- refers to the networks and network management functionality that must be in place to enable cloud computing.
- One example is the provisioning of high-performance and/or high-reliability networking between the provider and subscriber.

#### Cloud storage
Subset of cloud computing which consists of database storage and database applications hosted remotely on cloud servers.
- Small business and individuals take advantage of data storage at large scale.

#### Cloud Services
A cloud service provider (CSP) **maintains computing and data storage** resources that are available over the Internet or private networks.
- Virtually all cloud service is provided using one of three models SaaS, PaaS, and IaaS
##### Software as a Service (SaaS)
- Provide **service in the form of software, specifically application software**, running on and accessible in the cloud.
- Can be accessible through simple interface like  **Web browser**.
##### Platform as a Service (PaaS)
- Service in a form of a platform on which the **customer’s applications can run (Operating System in Cloud).**
- Provides useful software building blocks, some development tools, such as programming languages, run-time environments, and other tools that assist in deploying new applications.
##### Infrastructure as a Service (IaaS)
- Customer has access to the **underlying cloud infrastructure**.
- Provides virtual machines and other abstracted hardware and operating systems, maybe controlled through application programming interface (API).

## [[Machine, Software, and Program Design|Program Design]]
### [[Machine, Software, and Program Design#Software|Software]]
- Two types: Application software and System software
#### Application Software
- Programs designed to perform specific tasks that are transparent to the user
- Made using indispensable and popular
- Common application software
	- Word processors
	- Desktop publishing programs
	- Spreadsheets
	- Presentation managers
	- Drawing programs

#### System Software
- Support execution and development of other programs
- Major Types
	- Operating systems
	- Translation systems
##### Operating System
- Control and manages the computing resources
- Important services that an operating system provides
	- File system
	- Commands that allows for manipulation
		- Sort, delete, copy
	- Ability to perform I/O on devices
	- Management of running systems
##### Translation System
- Set of programs used to develop softwares
- Types of translators
	- Compiler
	- Linker


### [[Machine, Software, and Program Design#Software Development|Software Development]]
#### Software Development Activities
- Editing
- Compiling
- Linking with precompiled files
	- Object files
	- Library modules
- Loading and executing
#### Cycle
![[Pasted image 20230405132328.png]]

#### IDEs
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


### [[Machine, Software, and Program Design#Engineering Software|Engineering Software]]
#### Software Engineering
- Area of comp science with **building large software systems**
#### Challenge
- Advances in hardware have not been accompanies by comparable advances in software
#### [[Machine, Software, and Program Design#Complexity Trade-off|Complexity Trade-off]]
- Complexity tends to grow as system becomes more user friendly
#### [[Machine, Software, and Program Design#Soft Eng Goals|Software Engineering Goals]]
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

#### Principles
- **Abstraction** - Extract relevant properties while ignoring inessentials
- **Encapsulation** - Hide and protect essential information through a controlled interface
- **Modularity** - Dividing an object into smaller modules so that it is easier to understand and manipulate
- **Hierarchy** - Ranking or ordering of objects based on some relationship between them.


### OO Design and Programming
- Object-oriented design and programming methodology supports good software engineering
#### [[Machine, Software, and Program Design#Object Objects|Objects]]
- Almost everything with the following characteristics
	- Name
	- Properties
	- Ability to act upon receiving a message
