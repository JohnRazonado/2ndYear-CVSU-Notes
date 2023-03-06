![[Pasted image 20221205132517.png]]

Design for relational database management system


## Design Notes
![[Pasted image 20221205132856.png]]
Mas magandang design means less error


	![[Pasted image 20221205132942.png]]

Different system, means different design

![[Pasted image 20221205132957.png]]

### Evolution
![[Pasted image 20221205133150.png]]

![[Pasted image 20221205133248.png]]

Any company always have a filing cabinet to manually store physical data.

![[Pasted image 20221205133344.png]]

![[Pasted image 20221205133602.png]]

- Due to having it in a physical manner and so on.



![[Pasted image 20221205133717.png]]

Folders are called directories


### File System

![[Pasted image 20221205133807.png]]

![[Pasted image 20221205134026.png]]

![[Pasted image 20221205134057.png]]
- We can share info using LANs or WAN for the Internet.

![[Pasted image 20221205134214.png]]
![[Pasted image 20221205134234.png]]



#### File System Redux
![[Pasted image 20221205134308.png]]

Excel -> SQL or any DBMS

![[Pasted image 20221205134706.png]]

![[Pasted image 20221205134946.png]]

**Structural Dependence** - Need to be connected to its own structure
**Structural Independence** - How they manipulate through processing and so on independently.

![[Pasted image 20221205135156.png]]

**Data Dependence** - if data type change, the data will change too for example.

**Data Independence** - Doesn't connected to end so on.


![[Pasted image 20221205135341.png]]

- Storing same data at different places
- Put the "needed" information only to avoid redundancy
![[Pasted image 20221205135448.png]]

# Written Version
## Design Notes
- Focuses on the design of the database structure that will be used to store and manage end-user data
- Poorly designed databases causes difficult-to-trace errors
- Well-design database
	- Facilitates data management
	- Generates accurate and less error.

## Different Design
![[Pasted image 20221205132942.png]]

![[Pasted image 20221205132957.png]]

## Evolution of File System Data Processing
- Manual File System
	- Use of filing cabinet to manually store physical data.
	- Advantages
		- Cannot be destroyed by an accidental power loss
		- Hackers can't access a manual filing system from another computer
		- This helps security issues.
	- Disadvantage
		- Summarizing data and writing reports takes a lot of time
		- Data duplication
		- lack of security
		- Common errors
		- Repetition of work
		- Slow retrieval of data
- Computerized File System
	- Folders are called directories.
	- File System
		- Organize data expected to be retained after a program terminates by providing procedures to the store, retrieve and update data, as well as manage the available space on the device(s) which contain it.
		- ![[Pasted image 20221205134026.png]]
	- Advantages
		- Information Sharing
		- Database Management
		- Storage data
		- Easy access
	- Disadvantages
		- Program-data dependence
		- Duplication of Data
		- Limited data sharing
		- Lengthy Development Times
		- Excessive Program Maintenance
- File System Redux: Modern End-User Productivity tools
	- Personal computer spreadsheet programs such as Microsoft Excel are widely used by business users, and they allow the user to enter data in a series of rows and columns so the data can be manipulated using a wide range of functions.
	- Problems with File System Data Processing
		- Lengthy development times
		- Difficulty of getting quick answer
		- Complex system administration
		- Lack of security and limited data sharing
		- Extensive Programming

## Structural and Data Dependence
### Data dependence
- Data access changes when data storage characteristics change
-  if data type change, the data will change too for example.

### Data independence
- Data storage characteristics is changed without affecting the program's ability to access the dat
-  Doesn't connected to end so on.

## Data Redundancy
- Unnecessarily storing same data at different places.
- Islands of information
- Implications
	- Poor data security
	- Data inconsistency
	- Increased likelihood of data-entry errors when complex entries are made of different files
	- Data anomaly:
		- asdf