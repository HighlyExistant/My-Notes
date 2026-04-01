The probability of something occurring is simply a percentage $t\in[0,1]\subset\mathbb{R}$ value. The way we calculate the probability of something is by:
1. Grabbing the amount of states, or permutations, something can take. These will be denoted $S$.
2. Grabbing a subset of the states you are checking for the chance to happen. We will denote these $N$, such that $N\leq S$.
3. dividing both values $\frac{N}{S}$, which assures that it will not be greater than $1$.
We denote the probability of an event as $P(A)$.
## Example
Taking a simple coin flip, the states a coin can take are either heads or tails, which means the set of all possible states is $\{\text{heads}, \text{tails}\}$, so the count is $S=2$ possible states. The probability of it landing on heads then would be to take the subset only containing heads $\{\text{heads}\}$, getting the total count $N=1$ states, and then dividing. $\frac{1}{2}=0.5$. This means there's a $50\%$ chance of it landing heads.
# Logic Gates
Due to the fact we're dealing with subsets here, we can apply a similar logic as we would with [[Set Theory#Operations|set operations]].
# Laws
## Benford's Law
States that in distributions with large orders of magnitude, the probability for there to be a leading one is higher. The reasoning is that as you increase numbers, through the 1 digit numbers there will always be a larger than or equal to probability of there being a leading 1 and the probability for a leading $9$ will always be lesser than or equal:
### Example
$$\{1, 2, 3, 4, 5\}$$
This has a $\frac{1}{5}$ chance of getting a leading $1$ but as you increase the numbers: $$\{1, 2, 3, ..., 10, 11, 12\}$$
you now have a $\frac{4}{12}$ chance of getting a leading $1$.

# Combinations
## Choices
Given a set of choices $A$, the amount of options you have is $n(A)$. If You had multiple separate choices $A$ and $B$, then the amount of combined choices you have would be $n(A)\cdot n(B)$.
## Permutations
Given a set of items $A$, the amount of different ways to rearrange those items is $$n(A)!$$
If we wanted to put these permutations in a set amount of "slots", such as the permutations of fruits in a set amount of plates, we would use the generalized equation: $$\frac{n!}{(n-r)!}$$where $r$ is the amount of slots.
# Probability Distributions
A probability distribution graphs out the probabilities of every state. It has the property that: 
1. The sum of the probability distribution should be $1$.
2. No value of the probability distribution should be negative.
## Example
Denotes the probability of certain actions occurring. In the example given by [this khan academy video](https://www.youtube.com/watch?v=cqK3uRoPtk0) they use the probability distribution of the "number of 'heads' after 3 flips of a fair coin".
## Marginal Distribution
Is the probability distribution of a subset of variables, which only looks at one or a few variables, whilst ignoring the others. This focuses on the total information.
## Conditional Distribution
Distribution of one variable given something true of another variable. This focuses on the partial information.
# Expected Values
## Mean or Average
The mean, also known as the average of a distribution, is obtained through summing all the values in the distribution, and dividing by the count of total values in the distribution. For discrete functions, it is given by the sum: $$\overline{x}=\frac{1}{n}\sum_{i=1}^n{x_i}$$But for continuous functions it is given by the integral: $$\overline{f}=\frac{1}{b-a}\int_a^b{f(x)dx}$$
You'll notice that the $b-a$ term in the denominator is equivalent to the $n$ in the discrete form of the equation.

The ==**population mean**== is also sometimes designated by the symbol _mu_ $\mu$, so the mean of $x$ would me $\mu x$.
### Weighted Mean or Average
Given the probabilities of each possible outcome, you can get a weighted average which is $$\overline{x}=\frac{1}{W}\sum_{i=1}^n{x_i}w_i$$such that $w_i$ are the weights applies to $x_i$ and $W=\sum_{i=1}^n{w_i}$. The weighted mean then, considering that the sum of all the probabilities is $1$, we can remove the $\frac{1}{W}$ and it will give us the weighted mean equation: $$\overline{x}=\sum_{i=1}^n{x_i}w_i$$such that $w_i$ is the probability of the $x_i$.
## Median
The median is the value in the middle of the list. If the list splits evenly, and therefore there is no middle value, then the 2 values in the split will be averaged out.
## Mode
The mode is the value with highest frequency. 
