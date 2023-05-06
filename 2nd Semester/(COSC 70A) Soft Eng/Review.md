## Chapter 1
### WHY HAS REQUIREMENT ENGINEERING BECOME SO IMPORTANT?
1. The pace of product development has picked up drastically.
2. Turnover and technology change have impacted the experience levels of professionals engaged in the development of products.
	- Outsourcing and offshoring have dramatically changed the product life cycle. Specifications must now be created for implementation or manufacturing by organizations with potentially limited or no domain expertise.

### Misconceptions about Requirements Engineering
#### Misconception 1: Any Subject Matter Expert Can Become a Requirements Engineer after a Week or Two of Training
- First and foremost, to elicit requirements from stakeholders requires the ability to interact with a variety of roles and skill levels, from subject matter experts(detailed product requirements) to corporate officers (elicitation of business goals).
- Unified Modeling Language [UML]

#### Misconception 2: Nonfunctional and Functional Requirements Can Be Elicited Using Separate Teams and Processes
- The subject domains for nonfunctional and functional requirements are related, may impact each other, and may result in iterative changes as work progresses (see Chapter 5). Team isolation may do more harm than good.

#### Misconception 3: Processes That Work for a Small Number of Requirements Will Scale
- Filtering and prioritization become important in order to retrieve results that can be better understood, but the requirement annotations necessary to provide such filtering are often neglected up front because the database is initially small.
- Requirements engineering processes do not scale well unless crafted carefully.

### Key Success Factors in Requirements Engineering
- The Project Has a Full-Time, Qualified Chief Architect
- A Qualified Full-Time Architect Manages Nonfunctional Requirements
- An Effective Requirements Management Process Is in Place
- Requirements Elicitation Starts with Marketing and Sales
- Requirements Reviews Are Conducted for All New or Changed Requirements or Features
- Requirements Engineers Are Trained and Experienced
- Requirements Processes Are Proven and Scalable
- Subject Matter Experts Are Available as Needed
- All Stakeholders Are Identified
- The Customer Is Properly Managed
- Progress and Quality Indicators Are Defined
- The Core Project Team Is Full Time and Reports into a Single Chain of Command

The **architect** is responsible for managing nonfunctional requirements and the relationships among requirements analysis, development, and management.

CCB – Change Control Board
CMMI – Capability Maturity Model Integration

“**_Requirements_ _engineering_** [DoD 1991] involves all lifecycle activities devoted to identification of user requirements, analysis of the requirements to derive additional requirements, documentation of the requirements as a specification, and validation of the documented requirements against user needs, as well as processes that support these activities.”

### Characteristics of a Good Requirement
- Feasible
- Valid
- Unambiguous
- Verifiable
- Modifiable
- Consistent
- Complete
- Traceable

## Chapter 2
### Requirements Engineering Artifact Modeling
- “Without goals, and plans to reach them, you are like a ship that  has set sail with no destination.”

- **Requirements engineering artifact** purpose is to are <mark style="background: #FFB8EBA6;">used to support product design and project management decisions</mark> throughout the entire product life cycle.

#### Requirements engineering activities include
- Analyzing marketing information, stakeholder, and user needs to derive the functional and non-functional requirements to be met by the system’s design
- Understanding the effect of these requirements on the business that creates the product.
- Consolidating these requirements into consistent and complete requirements and systems specifications as defined in the Requirements Engineering  Artifact Model (REAM).

### Key components of requirements engineering artifact modelling
- An RE artifact model as a measurable reference model that can be used to support interdisciplinary communication and specifications development
- A process tailoring approach that specializes the RE artifact model to specific organizational or project needs
- RE artifact-centered process guidelines that define _completion levels_ of the RE artifact model.

### Taxonomy
-  is a <mark style="background: #FFB8EBA6;">collection of controlled vocabulary term</mark>s organized into a <mark style="background: #FFB8EBA6;">hierarchical structure</mark>.
- The difference between a _glossary_ and a taxonomy is that in a **glossary, terms are listed alphabetically and defined**, whereas in a **taxonomy, terms are grouped into classifications.** To create a glossary, we recommend starting with a taxonomy of RE terms

#### Any taxonomy for requirements engineering work products should, as a minimum, have the following attributes
1. **Complete -** At the leaf level, include every requirement type that will be used by the organization or project.
2. **Extensible -** Companies should be able to take a core taxonomy and extend it.
3. **Navigable** -  The taxonomy should be easy to navigate, possibly with hyperlinks on web pages.
4. **Valid** - There are many potential taxonomy source.
5. **Systematic** - The categories should be well chosen and be at the same level.

#### Steps in creation of Taxonomy
1. **Identify the tooling** that will be used and how the taxonomy will be presented.
2. **Collect** all the **requirement types**.
3. If the project is an **incremental development**, **mine the requirements for classes**.
4. Categorize by **grouping** and create a **draft taxonomy**.
5. Make sure that **complete, agreed-upon definitions** are  available for every term that will be in the requirements taxonomy, including parent terms.
6. Create a **draft taxonomy**
7. **Revise and publish** (usually to the web)
8. **Provide feedback and maintenance mechanism** for keeping the taxonomy up to-date.

### Elements of an Artifact Model
![[Pasted image 20230426162818.png]]
It consists of the following elements:
- **Artifact -**  a rectangular box with the name of the artifact.
- **Association** - a line connecting two artifacts. The line indicates that there is a relationship between the artifacts. Every association must be labeled to indicate the relationship between the artifacts.
- **Cardinality** - the cardinality indicates quantities.

#### Creation of a Requirements Engineering Artifact Model
Across the entire organization and product life cycle, then, these questions must be asked
- What are the artifacts that the roles use?
- How are the artifacts related?
- Who creates them?
- Who modifies them?
- How do they become obsolete?

In small company creating a software product, the following are artifacts must have:
- Business plan
- Business goals
- Marketing brochure(s)
- Product features
- Customers
- Product definition
- Test plan
- Test cases
- System requirements
- Customer requirements
- Product design

The artifact model that is created prior to the start of a project is like **looking at the X-ray of a patient** prior to starting surgery.

### Eliciting Requirement
 _“The hardest single part of building a system is deciding what to build... No other part of the work so cripples the resulting system if done wrong. No other part is more difficult to rectify later.”_  -  Dr. Fredrick P. Brooks, Jr.

### Requirements Elicitation
- is the process of **discovering the requirements for a system** by **communication with customers, system users and others who have a stake**(stakeholders) in the system development.
- process of identifying the needs and bridging the disparities among involved communities for the purpose of defining and distilling requirements to meet the needs of an organization or project while staying within imposed constraints.

**Issues and Problems in Requirements Elicitation**
- The Missing Ignoramus
- The Wrong Stakeholders
- Untrained Analysts - may be a very senior, skilled, or business-savvy person.

### Requirements Elicitation Methods
![[Pasted image 20230426164846.png]]
## Chapter 3

 _“The hardest single part of building a system is deciding what to build... No other part of the work so cripples the resulting system if done wrong. No other part is more difficult to rectify later.”_    - Dr. Fredrick P. Brooks, Jr.

### Issues and Problems in Requirements Elicitation
- **The Missing Ignoramus**
- **The Wrong Stakeholders**
- **Untrained Analysts**
- **Not Identifying Requirements Level**      
	- Requirements are often captured at different levels of detail.
- **Failure to Accurately Identify Stakeholders**
- **Problems Separating Context from Requirement**
- **Requirements Are Too Volatile**
- **System Boundaries Are Not Identified**
- **Understanding of Product Needs Is Incomplete**
	- Analysts are often asked to help define requirements for products where the stakeholders are uncertain of their needs.
- **Users Misunderstand What Computers Can Do**
	- Stakeholders may ascribe virtues to computer systems that are futuristic, wishful thinking, or simply impractical.
- **The Requirements Engineer Has Deep Domain Knowledge**
	- If a requirements analyst has strong domain knowledge, there may be a tendency to minimize communication with stakeholders.
- **Stakeholders Speak Different Natural and Technical Languages**
	- When stakeholders are from different domains or speak different languages, communication can be even more difficult. Problems may arise in several areas, such as
		- Ensuring efficient quality reviews of requirements
		- Smoothly running elicitation sessions
		- Domain experts understanding the impact of stakeholder requests made in one area on their area
	- Understanding complex needs, processes, or algorithms
- **Stakeholders Omit Important, Well-Understood, Tacit Information**

### Requirements Elicitation Methods
![[Pasted image 20230426165407.png]]

**Goal modeling** is a nice way to crystallize ideas, to present corporate goals in a simple-to-understand and unambiguous way, and to identify and balance difficult choices.

**Goal models** can be as simple or as complex as necessary.

#### Example Customer-Specific Business Rules
A sample business policy, rules, and some derived requirements are shown here:
- **Policy** The hospital shall be able to define the difference between adult and child patients for check-in and medical records purposes.
- **Rule** Any patient under the age of 14 checking in shall be considered a child.
	- When a child checks into the hospital, depending on the hospital’s business policy, a parent or guardian may have to accompany the child and sign all the admission forms. Detailed rules explain under what circumstances (e.g., an accident, emergency, or life-threatening situation) a child may be checked in without a parent’s or guardian’s consent.

- **Requirement** A facility shall be provided with the system such that the hospital check-in process for adults and children can be changed by hospital administrators without the need for system or software modifications.

Note in the preceding example, the hospital may, at any time, <mark style="background: #ADCCFFA6;">change the age at which a patient is considered a child</mark>, as well as the rules governing the emergency check-in of a child without parental consent. The relationships among business policies, rules, and requirements are illustrated in Figure
![[Pasted image 20230503213319.png]]

##### Ethnographic Techniques
- Ethnographic research tends to focus on a particular community or culture. Typical collection methods are interviews and surveys.

- **Kano** modeling provides three variables to measure customer interest: one-dimensional, expected, and attractive quality.

##### Process Modeling Techniques
**Data flow diagrams (DFDs)**- effective diagramming techniques for analyzing business needs. The primary difference between the data flow and newer (object-oriented) techniques is the focus on data flows and data structures rather than services.

**Use case analysis** - involves either defining a customer process  or showing the relationship of a system or product to the outside world.

A use case consists of the following:
- **Actors** People or things interacting with the use case
- **Events** Things that cause the use case to happen
- **Preconditions** Things that must be true for the use case to happen
- **Postconditions** Things that must be true if the use case has successfully completed
- **Activities** The processes that occur in the use case
- **Included use cases** Other processes used by this use case
- **Extending use cases** Other processes that may optionally take place during the occurrence of this use case