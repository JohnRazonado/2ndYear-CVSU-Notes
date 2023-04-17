**1. Origin or great history of Database**
From the book “Database Management Systems” by Ramakrishnan (1997), he states that in the earliest days of computers, storing and manipulating data have been a major application focus. The first general-purpose DBMS, designed by Charles Bachman at General Electric in the early 1960s, was called the Integrated Data Store. Formed the basis for the network data model, standardized by the Conference on Data Systems Languages (CODASYL), and strongly influenced database systems through the 1960s. Early systems only provide programming language interfaces. This made it time-consuming and expensive to implement new queries and transactions since new programs had to be written, tested, and debugged.

In the late 1960s, IBM developed the Information Management System (IMS) DBMS, which formed the basis for the hierarchical data model. The SABRE system for making airline reservations was jointly developed by American Airlines and IBM around the same time, and it allowed several people to access the same data through a computer network. Interestingly, today the same SABRE system is used to power popular Web-based travel services such as Travelocity.

In 1970, Edgar Codd, at IBM’s San Jose Research Laboratory, proposed a new data representation framework called the relational data model. This starts the rapid development of several DBMSs based on the relational model, along with a rich body of theoretical results that placed the field on a firm foundation. Codd won the 1981 Turing Award for his seminal work.

In the 1980s, the relational model consolidated its position as the dominant DBMS paradigm, and database systems continued to gain widespread use. The SQL query language for relational databases, developed as part of IBM’s System R project, is now the standard query language. SQL was standardized in the late 1980s, and the current standard, SQL:1999, was adopted by the American National Standards Institute (ANSI) and International Organization for Standardization (ISO). James Gray won the 1999 Turing award for his contributions to database transaction management.

In the late 1980s and the 1990s, advances were made in many areas of database systems. Several vendors (e.g., IBM’s DB2, Oracle 8, Informix2 UDS) extended their systems with the ability to store new data types such as images and text and to ask more complex queries.

**2. What is Database?  
**Database is an organized collection of data stored and accessed electronically (Tsichritzis & Lochovsky, 1982). Databases can be used for various purposes, such as storing data for a website, keeping track of customer information, or managing inventory which is often controlled by database management systems (DBMS) (Simplilearn, 2023). Small databases can be stored on a file system, while large databases are hosted on computer clusters or cloud storage.

**3. Characteristics of Database**

**Self-describing nature of a database system**
Insulation between programs and data, and data abstraction. Support of multiple views of the data. Sharing of data and multiuser transaction processing (Watt, 2014a).

**Structured and Described Data**
Fundamental feature of the database approach is that the database system does not only contain the data but also the complete definition and description of these data.

This kind of stored data is called metadata ("data about data") which describes and defines the data and relationship among tables (Watt, 2014a).

**Separation of Data and Applications**
Application software does not need any knowledge about the physical data storage like encoding, format, storage place, etc. It only communicates with the management system of a database (DBMS) via a standardized language like SQL. This insulation between the programs and data is also called program-data independence (Watt, 2014a).

**Data Integrity:**
Data integrity is a byword for the quality and reliability of the data of a database system.

It means there’s an enforcement of database restricting from unauthorized access (confidentiality) and unauthorized changes. Data reflect facts of the real world, which needs constraints from data types (use of dates, fields that accept numbers only, and more), and restrictions of data access (Watt, 2014a).

**Transactions:**
A transaction is a bundle of actions that are done within a database to bring it from one consistent state to a new consistent state. In between the data are inevitably inconsistentnt even if other users update the same data/information. Since by nature, DBMS allows many users to access the database individually or simultaneously (CseWorld Online, 2020).

**Data Persistence:**
Data persistence means that in a DBMS all data is maintained as long as it is not deleted explicitly. The database system provides a separate process, from that of a network backup, for backing up and recovering data. If a hard drive fails and the database stored on the hard drive is not accessible, the only way to recover the database is from a backup. The life span of data needs to be determined directly or indirectly by the user and must not be dependent on system features (CseWorld Online, 2020).

**4. What is DBMS/ RDBMS**
A database management system, or DBMS, is software designed to assist in maintaining and utilizing large collections of data. Allowing users to enable users to create, update, and delete data in the database. The need for such systems, as well as their use, is growing rapidly (Ramakrishnan, 1997).

**Types of DBMS**

There are four main types of DBMS: relational, object-oriented, graph-based, and NoSQL (Simplilearn, 2023).
- Relational DBMSs are the most common and use a tabular structure to store data.
- Object-oriented DBMSs use an object-oriented model to store data, and Graph-based DBMSs use a graph structure to store data.
- NoSQL DBMSs are a newer DBMS type that uses a non-tabular structure to store data.

**RDBMS**
A relational database is a type of database that stores and provides access to data points that are related to one another it is based on relational model, an intuitive, straightforward way of representing data in tables. In a relational database, each row in the table is a record with a unique ID called the key. The columns of the table hold attributes of the data, and each record usually has a value for each attribute, making it easy to establish relationships among data points (Oracle, 2020).

**5. Differentiate DBMS vs. RDBMS**
The database which stores data in the tables that have relationships with other tables in the database is called RDBMS or Relational Database Management System. However, in DBMS or Database Management System, there are no relationships among tables. Most prevalent difference is that RDBMS is a more robust and sophisticated tool than DBMS. RDBMS can handle large amounts of data more efficiently and effectively than DBMS. Additionally, RDBMS offers more features and tools for managing and manipulating data than DBMS. For these reasons, RDBMS is the more popular choice between the two.

The main difference between a DBMS and an RDBMS is that a DBMS is a software application used to store, retrieve, and manage data in a database, while an RDBMS is a type of DBMS that stores data in a relational database (Simplilearn, 2023).

**B.**
**1.  What is Data model?**
A data model is a collection of high-level data description constructs that hide many low-level storage details. A DBMS allows a user to define the data to be stored in terms of a data model. Most database management systems today are based on the relational data model (Ramakrishnan, 1997).

Most data models also include a set of basic operations for specifying retrievals and updates on the database. Many data models can be categorized according to the types of concepts they used: High-level or conceptual data models; provides concepts that are close to users’ perceived data, or low-level or physical data models provides concepts details how data is stored on computer storage like a hard disk (Elmasri & Navathe, 2016).

It is based on two concepts:
- Entities, tables that hold specific information (data)
- Relationships, the associations or interactions between entities.

Data model in general is a collection of concepts or notations for describing data, data relationships, data semantics, and data constraints. Most data models also include a set of basic operations for manipulating data in the database (Watt, 2014b). Also, **attribute** can be a part of the concept of data models which represents some property of interest that further describes an entity (Elmasri & Navathe, 2016).

**2.  What is ERD?**
The entity-relationship (ER) data model allows us to describe the data involved in a real-world enterprise in terms of objects and their relationships and is widely used to develop an initial database design. It provides useful concepts that allow us to move from an informal description of what users want from their database to a more detailed, precise description that can be implemented in a DBMS (Ramakrishnan, 1997).

![[Pasted image 20230416223130.png]]

![[Pasted image 20230416223133.png]]

**3.  What is Relational Model?**
The relational model represents the database as a collection of relations. It resembles relationship of a table of values or, to some extent, a flat file (simple or linear structure of records) of records. For example, the database of files that was shown in below is similar to the basic relational model representation (Elmasri & Navathe, 2016). It is an abstract model in general used for relational databases to perform database management.

When a relation is thought of as a table of values, each row in the table represents a collection of related data values. A row represents commonly corresponds to a real-world entity or relationship. The table name and column names are used to help to interpret the meaning of the values in each row. The figure bellow is called STUDENT because each row represents facts about a particular student entity. The column names—Name, Student_number, Class, and Major—specify how to interpret the data values in each row, based on the column each value is in.

![[Pasted image 20230416222844.png]]
The most fundamental elements in the relational model are relations, which users and modern RDBMSs recognize as tables (Drake, 2021). A relation is a set of tuples, or rows in a table, with each tuple sharing a set of attributes, or columns:

![[Pasted image 20230416222828.png]]
