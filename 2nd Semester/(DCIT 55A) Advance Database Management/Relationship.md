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

**When should a relationship with *attributes* instead be an *associative entity*?![[Pasted image 20230416182955.png]]**
- All relationships for the associative entity should be many
- The associative entity could have meaning independent of the other entities
- The associative entity preferably has a unique identifier, and should also have other attributes
- The associative entity may participate in other relationships other than the entities of the associated relationship
- Ternary relationships should be converted to associative entities.

- Is like a relationship with an attribute, but it is also considered to be an entity in its own rights.
- Note that the many-to-many cardinality between entities in figure below has been replaced by two one-to-many relationships with the associative entity.
![[Pasted image 20230416182955.png]]
