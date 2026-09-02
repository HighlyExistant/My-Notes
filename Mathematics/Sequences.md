A sequence is a set of numbers which follow a particular pattern or rule to get from one term to the next. To define a sequence we choose a variable and an index to identify which step of the sequence we are in. As an example we can use the Fibonacci sequence:
$$
	F_{0}=0
$$
$$
	F_{1}=1
$$

$$
	F_{n}=F_{n-1}+F_{n-2} \text{ for }n>1
$$
## Grades of a Sequence
The grade of a sequence is the number of initial values used. More specifically you try to find the least amount of initial values. For example, the Fibonacci sequence is degree 2, since it uses 2 initial values.
## Sequences as Functions
We can describe a sequence as a function which takes in natural numbers and produces some other number:  $$S:\mathbb{N}\to X$$
You can also represent it via finite sets, since they are countable, such as: $$S:\{1,2,...,n\}\to X$$

## Arithmetic Sequence
These sequences are of the form $a_1+(n-1)d$ where:
* $a_1$ is the first term in the sequence
* $d$ is the difference from one element to another
* $n$: Is the nth term in the sequence.
A sum in an arithmetic sequence is presented as:$$
S_n=\frac{n}{2}(2a_1+(n-1)d)
$$ or $$
S_n=\frac{n}{2}(a_1+a_n)
$$
## Geometric Sequence
A geometric sequence is of the form $a_1r^{n-1}$ where: 
* $a_1$ is the first term in the sequence
* $r$ is the common ratio from one element to another and $n$ is the term in the sequence.
* $n$: Is the nth term in the sequence.
The nth value is given by $$
	S_n=a_1(\frac{1-r^n}{1-r})
$$
### Convergence on Infinite Sum
$$
	\sum_{i=1}^{\infty}{ar^{i-1}}=a+ar+ar^2...=\frac{a}{1-r}
$$

## Cauchy Sequence
Is an infinite sequence whose elements get closer to one another (converges) as the sequence progresses. It's important to note that **all Cauchy sequences converge**, and all convergent sequences are Cauchy sequences. This is useful as the [[Rhetoric#Vocabulary|criterion]], for convergence depends only on the terms of the sequence, not on some definition of convergence, which **uses a limit value** as well as the terms.

A sequence $\langle s_n \rangle$ is called a **Cauchy Sequence** if for every $\epsilon > 0$ there exists an $N \in \mathbb{N}$ such that for all $m, n \in \mathbb{N}$, if $m, n > N$,  then $|s_{n} - s_{m}| < \epsilon$.$^{\text{(1)}}$

What is the definition above saying? Well $\epsilon > 0$ is any arbitrary real number. At some point in the sequence at step $N \in \mathbb{N}$ all following numbers $m, n > N$, will have the property that $|s_{n}-s_{m}| < \epsilon$, meaning that it has converged.
 
# Series
These are infinite sums, denoted as: $$\sum_{i=1}^\infty a_i$$which can be rewritten as: $$\lim_{n\to\infty}\sum_{i=1}^n a_i$$
## Types of Series
### Telescopic Series
$$\sum_{k=1}^n{\frac{1}{k(k+1)}}=1$$
### Geometric Series
$$S_n=\sum_{k=1}^n{ar^{k-1}}=a(\frac{1-r^n}{1-r})$$
That said, for $|r|<1$: $$\lim_{n\to\infty}S_n=\frac{a}{1-r}$$
### Alternating Series
These are of the form: $$S_n=\sum_{i=1}^\infty(-1)^{n-1}a_n$$
# Testing for Convergence
In the previous sections we've seen how to get the exact value of a convergent sequence, but sometimes we just want to check if a series converges, in which case we can use estimation techniques to acquire the value. This is especially useful for series which are complicated and might not have an exact solution.
## Comparison Tests
Let $a_n$ be a sequence, and $b_n$ be a sequence such that $\forall n$ $b_n\geq a_n$. Then if a series on $b_n$ converges, so does a series on $a_n$. This is because the sum of $b_n$ is greater than $a_n$. 
## Integral Test
Let $a_n$ be a sequence with series $S_n$, then $$S_n\leq \int_1^\infty{a_x}dx$$
This means that if $\int_1^\infty{a_x}dx$ converges, so does $S_n$.
## Absolute Convergence
Let $a_n$ be a sequence, and $|a_n|$ be the absolute value of $a_n$, then if $|a_n|$ converges, $a_n$ also converges. Important to note that if $|a_n|$ diverges, that does not mean that $a_n$ diverges. When $|a_n|$ diverges and $a_n$ converges, it is conditionally convergent. 
## Test for Alternating Sequences
Given an alternate sequence $S_n$ with sum over $a_n$ if $$a_n\geq a_{n+1}> 0$$ ($a_n$ is monotonically decreasing) and $$\lim_{n\to \infty}a_n=0$$ then the series is convergent.
# RESEARCH THE CONSTRUCTION OF REAL NUMBERS USING CAUCHY SEQUENCES, AS WELL AS CAUCHY NUMBERS AND BANACH SPACES.

# References
(1) Found in Definition 3.6.1 at [Faculty at Buffalo State University](https://faculty.buffalostate.edu/cunnindw/417Sec3-6.pdf)
