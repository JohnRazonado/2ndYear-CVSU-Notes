**Property or characteristics** of an entity or relationship type.

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

