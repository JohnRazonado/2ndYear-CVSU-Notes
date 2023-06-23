## Half Adder and Full Adders Applications
1. **ALU** - essential components of CPUs, responsible for logical operations. Half adders and full adders are key building blocks to carry out addition and subtraction on binary numbers
2. **Binary Counters** - utilizes full adders to increment binary values.
3. **Data transmission and error detection**
4. **Multiplexers and Demultiplexers**
5. **Binary Encoder and Decoders**
6. **Parallel Adders/Subtractors**

## Half Adder
- Basic digital circuit
- Add two single-bit binary -> two outputs: **sum** and **carry**
- Doesn't consider any carry input from previous stages

![[Pasted image 20230623133158.png]]

## Full Adder
- Advance circuit
- Adds three single-bit binary (input A and B and a carry input [Cin]) -> Sum and Carry [Cout]  
![[Pasted image 20230623135717.png]]

## Encoder and Decoder
Digital circuits used in digital systems to convert data between different formats or representations.

### Encoder
- combinational circuit that converts input signal or data into coded output based on specific encoding scheme
- multiple input lines, fewer output lines
- purpose is to represent input data into more compact or efficient form

![[Pasted image 20230623144518.png]]

#### Key Components of Encoder
- **Input lines** - multiple input lines, and each input combination represents unique code or symbol
- **Output lines** - typically fewer than the number of input lines
- **Encoding Scheme** - encoders follow specific encoding scheme to map input data to the corresponding output.
	- Common encoding schemes
		- Binary encoders
		- Gray code encoders
		- BCD (Binary-Coded Decimal) encoders.
- **Function** - Reduce the number of output lines required to represent input data. Giving out compact representation of input, suitable for transmission and storage purposes.

#### Application of Encoders
- **Data Compression** - Like Huffman coding and run-length encoding. Convert input data into compressed form, reducing size and facilitating efficient storage and transmission.
- **Digital communication** - They're utilized in digital communication systems for:
	- Data modulation
	- Error detection
	- Error correction
	- Convert digital data into specific modulation schemes
- **Multiplexing** - Where multiple data streams are combined into a single channel for transmission. 
	- Encoder assign unique codes or symbols to each input stream to be distinguished at the receiving end.
- **Address Encoding** - Employed in memory systems and microprocessors to convert memory addresses into encoded forms.
- **Remote Control Systems** - Utilized in remote control system to encode button presses or commands into specific codes that can be transmitted wirelessly.


### Decoder
- combinational circuit that performs reverse operation of encoder
- Takes encoded input and converts back to its original format or representation.
- Typically fewer input lines and multiple output lines.

#### Key characteristics of Decoder
- **Input lines** - smaller no. of input lines. Cary encoded data or control signals
- **Output lines** - multiple output lines, each output line represents unique combination of input values. Provide the decoded representation of input data.
- **Decoding scheme** - decoder follows specific decoding scheme to map input codes to corresponding output values. Inverse of the encoding scheme used by encoder.
- **Function** - retrieve original data or control signals from the encoded input. Used to restore original format of data or enable specific operations.


#### Applications of Decoders
- **Digital-to-Analog Conversions** - Used in digital-to-analog converters (DACs) to convert digital signals -> analog voltage or current outputs.
- **Display Systems** - Like seven-segment displays, to decode input codes and drive the appropriate segments or elements to display numeric or alphanumeric characters.
- **Address Decoding** - employed in memory systems and microprocessors to decode memory addresses and enable specific memory locations to read/write operations.
- **Data Demultiplexing** - This separate multiplexed data streams. Basically decode input codes and route data to appropriate output channel or destination (made by a multiplexer).
- **Error Detection and Correction** - Such as parity checking and error-correcting codes. They decode received codes and check for errors, allowing detection and correction of transmission errors.

![[Pasted image 20230623150801.png]]