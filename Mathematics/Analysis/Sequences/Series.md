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