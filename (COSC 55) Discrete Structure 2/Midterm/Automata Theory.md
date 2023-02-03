- One of the foundation of Computer Science
- From the Greek word "αὐτόματος" means "self-acting, self-moving"
- Deals with the logic of computation with respect to simple machines, referred to as automata.
- **Automatons** are abstract models of machines that perform computations on an input by moving through a series of states or configurations. 
- At each state of the computation, a transition function determines the next configuration on the basis of a finite portion of the present configuration. As a result, once the computation reaches an accepting configuration, it accepts that input. The most general and powerful automata is the **[[Computability Theory#Turing Machine|Turing machine]]**.
- Compilers and parsers sits in this automata abstraction.

<!--%%The major objective of automata theory is to develop methods by which computer scientists can describe and analyze the dynamic behavior of discrete systems, in which signals are sampled periodically. The behavior of these discrete systems is determined by the way that the system is constructed from storage and combinational elements. Characteristics of such machines include:%%
-->

**Inputs:** assumed to be sequences of symbols selected from a finite set I of input signals. Namely, set I is the set {x1, x,2, x3... xk} where k is the number of inputs.
**Outputs:** sequences of symbols selected from a finite set Z. Namely, set Z is the set {y1, y2, y3 ... ym} where m is the number of outputs. 
**States:** finite set Q, whose definition depends on the type of automaton

![[Pasted image 20221118214355.png]]

<!--%%Simply stated, automata theory deals with the logic of computation with respect to simple machines, referred to as automata. Through automata, computer scientists are able to understand how machines compute functions and solve problems and more importantly, what it means for a function to be defined as computable or for a question to be described as decidable .%%

%%### Trivia 
The exciting history of how finite **automata** became a branch of computer science illustrates its wide range of applications. 

The first people to consider the concept of a finite-state machine included a team of biologists, psychologists, mathematicians, engineers and some of the first computer scientists. They all shared a common interest: to model the human thought process, whether in the brain or in a computer.%%

![[Pasted image 20221117204905.png]]

-->