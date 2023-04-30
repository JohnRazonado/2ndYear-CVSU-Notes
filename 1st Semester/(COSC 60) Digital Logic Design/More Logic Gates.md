### NOR Gates
- Has two or more input signal but only one output signal
- All inputs must be low to get a high output.
- NOR gates only recognizes input [[Gates#^2d4f3a|word]] whose bits are all 0s'
- The IC has a "02" at the end.
#### Symbol
![[Pasted image 20230201230218.png]]
> NOR gate is basically an OR gate followed by an inverter (NOT gate)

#### Two-input 
![[Pasted image 20230201230420.png]]
> Reads as "Y equals NOT A OR B"
> The OR gate comes first, then the inversion.

![[Pasted image 20230201230956.png]]
> If all inputs are low, then the output is high

![[Pasted image 20230201231032.png]]



### De Morgan's First Theorem
- **Augustus De Morgan**
- He paved the way for boolean algebra
- First theorem dictates that a NOR gate expression has a similar output to an AND gate with inverted input of expressions.
![[Pasted image 20230201234215.png]]

![[Pasted image 20230201234225.png]]

Hence the first theorem says:
![[Pasted image 20230201234431.png]]

De Morgan's first theorem also refer to the  Inverted first ANDing as *bubble AND gate* which has equal output to an NOR gate:

![[Pasted image 20230201235212.png]]


#### Example
![[Pasted image 20230202002452.png]]
> If we want to prove figure A and C are equivalent. We need to look at the last NOR gate at figure A, we can change that to a *bubbled AND* gate allowing us to have figure A looking like a figure B.
> 
> If that's the case, we could use the Double inversion which produced a noninversion. Giving us a figure C since we cancelled out all of the inversion. Leaving the simplified circuit of figure C.


### NAND Gates
- Has two or more input signal but output one only.
- All input signals must be high to get a low output.
- The IC has a "00" at the end.
#### Symbol
![[Pasted image 20230202003359.png]]

NAND gate recognizes any input [[Gates#^2d4f3a|word]] that has a 0s

![[Pasted image 20230202003711.png]]

#### Sample
![[Pasted image 20230202003735.png]]
> Read this as "Y equals NOT AB" where the ANDing happens first before the inversion (NOT gate)

### De Morgan's Second Theorem
> The second theorem will most likely similar to the first.

![[Pasted image 20230202004110.png]]

Symbolically, the following boolean algebra is like this figure:
![[Pasted image 20230202004243.png]]
> Where figure A is a two-input NAND gate and figure B is an OR gate with inverted inputs having us figure C as a "*bubbled OR* gate".
> A **bubbled OR** gate is a gate where the inversion takes first before the ORing (OR gate function).

Two which it the end it boils down to NAND gate is the same as an *bubbled OR* gate
![[Pasted image 20230202004456.png]]

Here are some sample with two or more inputs:
![[Pasted image 20230202004628.png]]

#### Example
![[Pasted image 20230202004708.png]]
> Similar to the example of the first theorem, we can replace the final NAND gate on figure A as a *bubbled OR* gate giving us figure B.
> 
> Now we can cancel the negations or inversion due to *double inversion* leaving us to a simplified expression equivalent to figure C.


### Exclusive-Or Gates (XOR)
- It recognizes only [[Gates#^2d4f3a|words]] that have an odd 1s unlike OR gate that recognizes [[Gates#^2d4f3a|words]] with one or more 1s.
- Abbreviated as XOR.
- The IC has a "86" at the end.

#### Symbol
![[Pasted image 20230202005421.png]]
The figure A gives us a detailed view of how a XOR gate works using [[Gates|basic gates]] which is can be as:
![[Pasted image 20230202005529.png]]
![[Pasted image 20230202005543.png]]

#### Boolean Symbol
![[Pasted image 20230202005609.png]]
> Reads as "Y equals A XOR B"

![[Pasted image 20230202005644.png]]

Here's an example of XOR four-inputs:
![[Pasted image 20230202005711.png]]
![[Pasted image 20230202005725.png]]
![[Pasted image 20230202005758.png]]



### The Controlled Inverter
- It is a circuit that transmits 1's complements.

#### Example
Given that you have a new input word:
$$\Large 1100 \ 0111$$
the 1's complement is:
$$\Large 0011 \ 1000$$ 

![[Pasted image 20230202011228.png]]

![[Pasted image 20230202011258.png]]

### Exclusive-Nor Gates (XNOR)
- It is a XOR gate with an inverter
- Because of the inversion, XNOR only recognizes input word with the same values or all input must only be high or low. 
- The IC has a "" at the end.

#### Symbol
![[Pasted image 20230202005950.png]]
![[Pasted image 20230202010147.png]]
![[Pasted image 20230202010205.png]]

## Summary of Terms
### Controlled inverter
This circuit produces the 1’s complement of the input [[Gates#^2d4f3a|word]]. One application is binary subtraction. It is sometimes called a *programmed inverter*.
### De Morgan's theorems
The first theorem says that a NOR gate is equivalent to a bubbled AND gate. The second theorem says that a NAND gate is equivalent to a bubbled OR gate.
### Even parity
An even number of 1s in a binary [[Gates#^2d4f3a|word]].
### NAND gate
Equivalent to an AND gate followed by an inverter. All inputs must be high to get a low output. 
### NOR gate
Equivalent to an OR gate followed by an inverter. All inputs must be low to get a high output.
### Odd parity
An odd number of 1s in a binary [[Gates#^2d4f3a|word]].
### Parity generator
A circuit that produces either an odd- or even-parity bit to go along with the data.
### XNOR gate
Equivalent to an EXCLUSIVE-OR gate followed by an inverter. The output is high only when the input word has even parity.
### XOR gate
An EXCLUSIVE-OR gate. It has a high output only when the input word has odd parity. For a 2-input XOR gate, the output is high only when the inputs are different.