## Objectives
-  Define terms 
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
#### Entities
- Entity instance-person, place, object, event, concept (often corresponds to a row in a table)
- Entity Type-collection of entities (often corresponds to a table)
#### Relationships
- Relationship instance-link between entities (corresponds to primary key - foreign key equivalencies in related tables)
- Relationship type-category of relationship...link between entity types.
#### Attributes:
- Properties or characteristics of an entity or relationship type (often corresponds to a field in a table)

![[Pasted image 20230416155921.png]]

![[Pasted image 20230416155957.png]]

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

## A Good Business Rule Is:
- Declarative-what, not how
- Precise-clear, agreed-upon meaning
- Atomic-one statement
- Consistent-internally and externally
- Expressible-structured, natural language
- Distinct-non-redundant
- Business-oriented-understood by business people


## Entities and Attributes
![[Pasted image 20230416162603.png]]

![[Pasted image 20230416163203.png]]
### Entities
- A person, a place, an object, an event, or a concept in the user environment
**Entity Type**
- A collection of entities that share common properties or characteristics
**Entity instance**
- A single occurrence of an entity type

![[Pasted image 20230416163259.png]]
>Figure 2-4 Example of inappropriate entities


#### Strong vs. Week Entities, and Identifying Relationships
##### Strong Entity
- Exists independently of other types of entities
- Has its own unique identifier
	- Identifier underlined with single line.
##### Weak Entity
- Dependent on a strong entity (identifying owner)... cannot exist on its own
- Does not have a unique identifier (only a partial identifier)
- Entity box an partial identifier have double lines
##### Identifying relationship
- links strong entities to weak entities

### Attribute
- Property or characteristics of an entity or relationship type.

#### Naming Attributes
- Name should be a singular noun or noun phrase
- Name should be unique
- Name should follow a standard format
	- e.g. [Entity type name {[Qualifier]}] Class
- Similar attributes of different entity types should use the same qualifiers and classes.

#### Defining Attributes
- State what the attribute is and possibly why it is important
- Make it clear what is and is not included in the attribute's value
- Include aliases in documentation
- State source of values
- Specify required vs. optional
- State min and max number of occurrences allowed
- Indicate relationships with other attributes

#### Classifications of Attributes
- Required versus Optional Attributes
- Simple versus Composite Attribute
- Single-Valued versus Multivalued Attribute
- Stored versus Derived Attributes
- Identifier Attributes

#### Required vs. Optional Attributes
**Required** - Must have a value for every entity (or relationship) instance with which it is associated
**Optional** - May not have a value for every entity (or relationship) instance with which it is associated
![[Pasted image 20230416173501.png]]

#### Simple vs. Composite Attributes
**Composite attribute** - An attribute that has meaningful component parts (attributes)

![[Pasted image 20230416173819.png]]

#### Multi-valued and Derived Attributes
**Multivalued** - may take on more than one value for a given entity (or relationship) instance

**Derived** - values can be calculated from related attribute value (not physically stored in the database).

![[Pasted image 20230416174656.png]]


#### Identifiers (Keys)
- An attribute (or combination of attributes) that uniquely identifies individual instances of an entity type.
- [[Modeling in the Data Organization#Simple vs. Composite Attributes|Simple versus Composite Identifier]] 
- **Candidate Identifier** - An attribute that could be a key... satisfies the requirements for being an identifier.

##### Criteria for Identifiers
- Choose that
	- Will not change in value
	- Will not be null
- **Avoid intelligent identifiers** (e.g. containing locations or people that might change)
- Substitute new, simple keys for long, composite keys

![[Pasted image 20230416175229.png]]
> Simple and composite identifier attributes


## Modeling Relationships
- **[[Modeling in the Data Organization#Relationship types and Instances|Relationship types vs. Instances]]**
	- The relationship is modeled as lines between entity types... the instance is between specific entity instances.
- Relationships can have attributes
	- Those describe features pertaining to the association between the entities in the relationship
- Two entities can have more than one type of relationship between them (multiple relationships)
- **Associative Entity** - Combination of relationship and entity

### Relationship types and Instances
- The relationship is modeled as lines between entity types... the instance is between specific entity instances.
![[Pasted image 20230416175606.png]]

### Degree of Relationships
- Number of entity types that participates in it.
- Unary Relationship
	- ![[Pasted image 20230416180505.png]]
- Binary Relationship
	- ![[Pasted image 20230416180522.png]]
- Ternary Relationship
	- ![[Pasted image 20230416180543.png]]

![[Pasted image 20230416180414.png]]

### Cardinality of Relationships
##### One-to-one
- Each entity in the relationship will have exactly one related entity
##### One-to-Many
- An entity on one side of the relationship can have many related entities, but an entity on the other side will have a maximum of one related entity
##### Many-to-Many
- Entities on both sides of the relationship can have many related entities on the other side

#### Cardinality Constraints
- The number of instances of one entity that can or must be associated with each instance of another entity
##### Minimum Cardinality
- If zero, then optional
- If one or more, then mandatory
##### Maximum Cardinality
- The maximum number

![[Pasted image 20230416181753.png]]
![[Pasted image 20230416181910.png]]
![[Pasted image 20230416181940.png]]

#### Cardinality Constraints in a ternary relationship
![[Pasted image 20230416183248.png]]

![[Pasted image 20230416183307.png]]
> 1. Each vendor can supply many parts to any number of warehouses but need not supply any parts.
> 2. Each part can be supplied by any number of vendors to more than one warehouse, but each part must be supplied by at least one vendor to a warehouse.
> 3. Each warehouse can be supplied with any number of parts from more than one vendor, but each warehouse must be supplied with at least one part.

#### Examples of Multiple Relationships
![[Pasted image 20230416182013.png]]
![[Pasted image 20230416182031.png]]

#### Multivalued attributes can be represented as relationships
![[Pasted image 20230416182124.png]]

### Associative Entities
- An entity has attributes
- A relationship-links entities together

**When should a relationship with *attributes* instead be an *associative entity*?**
- All relationships for the associative entity should be many
- The associative entity could have meaning independent of the other entities
- The associative entity preferably has a unique identifier, and should also have other attributes
- The associative entity may participate in other relationships other than the entities of the associated relationship
- Ternary relationships should be converted to associative entities.

- Is like a relationship with an attribute, but it is also considered to be an entity in its own rights.
- Note that the many-to-many cardinality between entities in figure below has been replaced by two one-to-many relationships with the associative entity.
![[Pasted image 20230416182955.png]]

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

