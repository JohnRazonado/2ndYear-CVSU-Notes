## What's Data Structure?
- Data structure is a representation of data and the operations allowed on that data.
- A data structure is a way to store and organize data in order to facilitate the access and modifications.
- Data Structure are the method of representing of logical relationships between individual data elements related to the solution of a given problem.
### Classifications
![[Pasted image 20230412225902.png]]
>Non-linear = Diagram, branched out.

![[Pasted image 20230412225930.png]]![[Pasted image 20230412225936.png]]

![[Pasted image 20230412225945.png]]

![[Pasted image 20230412225957.png]]

![[Pasted image 20230412230004.png]]

## What to Use
- The choice of particular data model depends on two consideration:
	- It must be rich enough in structure to represent the relationship between data elements
	- The structure should be simple enough that one can effectively process the data when necessary
## Types of Data Structures
### Linear
In Linear data structure, values are arrange in linear fashion.
- Array: Fixed-size
- Linked-list: Variable-size
- Stack: Add to top and remove from top
- Queue: Add to back and remove from front
- Priority queue: Add anywhere, remove the highest priority

### Non-Linear
The data values in this structure are not arranged in order.
- Hash tables: Unordered lists which use a ‘hash function’ to insert and search
- Tree: Data is organized in branches.
- Graph: A more general branching structure, with less strict connection conditions than for a tree

### Homogenous
In this type of data structures, values of the same types of data are stored.
- Array

### Non-Homogenous
Data values of different types are grouped and stored.
- Structure
- Classes

>No single data structure works well for all purposes, and so it is important to know the   strengths and limitations of several of them

## Stack
Collection with access only to the last element inserted
- Last in first out
- insert/push
- remove/pop
- top
- make empty
![[Pasted image 20230412230413.png]]

## Queues
Collection with access only to the item that has been present the longest

- Last in last out or first in first out
- enqueue, dequeue, front
- priority queues and dequeue

![[Pasted image 20230412230527.png]]

## List
A **flexible** structure, because can grow and shrink on demand.

Elements can be:
- Inserted
- Accessed
- Deleted
At **any** position
![[Pasted image 20230412230624.png]]

## Tree
A Tree is a collection of elements called **nodes**.
- One of the node is distinguished as a **root**, along with a relation (“parenthood”) that places a hierarchical structure on the nodes.
![[Pasted image 20230412230727.png]]

## Algorithm
A process or set of rules to be followed in calculations or other problem-solving operations, especially by a computer:
![[Pasted image 20230412230754.png]]

### Characteristics of an Algorithm
1. **Each step of an algorithm must be exact**; this means that an algorithm must be precise and unambiguously described. This eliminates any uncertainty. It can also be said to the characteristic of precision, i.e. the steps are precisely stated (defined).
2. **Algorithms must terminate**; since the ultimate aim of an algorithm is to solve a problem, then it must terminate otherwise there won't be a solution for the problem. This leads to the fact that an algorithm must have a finite number of steps in its execution. The presence of endless (infinite) loops must be avoided.
3. **An algorithm must be effective**; this means that an algorithm must provide the correct answers at all times.
4. **An algorithm must be general**; this means that an algorithm must solve every instance of a problem.
5. **Uniqueness:** results of each step are uniquely defined and only depend on the input and the result of the preceding steps.
6. **Finiteness:** the algorithm stops after a finite number of instructions are executed.
7. **Output:** the algorithm produces output.