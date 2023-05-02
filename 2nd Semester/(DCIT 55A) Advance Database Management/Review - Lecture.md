#inProgress 

## [[Structured Query Language#History|Origin of Database]]
- **1960's** -  First general-purpose DBMS, designed by Charles Bachman at General Electric called "Integrated Data Store"
	- Form a data model standardized by Conference on Data Systems Languages (CODASYL)
- **1970** - Dr. E. F. "Ted" of IBM is known as the father of relational databases. He described a relational model for databases.
- **1974** - Structured Query Language appeared
- **1978** - IBM worked to develop Codd's ideas and released a product named **System R**
- **1986** - IBM developed the first prototype of relational database and standardized by ANSI.
- First relational database was release by **Relational Software** later becoming **Oracle**.

## Database
- organized collection of data stored and accessed electronically
- Databases can be used for various purposes, such as storing data for a website, keeping track of customer information, or managing inventory which is often controlled by database management systems (DBMS)

### [[Advance Database Introduction#Characteristics|Characteristics of Database]]
- **Self-describing nature of a database system**
- **Structured and Described Data**
- **Separation of Data and Applications**
- **Data Integrity**
- **Transactions**
- **Data Persistence**
- **Security**
- **Efficiency**
- **Recovery**
- **Flexibility**
- **Scalability**

### DBMS and RDMS
####  DBMS 
- stands for Database Management System
- a software specifically formatted and encoded to facilitate data, retrieve and run queries on data and in simple description a computerize datakeeping system. 
- DBMS functionality is to store data in a file format and in small quantity, has the accessibility to individual elements. Data stored in DBMS are not linked however data is redundancy and does not have support of distributed database
#### RDBMS
-  Relational Database Management System
- Provide interface between users and applications that is oriented in a data model (stores data in row-based element) and additionally contains administrative functionality to improve performance and managing data.
- RDBMS on the other hand stores data in large quantity and in a tabled format, have efficient accessibility to multiple data elements together, supports distributed data and reduces the redundancy of data.

### Data Model
A data model is a collection of high-level data description constructs that hide many low-level storage details. A DBMS allows a user to define the data to be stored in terms of a data model. Most database management systems today are based on the relational data model.

Based on two concepts:
- Entities, tables that hold specific information (data)
- Relationships, the associations or interactions between entities.

#### [[Modeling in the Data Organization#Data Modeler Drawing Conventions (Barker Notation)|Data Modeler Drawing Conventions (Barker Notation)]]
- Entities are represented by softboxes
- Entity names go in the softboxes
- Entity names are always singular and written in capital letters
- Attributes are listed under entity names
- Mandatory attributes are marked with an asterisk: "\*"
- Optional attributes are marked with a circle: "o"
- Unique identifiers are marked with a hash sign: "#"


## [[Modeling in the Data Organization#Entity Relationship Diagram|Entity-Relationship Diagram(ERD)]]
- describe the data involved in a real-world enterprise in terms of objects and their relationships and is widely used to develop an initial database design. 
### Data Definitions
- Explanation of a term or fact
	- Term-word or phrase with specific meaning
	- Fact-association between two or more terms
- Guidelines for good data definition
	- A concise description of essential data meaning
	- Gathered in conjunction with systems requirements
	- Accompanied by diagrams
	- Achieved by consensus, and iteratively refined
#### Good Data Name is:
- Related to business, not technical, characteristics
- Meaningful and self-documenting
- Unique
- Readable
- Composed of words from an approved list
- Repeatable
- Written in standard syntax

### E-R Model Constructs
#### [[Entities]]
**A person, a place, an object, an event, or a concept** in the user environment
- **Entity instance** - single occurrence of an entity type
- **Entity Type** - collection of entities (often corresponds to a table)
##### Strong vs. Week Entities
###### Strong Entity
- Exists independently of other types of entities
- Has its own unique identifier
	- Identifier underlined with single line.
###### Weak Entity
- Dependent on a strong entity (identifying owner)... cannot exist on its own.
- Does not have a unique identifier (only a partial identifier)
- Entity box an partial identifier have double lines
###### Identifying Relationship
- Links strong entities to weak entities

#### [[Relationships]]
- modelled as lines between entity types. The instance is between specific entity instances
- Can have attributes
- **Relationship instance** - link between entities (corresponds to primary key - foreign key equivalencies in related tables)
- **Relationship type** - category of relationship...link between entity types.
	- Two entities can have more than one type of relationships (**multiple relationship**)
##### Degree of Relationships
Number of entity types that participates in it.
- Unary relationship
- Binary relationship
- Ternary relationship
##### Cardinality of Relationship
- **One-to-one**
	- exactly have one related entity in a relationship
- **One-to-many**
	- one entity on one side can have many related entities while other side have max of one
- **Many-to-many**
	- both entity in the relationship can have many related entities.
##### Cardinality Constraints
The number of instances of one entity that can or must be associated with each instance of another entity
- **Minimum Cardinality**
	- if zero, then optional
	- one or more, then mandatory
- **Maximum Cardinality**
	- The maximum number
##### Associative Entities
- An entity has [[attributes]]
- A relationship-links entities together

#### [[Attributes]]
**Property or characteristics** of an entity or relationship type.

##### Naming Attributes
- Should be a singular noun or noun phrase
- Unique
- Follow a standard format
- Similar attributes of different entity types should use the same qualifiers and classes.
##### Defining Attributes
- State what the attribute is and possibly why important
- Make it clear what is and is not included in the attribute's value
- Include aliases in documentation
- State source of values
- Specify required vs. optional
- State min and max number of occurrences allowed
- Indicate relationships with other attributes
##### Classifications of Attributes
- **Required versus Optional Attributes**
	- **Required** - Must have a value for every entity (or relationship) instance with which it is associated
	- **Optional** - May not have a value for every entity (or relationship)
- **Simple versus Composite Attribute**
	- **Composite attribute** - An attribute that has meaningful component parts (attributes)
- **Single-Valued versus Multivalued Attribute**
	- **Multivalued** - may take on more than one value for a given entity (or relationship) instance
- **Stored versus Derived Attributes**
	- **Derived** - values can be calculated from related attribute value (not physically stored in the database).
- **Identifier Attributes**
	- An attribute (or combination of attributes) that **uniquely identifies individual instances** of an entity type.
#### [[Identifier]]
 An attribute (or combination of attributes) that uniquely identifies individual instances of an entity type.
- [[Attributes#Simple vs. Composite Attributes|Simple versus Composite Identifier]] 
- **Candidate Identifier** - An attribute that could be a key... satisfies the requirements for being an identifier.
##### Criteria for Identifiers
- Choose that
	- Will not change in value
	- Will not be null
- **Avoid intelligent identifiers** (e.g. containing locations or people that might change)
- Substitute new, simple keys for long, composite keys

#### [[Modeling in the Data Organization#Business Rules|Business Rules]]
- Are statements that define or constrain some aspect of the business
- Are derived from policies, procedures, events, functions
- Assert business structure
- Control/influence business behavior
- Are expressed in terms familiar to end users
- Are automated through DBMS software
##### A Good Business Rule Is:
- **Declarative** - what, not how
- **Precise** - clear, agreed-upon meaning
- **Atomic** - one statement
- **Consistent** - internally and externally
- **Expressible** - structured, natural language
- **Distinct** - non-redundant
- **Business-oriented** - understood by business people

## Relational Model
- Represents the database as a **collection of relations**. 
- It resembles relationship of a table of values or, to some extent, a flat file (simple or linear structure of records) of records.
- A relation is a **set of tuples**, or rows in a table, with each tuple sharing a set of **attributes**, or **columns**


