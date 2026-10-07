Is concerned with how to measure size of [[Set Theory|subsets]]. For example it can be things like Length, Area and Volume. Measure theory works by generalizing the notion of lengths.
# $\Large\sigma$ Algebra
These are used to define measurable sets. The $\sigma$ is used because it represents sum.
## Definition
Consider a set $X$.
	A $\sigma$-algebra $\mathcal{F}$ of subsets of $X$ is a collection $\mathcal{F}$ of subsets of $X$ satisfying the following conditions:
	1. $\emptyset\in\mathcal{F}$
	2. if $B\in\mathcal{F}$ then its [[Set Theory#Complements|complement]] $B^C$ is also in $\mathcal{F}$
	3. if $B_1, B_2, ...$ is a countable collection of sets in $\mathcal{F}$ then their union $\bigcup_{n=1}^\infty{B_n}\in\mathcal{F}$.
From this definition we can also derive that $X\in\mathcal{F}$ since it is the complement of $\emptyset$. The reason it is defined this way is because if we know the size of a set $A\subset X$ from a whole $X$ then we know the difference from that whole $X\setminus A$. 
from [math.lsu.edu](https://www.math.lsu.edu/~sengupta/7312s02/sigmaalg.pdf) and [bauer.uh.edu](https://www.bauer.uh.edu/rsusmel/phd/sR-0.pdf)

* ==**measurable sets**==: What the elements of the $\sigma$-algebra will be called.
### Examples
These examples are fairly similar to that of a [[Topology OLD#Topological Space|topology]], and they are the $\sigma$-algebra over $X$ equal to:
1. $\mathcal{X}=\{\emptyset, X\}$. This is also called an **atom**.
2. $\mathcal{X}=\mathcal{P}(X)$.
## Properties
1. Given a list of sigma algebras $\mathcal{X}_i$ on $X$ s.t. $i$ corresponds to an arbitrary index set. The intersection between distinct $\mathcal{X}_i$ will give another $\sigma$-algebra on $X$.
2. Is closed under countable unions, intersections and complements.
## Theorems
1. If $\mathcal{X}$ is a sigma algebra then $\mathcal{X}$ is also a [[Structures#$ sigma$ Rings|sigma ring]]. Conversely any sigma ring $\mathcal{R}\subseteq \mathcal{P}(X)$ is a sigma algebra if and only if $X\in \mathcal{R}$. 
2. 
# Borel $\Large\sigma$ Algebra
## Definition
Let $(X, {\Large\tau})$ be a [[Topology OLD#Topological Space|topological space]].
A Borel $\sigma$-algebra is the smallest $\sigma$-algebra containing all open sets of $X$. 
## Finding the Smallest $\sigma$-algebra
To find the smallest sigma algebra containing $M$, such that $M\subseteq \mathcal{P}(X)$, using the 1st property described in the previous section, we utilize the function $$\sigma(M):=\bigcap_{A\supseteq M}A$$
We can say then, that the Borel $\sigma$-algebra $\mathcal{B}(\mathcal{F})$ generated from $\sigma$-algebra $\mathcal{F}$ is $\sigma({\Large\tau})$.
# Measurable Space
## Definition
Is an ordered pair $(X, \mathcal{X})$ where $X$ is a set and $\mathcal{X}$ is a sigma algebra.
# Measure
## Definition
Given a map from a sigma algebra $\mu:\mathcal{X}\to\mathbb{R}\cup \{\infty\}$. To simplify the notation we write: $$\mu:\mathcal{X}\to[0,\infty]$$such that it holds the following properties:
1. ==**Empty Measure**==: The $\emptyset=0$.
2. ==**Additivity**==: the $\sum_{i=1}^n{\mu(\mathcal{X}_i)}$ s.t. $\mathcal{X}_i\neq\mathcal{X}_j$, (They are [[Set Theory#Vocabulary#Disjoint Sets|pairwise disjoint]]) is equal to $\mu(\bigcup_{i=1}^n{\mathcal{X}_i})$, $\forall \mathcal{X}_i\in\mathcal{X}$.
### $\infty$ properties
1. ==**Additive Absorption**==: $x+\infty=\infty, \forall x\in[0,\infty]$.
2. ==**Multiplicative Absorption**==: $x\cdot\infty=\infty, \forall x\in(0,\infty]$.
3. $0\cdot\infty$: Occasionally undefined, but in the worst cases some people set $0\cdot\infty=0$.
## $\sigma$-additive
We can approximate volumes through infinite sums, similar to how we would in something like calculus. The way we do this is by using the 2nd property and making $n=\infty$: $$\mu(\bigcup^{\infty}_{i=1}{\mathcal{X}_i})=\sum_{i=1}^\infty{\mu(\mathcal{X}_i)}$$
## Measure Space
Is an ordered trio similar to the measurable space, but now with a measure $\mu$. We denote this $$(X, \mathcal{X}, \mu)$$
### Properties
1. ==**Monotonicity**==: If $E, F\in \mathcal{X}$ and $E\subset F$ then $\mu(E)\leq \mu(F)$. This is clear to see as $E$ is part of $F$ and the part can never be larger than the whole.
2. ==**Subadditivity**==: Given a set of open sets in the sigma algebra $\{E_j\}_{j=1}^\infty=E\subset\mathcal{X}$ then $\mu(\bigcup_{j=1}^\infty E_j)\leq \bigcup_{j=1}^\infty{\mu(E_j)}$.

## Examples
### The Counting Measure
This can be used for any set. It is the map: $$\mu(A):=\begin{cases}A\text{ is finite: }n(A)\\\infty\end{cases}$$ such that $A\in\mathcal{X}$.
### Dirac Measure for $p\in X$
Is a measure concentrated in one point. We use: $$\delta_p(A):=\begin{cases}p\in A:1\\p\not\in A:0\end{cases}$$
such that $A\in\mathcal{X}$.
## Measures on $X=\mathbb{R}^n$
These have the properties such that for sets $A\in\mathcal{X}$:
1. ==**Unit Volume**==: $\mu([0,1]^n)=1$
2. ==**Translation invariance**==: $\mu(x+A)=\mu(A)$ $\forall x\in X$.
## Measurable Maps
These are maps such that they go from a sigma algebra $\mathcal{X}$ to the Borel sigma algebra $\mathbb{R}$, represented as: $$f: \mathcal{X}\to\mathbb{R}$$
# Integrals
Given a measure space $(X, \mathcal{X}, \mu)$, the integral over this space is $$I(X_A):=\mu(A)$$
