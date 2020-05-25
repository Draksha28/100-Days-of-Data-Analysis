##  ** Informational Edge ** ##

- This module gives methods for quantifying exactly the reduction in uncertainty 
      or informational content of all of those different types of scenarios.

## ** Probability And Entropy ** ##

- Our basic definitions about probability, that probabilities need to be less than or equal to one. 
That the sum of all probabilities for a given probability distribution need to sum to one and that
 the individual events x of i need to be exhaustive, meaning they sum to one. But they also need to be mutually exclusive. 
Okay and, what we said before, which is that certainty is represented by zero and one. 
And all other states are represented by values greater than zero and less than one.
- Entropy written H(x) for the random variable, is a measure of the uncertainty of the whole probability distribution measured in bits of information.
- Entropy is calculated as follows. It's the sum of each probability,times.The log to the base two of one over that probability.
         H(X) = ? pi log2(1/pi)
- It turns out that if we have a uniform distribution with n possible outcomes the entropy is equal to log n.
 That's also the maximum entropy for a discrete distribution.

* Entropy Of Guessing Game * 

- If an individual chooses a number between any two numbers (as b/w 0-100); For us to find the number we ask questions that can eliminate the possibilities.
   EX:- If the number chosen is 24; we first is the number below 50 or above...(Similar way)
     The number of bits required to encode 100 possible states. Or, to put it another way, 2 to the 6.64 equals 100. Or log to the base 2 of 100 equals 6.64.
- The concept of conditional entropy,which is equal to the probability that y equals y 1, times the entropy of x, 
given that y equals y1 plus the probability that y equals y2 times the entropy of x, given that y equals y2.
- H(X)-H(X/Y) = Mutual Information [ I(X,Y)]
- The definition of independence is that the joint distribution is equal to the product distribution. [ e=ac; f=ad; g=bc; h=bd ]  [ I(X;Y) = 0]
- Mutual Information is always greater than or equal to 1.

 * The Monty Hall Problem *

- Suppose you're on a game show, and you're given the choice of three doors: 
Behind one door is a car; behind the others, goats. You pick a door, say No. 1, and the host, 
who knows what's behind the doors, opens another door, say No. 3, which has a goat. 
He then says to you, "Do you want to pick door No. 2?" Is it to your advantage to switch your choice?
Under the standard assumptions, contestants who switch have a 2/3 chance of winning the car, while contestants who stick to their initial choice have only a 1/3 chance.
       P(X/Y) P(Y) = P(XnY)
   Baye's Theorem:-  P(X/Y) = P(Y/X)P(X) / P(Y/X)P(X) + P(Y/-X)P(-X)

