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
Is an i``nfinite sequence whose elements get closer to one another (converges) as the sequence progresses. It's important to note that **all Cauchy sequences converge**, and all convergent sequences are Cauchy sequences. This is useful as the [[Rhetoric#Vocabulary|criterion]], for convergence depends only on the terms of the sequence, not on some definition of convergence, which **uses a limit value** as well as the terms.

A sequence $\langle s_n \rangle$ is called a **Cauchy Sequence** if for every $\epsilon > 0$ there exists an $N \in \mathbb{N}$ such that for all $m, n \in \mathbb{N}$, if $m, n > N$,  then $|s_{n} - s_{m}| < \epsilon$.$^{\text{(1)}}$

What is the definition above saying? Well $\epsilon > 0$ is any arbitrary real number. At some point in the sequence at step $N \in \mathbb{N}$ all following numbers $m, n > N$, will have the property that $|s_{n}-s_{m}| < \epsilon$, meaning that it has converged.
 
# RESEARCH THE CONSTRUCTION OF REAL NUMBERS USING CAUCHY SEQUENCES, AS WELL AS CAUCHY NUMBERS AND BANACH SPACES.

# References
(1) Found in Definition 3.6.1 at [Faculty at Buffalo State University](https://faculty.buffalostate.edu/cunnindw/417Sec3-6.pdf)

