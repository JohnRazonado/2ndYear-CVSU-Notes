
## Why Database Design is Important?

![[Pasted image 20221205132517.png]]
- It ensures data consistency
- ensures data elimination of redundancy
- efficient execution of queries 
- high performance application.

## Database Design
- Focuses on the design of the database structure that will be used to store and manage end-user data
- Poorly designed databases causes difficult-to-trace errors
- Well-design database
	- Facilitates data management
	- Generates accurate and less error. (accurate and valuable information)

## Different Design
![[Pasted image 20221205132942.png]]

![[Pasted image 20221205132957.png]]

## Evolution of File System Data Processing
![[Pasted image 20230127225222.png]]
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
		- Extensive Programming.

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