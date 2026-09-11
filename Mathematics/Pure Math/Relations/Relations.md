# What is a Relation?
A relation $R$ is ==**a set of ordered pairs**==. Intuitively you can think of these ordered pairs as mappings from one value to another, in a nodelike structure. [[Functions|Functions]] are one such relation. Just like functions, the values in the ordered pairs $(a,b)\in R$ are called the ==**domain**== and ==**range**== respectively, so if we had a relation $R\subseteq \{(x,y)|x\in X, y\in Y\}$ we would call $X$ the domain and $Y$ the range.
## Vocabulary
### Homogeneous Binary Relation
Is a relation between a set $X$ and itself. It is a subset of the cartesian product $X\times X$.
### Comparable
Two elements $x, y\in X$ are comparable with respect to a relation $R$ if at least one of these relations is true:
	$xR y$ or $yR x$
# Types/Properties of Relations
## Empty
The empty relation $R$ on a set $X$ relates no elements, it is basically the $\emptyset$.
## Universal
The universal relation $R$ on a set $X$ is the set which relates every element with one another. Put simply, it is the cartesian product $X\times X$. 
## Reflexive
Given a set $X$ and a relation on that set $R$, an operation is said to be reflexive if: $$\forall x\in X\Leftrightarrow (x,x)\in R$$
In simple words, for all $x$, it is related to itself.
### Identity
This is a special case of the reflexive relation $R$, where it only contains elements of the form $(x,x)$. We can say then that: $$R\subseteq \{(x,x)|x\in X\}$$
### Antireflexive
This can be seen as the opposite of a reflexive relation, as it assumes the negation: $$\forall x\in X\Leftrightarrow (x,x)\not\in R$$
## Transitive
Given a set $X$ an operation is said to be transitive if: $$\forall,a,b,c\in X\Rightarrow((a,b)\in R \wedge (b,c)\in R\Rightarrow (a,c)\in R)$$
In simple words, for all $a,b,c$ if there exists a relation between $a$ with $b$ and $b$ with $c$, then there must exist a relation between $a$ and $c$.
### Antitransitive
This can be seen as the opposite of a transitive relation, as it assumes the negation: $$\forall,a,b,c\in X\Rightarrow((a,b)\in R \wedge (b,c)\in R\Rightarrow (a,c)\not\in R)$$
# Symmetric
Given a set $X$ an operation is said to be symmetric if: $$\forall a,b\in X\Rightarrow ((a,b)\in R\Leftrightarrow (b,a)\in R)$$
## Asymmetric
This can be seen as the opposite of a symmetric relation, as it assumes the negation: $$\forall a,b\in X\Rightarrow ((a,b)\in R\Leftrightarrow (b,a)\not\in R)$$
# Antisymmetric
Given a set $X$ an operation is said to be antisymmetric if: $$\forall a,b\in X\Leftrightarrow ((a,b)\in R\wedge (b,a)\in R\Leftrightarrow a=b)$$This is a bit complicated to grasp, but you can think of it in terms of $\leq$. If $a\leq b$ and $b\leq a$ it implies that $a=b$.
## Trichotomy
A relation $R$ on some set $X$ such that for all $a, b\in X$
	either $aRb$ or $bRa$ or $a=b$
## Connected, Complete or Total
A relation $R$ on some set $X$ is connected when $\forall x,y\in X$:
	$x R y$ or $y R x$ or $x=y$
Any of those relations can hold for it to be related. A relation on a set is called connected if it relates all distinct pairs of the set in one direction or the other. 
### Strongly Connected 
These are strongly connected if it relates all pairs of elements with each other.
# Composing Relations
These are relations composed of various previously discussed relations:
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
# Operations on Relations
## Inverse
The inverse of a relation $R$ denoted $R^{-1}$, flips the ordered pairs. This means an element $(a,b)\in R$ will get mapped to the element $(b,a)\in R^{-1}$.
## Complement
This one is quite intuitive, as it simply gets the complement of the set $R$ with the Universal relation. 
