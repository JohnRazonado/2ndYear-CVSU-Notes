## Logic
- We all love computers. They can do so many amazing things. Within a couple of decades computers have completely revolutionized almost all the aspects of human life. 
- They can do tasks of varying degrees of sophistication, all by just flipping zeros (0) and ones (1). It is remarkable to see how such a simple action can lead to so much complexity. 
- But I'm sure you all know that such complexity cannot be achieved (practically) by just randomly flipping the numbers. There is indeed some reasoning behind it. There are rules that govern the way this should be done. In the next slide, we will discuss those rules and we will see how they govern the way computers "think".” 
- logic operators: NOT, AND, OR, and XOR; 
- A logical expression can only have the values .true. or .false.
- OR: Also known as Disjunction. This operation is performed on two Boolean variables. The output of the OR operation will be 0 when both of the operands are 0, otherwise it will be 1. 
- AND: Also known as Conjunction. This operation is performed on two Boolean variables. The output of AND operations will be 1 when both operands are 1, otherwise it will be 0. 
- NOT: Also known as Negation. This operation is performed only on one variable. If the value of the variable is 1 then this operation simply converts it into 0 and if the value of the variable is 0, then it converts it into 1. 
- XOR: XOR gate or Exclusive-OR gate is a special type of logic gate which gives 0 as output if both of the inputs are either 0 or 1, otherwise it gives 1

![[Pasted image 20221116092333.png]]

![[Pasted image 20221116092358.png]]

### Continuation
#### Overview
In logic, a rule of replacement is a transformation rule that may be applied to only a particular segment of an expression. A logical system may be constructed so that it uses either axioms, rules of inference, or both as transformation rules for logical expressions in the system. 

- In the philosophy of logic, A rule of **inference**, **inference rule** or **transformation rule** is logical for consisting of a function which takes premises, analyzes their syntax, and returns a conclusion. For example, the rule of inference called *modus ponens* take two premises, one in the form of "If p the q" and another in the form "p", and return the conclusion "q".  

#### Method of Deduction
Deductive reasoning, or deduction, starts out with a general statement, or hypothesis, and examines the possibilities to reach a specific, logical conclusion, according to California State University. The scientific method uses deduction to test hypotheses and theories.

- Deduction is **drawing a conclusion from something known or assumed**. This is the type of reasoning we use in almost every step in a mathematical argument. **<mark style="background: #FFB8EBA6;">For example, to solve 2x = 6 for x we divide both sides by 2 to get 2x/2 = 6/2 or x = 3.</mark>**

#### Modus Ponens
- Latin for "**method of affirming**"
- A rule of inference use to draw logical conclusions, which states that if p is true, and if p implies q (p q), then q is true.

**Modus Ponens** : Latin for "method of affirming"
**Modus Tollens**: Latin for "method of denying"


#### Rules of Replacement
- the rules of Double Negation (DN), De Morgan's Law (DM), Arrow (AR) and Contraposition (CN) are called rules or replacement, or "two-way rules"
- The derivation can got *both ways* - e.g., you can derive \~\~P from P, or vice versa (you can derive P from \~\~P)
- We use the special symbol :: to denote this special relationship (it's like a special type of "therefore" symbol)
- Double Negation (DN)
![[Pasted image 20221117184052.png]]

### Salient Points
Logic is the tool for reasoning about the truth and falsity of statements. There are two main directions in which logic develops.
- The first is the depth to which we explore the structure of statements. The study of the basic level of structure is called propositional logic. First order predicate logic, which is often called just predicate logic, studies structure on a deeper level. 
- The second direction is the nature of truth. For example, one may talk about statements that are usually true or true at certain times. We study only the simplest situation: a statement is either always true or it is considered false.
"True" and "false" could be replace by 1 and 0 (or any other two symbols) in our discussions. Using 1 and 0 relates logic to Boolean functions. In fact, *propositional logic* is the study of Boolean functions, where 1 plays the role of “true” and 0 the role of “false.” As we saw in Unit BF, Boolean functions can be thought of as computer circuits. Thus, propositional logic, Boolean functions, and computer circuits are different ways of interpreting the same thing. 

## Proposition

Propositional logic is not sufficient for all our logic needs. Mathematics requires predicate logic. This and other logics are employed in the design of expert systems, robots and artificial intelligence.

A proposition is a sentence that is either true or false.
The definition of a proposition is a statement putting forth an idea, suggestion or plan. An example of a proposition is the idea that the death penalty is a good way to stop crime. An example of a proposition is a suggestion for a change in the terms of company by laws.

In mathematics, we are interested in statements that can be proved or disproved. We define a **proposition** (sometimes called a **statement**, or an **assertion**) to be a sentence that is either true or false, but not both.

- Joe Biden is the president of the United States.
- 2 + 3 = 6
> These are propositions, because each of them is either true or false (but not both).


### Salient Points 
- Usually use the lowercase letters (symbolism) p, q, and r to represent propositions. This can be compared to using variables x, y and z to denote real numbers. Since the truth values of p, q, and r vary, they are called *propositional variables*. A proposition has only two possible values: it is either true or false. We often abbreviate these values as T and F, respectively
![[Pasted image 20221116101331.png]]

![[Pasted image 20221116101346.png]]

#### Math Symbols
|Symbol| Symbol Name | Meaning/Definition |Example| Programming|
|:---:|---|---|---|:---:|
|$=$ | equals sign| equality| 5 = 2 + 3| \=\=|
|$\neq$| not equal sign| inequality| 5 $\neq$ 4| !=|
|$>$| strict inequality| greater than| 5 > 4 |>  |
| $<$ | strict inequality| less than| 4 < 5| < |
| $\geq$ | strict inequality | greater than or equal to | 5 $\geq$ 4| >=|
|$\leq$| inequality| less than or equal to|  4 $\leq$ 5| <= |
| $()$ | parentheses| calculate expression inside first | 2 x (3 + 5) = 16| ( )|
| [ ] | brackets| calculate expression inside first | [(1+2)\* ( 1+5)] = 18 | [ ] | 
| + | plus sign| addition | 1 + 1 = 2| + | 
| - | minus sign | subtraction | 2 - 1 = 1| -  | 
| x or \* | multiply sign | multiplication | 2 \* 2 = 4| \*| 
| $\div$ | division sign | divided by | 6 $\div$ 2 = 3 | / |

##### PEMDAS
- acronym for the words:
	- Parenthesis
	- Exponents
	- Multiplication
	- Division
	- Addition
	- Subtraction
- Given two or more operations in a single expression, tells you the order to which you follow the letters in PEMDAS.
- Tells you what to calculate first, second, and so on.






## Set
In mathematics, a set is a well-defined collection of distinct objects, considered as an object in its own right. The arrangement of the objects in the set does not matter. A set may be denoted by placing its objects between a pair of curly braces.
- A collection of distinct object, called **elements** of the set
- Can be defined by describing the contents(set-builder notation), or by listing the elements of the set, enclosed in curly brackets(roster notation).

![[Pasted image 20221116101431.png]]

### Describing a Set
#### Enumerated/ Roster Notation
- When the elements of a set are enumerated (or listed) it is traditional to enclose them in braces.
- For example, the set of binary digits is {0,1} and the set of decimal digits is {0,1,2,3,4,5,6,7,8,9}.
- The choice of a name for these sets would be arbitrary; but it would be "logical" to call them **B** and **D**, respectively.
-  For example, the letters of the alphabet and the integers from 1 to 100 could be described as A={a,b,c,...,x,y,z} and G={1,2,...,99,100}.
##### Ellipsis
- The three consecutive "dots" are called an ellipsis. 
- We use them when it is clear what elements are included but not listed.
- An ellipsis is used in two other situations. To enumerate the positive integers, we would write {1,2,3,...}

#### Set-Builder Notation
-  Another way of describing sets is to use set-builder notation. For example, we could define the rational numbers as
$$
\mathbb{Q} = {a/b | a, b ∈ \mathbb{Z}, b \neq 0}
$$
> - a/b indicates that a typical element of the set is a "fraction".
> - The vertical line, |, is read "such that" or "where", and is used interchangeably with a colon.
> - a, b ∈ $\mathbb{Z}$ is an abbreviated way of saying a and b are integers.
> - Commas in mathematics are read as "and".

- The important fact to keep in mind in set notation, or in any mathematical notation, is that it is meant to be a help, not a hindrance.

##### Standard Symbols
- Sets that are frequently encountered are usually given symbols that are reserved for them alone. For example, since we will be refer-ring to the positive integers throughout this book, we will use the symbol $\mathbb{P}$ instead of writing {1,2,3,...}. A few of the other sets of numbers that we will use frequently are:
$\mathbb{N}$: the natural numbers {0, 1, 2, 3, 4, ...} (positive numbers but including 0)
$\mathbb{Z}$: the integers {..., -3, -2, -1, 0, 1, 2, 3, ...}
$\mathbb{Q}$: the rational numbers
$\mathbb{R}$: the real numbers
$\mathbb{C}$: the complex numbers


### Types/Kind of Set
#### Empty Set
-  $\emptyset$ or empty set or null set
- A = { }
- B = $\emptyset$
#### Singleton Set
- Also known as unit set
- Set with exactly one element.

A = {0}
B = {a}
#### Finite Set
Set that has finite number of elements (means the amount of elements still has and end). 

- The set of letters in the English Alphabet
- A = {1,2,3,4,5}
#### Infinite Set
Set that has uncountable number of elements.
Uses ellipsis (...)

- A = {1,2,3,4,5,...}
- Set of counting numbers.
#### Universal Set
The totality of all the elements of the sets under consideration, denoted by U or μ (pronounced as mu for the greek letter "μ")
- The set of real numbers.
#### Cardinality
The number of elements in a set denoted by |A| where A is a set.
#### Subsets
Where a set has every element of another set.
Set wherein every element of which can be found on the second set.
> Let A and B be sets. We say that A is a subset of B if and only if every element of A is an element of A. We write A ⊆ B.

**Some Examples:**
If A={3,5,8} and B={5,8,3,2,6}, then A ⊆ B
N ⊆ Z ⊆ Q ⊆ R ⊆ C

If S={3,5,8} and T={5,3,8} then S ⊆ T and T ⊆ S
#### Proper Subset
Denoted by **⊂**
If a set has “n” elements, then the number of subset of the given set is 2n and the number of proper subsets of the given subset is given by 2n-1.
#### Improper Subset/ Set Equality
- The element of the set contains only the element of another set. Denoted by *A = B* where *A* and *B* are sets.

> Let A and B be sets. We say that A is equal to B (notation A=B ) if and only if every element of A is an element of B and conversely every element of B is an element of A; that is, A ⊆ B and B ⊆ A

 if A={1,5,3,5} and A={1,5,3}, then A=B
 
 > $\emptyset$ or empty set or null set is important to be discuss here since $\emptyset$ is a proper subset of every set. Also, the empty set is an improper subset of itself.


## Set Theory
- Is a branch of mathematics which deals with the study of sets or the collection of similar objects.
- One of the most fundamental branches of mathematics, but also very complex if you try to analyze three or more sets.
- Thus, set theory has become the standard foundation for mathematics, as every mathematical object can be viewed as a set, and every theorem of mathematics can be logically deduced in the Predicate Calculus from the axioms of set theory.
### Notations
|Notation| Definition|
|---|---|
| $\in$ | Element of... (the symbol is called "Epsilon")|
|$\notin$| Not an element of...|
|$\subset$| Subset of...|
|$\not\subset$| Not a subset of...|
|$\subseteq$ | A subset and equal to...|
|$\cup$| Union (all together) 'OR'|
|$\cap$ | Intersection (Overlap) 'AND'|
|' | Not (complement) [A']|
|$\varnothing$| Empty set|


### Set Operations
![[Pasted image 20221118145707.png]]
#### Union
- Use the symbol **U**
- set A and B is given, if A U B then the answer will **consist of all elements in sets A and B**.
- formally, x $\in$ A $\cup$ B if x $\in$ A or x $\in$ B (or both)
- ![[Pasted image 20221118145635.png]]
#### Intersection
- Use the symbol **$\cap$**
- set A and B is given if A $\cap$ B then the answer will **contains only the elements that are in both set**.
- formally, x $\in$ A $\cap$ B if x $\in$ A and x $\in$ B.
- ![[Pasted image 20221118145644.png]]
#### Difference
- Use the Symbol **-** or **\\**
- set A and set B is given, if A - B then the answer are elements found in set A but not in B.
- formally, x $\in$ A - B if x $\in$ A $\cap$ x $\notin$ B
Let A = {a, b, c, d}
B = {c, d, e}

Then A-B = {a, b}

#### Symmetric Difference
- Use the symbol $\triangle$ or $\ominus$
- set A and set B are given, if A $\ominus$ B or A $\triangle$ B, the answer will be elements in **either of the sets, but not in their intersection.**
- Sometimes called **disjunctive union**
- formally, (A \ B) ∪ (B \ A) = {x | (x ∈ A) ⊕ (x ∈ B)}
- if A = {1, 2, 3, 4, 5} and B = {1, 3, 5, 7, 9} then
	- A $\triangle$ B = {2, 4, 7, 9}

#### Complement of Set
- Use the symbol **'**
- set A is given, if A' then the answer will be **elements found in the universal set but not A**
- formally, x $\in$ A' if x $\notin$ A

#### Cartesian Product
![[Pasted image 20221118151842.png]]
- Use the symbol **x**
- set A and set B are given, if A x B then the answer will be the **set of ordered pairs from A and B**
- formally, x $\in$ A x B if x = (a, b) where a $\in$ S $\cap$ b $\in$ B

- If A = {H, T} and B = {1, 2, 3}, then A x B = {(H, 1), (H, 2), (H, 3), (T, 1), (T, 2), (T, 3)}
- If A = {T, H} and B = {1, 2, 3}, then A x B = {(T, 1), (T, 2), (T, 3), (H, 1), (H, 2), (H, 3)}



### Venn Diagram
- Represents each set by a circle, usually drawn inside of a containing box representing the universal set.
- Overlapping areas indicate elements common to both sets.
![[Pasted image 20221118144035.png]]

### SQL Application 
#### SQL
- A database computer language designed for the retrieval and management of data in a relational database. 
- Stands for **Structured Query Language**
![[Pasted image 20221116101517.png]]

![[Pasted image 20221116101611.png]]

![[Pasted image 20221116101641.png]]

### Relation
- A Relation between two sets is a collection of ordered pairs containing one object from each set. If the object x is from the first set and the object y is from the second set, then the objects are said to be related if the ordered pair (x,y) is in the relation. A function is a type of relation
![[Pasted image 20221116230130.png]]

![[Pasted image 20221116230205.png]]
#### Entity Relationship Diagram
- Diagram to represent all the relationship of the table. It is needed to be used before creating the table itself on SQL or any database management.
![[Pasted image 20221116230219.png]]

### Function
- An expression, rule, or law that defines a relationship between one variable (the independent variable) and another variable (the dependent variable). 
- If a variable y is so related to a variable x that whenever a numerical value is assigned to x, there is a rule according to which a unique value of y is determined, then y is said to be a function of the independent variable x. 
- “This relationship is commonly symbolized as y = f(x).”
![[Pasted image 20221116230255.png]]

#### Applications
![[Pasted image 20221116230318.png]]

![[Pasted image 20221116230330.png]]

![[Pasted image 20221116230415.png]]