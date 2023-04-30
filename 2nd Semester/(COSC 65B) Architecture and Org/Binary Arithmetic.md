- Individual digits of a binary number are referred to as bits
	- Each bit represents a power of two

01011 = 0 \* 2<sup>4</sup>  \* 1 \* 2<sup>3</sup> + 0 \* 2<sup>2</sup> + 1 \* 2<sup>1</sup> + 1 \** 2<sup>0</sup> = 11
00010 = 0 \* 2<sup>4</sup> + 0 \* 2<sup>3</sup> + 0 \* 2<sup>2</sup> + 1 \* 2<sup>1</sup> + 0 \* 2<sup>0</sup> = 2

|Binary Addition| Equivalent Decimal Addition|
|---|---|
|![[Pasted image 20230405142344.png]]|![[Pasted image 20230405142400.png]]|

|Binary Multiplication| Equivalent Decimal Multiplication|
|---|---|
|![[Pasted image 20230405142811.png]]|![[Pasted image 20230405142821.png]]|

### Two's Complement
- Representation of signed binary numbers
- Leading bit is a sign bit
	- Binary number with leading 0 is positive
	- Binary number with leading 1 is negative
- Magnitude of positive numbers is just the binary representation
- Magnitude o negative numbers is found by
	- Complement the bits
	- Replace all the 1's with 0's, and all the 0's with 1's
	- Add one to the complemented number
- The carry in the most significant bit position is thrown away when performing arithmetic

#### Sample
- Performing two's complement on the decimal 7 to get -7
	- Using a five-bit representation

![[Pasted image 20230405143303.png]]


- Computing 8 - 7 using a two's complement representation with five-bit numbers

8 - 7 = 8 + (-7) = 1

![[Pasted image 20230405143448.png]]