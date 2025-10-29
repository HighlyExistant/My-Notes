Some vocabulary before talking about relations, we'll be using $x \text{R} y$ to denote a relation between $x$ and $y$, but the symbol used might be different depending on context.  
## Reflexive
A relation on some set $A$ is reflexive if $x\text{R} x, \forall x \in A$. This can for example be the identity function, a function that makes $f: x\to x$.
## Symmetric 
A relation on some set $A$ is symmetric if $\forall x, y\in A, \text{ if } x\text{R} y \text{ then } y~x$. An example of this is $f: x \leftrightarrow y$. Another example can be a function $f(x,y)=f(y,x)$.
## Asymmetric
A relation on some set $A$ is asymmetric if $\forall x, y \in A$, if $x R y \text{ then } y$ does not have a relation with $x$. It's a one way relation: $f: x \to y$.
## Transitive
A relation on some set $A$ is transitive if $\forall x,y,z\in A, \text{ if } x\text{R} y \text{ and } y\text{R} z \text{ then } x\text{R} z$. Lets take as an example the function $f(x)=x+1$. there is a transitive relation between $1, 2$ and $3$ because $f(1): 1\to 2$ and $f(2):2\to 3$ therefore there exists a relation $(f \circ f)(1): 1\to3$.
## Equivalence
Operation which is **reflexive, symmetric and transitive**. The symbol for this is $\equiv$ or $\sim$. When you want to represent the relation explicitly you write: $\equiv_R$ or $\sim_R$.while nonequivalence is $\not\equiv$ or $\not\sim$.
### Equivalence Classes
Are denoted as 
$$
	[a]=\{x\in X: a \sim x\}
$$
where $X$ is the set where the binary relation $\sim$ is acting on. A way to denote the set of all equivalence classes in $X$ with respect to an equivalence relation $R$ is by saying $X/R$, also called $X$ modulo $R$ which is often referred to as the ==quotient set== or ==quotient space==. ==**When talking of an equivalence class, we need to talk about what it is equivalent to**==. For example in modulo arithmetic of $mod(5)$ the numbers $4$ and $9$ are fundamentally equivalent as $2+4=1$ and $2+9=1$. Each one will give an equivalent result, even when the operation is different. Another example are rotations, specifically equivalent angles. When rotating $380^{\circ}$ it will give you the same result had you just rotated $20^{\circ}$, and are equivalent.
### Example
A good example of an equivalence class is modulo 2 on the set of integers $\mathbb{Z}$. Lets take the equivalence relation such that for $x, y \in \mathbb{Z}\text{ s.t. }x \sim y \text{ iff }x-y=2n, \text{ where } n\in \mathbb{Z}$. This makes it so that the elements $[5]$, $[7]$, $[9]$, etc, represent the same elements of $\mathbb{Z}/\sim$ since the equivalence relation forms two equivalence classes: odd and even numbers. 
## Congruence (Equivalence Relation)
A congruence relation depends on an operation where a value is interchangeable and gives you the same result.
### Example
$$
	a_1\equiv a_2 \text{ and } b_1 \equiv b_2 \Rightarrow a_1+b_1\equiv a_2+b_2
$$
### Modular Arithmetic (Congruence)
When talking about congruence within modular arithmetic, we use a modified version of the congruence operation $\equiv_n$ where $n$ is the mod. For example 
$$
	a+6=a+2\text{ mod(4)} \text{ then } 2\equiv6 \text{ mod(4)}
$$
can be rewritten as 
$$
	a+6=a+2 \text{ mod(4) then } 2 \equiv_4 6
$$
