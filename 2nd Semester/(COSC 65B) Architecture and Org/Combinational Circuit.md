## Introduction
**Combinational circuits** are a type of logic circuit where the output at any given time is solely determined by the current input values.

- It is an <mark style="background: #ADCCFFA6;">interconnected set of gates whose output at any time is a function only of the input at that time</mark>.
	- As with a single gate, the appearance of the input is followed almost immediately by the appearance of the output, with only gate delays.
- These circuits don't have any memory or feedback, meaning that the output is purely a function of the inputs at that instant, and there are no internal state elements that retain information.
- Built using logic gates, such as AND gates, OR gates, NOT gates, and others. These gates take one or more input signals and produce an output signal based on their defined logic function.
- The behavior of a combinational circuit can be described using truth tables or Boolean expressions. 
	- A truth table<mark style="background: #ADCCFFA6;"> lists all possible input combinations and the corresponding output</mark> for each combination. A *Boolean expression* represents the<mark style="background: #ADCCFFA6;"> relationship between the inputs and outputs</mark> using logical operators like AND, OR, and NOT.
- Combinational circuits are used in various applications, including **arithmetic circuits** (adders, subtractors, etc.), **multiplexers**, **demultiplexers**, **encoders**, **decoders**, and more.
- They are also<mark style="background: #ADCCFFA6;"> fundamental building blocks in the design of more complex digital systems</mark>, such as processors and memory units.


### Core Meaning of Combinational Circuit
In general terms, a combinational circuit consists of ***n*** binary inputs and ***m*** binary outputs. As with a gate, a combinational circuit can be defined in
three ways:
- **Truth table:** For each of the $2^n$ possible combinations of input signals, the binary value of each of the *m* output signals is listed.
- **Graphical symbols:** The interconnected layout of gates is depicted.
- **Boolean equations:** Each output signal is expressed as a Boolean function of its input signals.
![[Pasted image 20230518233047.png]]

- Design methods: Combinational circuits can be designed using various methods, including *truth tables*, *Boolean algebra*, *Karnaugh maps*, and *logic gates*.
	- These methods help in determining the logic expressions and selecting appropriate gate combinations to achieve the desired functionality.

## Implementation of Boolean Functions
Any Boolean function can be implemented in electronic form as a network of gates. For any given function, there are a number of alternative realizations.
Consider the Boolean function represented by the truth table in Table 11.3. We can express this function by simply itemizing the combinations of values of A, B,
and C that cause F to be 1:
![[Pasted image 20230518233328.png]]


There are three combinations of input values that cause F to be 1, and if any one of these combinations occurs, the result is 1.

This form of expression, for self-evident reasons, is <mark style="background: #ADCCFFA6;">known as the <b>sum of products (SOP)</b> form.</mark> (for table 11.3)

Figure 11.4 shows a straightforward implementation with AND, OR, and NOT gates.
![[Pasted image 20230518233440.png]]


Another form can also be derived from the truth table. The <mark style="background: #ADCCFFA6;">SOP form expresses that the output is 1 if any of the input combinations that produce 1 is true. We can also say that the output is 1 if none of the input combinations that produce 0 is true.</mark> Thus,

![[Pasted image 20230518233505.png]]

This can be rewritten using a generalization of DeMorgan’s theorem:
![[Pasted image 20230518233559.png]]

Thus, 
![[Pasted image 20230518233613.png]]

This is in the <mark style="background: #ADCCFFA6;"><b>product of sums (POS)</b> form, which is illustrated in Figure 11.5</mark>. For clarity, NOT gates are not shown.
Rather, it is assumed that each input signal and its complement are available. This simplifies the logic diagram and makes the inputs to the gates more readily apparent.

Thus, a Boolean function can be realized in either SOP or POS form. At this point, it would seem that the choice would depend on whether the truth table contains more 1s or 0s for the output function:

![[Pasted image 20230518233711.png]]
>Figure 11.5 Product-of-Sums. Implementation of Table 11.3

The SOP has one term for each 1, and the POS has one term for each 0. However, there are other considerations:
- It is often possible to derive a simpler Boolean expression from the truth table than either SOP or POS.
- It may be preferable to implement the function with a single gate type (NAND or NOR).
The significance of the first point is that,<mark style="background: #ADCCFFA6;"> with a simpler Boolean expression, fewer gates will be needed to implement the function</mark>. Three methods that can be used to achieve simplification are:

- **Algebraic simplification.** Algebraic simplification involves the <mark style="background: #FFB8EBA6;">application of the identities or postulates to reduce the Boolean expression</mark> to one with fewer elements.
- **Karnaugh maps.** For purposes of simplification, the <mark style="background: #ADCCFFA6;">Karnaugh map is a convenient way of representing a Boolean function of a small number (up to four) of variables</mark>.
	- The map is an array of $2^n$ squares, representing all possible combinations of values of n binary variables.

Figure 11.7a shows the map of four squares for a function of two variables. It is essential for later purposes to list the combinations in the order 00, 01, 11, 10.
![[Pasted image 20230518233948.png]]

- Because the squares corresponding to the combinations are to be used for recording information, the combinations are customarily written above the squares.

In the case of<mark style="background: #ADCCFFA6;"> three variables, the representation is an arrangement of eight squares </mark>(Figure 11.7b), with the values for one of the variables to the left and for the other two variables above the squares.
![[Pasted image 20230518234015.png]]

For <mark style="background: #ADCCFFA6;">four variables, 16 squares are needed</mark>, with the arrangement indicated in Figure 11.7c.
![[Pasted image 20230518234027.png]]

The map can be used to represent any Boolean function in the following way. <mark style="background: #FFB8EBA6;">Each square corresponds to a unique product in the sum-of-products form, with a 1 value corresponding to the variable and a 0 value corresponding to the NOT of that variable.</mark>



Once the map of a function is created, we can often write a simple algebraic expression for it by noting the arrangement of the 1s on the map. We can summarize the rules for simplification as follows:
1. Among the marked squares (squares with a 1), *find those that belong to a unique largest block of 1, 2, 4, or 8 and circle those blocks.*
2. Select additional blocks of <mark style="background: #ADCCFFA6;">marked squares that are as large as possible and as few in number as possible</mark>, but *include every marked square at least once*. The results may not be unique in some cases.
	- For example, if a marked square combines with exactly two other squares, and there is no fourth marked square to complete a larger group, then there is a choice to be made as to which of the two groupings to choose.
	- When you are <mark style="background: #ADCCFFA6;">circling groups, you are allowed to use the same 1 value</mark> more than once.
3. Continue to draw loops around single marked squares, or pairs of adjacent marked squares, or groups of four, eight, and so on in such a way that every marked square belongs to at least one loop; then <mark style="background: #ADCCFFA6;">use as few of these blocks as possible to include all marked squares.</mark>
4. Finally, before going from the map to a simplified Boolean expression,<mark style="background: #ADCCFFA6;"> any group of 1s that is completely overlapped by other groups can be eliminated.</mark>


-  **Quine-McCluskey**. A tabular approach for more than four variables.
This method is <mark style="background: #ADCCFFA6;">suitable for programming on a computer to give an automatic tool for producing minimized Boolean expressions</mark>.®

![[Pasted image 20230518234158.png]]

![[Pasted image 20230518234220.png]]