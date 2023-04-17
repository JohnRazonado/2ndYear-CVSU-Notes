- The *conditional probability* of an event **B** is the probability that the event will occur given the knowledge that an event **A** has already occurred.
- It is written as *P(B|A)* notation for the *probability of B given A*
## Objective
- This course intends to help learners develop their computing skills in probability statistics
- To enhance student's ability to solve practical problems using mathematical concepts.
- Understand the Conditional Probability
- Familiarize on Bayes' Rule/Theorem
- Application of Bayes' Rule

## Independent and Dependent Probability
### Independent Probability
Events can be "Independent", meaning each event is not affected by any other events.

- Each toss of a coin is a perfect isolated thing.
	- What it did in the past will not affect the current toss. The chance is simply 1-in-2, or 50%, just like ANY toss of the coin. 
	- So each toss is an **Independent Event**

### Dependent Probability
Events that is affected by previous events

- 2 blue and 3 red marbles are in a bag. What are the chances of getting a blue marble?
	- The chance is 2 in 5 But after taking one out the chances change!
	- So the next time: if we got a red marble before, then the chance of a blue marble next is 2 in 4
	- If we got a blue marble before, then the chance of a blue marble next is 1 in 4.

## Formula
![[Pasted image 20230203011200.png]]

![[Pasted image 20230203011213.png]]


## Bayes' Rule/Theorem
### Thomas Bayes
- named after 18th-century British mathematician Thomas Bayes
- a mathematical formula for determining conditional probability. The theorem provides a way to revise existing predictions or theories (update probabilities) given new or additional evidence.
- In finance, Bayes' theorem can be used to rate the risk of lending money to potential borrowers.

### Key takeaways
- Bayes' Theorem allows you to update predicted probabilities of an event by incorporating new information. 
- It is often employed in finance in updating risk evaluation. 
- Bayes' theorem is also called Bayes' Rule or Bayes' Law and is the foundation of the field of Bayesian statistics.

### Formula


![[Pasted image 20230203011320.png]]

>  P (A|B) is also called **Conditional Probability of A given B**

### Application
- Bayes' theorem can be used to determine the accuracy of medical test results by taking into consideration how likely any given person is to have a disease and the general accuracy of the test. 
- Bayes' theorem relies on incorporating prior probability distributions in order to generate posterior probabilities. 
- **Prior probability**, in Bayesian statistical inference, is the probability of an event before new data is collected. This is the best rational assessment of the probability of an outcome based on the current knowledge before an experiment is performed. 
- **Posterior probability** is the revised probability of an event occurring after taking into consideration new information. Posterior probability is calculated by updating the prior probability by using Bayes' theorem. In statistical terms, the posterior probability is the probability of event A occurring given that event B has occurred.

## More probability
![[Pasted image 20230203011630.png]]
>Bayes' theorem shows that even if a person tested positive in this scenario, it is actually much more likely the person is not a user of the drug.


![[Pasted image 20230203011510.png]]
![[Pasted image 20230203011543.png]]
> Although factory B produces 50% of the bulbs, the probability that the selected (defective) bulb comes from this factory is low because the bulbs produced by this factory have low probability (1%) of being defective.

