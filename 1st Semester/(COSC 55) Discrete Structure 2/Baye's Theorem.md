
## Conditional Probability 
Imagine a couple with two children, each of whom is equally likely to be a boy or a girl. Now suppose you are given the information that one is a boy. What is the probability that the other child is a boy? 

Figure 9.9.1 shows four equally likely combinations of gender for the children. You can imagine that the first letter refers to the older child and the second letter to the younger. Thus the combination BG indicates that the older child is a boy and the younger is a girl.

![](Pasted%20image%2020221106225306.png)

There are three combinations where one of the children is a boy, and in one of these three combinations the other child is also a boy. Given that you know one child is a boy, only these three combinations could be the case. So you can think of the set of those outcomes as a new sample space with three elements, all of which are equally likely. Within the new sample space, there is one combination where the other child is a boy. Thus, it would be reasonable to say that the likelihood that the other child is a boy, given that at least one is a boy, is 1/3 = 33 1/3%. Given that the original sample space contained four outcomes note that the following computation gives the same result: 

![](Pasted%20image%2020221106225459.png)

> Continuation on Page 666 | 689 of the book **Susana Epp. Discrete Mathematics with Applications**

A pair of fair dice, one blue and the other gray, are rolled. What is the probability that the sum of the numbers showing face up is 8, given that both of the numbers are even?

**Solution** The sample space is the set of all 36 outcomes obtained from rolling the two dice and noting the numbers showing face up on each. As in Section 9.1, denote by ab the outcome that the number showing face up on the blue die is a and the one on the gray die is b. Let A be the event that both numbers are even and B the event that the sum of the numbers is 8. Then *A* = {22, 24, 26, 42, 44, 46, 62, 64, 66}, *B* = {26, 35, 44, 53, 62}, and A ^ B = {26, 44, 62}. Because the dice are fair (so all outcomes are equally likely), *P(A)* = 9/36, *P(B)* = 5/36, and P(A ^ B) 5 3/36. By definition of conditional probability.
![](Pasted%20image%2020221107105239.png)

## Main Baye's Theorem

Suppose that one turn contains 3 blue and 4 gray balls and a second urn contains 5 blue and 3 gray balls. A ball is selected by choosing one of the urns at random and then picking a ball at random from that urn. If the chosen ball is blue, what is the probability that it came from the first urn? 

This problem can be solved by carefully interpreting all the information that is known and putting it together in just the right way. Let A be the event that the chosen ball is blue, B1 the event that the ball came from the first urn, and B2 the event that the ball came from the second urn. Because 3 of the 7 balls in urn one are blue, and 5 of the 8 balls in urn two are blue.

![](Pasted%20image%2020221107105851.png)

And because the urns are equally likely to be chosen,

![](Pasted%20image%2020221107110106.png)

Moreover, by formula (9.9.2),

![](Pasted%20image%2020221107110130.png)

![](Pasted%20image%2020221107110148.png)

Thus, if the chosen ball is blue, the probability is approximately 40.7% that it came from the first turn. 

The steps used to derive the answer in the previous example can be generalized to prove Bayes’ theorem. (See exercises 9 and 10 at the end of this section.) Thomas Bayes was an English Presbyterian minister who devoted much of his energies to mathematics. The theorem that bears his name was published posthumously in 1763. The portrait at the left is the only one attributed to him, but its authenticity has recently come into question.

![](Pasted%20image%2020221107110214.png)

### Application

Most medical tests occasionally produce incorrect results, called false positives and false negatives. When a test is designed to determine whether a patient has a certain disease, a false positive result indicates that a patient has the disease when the patient does not have it. A false negative result indicates that a patient does not have the disease when the patient does have it. When large-scale health screenings are performed for diseases with relatively low incidence, those who develop the screening procedures have to balance several considerations: the per-person cost of the screening, follow-up costs for further testing of false positives, and the possibility that people who have the disease will develop unwarranted confidence in the state of their health. Consider a medical test that screens for a disease found in 5 people in 1,000. Suppose that the false positive rate is 3% and the false negative rate is 1%. Then 99% of the time a person who has the condition tests positive for it, and 97% of the time a person who does not have the condition tests negative for it. (See exercise 4 at the end of this section.) a. What is the probability that a randomly chosen person who tests positive for the disease actually has the disease? b. What is the probability that a randomly chosen person who tests negative for the disease does not in fact have the disease?