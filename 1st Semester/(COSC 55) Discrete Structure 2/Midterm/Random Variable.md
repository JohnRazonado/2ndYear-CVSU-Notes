![[Pasted image 20221117215835.png]]

%%## Objectives
- Understand Random variable, Discrete and continuous random variables
- Familiarize on Random phenomena, trial, and event
- Application of Random variable and Probability distribution%% 

# Random Variable
- “A random variable is a numerical description of the outcome of a statistical experiment.” 
- “A Random Variable is a set of possible values from a random experiment.”

![[Pasted image 20221117220613.png]]

Thus, We have an experiment (such as tossing a coin) 
We give **values** to each event
The **set of values** is a **Random Variable**

### Discrete vs Continuous
- A **random variable** that may assume only a finite number or an infinite sequence of values is said to be **discrete**; 
- One that may assume any value in some interval on the real number line is said to be **continuous**.
- For instance, a random variable representing the number of automobiles sold at a particular dealership on one day would be discrete.
- While a random variable representing the weight of a person in kilograms (or pounds) would be continuous.

## Random Variable vs. Algebra Type Variable

- We use a capital letter, like X or Y, to avoid confusion
	- Example: X = {0, 1, 2, 3}
	- X could be 0, 1, 2, or 3 **randomly**
	- Having a **[[Sets and Logic#Set|set]]** of values
- Not Like an Algebra Variable 
- In Algebra a variable, like x, is an unknown value:
	- Example: x + 2 = 6
	- we can find that x = 4

## Sample Space
A Random Variable's set of values is the Sample Space

### Example:
1. Throw a die once
Random Variable X = "The score shown on the top face".

X could be 1, 2, 3, 4, 5, or 6

2. Old Faithful erupts every 91 minutes. You arrive there at random and wait for 20 minutes... what is the probability you will see it erupt?
	- Compute it base on 20 minutes out of 91 minutes:
	- p = 20/91 = 0.22 (2 decimals)

## Range Of Values
We could also calculate the probability that a random variable takes on a range of values.

### Example: Rolling two dice
What is the probability that the sum of the scores is 5, 6, 7, or 8?

In other words: What is **P(5 $\leq$ X $\leq$ 8 )**?
$$P(5 \leq X \leq 8) = P(X=5) + P(X=6) + P(X=7) + P(X=8)$$
$$= (4+5+6+5)/36$$
$$= 20/36$$
$$=5/9$$

## The Normal Distribution

- The most important continuous distribution is the **[Standard Normal Distribution](https://www.mathsisfun.com/data/standard-normal-distribution.html)**
- It is so important the **Random Variable** has its own special letter **Z**.
- The graph for Z is a symmetrical bell-shaped curve:
- There are many cases where the data tends to be around a central value with no bias left or right, and it gets close to a "Normal Distribution" like this:
![[Pasted image 20221117220929.png]]
> Many things closely follow a Normal Distribution
> - heights of people 
> - size of things produced by machines
> - errors in measurements
> - blood pressure
> - marks on a test


We say the data is "normally distributed":

![[Pasted image 20221117221034.png]]
The **Normal Distribution has: mean = median = mode**
- symmetry about the center
- 50% of values less than the mean and 50% greater than the mean

## Salient Points
- A Random Variable is a set of possible values from a random experiment.
- The **set of possible values** is called the <u>Sample Space</u>.
- A Random Variable is given a **capital letter**, such as X or Z.
- Random Variables **can be discrete or continuous**. 
- An important example of a continuous Random variable is the Standard Normal variable, **Z**.
