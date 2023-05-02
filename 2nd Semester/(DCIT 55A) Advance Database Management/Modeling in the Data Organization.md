## Objectives
- Define terms 
- Understand importance of data modeling 
- Write good names and definitions for entities, relationships, and attributes 
- Distinguish unary, binary, and ternary relationships 
- Model different types of attributes, entities, relationships, and cardinalities 
- Draw E-R diagrams for common business situations 
- Convert many-to-many relationships to associative entities

## Entity Relationship Diagram
### Data Definitions
- Explanation of a term or fact
	- Term-word or phrase with specific meaning
	- Fact-association between two or more terms
- Guidelines for good data definition
	- A concise description of essential data meaning
	- Gathered in conjunction with systems requirements
	- Accompanied by diagrams
	- Achieved by consensus, and iteratively refined
### A Good  Data Name Is:
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
- **Entity instance** - person, place, object, event, concept (often corresponds to a row in a table)
- **Entity Type** - collection of entities (often corresponds to a table)
#### [[Relationship|Relationships]]
The relationship is modeled as lines between entity types... the instance is between specific entity instances.
- **Relationship instance** - link between entities (corresponds to primary key - foreign key equivalencies in related tables)
- **Relationship type** - category of relationship...link between entity types.
#### [[Attributes]]:
- Properties or characteristics of an entity or relationship type (often corresponds to a field in a table)

#### [[Identifier|Identifiers]] (Keys)
An attribute (or combination of attributes) that **uniquely identifies individual instances** of an entity type.
- [[Attributes#Simple vs. Composite Attributes|Simple versus Composite Identifier]] 
- **Candidate Identifier** - An attribute that could be a key... satisfies the requirements for being an identifier.

### Entities and Attributes
![[Pasted image 20230416162603.png]]

![[Pasted image 20230416163203.png]]

## Data Modeler Drawing Conventions (Barker Notation)
- Entities are represented by softboxes
- Entity names go in the softboxes
- Entity names are always singular and written in capital letters

![[Pasted image 20230416161328.png]]

- Attributes are listed under entity names
- Mandatory attributes are marked with an asterisk: "\*"
- Optional attributes are marked with a circle: "o"
- Unique identifiers are marked with a hash sign: "#"

![[Pasted image 20230416161717.png]]

## Business Rules
- Are statements that define or constrain some aspect of the business
- Are derived from policies, procedures, events, functions
- Assert business structure
- Control/influence business behavior
- Are expressed in terms familiar to end users
- Are automated through DBMS software

### A Good Business Rule Is:
- **Declarative** - what, not how
- **Precise** - clear, agreed-upon meaning
- **Atomic** - one statement
- **Consistent** - internally and externally
- **Expressible** - structured, natural language
- **Distinct** - non-redundant
- **Business-oriented** - understood by business people

## ERD Samples
### Business Rules
- A library system contains books, authors and patrons, with attributes book number, author number and patron number, respectively.
- Books are further described by title and page count
- Authors by author name, and 
- Patrons by patron name
- Books should have at least one author or can have more. An author can author a book or many books.
- Patron borrow books but at any point in time, may not have anything checked out. When they do have a book checked out, there is a due date associated with it.
![[Pasted image 20230416184911.png]]

![[Pasted image 20230416184955.png]]

