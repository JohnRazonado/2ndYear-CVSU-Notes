#inProgress 
> Need to be connected on Digital Logic Design notes and Boolean Algebra part of the notes.

## Objectives:
- Define what logic gates are and how they function in digital circuits.
- Explain the different types of logic gates, including AND, OR, NOT, XOR, and NAND gates.
- Describe the truth tables for each type of logic gate and explain how they are used to determine
the output of a circuit.

## Gates
- A gate is a basic building block that performs a specific logical operation on one or more binary inputs to produce a binary output.
- Logical functions are implemented by the interconnection of gates.
- A gate is an electronic circuit that produces an output signal that is a simple Boolean operation on its input signals.
- Gates are used to construct more complex digital circuits, such as adders, multiplexers, and memory units.
- Gates are typically represented using symbolic notation, such as the Boolean algebraic expressions, truth tables, or logic diagrams.
	- They can be implemented using a variety of electronic devices, such as transistors, diodes, or relays, depending on the specific application.
- All of the gates except NOT can have more than two inputs.
  
- The basic gates used in digital logic are AND, OR, NOT, NAND, NOR, and XOR.
	- AND gate: Produces a high output only when all inputs are high.
	- OR gate: Produces a high output when any input is high.
	- NOT gate: Produces the logical complement of its input.
	- XOR gate: Produces a high output when the number of high inputs is odd.
	- NAND gate: Produces a low output only when all inputs are high.
	- NOR gate: Produces a low output when any input is high.

The symbology used in this table is from the IEEE standard, IEEE Std 91. Note that the inversion (NOT) operation is indicated by a circle.
![[Pasted image 20230428011154.png]]


- Typically, not all gate types are used in implementation. Design and fabrication are simpler if only one or two types of gates are used. 
- A functionally complete set of gates is a set of logic gates that can be used to implement any possible Boolean function.
	- This means that any logical operation, no matter how complex, can be expressed using only the gates from the set.
-  The following are functionally complete sets:
	- AND, OR, NOT
	- AND, NOT
	- OR, NOT
	- NAND
	- NOR
- There are several sets of functionally complete gates, but the most commonly used set is
made up of the NAND and NOR gates. This is because both NAND and NOR gates can
be used to implement all other gates, including AND, OR, NOT, and XOR.

For example:
- A NOT gate can be implemented using a NAND gate, where the input and output are connected to the same terminal. To implement a NOT gate using a NOR gate, the input is connected to both inputs of the NOR gate.
- An AND gate can be implemented using a combination of NAND gates, by connecting two inputs to a NAND gate and then applying the output to another NAND gate.
- An OR gate can be implemented using a combination of NOR gates, by connecting two inputs to a NOR gate and then applying the output to another NOR gate.
- An XOR gate can be implemented using a combination of NAND and NOR gates.


- Figure 11.2 shows how the AND, OR, and NOT functions can be implemented solely with NAND gates, and Figure 11.3 shows the same thing for NOR gates.

For this reason, digital circuits can be, and frequently are, implemented solely with NAND gates or solely with NOR gates.
![[Pasted image 20230428154308.png]]

![[Pasted image 20230428154354.png]]
#### NAND-based implementation of an OR gate:
To implement an OR gate using NAND gates, we can connect the inputs to two separate NAND gates and then connect the outputs of those two NAND gates to a third NAND gate. The final output of the third NAND gate is the output of the OR gate.


#### NOR-based implementation of an AND gate:
To implement an AND gate using NOR gates, we can connect the inputs to two separate NOR gates and then connect the outputs of those two NOR gates to a third NOR gate. The final output of the third NOR gate is the output of the AND gate. ®