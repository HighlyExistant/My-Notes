# Introduction
* Person that's teaching me: Dr. Jose Emilio.
# Preliminary
1. [[Set Theory]]
2. [[Sequences]]
# The Characteristic Polynomial of a Sequence
The way we find the characteristic polynomial of a sequence is by the given number of initial values $k$, where $a_n$ are the initial values. We define it by $$a_n=c_1a_{n-1}+c_2a_{n-2}+...+c_ka_{n-k}$$where $c_1,...,c_k$ are constants. It is called the linear homogeneous equation with constant coefficients. To try and find a close formed solution of the form $a_n=r^n$, we utilize the characteristic polynomial of the form: $$p(r)=r^k-c_1r^{k-1}-c_2r^{k-2}-...-c_k$$

# The Characteristic Function
## Definition
Given a set $A$, then the characteristic function $f_A(x)$ is: $$f_A(x)=\begin{cases}x\in A:1\\x\not\in A: 0\end{cases}$$
## Properties
Given a universal set $U$ then the characteristic function has the following properties.
1. $f_{A\cap B}(x)=f_A(x)f_B(x)$
2. $f_{A\cup B}(x)=f_A(x)+f_B(x)-f_A(x)f_B(x)$
3. $f_{A\oplus B}(x)=f_A(x)+f_B(x)-2f_A(x)f_B(x)$
4. $f_\overline{A}(x)=1-f_A(x)$
# String or Words
A string is a finite [[Sequences|sequence]] of symbols, be it letters, numbers, etc. This can be represented for example as:
	abcdefg
or
	1234567
In abstract algebra this is called a ==**word**==, in computer science it is called a ==**string**==.
## Alphabets
It is a set, such that their elements are interpreted as symbols:
### Examples
* $A^*$: The set of all strings which could be formed with the letter $A$, for example: $a\in A$, $aa\in A$, etc. For such a reason, $|A^*|=\infty$.
* Given an array $|A|=m$, there are $m^n$ elements $a\in A$ s.t. $|a|=n$.
* The cardinality of $|A^*|$ would then be $1+\sum^n_{n=1}m^n$ which diverges due to $m\geq 1$. (The plus 1 is for the empty string)
## Empty String
The empty string of symbols is represented by the symbol $\Lambda$. 
## Operations
### Concatenation
Given a string $w_1=s_{11} s_{12}...s_{1m}$, and $w_2=s_{21}s_{22}...s_{2m}$. the concatenation would be represented as: $$w_1w_2=w_1=s_{11} s_{12}...s_{1m}s_{21}s_{22}...s_{2m}$$and this new string would have $|w_1w_2|=n+m$
* My professor utilized in their thesis the symbol $\odot$ for concatenation.
#### Identity
The identity of concatenation is the empty string $\Lambda$: $$\Lambda A=A\Lambda=A$$
#### Examples
Given the set of English letters, and a space, we could represent the sentence:
1. $w_1=\text{I}$ $w_2=\text{eat}$ $w_3=\text{pasta}$ $s= \text{ }$ we would get: $$w_1sw_2sw_3=\text{I eat pasta}$$
## Regular Expressions
A regular expression over $A$ is a string constructed via $()$, $\vee$ $*$, $\Lambda$.
* REI. $\Lambda$ is a regular expression
* RE2. If $x\in A$, then $x$ is a regular expression
* RE3. If $\alpha$ and $\beta$ are norma expressions, then $\alpha\beta$ is a regular expression.
* RE4. If $\alpha$ and $\beta$ are regular expressions, then $\alpha \vee\beta$ is a regular expression.
* RE5. If $\alpha$ is a regular expression then $(a)^*$ is also a regular expression.
### Or Symbol
The regular expression $a\vee b$ represents a string which can be either $a$ or $b$.
### Asterisk Symbol
The regular expression $(a)^*$ is used to represent all possible expressions which can be formed via the string $a$.
# Arrays
It is a [[Sequences|sequence]] of positions, in which every position has an element. This is usually represented as `S[n]`.
# Properties of Integers
## Well Ordering of Integers
for any nonempty $S\subseteq \mathbb{Z_{>0}}$, there exists $r\in S$ s.t. $r\leq s$ $\forall s\in S$.
## Algorithm of Divisibility
For $m,n\in \mathbb{Z}$ and $n>0$ then $\exists ! q,r$ s.t.  
## Divisibility Rules
We say $a|b$ if there exists $k\in\mathbb{Z}$ s.t. $b=ak$.
### Properties of Divisibility
For $a,b,c\in\mathbb{Z}$:
1. $a|b\vee a|c\Rightarrow a|bx+cy, \forall x,y\in \mathbb{Z}$ it also implies $a|b+c$ and $a|b-c$
2. $a|b\wedge a|c\Rightarrow a|bc$.
3. [[Mathematics/Pure Math/Relations/Relations#Transitive|transitive]]: $a|b\vee b|c\Rightarrow a|c$.
### Testing for Primes
When trying to find whether a given number is prime, we can test divisors of some supposedly prime $N$, such that $a|N\Rightarrow a\leq \sqrt{N}$, then we can reduce the number of checks we do from $N$ to $\sqrt{N}$.
#### Reasoning
Suppose $N$ is composite, then $N=ab$, with $1<a<N$ and $1<b<N$. Suppose then that both $a>\sqrt{N}$ and $b> \sqrt{N}$, then $ab>N$, but $N=ab$, therefore $N$ cannot be composite.
### Theorems
For all $n>1$
1. $n$ is prime or
2. $n=p_1p_2...p_k$ for some $p_1,p_2,...,p_k$ primes.
### Greatest Common Divisor
The $\gcd(a,b)$ function denotes the greatest common divisor between two whole numbers, it maps: $$\gcd:\mathbb{Z}^2\to\mathbb{Z}_{>}$$returning their greatest common factor.
#### Properties
* $\gcd(a,1)=1$
* $\gcd(a,b)\geq 1$
* $\gcd(a,b)=\gcd(|a|,|b|)$
* $\gcd(a,0)=|a|$
* $\gcd(ka,kb)=|k|\gcd(a,b)$
* for $a,b\in\mathbb{N}\wedge b>a\Rightarrow \gcd(b,b-a)=\gcd(b,b+a)$.
### Euclids Lemma
If $a|bc$ and $\gcd(a,b)=1$ then $a|c$.
### Fundamental Theorem of Arithmetic
for all $n\in\mathbb{N}$, it is either prime or a product of powers of primes, that is: $$n=p_1^{k_1}p_2^{k_2}...p_m^{k_m}$$
We say that $d=\gcd(a,b)$ if $c|a$ and $c|b$ implies $c|d$
#### Example
given $\gcd(40,60)=20$, we can also see that $10$ is a divisor which is a common factor, and also divides $20$, so on and so forth.
#### Bezout Identity
If $d=\gcd(a,b)$, then there exists $x,y$ such that $$d=ax+by$$This states that we can form $d$ as a sum of linear combinations of those who have its $\gcd$ and 2 integers.
#### Proposition
If $a=bq+r$ with $0\leq r\leq b$, then $\gcd(a,b)=\gcd(b,r)$
##### Example
$$\gcd(120,340)=\gcd(120,340\% 120=100)=\gcd(120,120\% 100=20)=20$$
#### Diophantine Equations 
These are solutions for the equation $ax+by=c$ s.t. $x,y,c\in\mathbb{Z}$. The condition for these types of equations to have a solution is if:
$$ax+by=c,s.t. \exists c\in\mathbb{Z}\Leftrightarrow\gcd(a,b)| c$$
### Least Common Multiple
We say that $\text{lcm}(a,b)=m>0$ if:
1. $a|m\wedge b|m$
2. if $\exists c$ another common multiple $c$, where $m|c$.
#### Theorem
For $a,b,\in\mathbb{Z}$. $$\gcd(a,b)\cdot\text{lcm}(a,b)=|ab|$$
From this we can gather that: $$\text{lcm}(a,b)=\frac{|ab|}{\gcd(a,b)}$$
Notice that if $a,b$ is a product of primes: $$\begin{matrix}a=p_1^{\alpha_1}\cdot p_2^{\alpha_2}\cdot...\cdot p_k^{\alpha_k}\\b=p_1^{\beta_1}\cdot p_2^{\beta_2}\cdot...\cdot p_k^{\beta_k}\end{matrix}$$
then: $$\begin{matrix}\gcd(a,b)=p_1^{\min(\alpha_1,\beta_1)}\cdot p_2^{{\min(\alpha_2,\beta_2)}}\cdot...\cdot p_k^{\min(\alpha_k,\beta_k)} \\ \text{lcm}(a,b)=p_1^{\max(\alpha_1,\beta_1)}\cdot p_2^{{\max(\alpha_2,\beta_2)}}\cdot...\cdot p_k^{\max(\alpha_k,\beta_k)}\end{matrix}$$
##### Proof
By TFA for $a,b\in\mathbb{N}$ by TFA: $$\begin{matrix}a=p_1^{\alpha_1}\cdot p_2^{\alpha_2}\cdot...\cdot p_k^{\alpha_k}\\b=p_1^{\beta_1}\cdot p_2^{\beta_2}\cdot...\cdot p_k^{\beta_k}\end{matrix}$$
with $\alpha_i,\beta_i>0$ then: $$\gcd(a,b)\cdot\text{lcm}(a,b)=p_1^{\min(\alpha_1,\beta_1)+\max(\alpha_1,\beta_1)}\cdot p_2^{\min(\alpha_2,\beta_2)+\max(\alpha_2,\beta_2)}\cdot...\cdot p_k^{\min(\alpha_k,\beta_k)+\max(\alpha_k,\beta_k)}=ab$$
if $\min(\alpha_1,\beta_1)=\alpha_1$ then $\max(\alpha_1,\beta_1)=\beta_1$ then: $$\gcd(a,b)\cdot\text{lcm}(a,b)=p_1^{\alpha_1+\beta_1}\cdot p_2^{\alpha_2+\beta_2}\cdot...\cdot p_k^{\alpha_k+\beta_k}=ab$$which is what we were looking for to prove the above statement.
# Principles of Countability

## Principle of Multiplication
If a work can be done in $n_1$ forms, and a second work can be done in $n_2$ forms, then doing them consecutively can be done in $n_1n_2$ forms.

In general this can be written as:
given a task $T_i$, which can be done in $n_i$ forms, then doing these tasks in sequence $T_1,T_2,... T_k$ can be done in $n_1 n_2 ... n_k$ forms
### Sequences without Repetitions
If instead the elements cannot repeat and we select $r$ elements, then there are $$\frac{n!}{(n-r)!}$$ permutations.
### Sequences with Repetitions
Given a set with $n$ elements and we want to form a sequence of length $r$, where the elements can repeat, then there are $n^r$ options. That said, we can generalize this.

The amount of permutations that a set of $n$ objects where some are indistinguishable, each one with a multiplicity of $K_1,K_2,...,K_r$ and $K_1+...+K_r$ then there are: $$\frac{n!}{K_1!\cdot ...\cdot K_r!}$$
* The ==**multiplicity**== denotes the amount of repetitions of the specific element.
* The word ==**indistinguishable**== means that the elements that repeat have some where permuting them with themselves would give the same sequence.
* ==**Permutation**==, implies that the ordering of the elements matters.
### Circular Permutations
Given $n$ objects ordered around in a circular array, such that the same sequence of objects appearing at some point is equivalent, then the amount of permutations in the circular array is: $$(n-1)!$$
### Examples
Ways of organizing people in seats. Given people $a, b, c$ and $3$ seats, then there are $3\cdot 2\cdot 1$ different ways of doing it, or $3!$. This is because the number of options (people) given, reduce every time you use one of the options.