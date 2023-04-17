> This part is detailed on the book **Digital Computer Electronics** by Albert Paul Malvino And Jerald A Brown at *page 70*

Many engineers and technicians don’t simplify equations with boolean algebra. Instead, they use a method based on *Karnaugh maps*. This section tells you how to construct a Karnaugh map.


![[Pasted image 20230128162829.png]]

### Definition
 It is a method to simplify Boolean algebra expressions. Introduced by Maurice Karnaugh in 1935 as a refinement of Edward W. Veitch's 1952 Veitch chart. The Karnaugh map reduces the need for extensive calculations by taking advantage of humans' pattern-recognition capability. Karnaugh maps are used to simplify real-world logic requirements so that they can be implemented using a minimum number of logic gates. A sum-of-products expression (SOP) can always be implemented using AND gates feeding into an OR gate, and a product-of-sums expression (POS) leads to OR gates feeding an AND gate.

>If the given Boolean expressions are in SOP form (minterms), then the array of K-map is represented with the binary value ‘1’. Similarly, if the given expression is in POS form (max terms), then the array of K-map is represented with ‘1’. After finding minterms and max terms, the expression can be reduced by making groups. The karnaugh map gives detailed information better than the truth table.

### Pairs, Quads, and Octets
![[k-map order.png]]

### Karnaugh Simplifications


### Don't-Care Conditions


## Summary of Terms
### Bus 
A group of wires carrying digital signals
### Don't care
An output that may be either low or high without affecting the operation of the system.
### Fundamental product
The logical product of variables and complements that produces a high output for a given input condition.
### Karnaugh Map
A graphical display of the fundamental products in a truth table.
### Octet
A group of eight adjacent 1s on a [[Karnaugh Mapping|Karnaugh map]].
### Pair 
A group of two adjacent 1s on a [[Karnaugh Mapping|Karnaugh map]]. These 1s may be horizontally or vertically aligned. 
### Quad
A group of four adjacent 1s on a [[Karnaugh Mapping|Karnaugh map]]. 
### Redundant group
A group of 1s on a [[Karnaugh Mapping|Karnaugh map]] all of which are overlapped by other groups.
### Sum-of-products circuits
An AND-OR circuit obtained by ORing the fundamental products that produce output 1s in a truth table.


## Extra
### Other laws from Logic theories
![[Pasted image 20230202235102.png]]