
## Principles and Learning Objectives
- Data management and modeling are key aspects of organizing data and information
	- Define general data management concepts and terms, highlighting the advantages of the database approach to data management
	- Describe logical and physical database design considerations, the function of data centers, and the relational database model
- A well-designed and well-managed database in an extremely valuable tool in supporting decision making
	- Identify the common functions performed by all database management systems, and identify popular database management systems.
- The number and types of database applications will continue to evolve and yield real business benefits
	- Identify and briefly discuss business intelligence, data mining, and other database applications.

## Why Learn About Database Systems, Data Centers, and Business Intelligence?

- Database:
	- Organized collection of data
- Database management system (DBMS):
	- Group of programs that manipulate the database
	- Provide an interface between the database and its users and other application programs

- Database administrator (DBA):
	- Skilled IS professional who directs all activities related to an organization’s database

## Data Management
- Without data and the ability to process the data:
	- An organization could not successfully complete most business activities
- Data consists of raw facts
- To transform data into useful information:
	- It must first be organized in a meaningful way

### Hierarchy of Data
- Bit (a binary digit):
	- Circuit that is either on or off

- Byte:
	- Typically made up of eight bits
- Character:
	- Basic building block of information
- Field:
	- Name, number, or combination of characters that describes an aspect of a business object or activity.
- Record:
	- Collection of related data fields
- File:
	- Collection of related records
- Database:
	- Collection of integrated and related files

- Hierarchy of data:
	- Bits, characters, fields, records, files, and databases
![[Pasted image 20230102165140.png]]

### Data Entities, Attributes, and Keys
- Entity:
	- General class of people, places, or things (objects) for which data is collected, stored, and maintained
- Attribute:
	- Characteristic of an entity
- Data item:
	- Specific value of an attribute
![[Pasted image 20230102165605.png]]

- Key:
	- Field or set of fields in a record that is used to identify the record
- Primary key:
	- Field or set of fields that uniquely identifies the record
	
### The Database Approach
- Traditional approach to data management:
	- Each distinct operational system used data files dedicated to that system
- Database approach to data management:
	- Pool of related data is shared by multiple application programs

![[Pasted image 20230102170007.png]]

Table 3.1: Advantages of the Database Approach
![[Pasted image 20230102170552.png]]

Table 3.2: Disadvantages of the Database Approach
![[Pasted image 20230102171557.png]]

## Data Modeling and Database Characteristics
- When building a database, an organization must consider:
	- Content: What data should be collected and at what cost?
	- Access: What data should be provided to which users and when?
	- Logical structure: How should data be arranged so that it makes sense to a given user?
	- Physical organization: Where should data be physically located?
### Data Center
- Climate-controlled building or set of buildings that:
	- Houses database servers and the systems that deliver mission-critical information and services
- Traditional data centers:
	- Consist of warehouses filled with row upon row of server racks and powerful cooling systems
### Data Modelling
- Building a database requires two types of designs:
	- Logical design:
		- Abstract model of how data should be structured and arranged to meet an organization’s information needs
	- Physical design:
		- Starts from the logical database design and fine-tunes it for performance and cost considerations
- Planned data redundancy:
	- Done to improve system performance so that user reports or queries can be created more quickly
- Data model:
	- Diagram of data entities and their relationships
- Enterprise data modeling:
	- Starts by investigating the general data and information needs of the organization at the strategic level
- Entity-relationship (ER) diagrams:
	- Data models that use basic graphical symbols to show the organization of and relationships between data
![[Pasted image 20230102172654.png]]

## The Relational Database Model
- Relational model:
	- Describes data using a standard tabular format
	- Each row of a table represents a data entity (record)
	- Columns of the table represent attributes (fields)
	- Domain:
		- Allowable values for data attributes

Figure 3.8: A Relational Database Model
In the relational model, all data elements are placed in two-dimensional tables, or relations. As long as they share at least one common element, these relations can be linked to output useful information.
![[Pasted image 20230102172943.png]]

- **Manipulation data:**
	- Selecting:
		- Eliminates rows according to certain criteria
	- Projecting:
		- Eliminates columns in a table
	- Joining:
		- Combines two or more tables
	- Linking:
		- Manipulating two or more tables that share at least one common data attribute
![[Pasted image 20230102173658.png]]

**Figure 3.10: Linking Data Tables to Answer an Inquiry**
In finding the name and hire date of the manager working on the sales manual project, the president needs three tables: project, department, and manager. The project description (Sales manual) leads to the department number (598) in the project table, which leads to the manager’s SSN (098-40-1370) in the department table, which leads to the manager’s name (Fiske) and hire date (01-05-1985) in the manager table. Again, note that some organizations might use employee number instead of Social Security number (SSN).
![[Pasted image 20230102173802.png]]

### Database Management Systems
- Creating and implementing the right database system:
	- Ensures that the database will support both business activities and goals
- Capabilities and types of database systems vary considerably
#### Overview of Database Types
- Flat file:
	- Simple database program whose records have no relationship to one another
- Single user:
	- Only one person can use the database at a time
	- Examples: Access, FileMaker Pro, and InfoPath
- Multiple users:
	- Allow dozens or hundreds of people to access the same database system at the same time
	- Examples: Oracle, Sybase, and IBM
#### Providing a User View
- Schema:
	- Used to describe the entire database
	- Can be part of the database or a separate schema file
- DBMS:
	- Can reference a schema to find where to access the requested data in relation to another piece of data
#### Creating and Modifying the Database
- Data definition language (DDL):
	- Collection of instructions and commands used to define and describe data and relationships in a specific database
	- Allows database’s creator to describe data and relationships that are to be contained in the schema
- Data dictionary:
	- Detailed description of all the data used in the database

**Figure 3.13: Using a Data Definition Language to Define a Schema**
![[Pasted image 20230102174654.png]]

**A Typical Data Dictionary Entry**
![[Pasted image 20230102174746.png]]

#### Storing and Retrieving Data
- When an application program needs data:
	- It requests the data through the DBMS
- Concurrency control:
	- Method of dealing with a situation in which two or more users or applications need to access the same record at the same time
**Figure 3.15: Logical and Physical Access Paths**
![[Pasted image 20230102174920.png]]

#### Manipulating Data and Generating Reports
- Data manipulation language (DML):
	- Commands that manipulate the data in a database
- Structured Query Language (SQL):
	- Adopted by the American National Standards Institute (ANSI) as the standard query language for relational databases
- Once a database has been set up and loaded with data:
	- It can produce reports, documents, and other outputs
#### Database Administration
- DBA:
	- Works with users to decide the content of the database
	- Works with programmers as they build applications to ensure that their programs comply with database management system standards and conventions
- Data administrator:
	- Responsible for defining and implementing consistent principles for a variety of data issues

#### Popular Database Management Systems
- Popular DBMSs for end users:
	- Microsoft’s Access and FileMaker Pro
- Database as a Service (DaaS):
	- Emerging database system
	- Database administration is provided by the service provider
	- The database is stored on a service provider’s servers and accessed by the client over a network
#### Special-Purpose Database Systems
- Some specialized database packages are used for specific purposes or in specific industries
	- Rex-Book from Urbanspoon
- Morphbank (www.morphbank.net):
	- Allows researchers to continually update and expand a library of over 96,000 biological images
### Selecting a Database Management System
- Important characteristics of databases to consider:
	- Database size
	- Database cost
	- Concurrent users
	- Performance
	- Integration
	- Vendor
### Using Databases with Other Software
- DBMSs can act as front-end or back-end applications:
	- Front-end applications interact directly with people
	- Back-end applications interact with other programs or applications

## Database Applications
- Today’s database applications manipulate the content of a database to produce useful information
- Common manipulations:
	- Searching, filtering, synthesizing, and assimilating data contained in a database using a number of database applications
### Linking Databases to the Internet
- Semantic Web:
	- Developing a seamless integration of traditional databases with the Internet
	- Provides metadata with all Web content using technology called the Resource Description Framework (RDF)
### Data Warehouses, Data Marts, and Data Mining
- Data warehouse:
	- Database that holds business information from many sources in the enterprise
- Data mart:
	- Subset of a data warehouse
- Data mining:
	- Information-analysis tool that involves the automated discovery of patterns and relationships in a data warehouse

**Figure 3.22: Elements of a Data Warehouse**
![[Pasted image 20230102180110.png]]

- Predictive Analysis:
	- Form of data mining that combines historical data with assumptions about future conditions to predict outcomes of events
	- Used by retailers to upgrade occasional customers into frequent purchasers
	- Software can be used to analyze a company’s customer list and a year’s worth of sales data to find new market segments

**Table 3.5: Common Data-Mining Applications**
![[Pasted image 20230102180343.png]]

## Business Intelligence
- Involves gathering enough of the right information:
	- In a timely manner and usable form and analyzing it to have a positive impact on business strategy, tactics, or operations
- Competitive intelligence:
	- Limited to information about competitors and the ways that knowledge affects strategy, tactics, and operations
- Counterintelligence:
	- Steps organization takes to protect information sought by “hostile” intelligence gatherers
- Data loss prevention (DLP):
	- Refers to systems designed to lock down data within an organization
	- Powerful tool for counterintelligence
	- A necessity in complying with government regulations that require companies to safeguard private customer data
### Distributed Databases
- Distributed database:
	- Database in which the data may be spread across several smaller databases connected via telecommunications devices
	- Gives corporations more flexibility in how databases are organized and used
- Replicated database:
	- Holds a duplicate set of frequently used data
**Figure 3.23: The Use of a Distributed Database**
For a clothing manufacturer, computers might be located at corporate headquarters, in the research and development center, in the warehouse, and in a company-owned retail store. Telecommunications systems link the computers so that users at all locations can access the same distributed database no matter where the data is actually stored.
![[Pasted image 20230102180615.png]]

#### Online Analytical Processing (OLAP)
- Software that allows users to explore data from a number of different perspectives
- Provides top-down, query-driven data analysis
- Requires repetitive testing of user-originated theories
- Requires a great deal of human ingenuity and interaction with the database to find information

**Table 3.6: Comparison of OLAP and Data Mining**
![[Pasted image 20230102180957.png]]

## Object-Relational Database Management Systems
- Object-oriented database:
	- Stores both data and its processing instructions
	- Uses an object-oriented database management system (OODBMS) to provide a user interface and connections to other programs
- Object-relational database management system (ORDBMS):
	- Provides the ability for third parties to add new data types and operations to the database
### Visual, Audio, and Other Database Systems
- Visual databases:
	- Can be stored in some object-relational databases or special-purpose database systems
- Virtual database systems:
	- Allow different databases to work together as a unified database system
- Spatial data technology:
	- Using database to store and access data according to the locations it describes

# Summary
- Data:
	- One of the most valuable resources that a firm possesses
- Entity:
	- Generalized class of objects for which data is collected, stored, and maintained
- Traditional file-oriented applications:
	- Often characterized by program-data dependence
- Relational model:
	- Places data in two-dimensional tables
- DBMS:
	- Group of programs used as an interface between a database and its users and other application programs
	- Basic functions:
		- Providing user views
		- Creating and modifying the database
		- Storing and retrieving data
		- Manipulating data and generating reports
- Data warehouses:
	- Relational database management systems specifically designed to support management decision making
- Data mining:
	- Automated discovery of patterns and relationships in a data warehouse
- Business intelligence:
	- Process of getting enough of the right information in a timely manner and usable form