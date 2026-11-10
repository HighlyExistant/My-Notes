# Big Int Representation
We represent big integers as a list of integers $a_0,...,a_n$ of $\omega$ possible combinations (which will be constant in application) for each $a_i$ and a sign bit $s\in \{-1, 0, 1\}$. Big ints can therefore be represented as an ordered triplet: $$(a_i,s,n)$$
The actual number representation is as follows. Let $\omega$ represent the total number of combinations (for standard integers it will be $2^{32}$), in this big integers will represent the number: $$\omega^{n}a_0+\omega^{n-1}a_1+...+\omega^0a_n$$
## Multiplication
Let $N=(a_N,s_N,n_N), M=(a_M,s_M,n_M)$ represent two big integers. Multiplication is performed by:
1. allocating a new integer $I$ such that:
	* $n_I=n_N+n_M$
	* $$s_I=\begin{cases}s_N:s_N=s_M\\0:s_N=0\vee s_M=0\\-1: s_N\neq s_M\neq 0\end{cases}$$
	* Finally $a_I$ will be retrieved from a fourier multiplication, obtained from $2^{N+M}$ terms.
# Big Decimal Representation
Big floats will allocate all their decimals. Instead of it being represented in floating point format, it will be treated similarly to an integer. For that reason let $I$ be the previously denoted big int representation. Decimals will also have an exponent $e$ which will denote where to put the decimal point. If $e=0$ then the number will be represented as: $$I.0$$
## Multiplication
