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
## Cauchy Sequence
Is an infinite sequence whose elements get closer to one another (converges) as the sequence progresses. It's important to note that **all Cauchy sequences converge**, and all convergent sequences are Cauchy sequences. This is useful as the **criterion**, for convergence depends only on the terms of the sequence, not on some definition of convergence, which **uses a limit value** as well as the terms.

A sequence $\langle s_n \rangle$ is called a **Cauchy Sequence** if for every $\epsilon > 0$ there exists an $N \in \mathbb{N}$ such that for all $m, n \in \mathbb{N}$, if $m, n > N$,  then $|s_{n} - s_{m}| < \epsilon$.$^{\text{(1)}}$

What is the definition above saying? Well $\epsilon > 0$ is any arbitrary real number. At some point in the sequence at step $N \in \mathbb{N}$ all following numbers $m, n > N$, will have the property that $|s_{n}-s_{m}| < \epsilon$.
 
# RESEARCH THE CONSTRUCTION OF REAL NUMBERS USING CAUCHY SEQUENCES, AS WELL AS CAUCHY NUMBERS AND BANACH SPACES.

# References
(1) Found in Definition 3.6.1 at [Faculty at Buffalo State University](https://faculty.buffalostate.edu/cunnindw/417Sec3-6.pdf)

