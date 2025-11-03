Every positive integer can be written as a product of primes, as an example the number $12$ can be written as:
$$
	2^2\cdot3^1\cdot5^0\cdot7^0\cdot11^0...
$$
And is called the ==**canonical factorization**==. The number $1$ can then be represented as all the prime numbers raised to the zero, multiplied by each other, equal to $1$.
The tau function $\tau(n)$ is supposed to give you the number of factors of a number. As an example we can have the number $16$, who's factors are $[1, 2, 4, 8, 16]$, well $\tau(16)=5$, as there are 5 factors in the number. The sigma function $\sigma(n)$ is just the sum of these divisors $\sigma(16)=1+2+4+8+16=31$. The way we calculate this $\tau$ function is by:
1. Step 1: Determining the prime factorization of the numbers. Ej. $72=2^3*3^2$
2. Make an infinite product of how many times each prime number appears $$\prod{(p_n+1)}$$ such that $p_n$ is the number of times each prime appears in the prime factorization. In the case of $72$, then $\tau(72)=(3+1)(2+1)(0+1)(0+1)...=12$ which if we look at the factor tree of $72=[1, 2, 3, 4, 6, 8, 9, 12, 18, 24, 36, 72]$ which is a total of 12 factors.
# Vocabulary
* $D$: [[Algebraic Structures#Integral Domain|Integral Domain]]
* $D^{*}$: Set of nonzero elements of $D$, basically $D-\{0\}$.
* $U(D)$: [[Algebraic Structures#Rings|Group of units]] of $D$.
* $D^{\#}$: Set of [[Algebraic Structures#Rings|nonzero nonunit]] elements of $D$.
* $\tau$: A [[Relations#Symmetric|symmetric relation]] on $D^{\#}$.
	* We say that $\tau$ is ==**associate preserving**== if for $a, b, b' \in D^{\#}$ with $b \sim b', a\tau b\Rightarrow a\tau b'$ and $b\tau a\Rightarrow b'\tau a$  
* $|_{\tau}$ is used to denote something as a $\tau$-factor. ej. $a_i|_{\tau}a$ means that $a_i$ is a $\tau$-factor of $a$.
* $*$ is the symbol to denote a $\tau$-product.
* ==**Definition 1**==: $\tau$-factorization of element $a\in D^{\#}$  is an expression $a=\lambda a_1 *...* a_k$ where $a_j \in D^{\#}$ and $\lambda \in U(D)$ and for any $i\neq j, a_i\tau a_j$.
* ==**Definition 2**==: $\tau$-factorization for $a\in D^{\#}$, where $D$ is an integral domain and $\tau$ a relation on $D^{\#}$, we define $$a=\lambda a_1 ... a_n$$ such that $n \geq 1$
	* $\lambda \in U(D)$
	* $a_i \in D^{\#}$ 
	* $a_i \tau a_j$ for each $i\neq j$
# Example
* Let $\mathbb{Z}$ be the set of integers
* $D=(\mathbb{Z}, *)$ be our integral domain. 
* $U(D)=\{1\}$
* $D^{\#}$ would then contain in its objects $\mathbb{Z}-\{0, 1\}$.
* $\tau$ will be the equivalence relation $[a]_4$ a $mod(4)$ on the integers.
* $4 |_{\tau} 32$ and so is $8 |_{\tau} 32$  
* $\lambda=1$
* $32=1(4*8)$
