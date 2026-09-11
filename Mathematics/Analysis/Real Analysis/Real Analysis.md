
Is the study of the set $\mathbb{R}$ and its properties. Defining $\mathbb{R}$ axiomatically, it satisfies the following:
1. $\mathbb{R}$ is a ==**complete**== [[Relations#Total Order|totally ordered]] [[Algebraic Structures#Fields|field]] ([[Algebraic Structures#Ordered Fields|ordered field]]) and their subfield is $\mathbb{Q}$, that is to say $\mathbb{R}\supset \mathbb{Q}$
2. By [[Relations#Trichotomy|trichotomy]] in the real numbers it suggests that $\forall a, 0\in \mathbb{R}$ it is either $a>0$, $a<0$ or $a=0$. 
#### Definition of the Supremum
Let $F$ be an ordered field, and let $A\subset F$. 
	We say that $A$ is bounded from above by $\alpha \in F$ if $$\forall x\in A, x\leq \alpha$$. In this case, $\alpha$ is called an upper bound of $A$.
If $A$ is bounded from above, then we say that $\alpha=\text{sup}(A)$ if
1. $\alpha$ is an upper bound of $A$, also denoted as $\forall x\in A$, $x\leq \alpha$. It is important to note that all numbers larger than $\alpha$ are also upper bounds.
2. $\alpha$ is the ==**least upper bound**== of $A$, also denoted as $\forall c\in A$ then $c\geq \alpha$.
$\alpha$ is not necessarily an element of $A$.

For an interval $(0,1)\subset\mathbb{R}$, the upper bound would be $1$. the element $1$ is not the maximum of the set however, since it is not included.
#### Definition of the Infinum
Let $F$ be an ordered field, and let $A\subset F$. 
	We say that $A$ is bounded from below by $\alpha \in F$ if $$\forall x\in A, x\geq \beta$$. In this case, $\alpha$ is called a lower bound of $A$.
If $A$ is bounded from below, then we say that $\beta=\text{inf}(A)$ if
1. $\beta$ is a lower bound of $A$, also denoted as $\forall x\in A$, $x\geq \beta$. It is important to note that all numbers lesser than $\beta$ are also lower bounds.
2. $\beta$ is the ==**greatest lower bound**== of $A$, also denoted as $\forall c\in A$ then $c\leq \beta$.
$\beta$ is not necessarily an element of $A$

For an interval $(0,1)\subset\mathbb{R}$, the lower bound would be $0$. the element $0$ is not the minimum of the set however, since it is not included.
# The Completeness Axiom
Since $\mathbb{R}$ is a *complete* ordered field, then every set $A\subseteq F$ bounded from above has a supremum $\alpha=\text{sup}(A)\in F$
# Density of $\mathbb{Q}$ in $\mathbb{R}$
For every open interval $(a,b)\subseteq \mathbb{R}, a < b, \exists q\in \mathbb{Q}$ s.t. $q\in (a,b)$.
# Archimedean Principle
$$\forall \epsilon > 0, \forall m\in \mathbb{R}, \exists n\in \mathbb{N}\text{ s.t. }n\epsilon > m$$
# Countability and Uncountability
Any set that can be enumerated by $\mathbb{N}$ is countable. This makes $\mathbb{N}, \mathbb{Z}$ and $\mathbb{Q}$ countable infinities because they have the same [[Set Theory#Cardinality|cardinality]]. However $\mathbb{R}$ is uncountably infinite as there is no bijection in $\mathbb{Z}$.
# Limits of Sequences
Convergence on [[Sequences|sequences]] is defined as follows:

A sequence $a_n$ converges to a real number $a$ if, for every positive number $\epsilon$, there exists $N\in\mathbb{N}$ such that whenever $n\geq N$ it follows that $|a_n-a|<\epsilon$.

$$a_n\text{ converges to }a\Leftrightarrow \forall\epsilon >0(\exists N,n\in\mathbb{N}\text{ s.t. }n\geq N\Rightarrow |a_n - a|<\epsilon)$$
## Limit Proof Template
1. Let $\epsilon > 0$ be arbitrary
2. Demonstrate a choice of $N\in \mathbb{N}$.
3. Show $N$ works
4. Assume $n\geq N$.
5. With $N$ chosen, then it should be possible to do $|x_n-x|<\epsilon$.
# Sources
1. [Big Epsilons videos on Real Analysis](https://www.youtube.com/@BigEpsilon)
