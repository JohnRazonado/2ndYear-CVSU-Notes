
![[Lesson 3--Binary Search Tree.pptx]]
## Trees
- A tree is a non-linear data structure. Compared to arrays, linked lists, stacks and queues which are linear data structures, a tree can be empty with no nodes or consist of only one node called the root, and zero or one or more sub-trees.
- Tree is a non-linear data structure which organizes data in a hierarchical structure and this is a recursive definition. It is a connected graph without any circuits. If in a graph, there is one and only one path between every pair of vertices, then it is called a tree.

### Important properties of tree data structure:
- There is one and only one path between every pair of vertices in a tree.
- A tree with n vertices has exactly (n-1) edges.
- A graph is a tree if and only if it is minimally connected.
- Any connected graph with n vertices are (n-1) edges is a tree.

![[Pasted image 20230630002022.png]]

![[Pasted image 20230630002033.png]]


## Binary Tree

### Types of Binary Tree
- Full binary tree is composed of 0 or 2 children in every node.
- It can also be called as such if all nodes except leaf nodes have two children.
![[Pasted image 20230728224655.png]]
> Number of leaf nodes is the number of internal nodes plus 1
> L = I + 1
> L = number of leaf nodes
> I = number of internal nodes

- A **complete binary tree** is characterized by having all the levels completely filled except (possibly) for the last level.
- Last level has all keys as left as possible.
![[Pasted image 20230728224946.png]]

- If  the left child node or right child node dominates the tree, it is then called **skewed binary tree**.
- All nodes except one have only one child node while the remaining node has no child.
- Left skewed tree is characterized by a left child in most of the nodes with no corresponding right child.
- Right skewed tree is the opposite of the left.
![[Pasted image 20230728225012.png]]

### Size, Degree & Depth of Binary Tree
- Total number of edges from root node to a particular node is known as depth of that node.  
- **Depth of a tree** is the total number of edges from root node to a leaf node in the longest path.  Depth of all root node = 0.
- **depth of a tree** = height of a root node.
- The terms “level” and “depth” are used interchangeably.

![[Pasted image 20230728223706.png]]
![[Pasted image 20230728224215.png]]

- each child from a node forms a subtree recursively.
- Every child node forms a subtree on its parent node.
![[Pasted image 20230728224246.png]]

- A forest is a set of disjoint trees.
![[Pasted image 20230728224615.png]]






## Level and height of a tree
- each step from top to bottom is called **level of a tree**.
- The level count starts with 0 and there is increments of 1 at each level or step.
![[Pasted image 20230728222407.png]]

- Total number of edges that lies on the longest path from any leaf node to a particular node is called a **height of that node**.  Height of all leaf nodes = 0.
- **Height of a tree** is equal to the height of a root node.

![[Pasted image 20230728222952.png]]
![[Pasted image 20230728223311.png]]




## Root, node, and leaf of a tree
- first node from where the tree originates is known as **root node.**
- In a tree, there must be only one root node
- Tree data structure can *never* have multiple root nodes
![[Pasted image 20230728214205.png]]

- connecting link between any two nodes is called **edge**
- In a tree with n number of nodes, there are exactly (n-1) number of edges.
![[Pasted image 20230728214337.png]]
- node which has a branch from it to any other node is known as **parent node.**
- **Parent node** can have any number of child nodes.

![[Pasted image 20230728214712.png]]

- Nodes that are descendant of some node is called **child node**
- All nodes except the root node are child nodes.
![[Pasted image 20230728215302.png]]
![[Pasted image 20230728215324.png]]

- Nodes belong to same pare are **siblings**
![[Pasted image 20230728215409.png]]
![[Pasted image 20230728215415.png]]

- **Degree of node** - total number of children of that node.
- **Degree of tree** - highest degree of a node among all nodes in the tree.
![[Pasted image 20230728220229.png]]

- Node having at least one child is "**internal node**"
- Internal nodes are known as "**non-terminal nodes**"
- Every non-leaf node is internal node
![[Pasted image 20230728221308.png]]

- **Leaf node** - node that doesn't have any child
- Leaf nodes are **external nodes** or **terminal nodes**
![[Pasted image 20230728221527.png]]
> Nodes D, I, J, F, K, and H are leaf nodes

## Binary Trees and Terminologies
### Non-linear Data Structure
- These data structures do not have their elements in a sequence
- Trees is an example
- **Trees** - mainly used to represent data containing a hierarchical relationship between elements, ex: records, family trees and table of contents.

### Terminologies
- **Nodes** - boxes on the tree
- **Children** - nodes immediately below (to left and right of ) given node.
- **Parent** - Immediately above of a given node
- **Root** - (unique) node without a parent.
	- A non-empty tree has exactly one root
- **Leaf** - node with no children
- **Siblings** - two children of the same parent
- A node can be **ancestor** (gradparent) or a **descendant** (great-grandchild)
- **Path** - sequence of nodes `n1,n2,...,nk` such that n1 is the same parent of ni+1 for 1 <= i < k
	- sequence of hops to get from one node to another
	- length of path is the number of edges in the path, or 1 less than the number of nodes in it.

### Trees
- Tree nodes contain two or more links
	- All other data structures we have discussed only contain one
- **Binary Trees**
	- All nodes contain two links
		- None, one, or both of which may be NULL
	- The root node is the first node in a tree.
	- Each link in the root node refers to a child.
	- Node with no children is called **leaf node**


### Binary Trees
- Special type of tree in which every node or vertex has either no children, one child or two children.
- Characteristics:
	- Every binary tree has a root pointer which points to the start of the tree
	- A binary tree can be empty
	- It consists of a node called root, a left subtree and right subtree both of which are binary trees themselves.

### Examples 
![[Pasted image 20230707235127.png]]
![[Pasted image 20230707235137.png]]

Root of tree is node having info as X:
1. Only node is root
2. Root has left child Y
3. Root X has right child Z
4. Root X has left child Y and right child Z which is again a binary tree with its parent as Z and left child of Z is A, which in turn is parent for left child B and right child C.

- Diagram of binary tree
- ![[Pasted image 20230707235453.png]]
- 