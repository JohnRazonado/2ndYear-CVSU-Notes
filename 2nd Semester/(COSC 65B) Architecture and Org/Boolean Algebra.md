- A branch of algebra dealing with variables can only take two(2) values:
	- **1** and **0**
- Deals with **logic and truth values**.
	- involves a set of logical operations that can be used to manipulate and compare these values.
- Known to be used on digital circuitry in digital computers and other digital systems.
- Name in honor of English Mathematician **George Boole**,
	- Proposed basic principle in 1854 in his treatise
	- **An Investigation of the Laws of Thought on Which to Found the Mathematical Theories of Logic and Probabilities.**
- First utilized by Claude Shannon in 1938
	- In 1938, Claude Shannon, a research assistant in the Electrical Engineering Department at M.I.T., suggested that Boolean algebra could be used to solve problems in relay-switching circuit design. Shannon’s techniques were subsequently used in the analysis and design of electronic digital circuits.
- Convenient in two areas
	- **Analysis** - economical way of describing function of digital circuitry.
	- **Design** -  applied to develop a simplified implementation of that function.
- Widely used in Computer Science, electronics and other fields needing logical operations.
- Based on two values: **True** and **False**, represented as **1** and **0**, respectively. These values are also called binary digits or bits. Logical operations are performed on these values to produce new truth values.

## Logic Operations
> Need to expand more and connect to [[2nd Year/1st Semester/(COSC 60) Digital Logic Design/Boolean Algebra|Digital Logic Design]]

The basic logical operations are AND, OR, and NOT, which are symbolically represented by dot, plus sign, and overbar:
![[Pasted image 20230324121203.png]]

### AND
- AND yields true (binary value 1) if and only if both of its operands are
true. 

### OR
- The operation OR yields true if either or both of its operands are true. 

### NOT
- The unary operation NOT inverts the value of its operand.

### Example
![[Pasted image 20230405144729.png]]
>D is equal to 1 if A is 1 or if both B = 0 and C = 1. Otherwise D is equal to 0

- Several points concerning the notation are needed. In the absence of parentheses, the AND operation takes precedence over the OR operation. Also, when no ambiguity will occur, the AND operation is represented by simple concatenation instead of the dot operator. Thus,
![[Pasted image 20230405144806.png]]
> all mean: Take the AND of B and C; then take the OR of the result and A.

### Advance Operators
#### XOR
-  exclusive-or (XOR)
- XOR of two logical operands is 1 if and only if exactly one of the operands has the value 1
#### NAND
-  complement (NOT) of the AND function
#### NOR
- Complement of OR

![[Pasted image 20230405145002.png]]

### TRUTH TABLE
- A table that defines the basic logical operations.
- Lists the value of an operation for every possible combination of values of
operands.

![[Pasted image 20230405145053.png]]
> Boolean operators of two input variables


![[Pasted image 20230405145101.png]]
>Boolean operators extended to more than two inputs

## Postulate and Rules
### Identity law
This states that if we OR a variable with 0 or AND a variable with 1, the
result is the original variable.
### Commutative law
This states that the order in which variables are ORed or ANDed does not affect the result.

### Associative law
This states that the grouping of variables when ORed or ANDed does not affect the result.

### Distributive law
This states that ORing or ANDing a variable with a group of variables that are ORed or ANDed together is equivalent to ORing or ANDing the variable with each individual variable in the group.

### Complement law
This states that every variable has a complement, which is the value that makes the OR or AND operation with the original variable equal to 1 or 0, respectively.

### DeMorgan's laws
These laws relate the complement of a group of variables to the complement of each individual variable in the group.
	1. The first law states that the complement of a group of variables ORed together is equivalent to the AND of the complements of each individual variable in the group.
	2. The second law states that the complement of a group of variables ANDed together is equivalent to the OR of the complements of each individual variable in the group.

The table below summarizes key identities or postulates of Boolean algebra. The equations have been arranged in two columns to show the complementary, or dual, nature of the AND and OR operations.

![[Pasted image 20230324121431.png]]

There are two classes of identities: basic rules (or postulates), which are stated without proof, and other identities that can be derived from the basic postulates.

The postulates define the way in which Boolean expressions are interpreted. 