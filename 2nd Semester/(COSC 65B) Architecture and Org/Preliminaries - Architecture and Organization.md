> Some info here: https://hackmd.io/@HI3bjVEIT5KFpp6o0ZWvzw/BJgo5ake9

## What's Computer Architecture and Organization?
It is mostly the way computer systems designed and how its components works to perform tasks and instructions.

**Architecture** - overall design structure of a computer system. Including its instruction set architecture (ISA), processor organization, memory hierarchy, and input/output (I/O) systems.

**Organization** - Different components way and works together interconnected to implement computer architecture. Includes the design of Central processing unit (CPU), memory system, and I/O system.

## Types of Computer Architecture
### Von Neumann Architecture
- Proposed by mathematician John Vonn Neumann in 1940
- Has four main components:
	- CPU
	- Memory
	- I/O devices
	- Control Unit
- Widely used today for most general-purpose computers (desktops, laptops, and servers).
- Fundamental concept in computer science.
### Harvard Architecture
- Instruction and data stored in separate memories.
	- Allows faster access to instructions and data.
- Commonly used in embedded systems.
### SIMD (Single Instruction, Multiple Data) Architecture:
- Designed to perform same operation on multiple data simultaneously
- Commonly used in graphics processing units (GPUs)
### MIMD (Multiple Instructions, Multiple Data) Architecture
- Designed to execute multiple instructions on multiple data elements simultaneously.
- Commonly used in clusters of computers and in distributed computing system.
### CISC (Complex Instruction Set Computing) Architecture
- Commonly used in older desktop and server processors
### RISC (Reduced Instruction Set Computing) Architecture
- Commonly used in modern desktop and server processor, as well as mobile devices and embedded systems.

## Components of Computer Systems
### Central Processing Unit (CPU)
- Brain of the Computer
- Executing instructions and performing calculations
- Composed of the following:
	- Arithmetic Logic Unit (ALU)
		- Performs arithmetic and logical operations
			- Addition, subtraction, comparison
	- Control Unit (CU)
		- Instruction is executed bit by bit
		- Fetches instruction from memory
	- Register
		-  Fast memory, small capacity to hold data and instructions.
		- Currently being used by CPU
### Memory
- Critical component of computer system.
- Stores both data and instructions.

#### RAM (Random Access Memory)
- Volatile memory
- Contents are lost when the computer is turned off.

### ROM (Read-Only Memory)
- Non-volatile memory that retains content even in power loss.
	- **HDD** - Movable disk inside and has a moving parts.
	- **SSD**/**Flash Drive** -  Store on a flash storage chip has index under a tables and container

#### Types of Computer Memory
![[Pasted image 20230318203649.png]]


### Memory Hierarchy
![[Memory-Hierarchy.jpg]]
https://computerscience.chemeketa.edu/cs160Reader/ComputerArchitecture/MemoryHeirarchy.html
- Faster memory and closest to the CPU goes up the top
- Also, most on the top are on the CPU itself.

**Computer Top-Level Structure**
![[Pasted image 20230318210320.png]]

**Simplified View of Major Elements of a Multicore Computer**
![[Pasted image 20230318212438.png]]
### I/O Devices
- Responsible for communicating to the outside world.
- It includes buses, which are communication pathways allow to transfer between different components of computer system.
- Unknown ports
	- PS/2 port - Common interface of keyboard and mouse. No plug and play back then.
	- Parallel port - Printers
	- Serial Port - May use as a mouse interface.
	- IEEE Port - Some other old devices.


## Evolution of Computers
### First Generation
- Vaccum Tube
- Most famous compute are known as IAS computer like the Alan Turing EDVAC (Electronic Discrete Variable Computer) of 1946
### Second Generation
- Big Transistors - Smaller than vacuum, cheaper, and generates less heat.
- IBM 7094 [BELL71] introduced in 1952
### Third Generation
- Began to used integrated circuit (IC)
- IBM System/360 and the DEC PDP-8 in 1958.
### Fourth Generation (Last one)
- Based on advancement of Integrated  Circuits
- Introduction of Larger-scale Integration (LSI), VLSI, and ULSI chips.

### INTEL x86 Architecture
- Currently used in a large part of computers
	- Result of decades design effort on complex instruction set computers
- Incorporates sophisticated design principles from mainframes and supercomputers.
- Intel ranked as 1 maker of microprocessors for non-embedded systems for decades.
- Evolution of its flagship microprocessor = Good indicator of evolution of computer tech.

#### Evolution of Intel products
- **8080**: 8-bit machine
	- First personal computer, Altair.
- **8086**: More powerful than previous one, 16-Bit Machine
- **80286**: Extension of 8086, have 16 MB addressing memory instead of 1 MB
- **80386**: First 32-bit machine
- **80486**: Introduced sophisticated cache tech and sophisticated instruction pipelining.
		- Offered built-in math processor, offloading complex math operations complex math operations from main CPU.
- **Pentium**: use of superscalar techniques
	- Multiple instructions in parallel.
- **Pentium Pro**: Continued move into superscalar organization
	- Aggressive use of register renaming, branch prediction, data flow analysis, and speculative execution.
- **Pentium II**: Intel MMX technology
	- Process video, audio, and graphics data efficiently.
- **Pentium III**: Additional floating point instructions
	- Increase performance on multiple data objects.
		- Digital signal processing and graphics processing.
- **Pentium IV**: Additional floating-point
	- Other enhancement for multimedia
- **Core**: First x86 with dual core
	- Implementation of two cores on single chip.
- **Core 2**: Extends to 64 bits, with Core 2 Quad.
	- Four cores on a single chip
	- 256-bit Advanced Vector Extensions instructions.
		- "256 bits" means how many bits can be executed in a clock cycle (CPU time).
		- Then 512-bit instructions.

## Instruction Sets
- Collection of instructions/commands that a processor can understand and executed.
- Literally a vocabulary for processors
	- Specific operation of processors to be performed like arithmetic, logic, or I/O operations.
### ISA
- **Instruction Set Architecture**
- Defines instruction of a processor can execute.

### x86
- Most known in personal computers and servers
- large and complex instruction set

### [[ARM Architecture|ARM]]
- Energy efficient and simplicity
- Mobile devices and embedded systems

### MIPS
- Instruction set known for simplicity and efficiency
- Embedded systems and network equipment
- Calculators use it

### Types of Instruction Sets
#### RISC
- **Reduced Instruction Set Computing**
- Fewer instructions and simple operations

#### CISC
- **Complex Instruction Set Computing**
- One time big time execution of instruction
- Multiple operations in one instruction
- More complex instruction set.

#### RISC vs. CISC
There is no best architecture since different architectures can simply be better in some scenarios but less ideal in others.
- RISC-based machines execute one instruction per clock cycle.
- CISC machines can have special instructions as well as instructions that take more than one cycle to execute.
- This means that the same instruction executed on a CISC architecture might take several instructions to execute on a RISC machine.
- The RISC architecture will need more working (RAM) memory than CISC to hold values as it loads each instruction, acts upon it, then loads the next one.

|Differences|CISC| RISC|
|---|---|---|
|**Instruction set complexity**| Large and complex instruction sets| Smaller instruction|
|^^| Perform multiple operation in one instruction| One operation per instruction|
|**Register Usage**| Less available registers for programs| Have more registers available for programs|
|^^|^^| Faster execution times|
|**Transaction Decoding**| Complex instruction decoding logic| Simpler decoding logic|
|^^| More hardware resource, overall increase complexity of processor| easy to implement and faster execution times|
|**Memory Access**| Few registers more memory| Fewer memory access, low power and fast execution|
|**Pipelining**| Difficult to pipeline| Amenable/favorable to pipelining allowing multiple instructions executed simultaneously|
|^^|Due to larger and more complex instruction sets| Multiple instructions executed simultaneously|
|**Code density**| More compact code| More execution, more code|
| **Other**| Execute all at one, more complex instruction directly upon memory| More RAM but executes one instruction per clock cycle, good for pipelining.|

##### Major Differences
- RISC emphasizes efficiency in cycles per instruction but needs more RAM
- CISC emphasizes efficiency in instructions per program and smaller code size and uses less RAM.
- Overall, RISC processors are often designed for efficiency and simplicity, while CISC processors are designed for flexibility and code density.
- However, the distinction between RISC and CISC has become less clear over time, as many modern processors incorporate features of both architecture.


##### Conclusion
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



## Embedded Systems
- Fixed OS and functions, use of electronics and software within a product unlike to a general-purpose computer
- Can't reprogram and can't have any viruses at all.
- Types of devices with embedded systems
	- cell phones, digital cameras, video cameras, calculators, microwave ovens, home security systems, washing machines, lighting systems, thermostats, printers, various automotive systems (e.g., transmission control, cruise control, fuel injection, anti-lock brakes, and suspension systems), tennis rackets, toothbrushes, and numerous types of sensors and actuators in automated systems.
### Internet of Things (IoT)
- Major driver of proliferation of embedded system
- Primarily driven by deeply embedded devices:
	- low-bandwidth
	- low-repetition data-capture
	- low-bandwidth data-usage appliances
	- communicate and provide data via UI.
- Embedded appliances, such as high-resolution video security cameras, video VoIP phones, and a handful of others, require high-bandwidth streaming capabilities.

#### Generations
- Internet has gone through roughly four generations of deployment culminating in the IoT:
1. Information technology (IT):
	- PCs, servers, routers, firewalls, and so on.
	- bought as IT devices by enterprise IT primarily wired connectivity.
2. Operational technology (OT): 
	- Machines/appliances with embedded IT built by non-IT companies 
	- Such as medical machinery, SCADA (supervisory control and data acquisition), process control, and kiosks.
	- Bought by enterprise OT people primarily wired connectivity
3. Personal technology: 
	- Bought as IT devices by consumers (employees) exclusively wireless connectivity and multiple forms of wireless connectivity.
	- Smartphones, tablets, and eBook readers.
4. Sensor/actuator technology: 
	- Single-purpose devices bought by consumers, IT, and OT people exclusively using wireless connectivity
	- Generally single form, as part of larger systems.

It is the fourth generation that is usually thought of as the IoT, and it is marked by the use of **billions of embedded devices**.


## Cloud Computing
- A model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources that can rapidly provisioned and released with minimal effort.
- Concept of cloud computing is dated back 1950s, became available in early 2000s, particularly targeted at large enterprises.
-  Basically, with cloud computing, you get economies of scale, professional network management, and professional security management.
- The individual or company only needs to pay for the storage capacity and services they need.
- It offered services such as setting up a database system, the hardware and its maintenance, data backup as well as security.
### Cloud networking 
refers to the networks and network management functionality that must be in place to enable cloud computing.
- One example is the provisioning of high-performance and/or high-reliability networking between the provider and subscriber.
- Some or all of the traffic between an enterprise and the cloud bypasses the Internet and uses dedicated private network facilities owned or leased by the cloud service provider.
### Cloud storage
Subset of cloud computing which consists of database storage and database applications hosted remotely on cloud servers.
- Enables small businesses and individual users to take advantage of data storage that scales with their needs and to take advantage of a variety of database applications without having to buy, maintain, and manage the storage assets.

### Cloud Services
A cloud service provider (CSP) **maintains computing and data storage** resources that are available over the Internet or private networks.
- Virtually all cloud service is provided using one of three models SaaS, PaaS, and IaaS
#### Software as a Service (SaaS).
- Provide service in the form of software, specifically application software, running on and accessible in the cloud.
- SaaS enables the customer to use the cloud provider’s applications running on the provider’s cloud infrastructure and can be accessible through simple interface like  **Web browser**.
- **Saves the complexity** of software installation, maintenance, upgrades, and patches.
- Examples are Gmail, Google’s e-mail service, and Salesforce.com, which help firms keep track of their customers.
#### Platform as a Service (PaaS)
- Service in a form of a platform on which the customer’s applications can run (Operating System in Cloud).
- PaaS enables the customer to deploy onto the cloud infrastructure containing customer-created or acquired applications.
- Provides useful software building blocks, some development tools, such as programming languages, run-time environments, and other tools that assist in deploying new applications.
- It’s is an operating system in the cloud.
- Example of this are Google App Engine and the Salesforce1 Platform from Salesforce.com.
#### Infrastructure as a Service (IaaS)
- With IaaS, the customer has access to the **underlying cloud infrastructure**.
- Provides virtual machines and other abstracted hardware and operating systems, maybe controlled through application programming interface (API).
- Offers the customer processing, storage, networks, and other fundamental enabling them to deploy and run arbitrary software, which can include operating systems and applications.
- Examples are Amazon Elastic Compute Cloud (Amazon EC2) and Windows Azure.

![[Pasted image 20230319002341.png]]