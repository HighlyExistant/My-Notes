# Vocabulary
Some vocabulary before talking about relations, we'll be using $x \text{R} y$ to denote a relation between $x$ and $y$, but the symbol used might be different depending on context. 
* ==**A relation is a set of ordered pairs**==, where the first component is called the domain, and the second component is called the range. This can be represented as $(D, R)$.
* ==**Homogeneous Binary Relation**==: Is a relation between a set $A$ and itself. It is a subset of the cartesian product $A\times A$.
## Closure
Means that an operation on a set $X$ will bring about a result on $X$. That is to say for $x\in X, f: x \to y \Rightarrow y \in X$.
## Empty
A relation on some set $A$ is empty if it relates to no other element of $A$.
## Universal
A relation on some set $A$ is universal if every element of $A$ is related to every other element of set $A$, $R=A\times A$.
## Identity
A relation on some set $A$ is an identity relation if ==**it is related only to itself**==. That is $R=\{(a, a)\}$. As an example if $A=\{a, b, c\}$ then an identity relation is $R=\{(a, a), (b, b), (c, c)\}$, or put in function terms $f: x \to x$.
## Reflexive
A relation on some set $A$ is reflexive if $x\text{R} x, \forall x \in A$. This can for example be the identity function, a function that makes $f: x\to x$. 
### Properties
* Every element is related to itself
* Can contain extra pairs unlike the identity.
## Antireflexive
A relation on some set $A$ is antireflexive if $\forall x\in A\Rightarrow (x,x)\not\in R$. An example of an antireflexive relation is $<$ because there is no relation $x<x$.
### Properties
* Every element is not related to itself
### Example
* $x = x$ means that equality is reflexive
## Comparable
Two elements $x, y\in X$ are comparable with respect to a relation $R$ if at least one of these relations is true:
	$xR y$ or $yR x$
## Connected, Complete or Total
A relation $R$ on some set $X$ is connected when $\forall x,y\in X$:
	$x R y$ or $y R x$ or $x=y$
Any of those relations can hold for it to be related. A relation on a set is called connected if it relates all distinct pairs of the set in one direction or the other. 
### Strongly Connected 
These are strongly connected if it relates all pairs of elements with each other.
## Symmetric 
A relation on some set $A$ is symmetric if $\forall x, y\in A, \text{ if } x\text{R} y \text{ then } y\text{R}x$. An example of this is $f: x \leftrightarrow y$. Another example can be a function $f(x,y)=f(y,x)$.
### Example
* $x = y \Rightarrow y = x$ means that equality is symmetric
## Antisymmetric
A relation $R$ on some set $X$ such that for all $a, b\in X$, 
	if $aRb$ and $bRa$ then $a=b$
## Trichotomy
A relation $R$ on some set $X$ such that for all $a, b\in X$
	either $aRb$ or $bRa$ or $a=b$
## Asymmetric
A relation on some set $A$ is asymmetric if $\forall x, y \in A$, if $x R y \text{ then } y$ does not have a relation with $x$. It's a one way relation: $a<b$ is satisfied but not $b<a$.
## Transitive
A relation on some set $A$ is transitive if 
	$\forall x,y,z\in A, \text{ if } x\text{R} y \text{ and } y\text{R} z \text{ then } x\text{R} z$. 
# Antitransitive
As the name suggests this is the opposite of a transitive relation:
$$
	\forall a, b, c: aRb \wedge bRc\Rightarrow\neg(aRc)
$$
### Examples
* The inequality $1 < 3$. there is a transitive relation between $1, 2$ and $3$ because $1<2$ and $2<3$ therefore $1 < 3$.
* The function $S(x)=x+1$ is transitive, as $S(1)=2$, and $S(2)=3$, implies that $(S \circ S)(1)=3$.
## Equivalence
Operation which is **reflexive, symmetric and transitive**. The symbol for this is $\equiv$ or $\sim$. When you want to represent the relation explicitly you write: $\equiv_R$ or $\sim_R$.while nonequivalence is $\not\equiv$ or $\not\sim$.
### Equivalence Classes
Are denoted as 
$$
	[a]=\{x\in X: a \sim x\}
$$
where $X$ is the set where the binary relation $\sim$ is acting on. These equivalence classes actually form [[Set Theory#Partition of a set|partitions]] $P_\sim$ of $X$. We can say conversely that the partition belongs to some equivalence class. 
#### Quotient
A way to denote the set of all equivalence classes in $X$ and thus the partitions is through this operation: $$X/R:=P_R$$
### Example
A good example of an equivalence class is modulo 2 on the set of integers $\mathbb{Z}$. Lets take the equivalence relation such that for $x, y \in \mathbb{Z}\text{ s.t. }x \sim y \text{ iff }x-y=2n, \text{ where } n\in \mathbb{Z}$. This makes it so that the elements $[5]$, $[7]$, $[9]$, etc, represent the same elements of $\mathbb{Z}/\sim$. This would make: $${\mathbb{Z}/\sim}=\{[0]_\sim, [1]_\sim\}$$
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
### Modular Arithmetic as **Equality**
Another way of writing modular arithmetic is by giving the binary relation $a=0$. If we take for example $4=0$, we find that any operation $a + 0 = a$, therefore in modular arithmetic $\text{mod}(4)$ $7 - 0 = 8 - 4=3$.
# Combinations
## Transitive Closure
The transitive closure of the set denoted $R^+$, is the ==**smallest binary relation**== on a set $A$. That is to say that for all elements where there is a transitive relation, the set $A=\{a, b, c\}$ such that $R=\{(a, b), (b, c), (a, c)\}$, it can be reduced to just $R^{+}=\{(a,b), (b,c)\}$, since $a\to c$ can be expressed as $a\to b \to c$.
## Preorder
A binary relation that is ==**reflexive**== and ==**transitive**==. ==**it is not antisymmetric**==.
### Reflexive Transitive Closure (Smallest Preorder)
Is the transitive closure of a relation $(R) \cup (I)$ where $I$ is the identity relation. In other words it is the smallest preorder, by acquiring its transitive closure. Represented as $R^{*}$.
## Partial Orders
Is a binary relation that is ==**reflexive**==, ==**transitive**== and ==**antisymmetric**==. Not every element in the set needs to be comparable. That means ==**it is not strongly connected**==.
### Partially Ordered Sets (Poset)
These are represented as ordered pairs $P=(X, \leq)$ where $X$ is the set of elements and $\leq$ is the ordering.
### Example
Given a set of elements $A=\{a, b, c, d\}$ and a set of relations $$O=\{(x,x)|x\in A\}\cup\{(a,b), (b,c), (c,d)\}$$
where we must remember that $(a,b)$ is $a\to b$, then we can see that these relations are reflexive, transitive and antisymmetric. If we want to find the number that follows $b$ then it is $c$, and the one that follows after would be $d$.
## Total Order
Is a binary relation $\leq$ on some set $X$ such that it is ==**reflexive**==, ==**transitive**==, ==**antisymmetric**== and are ==**strongly connected**==. it also satisfies being ==**trichotomous**==.
## Strict Order
Is a binary relation $<$ on some set $X$ such that it is ==**antireflexive**==, ==**transitive**==, ==**asymmetric**==.
## Symmetric Closure
The union of the relation $\to$ with its converse $\leftarrow$. That is $(\to) \cup (\leftarrow)=\leftrightarrow$.
## Reflexive Transitive Symmetric Closure
Is the transitive closure of $(\leftrightarrow) \cup (I)$ where $I$ is the identity relation. Also known as its smallest ==**equivalence relation**== containing $\to$.
