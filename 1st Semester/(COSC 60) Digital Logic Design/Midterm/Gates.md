> Page 19/25

- Are digital (two-state) circuits due to input and output signals that either low or high voltages.
- Often called *logic circuits* due to they can analyze with boolean algebra.


## Inverter
- Gate that with only one input signal and one output signal
- Output is always the opposite of input.
-  The IC of it has a "04" number at the end
![[Pasted image 20221118221020.png]]

Symbol:
![[Pasted image 20221118221041.png]]

## AND
- Has two or more input signals but only one output signal
- All inputs must be high to get a high output.
- IC of it has a "08" at the end

![[Pasted image 20221118221413.png]]

![[Pasted image 20221118221420.png]]

Symbol:
![[Pasted image 20221118221431.png]]

## OR
- Has two or more input signals but only one output signals.
- If any input is high, the output signal is high.
- IC of it has a "32" at the end
![[Pasted image 20221118221147.png]]

Symbol:
![[Pasted image 20221118221200.png]]

## Boolean Algebra
### History
#### George Boole
- Invented the symbolic logic known today as **Boolean algebra** in 1854
- It has no practical use until 1938 when **Claude Shannon** used it to analyze telephone switching
### Equations
#### Inversion
![[Pasted image 20221118221647.png]]
- to use it, a variable can have a overbar for the inversion or NOT operation
- ![[Pasted image 20221118221538.png]]
	- Reads as "Y equals NOT A" or "Y equals the complement of A"
	- ![[Pasted image 20221118221611.png]]

#### OR sign
![[Pasted image 20221118221705.png]]
- Can be written using the plus "+" sign
	- ![[Pasted image 20221118221741.png]]
	- Reads as "Y equals A OR B"
	- ![[Pasted image 20221118221805.png]]

#### AND sign
![[Pasted image 20221118221838.png]]
- Can be written using the multiplication sign "\*" or "x"
- But it can also be
	- ![[Pasted image 20221118221934.png]]
	- ![[Pasted image 20221118221940.png]]
	- Reads as "Y equals A AND B"
	- ![[Pasted image 20221118222014.png]]

#### Decision-Making Elements
- Inverter, OR gate, and AND gate are often called **decision-making elements**
	- They can recognize some input [[Gates#^2d4f3a|words]] while disregarding others
	- A gate recognized a [[Gates#^2d4f3a|word]] when its output is high.
	- Disregards a [[Gates#^2d4f3a|word]] when its output is low.

### Truth Table
- A table that shows all input and output possibilities for a logic circuit.
- Input [[Gates#^2d4f3a|words]] are listed in binary progression.

> Note: The table always starts at 0 input [[Gates#^2d4f3a|words]] or the input are 0's

Sample:
![[Pasted image 20221118222256.png]]

The equation could be:
$$Y = AB + CD$$
The table could be:
![[Pasted image 20221118222348.png]]

Table 2-8 summarizes that the circuit recognizes these input words:
- 0011
- 0111
- 1011
- 1100
- 1101
- 1110
- 1111

**Word** - A string of bits that represent a coded instruction or data. ^2d4f3a