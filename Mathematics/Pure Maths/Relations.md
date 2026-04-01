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
### Example
* $x = x$ means that equality is reflexive
## Symmetric 
A relation on some set $A$ is symmetric if $\forall x, y\in A, \text{ if } x\text{R} y \text{ then } y~x$. An example of this is $f: x \leftrightarrow y$. Another example can be a function $f(x,y)=f(y,x)$.
### Example
* $x = y \Rightarrow y = x$ means that equality is symmetric
# Antisymmetric
A relation is antisymmetric if $aRb$ with $a\neq b$ then $bRa$ must not hold. As an example we can see the relation $a \leq b, a\neq b$, that implies that $b \nleq a$, therefore it is antisymmetric. If $a\leq b$ and $b \leq a$ then $a=b$.
## Asymmetric
A relation on some set $A$ is asymmetric if $\forall x, y \in A$, if $x R y \text{ then } y$ does not have a relation with $x$. It's a one way relation: $f: x \to y$. That is if it is both antisymmetric and irreflexive (not reflexive).
## Transitive
A relation on some set $A$ is transitive if $\forall x,y,z\in A, \text{ if } x\text{R} y \text{ and } y\text{R} z \text{ then } x\text{R} z$. 
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
where $X$ is the set where the binary relation $\sim$ is acting on. A way to denote the set of all equivalence classes in $X$ with respect to an equivalence relation $R$ is by saying $X/R$, also called $X$ modulo $R$ which is often referred to as the ==quotient set== or ==quotient space==. ==**When talking of an equivalence class, we need to talk about what it is equivalent to**==. For example in modulo arithmetic of $mod(5)$ the numbers $4$ and $9$ are fundamentally equivalent as $2+4=1$ and $2+9=1$. Each one will give an equivalent result, even when the operation is different. Another example are rotations, specifically equivalent angles. When rotating $380^{\circ}$ it will give you the same result had you just rotated $20^{\circ}$, so they are equivalent.
### Example
A good example of an equivalence class is modulo 2 on the set of integers $\mathbb{Z}$. Lets take the equivalence relation such that for $x, y \in \mathbb{Z}\text{ s.t. }x \sim y \text{ iff }x-y=2n, \text{ where } n\in \mathbb{Z}$. This makes it so that the elements $[5]$, $[7]$, $[9]$, etc, represent the same elements of $\mathbb{Z}/\sim$ since the equivalence relation forms two equivalence classes: odd and even numbers. This is because ==**any two odd numbers that subtract each other equal an even number, and any 2 even numbers that subtract each other make an even number**==.
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
# Order
Is a binary relation that is ==**reflexive**==, ==**transitive**== and ==**antisymmetric**==.
### Reflexive Transitive Closure (Smallest Preorder)
Is the transitive closure of a relation $(R) \cup (I)$ where $I$ is the identity relation. In other words it is the smallest preorder, by acquiring its transitive closure. Represented as $R^{*}$.
## Symmetric Closure
The union of the relation $\to$ with its converse $\leftarrow$. That is $(\to) \cup (\leftarrow)=\leftrightarrow$.
## Reflexive Transitive Symmetric Closure
Is the transitive closure of $(\leftrightarrow) \cup (I)$ where $I$ is the identity relation. Also known as its smallest ==**equivalence relation**== containing $\to$.