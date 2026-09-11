# Introduction
* Person that's teaching me: Dr. Jose Emilio.
# Preliminary
1. [[Set Theory]]
2. [[Sequences]]
# The Characteristic Polynomial of a Sequence
The way we find the characteristic polynomial of a sequence is by the given number of initial values $k$, where $A_n$ are the initial values. We define it by $$a_n=A_1x^{n-1}+A_2x^{n-2}... A_nx^{n-k}$$We can then solve this equation for $0$ to get the list of roots $C_i$ to get the explicit equation as:
$$B_0(C_0)^n+B_1(C_1)^n+...+B_k(C_k)^n$$ where we must then solve for $B_i$ and replace it unto this equation for us to get the explicit equation

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
