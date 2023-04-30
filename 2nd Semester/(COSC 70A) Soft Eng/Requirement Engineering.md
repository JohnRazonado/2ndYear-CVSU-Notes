## What's a Requirement?
- It is about **WHAT** not HOW
- Nothing can be said obvious
- Requirements are the descriptions of the services provided by a system and its operational constraints
	- Important to have all the "Requirement"
- It may range from a high level abstract statement to a detailed mathematical specification
- It may be as complex as a 500 pages of description
- It may serve as the basis for a bid for a contract or the basis for the contract itself.

## Requirement Engineering
To seek the requirements of a system, process are employed :
- **discovering** - checking and brainstorm.
- **analyzing**
- **documenting**
- **validating**
>each software development process goes through the phase of requirements engineering.

### Why Requirements?
What are the advantages of a complete set of documented requirements?
- Ensures the user (not the developer) drives system functionalities
- Helps avoiding confusion and arguments
- Helps minimizing the changes
- Changes in requirements are expensive. Changing the requirements costs:
	- 3 x as much during the design phase
	- 5-10 x as much during implementation
	- 10-100 x as much after release [Code Complete, p30]
- 2/3 of finished system errors are requirements and design errors [RG]
- A careful requirements process doesn’t mean there will be no changes later
	- Average project experiences about 25% changes in the requirements
	- This accounts for 70-80% if the rework of the project [Code Complete, p40]
	- Important to plan for requirements changes
- The case of critical applications

### Different Levels of Abstraction
- User requirements (abstract +)
	- Usually the first attempt for the description of the requirements
	- Services and constraints of the system
	- In natural language or diagrams
	- Readable by everybody
	- Serve business objectives
- System requirements (abstract -)
	- Services and constraints of the system in detail
	- Useful for the design and development
	- Precise and cover all cases
	- Structured presentation

## Types of Requirements
- Functional requirements
	- Services the system should provide
	- What the system should do or not in reaction to particular situations
- Non-functional requirements
	- Constraints on the services or functions offered by the system
	- Examples: Timing constraints, constraints on the development process (CASE, language, development method…), standards etc.
- Domain requirements
	- From the application domain of the system
	- May be functional or non-functional
	- Examples: Medicine, library, physics, chemistry
Note: You can have user/system functional/non-functional requirements.

## User Requirements
- First attempt to describe functional and non-functional requirements
	- Understandable by the user
- Problems:
	- Lack of clarity - ambiguous language
	- Requirements confusion - functional, non-functional requirements, design information are not distinguished
	- Requirements amalgamation – several requirements are defined as a single one
	- Incompleteness – requirements may be missing
	- Inconsistency – requirements may contradict themselves
- Guideline to minimize the issues:
	- Separate requirements – separate the requirements, separate functional and non-functional requirements, requirements must be clearly identified (e.g. by a number)
	- Include a rationale for each requirement – helps clarify reasoning behind the requirements and may be useful for evaluating potential changes in the requirements
	- Invent or use a standard form/template
	- Distinguish requirements priorities
	- Example: MoSCoW (Must, Shall, Could, Want/Will (no TBD))
	- Avoid technical jargon
	- Testable (write test cases)
	- Deliverables

## System Requirements
- Elaborate the user requirements to get a precise, detailed and complete version of them
- Used by designers and developers
- An important aspect is how to present/write system requirements
	- Natural language is often used!
- The difference between user and system requirements must not be thought as a detail
- Example: If sales for current month are below target sales, then report is to be printed unless difference between target sales and actual sales is less than half of difference between target sales and actual sales in previous month, or if difference between target sales and actual sales for the current month is less than 5%.
- Problems:
	- Difficult to read
	- Ambiguity: sales and actual sales, 5% of what?
	- Incomplete: what if sales are above target sales?
### Writing System Requirements
- Natural language (informal requirements)
	- Reviled by academics
	- But widely practiced: everybody can read them, finding a better notation is hard
- Structured natural language
	- Forms/templates are used to bring some rigor to natural language presentations
- Graphical notations
	- Using boxes, arrows… but they mean different things to different people
- Formal specification
	- Based on logic, state machines…
	- Hard to understand for many people
**Analogy**
- Archimedes (ca. 250 bc)
	- Any sphere is equal to 4 times the cone which has its base equal to the greatest circle in the sphere and its height equal to the radius of the sphere.
- Today
	- V = 4/3 pi r 3
- How is this bit of history relevant for software requirements?
	- Formal is better only if everybody understands it
	- It may take a long time to find a good notation
	- Software requirements is an area of research

### Non-functional Requirements
- They can be further categorized into:
	- Product requirements
		- Product behavior
		- Ex: Timing, performance, memory, reliability, portability, usability
- Organizational requirements
	- Policies and procedures in the customer’s and developer’s organizations
	- Example: Process requirements, implementation requirements, delivery requirements
- External requirements
	- Factors externals to the system and the development process
	- Example: Interoperability, legislation, ethics
Non-functional requirements may be more critical than functional requirements. (The system may be useless…)

![[Pasted image 20230330223720.png]]

![[Pasted image 20230330223730.png]]

## Project Elicitation
![[Pasted image 20230330223932.png]]

## Requirement Engineering
![[Pasted image 20230330224009.png]]

5 important activities:
- [[Requirement Engineering#Feasibility Study|Feasibility study]]
- Requirements elicitation and analysis
- Requirements documentation
- Requirements validation
- Requirements management

### Feasibility Study
- It is done at first to decide whether or not the project is worthwhile
- Look at different perspectives:
	- Market analysis, financial, schedule, technical, resource, legal…
- Should make you aware of the risks
- Doing the study
	- Consult information sources: managers, software engineers, end users…
	- Based on information collection (interviews, surveys, questionnaires…)
- Should be short (2-3 weeks)
#### Question
- What if the system wasn’t implemented?
- What are current process problems?
- Do technical resources exist?
- What is the risk associated with the technology?
- Is new technology needed? What skills?
- How will the proposed project help?
- How does the proposed project contribute to the overall objectives of the organization?
- Have the benefits identified with the system being identified clearly?
- What will be the integration problems?
- What facilities must be supported by the system?
- What is the risk associated with cost and schedule?
- What are the potential disadvantages/advantages?
- Are there legal issues?
- Are there issues linked with the fact that this is an offshore project?

…