![[Lesson 4 -- Tree Traversal.pptx]]

## Tree
- A tree is a collection of nodes. 
- The collection can be empty; otherwise, a tree consists of a distinguished node r, called the root, and zero or more non-empty (sub) trees T1, T2, …, Tk each of whose roots are connected by a directed edge from r.
- A tree is a collection of N nodes, one of which is the root and N-1 edges.

- The root of each subtree is said to be a child of r and r is said to be the parent of each subtree root.
- **Leaves**: nodes with no children (also known as external nodes)
- **Internal Nodes**: nodes with children
- **Siblings**: nodes with the same parent
- A **path** from node n1 to nk is defined as a sequence of nodes n1, n2, …, nk such that ni is the parent of ni+1 for 1<= i <= k. 
- The length of this path is the number of edges on the path namely k-1.
- The length of the path from a node to itself is 0.
- There is exactly one path from the root to each node.

- Depth (of node): the length of the unique path from the root to a node.
- Depth (of tree): The depth of a tree is equal to the depth of its deepest leaf.
- Height (of node): the length of the longest path from a node to a leaf.
	- All leaves have a height of 0
	- The height of the root is equal to the depth of the tree 


![[Pasted image 20230728230836.png]]
- root, leaf
- parent, child, sibling
- subtree
- external, internal node
- ancestor, descendant
- depth, height

## Binary trees
- A binary tree is a tree in which no node can have more than two children.
- Each node has an element, a reference to a left child and a reference to a right child.
- Each node has 0, 1, or 2 children
![[Pasted image 20230728231021.png]]

## Tree Traversals
- A binary tree is defined recursively: it consists of a root, a left subtree, and a right subtree
- To traverse (or walk) the binary tree is to visit each node in the binary tree exactly once
- Tree traversals are naturally recursive
- Since a binary tree has three “parts,” there are six possible ways to traverse the binary tree:
	- root, left, right
	- left, root, right
	- left, right, root
	- root, right, left
	- right, root, left
	- right, left, root


### Depth-First Traversals
![[Pasted image 20230728231504.png]]

#### Preorder (N-L-R)
- In preorder, the root is visited first
- Root, left right
- “A node is visited when passing on its left in the visit path”

- Visit the node
- Visit the left subtree, if any.
- Visit the right subtree, if any


![[Pasted image 20230728231544.png]]
code:
```C++
public void preorderTraversal(Visitor v){
   if(!isEmpty() && ! v.isDone()){
      v.visit(getKey());
      getLeft().preorderTraversal(v);
      getRight().preorderTraversal(v);
   }
}

```
#### Inorder (L-N-R)
- In inorder, the root is visited in the middle
- Left, root, right
- “A node is visited when passing below it in the visit path”

- Visit the left subtree, if any. Visit the node
- Visit the right subtree, if any.

![[Pasted image 20230728231635.png]]
>P   F   A   M   K   S   R   U   T
>Note: An inorder traversal can pass through a node without visiting it at that moment.


Code:
```c++
public void inorderTraversal(Visitor v){
   if(!isEmpty() && ! v.isDone()){
      getLeft().inorderTraversal(v);
      v.visit(getKey());
      getRight().inorderTraversal(v);
   }
}

```

### Postorder (L-R-N)
- In postorder, the root is visited last
- Left, right, root
- “A node is visited when passing on its right in the visit path”


- Visit the left subtree, if any.
- Visit the right subtree, if any.
- Visit the node

![[Pasted image 20230728232046.png]]
> P   A   M   F   R   S   T   U   K
> Note: An postorder traversal can pass through a node without visiting it at that moment.


Code
```C++
public void postorderTraversal(Visitor v){
   if(!isEmpty() && ! v.isDone()){
      getLeft().postorderTraversal(v) ;
      getRight().postorderTraversal(v);
      v.visit(getKey());
   }
}
```


### Tree Traversal using "Flags"
- The order in which the nodes are visited during a tree traversal can be easily determined by imagining there is a “flag” attached to each node, as follows:
	- ![[Pasted image 20230728232145.png]]
	- ![[Pasted image 20230728232158.png]]
	- ![[Pasted image 20230728232206.png]]
- To traverse the tree, collect the flags:
	- ![[Pasted image 20230728232352.png]]
	- ![[Pasted image 20230728232412.png]]
	- ![[Pasted image 20230728232418.png]]

### Other Traversals
- The other traversals are the reverse of these three standard ones
	- That is, the right subtree is traversed before the left subtree is traversed
- Reverse preorder: root, right subtree, left subtree
- Reverse inorder: right subtree, root, left subtree
- Reverse postorder: right subtree, left subtree, root

#### Reverse Depth-first traversals
- 6 different traversals
	- NLR (pre-order traversal)
	- NRL  (reverse pre-order traversal)
	- LNR (in-order traversal)
	- RNL  (reverse in-order traversal)
	- LRN (post-order traversal)
	- RLN (reverse post-order traversal)
- Reverse traversals are not common


## Arithmetic Expression Tree
- Binary tree for an arithmetic expression
	- internal nodes: operators
	- leaves: operands
- Example: arithmetic expression tree for the expression 
	- ((2 x (5 - 1)) + (3 x 2))

![[Pasted image 20230728232713.png]]

#### Inorder traversal
![[Pasted image 20230728232735.png]]
- ((2 x (5 - 1)) + (3 x 2))

#### Postorder traversal
- Recursively evaluate subtrees
- Apply the operator after subtrees are evaluated

![[Pasted image 20230728232821.png]]

