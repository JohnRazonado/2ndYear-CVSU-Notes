## Probability Research
### Objectives
- Learn what probability research is 
- Use of scientific data via probability research
- Familiarize on the role of Probability in probability research
- Relate Probability and Statistical Inference (how do they work together)

### Applications (in IT)
- Probability is everywhere in computer science. 
	- In networks and systems, it is a key tool that allows us to predict performance, to understand how delay changes with the system parameters, and more. 
	- In algorithms, randomization is used to design faster and simpler algorithms than their *deterministic counterpart
- Probability is commonly used by data scientists **to model situations where experiments, conducted during similar circumstances, yield different results** (as in the case of throwing dice or a coin). It also has many practical uses in the business world
**Practical Application of Probability?**
Probability plays a vital role in the day to day life. In the weather forecast, sports and gaming strategies, buying or selling insurance, online shopping, and online games, determining blood groups, and analyzing political strategies

> ### Review
> 
> #### Mathematics
> - is the science that deals with the logic of shape, quantity and arrangement. 
> - Math is all around us, in everything we do.
> - It is the building block for everything in our daily lives, including mobile devices, architecture (ancient and modern), art, money, engineering, and even sports 
> #### Statistics
> - is a form of mathematical analysis that uses quantified models, representations and synopses for a given set of experimental data or real-life studies. 
> - Statistics studies methodologies to gather, review, analyze and draw conclusions from data.
> - Some statistical measures include the following
> 	- Mean
> 	- Regression Analysis
> 	- Variance
> 	- Analysis of Variance



### Use of Scientific Data
- Defined as information collected using specific methods for a specific purpose of studying or analyzing. 
- **Data** collected in a lab experiment done under controlled conditions is an example of **scientific data**. 
- When conducting research, we use the scientific method to collect measurable, empirical evidence in an experiment related to a hypothesis (often in the form of an if/then statement), the results aiming to support or contradict a theory.

#### Steps of the Scientific Method
1. Make an observation or observations.
2. Ask questions about the observations and gather information.
3. Form a hypothesis — a tentative description of what's been observed, and make predictions based on that hypothesis.
4. Test the hypothesis and predictions in an experiment that can be reproduced.
5. Analyze the data and draw conclusions; accept or reject the hypothesis or modify the hypothesis if necessary.
6. Reproduce the experiment until there are no discrepancies between observations and theory.


## Understanding Probability
> What is the probability of picking up an ace or a king from a deck of 52 cards?

It is the likelihood or chance of an event occurring.

![[Pasted image 20221117215300.png]]
- The probability of something which is certain to happen is 1.
- The probability of something which is impossible to happen is 0.
- The probability of something not happening is 1 minus the probability that it will happen.

![[Pasted image 20221117215355.png]]


### Types of Probability
#### Mathematical Probability
- If the probability of an event can be calculated before the actual happening of the event, that is, even before conducting the experiment or the resulting probabilities are definitive. 
- a.k.a Classical or Priori or Theoretical Probability 
#### Statistical Probability 
- If the probability of an event can be determined only after the actual happening of the event or outcome is measured by experiment.
- a.k.a Posterior or Empirical Probability.


### Single Events
**Example**

There are 6 marbles in a bag, 3 are red, 2 are green and 1 is blue. What is the probability of picking a green? 

The probability is the number of greens in the bag divided by the total number of marbles, i.e. 2/6 = 1/3

There is a bag full of colored beads, red, blue, green and yellow. Beads are picked out and replaced. Pedro did this 1000 times and obtained the following results: 
- Number of <span style="color:lightblue;">blue</span> beads picked out: 300
- Number of <span style="color:red ;"> red </span>beads: 200
- Number of <span style="color:green;">green</span> beads: 450
- Number of <span style="color:yellow;">yellow</span> beads: 50
1. What is the probability of picking a green bead?
2. If there are 100 beads in the bag, how many of them are likely to be yellow?
### Possibility Spaces
When working out what the probability of two things happening is, a probability/ possibility space can be drawn. For example, if you throw two dice, what is the probability that you will get: a) 8, b) 9, c) either 8 or 9

![[Pasted image 20221117215627.png]]
a) The black blobs indicate the ways of getting 8 (a 2 and a 6, a 3 and a 5, ...). There are 5 different ways. The probability space shows us that when throwing 2 dice, there are 36 different possibilities (36 squares). With 5 of these possibilities, you will get 8.


### Salient Points
Probability is simply how likely something is to happen. Whenever we're unsure about the outcome of an event, we can talk about the probabilities of certain outcomes—how likely they are. The analysis of events governed by probability is called statistics.

#### How do you calculate probability?
Divide the number of events by the number of possible outcomes. This will give us the probability of a single event occurring. In the case of rolling a 3 on a die, the number of events is 1 (there's only a single 3 on each die), and the number of outcomes is 6.

What is the probability of drawing a king or queen? First, the probability of drawing a king at the first draw is 4/52=1/13. Conditionally on a king being drawn on the first draw, the probability of drawing a queen at the second draw is 4/51. Therefore, probability of drawing sequence KQ is

**1/13 * (4/51 )= 4/663**

## Summary
![[Pasted image 20221117215801.png]]