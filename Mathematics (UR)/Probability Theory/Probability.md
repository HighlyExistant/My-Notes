# Vocabulary
1. ==**Unordered**==: The order in which random events occur, does not matter.
2. ==**With Replacement**==: After a random event occurs, we do not eliminate it from the list of possible events $\Omega$.
3. ==**Independent**==: One trial and or event does not depend on the probability of another trial and or event.
4. ==**Without Replacement**==: After a random event occurs, we eliminate it from the list of possible events $\Omega$. This also makes events ==**Depenent**== on previous results.
# Probability Measures
These are [[Measure Theory#Measure|measures]] with a total mass equal to $1$. The [[Set Theory|set]] that contains our outcomes is called $\Omega$. We then have a measure $$P: A\to[0,1]\text{ s.t. }A\subseteq\mathcal{\Omega}$$where $\mathcal{\Omega}$ is the [[Measure Theory#$ Large sigma$ Algebra|sigma algebra]] of $\Omega$. The elements of a $\mathcal{\Omega}$ are called ==**events**==.
## Properties
1. $P(\Omega)=1$
2. $P(\emptyset)=0$
3. For $A,B\in \mathcal{\Omega}$, $P(A \cup B)=P(A)+P(B)$ if $A, B$ are [[Set Theory#Disjoint Sets|disjoint sets]] .
4. Has [[Measure Theory#$ sigma$-additive|sigma-additive property]].
## Definition
The definition of a probability measure is: $$P(A):=\frac{n(A)}{n(\Omega)}$$where $n$ is the function for the number of elements in a set.
# Conditional Probability
Two events are dependent if an event $B$ requires event $A$ to have occurred beforehand. We write this as $$P(A|B)$$and read it as "$A$ **given** $B$" (The $|$ means given) or "Probability of $A$ under the condition $B$". We can calculate this as the intersection of the two events, divided by the probability of $B$, or how many times has $A$ occurred, rather than not, assuming that $B$ has occurred: $$P(A|B)=\frac{P(A\cap B)}{P(B)}$$
The two events do not necessarily need to be dependent on one another.
## Bayes Theorem
This merely takes conditional probability and makes the denominators multiply the opposite sides: $$P(A|B)\cdot P(B)=P(B|A)\cdot P(A)$$

# Independence
==**Two events are independent**== if two sets $A, B\in \mathcal{\Omega}$ are disjoint sets. (The two events are mutually exclusive). We can say that the probability of $$P(A|B)=P(A)\text{ and }P(B|A)=P(B)$$


# Binomial Variable
This is such a variable which can be shown using a binomial distribution, as long as it satisfies the following conditions
1. A ==**fixed number**== of trials $n$
2. Trials are ==**independent**==.
3. Each trial can be ==**classified as either a success or a failure**==.
4. Each outcome has a ==**constant probability**== of $p$ and $1-p$.
## Binomial Distribution
Given a discrete set of events $\Omega=\{0, 1, 2, ..., n\}$ and a probability measure $P(A)$ such that $p$ is the probability of success and $1-p$ is the probability of failure. The binomial distribution gives you the probability of what are the chances of $k$ number of successes. This is given by the [[Factorization#Binomial Theorem|binomial theorem]], such that: $$P(\{k\})={n\choose k}p^k(1-p)^{n-k}$$
# Geometric Random Variables
These are variables which satisfy the following conditions
1. Trials are ==**independent**==.
2. Each trial can be ==**classified as either a success or a failure**==.
3. Each outcome has a ==**constant probability**== of $p$ and $1-p$.
Similar to the binomial variable, except that the number of trials is unknown. This is usually when we ask questions like "Number of rolls until you get $x$ on some random number generator". The reason why It's called a geometric random variable, is because its probability can be portrayed as a [[Sequences#Geometric Sequence|geometric sequence]], written as $$p(1-p)^{n-1}$$where $p$ is the probability of success, and $n$ is the number of trials. For you to need for example, $3$ tries to roll a $1$ on a $6$ sided die, then $p=\frac{1}{6}$ and $n=3$. For you to have gotten it on your third try, would mean that you had failed $2$ times and succeeded once.
## Mean and Standard Deviation
* [[What is Probability and Statistics#Mean or Average|The mean]] on these types of variables is simply the probability of success, so $\mu=p$.
* [[What is Probability and Statistics#Standard Deviation|The standard deviation]] is calculated as $\sigma=\frac{\sqrt{1-p}}{p}$.
# Law of large numbers
Given a large number of independent random samples  of $f(x)$ given a distribution $p(x)$, their average will approach the mean of $f(x)p(x)$. We write this down as: $$\lim_{n\to\infty}\sum_{i=1}^n{X_i}=\mu$$