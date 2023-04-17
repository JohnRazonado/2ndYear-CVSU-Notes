> The Powerpoint came from a different university called "Clemson University". A shameless used of other's university material indeed.

## Overview
- Modeling provides abstraction to bridge the gap between
	- High-level (world)
	- Low-level (code)
- Types of modeling:
	- Analysis modeling
		- Models problem domain (users, world)
	- System modeling
		- Models solution domain (software)

## Analysis Modeling
- Let us first look at modelling the problem domain

### Requirements Elicitation
- It is important to define *what* the software is supposed to do before
	- defining *how* to do it, or
	- before actually *doing* it
- “The hardest single part of building a software system is deciding what to build.” – Fred Brooks
- Requirements elicitation – gathering requirements from users and other stakeholders

### Difficulties in specifying requirements
- Customers often do not know what they want ... until they see it
- Customers often have a poor understanding of the ease or difficulty of implementing different capabilities
- The requirements change over time

### Steps in gathering requirements
- **Inception** – establish basic understanding of problem
- **Elicitation** – Ask the users what is needed
- **Elaboration** – Refine the model of the S/W functions, features, and constraints
- **Negotiation** – Reconcile conflicts by ranking requirements and discussing priorities
- **Specification** – Final work product describing the function and performance of the S/W
- **Validation** – Examine the specification to ensure that all requirements have been stated unambiguously, inconsistencies have been corrected, etc.

### Specifying requirements
Requirements can be specified in a number of ways:
- user scenarios 
- functions and feature lists
- analysis models
- specification 

### Traceability table
- Captures the relationships between
	- features and requirements
	- interfaces and requirements
	- requirements themselves (dependencies)
	- and more
![[Pasted image 20230412223020.png]]

### User scenarios
Usage scenarios
- identify a thread of usage for the system
- enable the S/W team to see how the functions and features will be used by different classes of end users
- often called *[[Modeling#Use cases|use cases]]*

### Use cases
- Use case tells a stylized story about how an end-user interacts with the system under a specific set of circumstances
- Can be either
	- narrative text
	- outline of tasks or interactions
	- template-based description, or
	- diagrammatic representation
- “A use-case captures a contract...” -- Alistair Cockburn, Writing Effective Use Cases. Addison-Wesley 2000. [http://www.usecases.org/](http://www.usecases.org/)
#### Example
**Use case:**  Withdraw money  
**Level:** User goal      *(Three levels:  Summary, User goal, and Sub-function level)*
**Primary actor:**  Client  
**Goal in context:**  To withdraw money from the client’s account  
**Preconditions:**  User has an account, ATM has power and connectivity  
**Main scenario:**
1. Client inserts card
2. Client types PIN
3. Client specifies which account
4. Client enters amount to withdraw
5. Money is dispensed
6. Card is ejected
7. Client removes card  
**Extensions:**
1a.  Card is invalid; card is ejected and client notified.
2a.  Pin is incorrect; client notified and given no more than two more attempts.
4a.  Amount exceeds limit; client notified, repeat step.
7a.  Client does not remove card within time limit; card is retracted.


## System modelling
- Now let us look at modelling the solution domain

### Data Flow Diagram (DFD)
- Data flow diagram (DFD) developed in late 1970s
	- part of Structured Design (one of the earliest methodologies for software development); aka Structured Systems Analysis and Design Method (SSADM), a waterfall method
	- invented by Larry Constantine, who also developed concepts of coupling and cohesion
- DFD is a forerunner of UML and may complement it
- Arcs are data; boxes are processes/actions
![[Pasted image 20230412224315.png]]

#### Gane and Sarson notation for DFDs
- squares – external entities
- round rectangles – processes
- arrows – data flow
- open-ended rectangles – data stores
![[Pasted image 20230412224409.png]]
> Sample of DFD from http://www.agilemodeling.com/artifacts/dataFlowDiagram.htm

#### DFD (Continuation)
- DFDs are refined iteratively
	- Level 0 is context-level DFD; represents s/w as a single bubble with input and output
	- Level 1 is achieved by expanding the bubble into additional bubbles; perform grammatical parse on narrative describing bubble
	- Continue refining until each bubble performs specific function; high cohesion
	- Components:  bubbles are processes, boxes are external entities, arrows are data or control objects, and double lines are data stores
- Process specification (PSPEC) describes all flow model processes that appear at the final level of refinement.  It is a minispec for each transform at the lowest level of a DFD
- Program design language description (PDL) is basically pseudocode.  One way to represent PSPEC

### CRC modeling
- Class Responsibility Collaborator (CRC) is a lightweight model  
  ![[Pasted image 20230412224721.png]]
- Write on 3”x5” index cards
- Used in extreme programming
- Can be used for
	- detailed object-oriented design
	- conceptual modeling
#### Example
![[Pasted image 20230412224805.png]]

#### Creating CRC cards
Iteratively
- Find classes
- Find responsibilities
- Define collaborators
- Move the cards around
![[Pasted image 20230412224856.png]]

### Unified Modelling Language (UML)
- Several competing object-oriented notations developed in 1980s and 1990s
- Rumbaugh and Booch began working together in 1994 at IBM Rational to standardize their notations (OMT and Booch)
- Result was Unified Modeling Language (UML)
- Rights owned by Object Management Group (OMG), [www.omg.org](http://www.omg.org/)
- Good reference:  M. Blaha and J. Rumbaugh, *Object-Oriented Modeling and Design with UML*, 2nd ed.
- Unified modeling language (UML) includes three models:
	- class model – structural aspects of system (class diagrams)
	- state model – temporal, behavioral aspects of system (state diagrams)
	- interaction model – collaboration of individual objects (use cases, sequence diagrams, and activity diagrams)

#### Brief simple problem for UML overview
![[Pasted image 20230412225105.png]]
1. Use Case Diagram
   ![[Pasted image 20230412225318.png]]
   Functionality from user's point of view
   
2. Class Diagram
   ![[Pasted image 20230412225339.png]]
   Structure of system(objects, attributes, associations, operations)
   
3. Sequence Diagram
   ![[Pasted image 20230412225414.png]]
   Messages between objects
   
   Collaboration Diagram
   ![[Pasted image 20230412225434.png]]
   More compact, but harder to interpret


4. Statechart Diagram
   ![[Pasted image 20230412225509.png]]
   Transitions between states of one object
   (Extension of Finite State Machine (FSM) model)
   
   Statechart Diagram (different objects)
   ![[Pasted image 20230412225540.png]]
   
5. Activity Diagram
   ![[Pasted image 20230412225551.png]]
   Actions are states

### Summary
The five UML diagrams
1. Use case diagrams  [Interaction Model]  
- models functionality from user’s point of view
2. Class diagrams    [Class Model]  
- models structure of system using objects
3. Interaction diagrams    [Interaction Model]  
(sequence and collaboration)  
- models messages passed between objects
4. Statechart diagrams   [State Model]  
- models transitions between states
5. Activity diagrams   [Interaction Model]  
- models flow control as transitions between activities

> The actual UML spec has 12 diagrams, but these five will be sufficient for us.