One of the most fundamental theories of modern mathematics. A set is simply an abstract mathematical object that contains ==**elements**==. The way we write sets is using open and closed brackets:
$$
	\{\}
$$
The following is what's known as an empty set, and can be rewritten as:
$$
	\{\}=\emptyset
$$
Sets are obviously however supposed to contain elements, and these elements can be anything ==**except the set itself**==. That means that $a=\{a\}$ is not a valid set. That said however we can put anything in a set such as numbers $\{1, 2, 3, ...\}$, letters $\{x, y, z\}$ or even just emojis $\{🤓\}$. Important to note however that a set does not have duplicate elements, meaning that $\{a, a\}=\{a\}$. There's multiple ways of writing a set, one of them we have already seen, where we discretely write the elements of the set. the other way is by defining rules for our set:
$$
	\{x|x>0\}
$$
the $|$ should be read as, "such that", or "given", therefore the way we read this set is "the set of all $x$ such that $x$ is larger than $0$". To denote that an element is part of some set $X$ we can use $\in$ symbol and say: $$x\in X$$
# Operations
## In
We say an element $a$ is inside a set $A$ using the $\in$ symbol and $\not\in$ it it is not in the set.
### Example
given a set $A=\{a, b, c, d\}$, then $a\in A$, but $e\not\in A$.
## Difference
The difference of two sets $A\setminus B$ removes all elements in $B$ from $A$. That is to say: $$A\setminus B=\{a\in A|a\not\in B\}$$
## Complements
Given a set $A$ which is a subset of a universal set $U$, so $A\subseteq U$, we say that the complement of $A$, written as either $A'$, $A^C$ or $\overline{A}$, is everything not in $A$ and in $U$. If we were thinking of this in terms of logic, this would be the [[General Logic#Logical Negation|logical not]]. We can think of the complement as: $$A\subseteq U\Rightarrow 
\overline{A}=U\setminus A$$
### Example
Given a set $A=\{a, b, c, d\}$ and a universal set $U=\{a, b, c, d, e, f, g, h\}$. the complement of $A$ would be: $$\overline{A}=\{e, f, g, h\}$$
## Union
Given a set $A$ and a set $B$ the union of a set $A\cup B$ combines the elements in both sets. If we were thinking of this in terms of logic, this would be the [[General Logic#Logical Disjunction|logical or]]
### Example
$A=\{a, b, c, d\}, B=\{a, d, e, f\}$, then the union would be $$A\cup B=\{a, b, c, d, e, f\}$$
## Intersection
Given a set $A$ and a set $B$ the intersection $A\cap B$ would be the set containing all the values they have in common. If we were thinking of this in terms of logic, this would be the [[General Logic#Logical Conjunction|logical and]].
* We say a set $A$ intersects a set $B$ if $A\cap B\neq \emptyset$.
## Cartesian Product
The cartesian product of two sets $X, Y$ is every ordered pair that can be created from them. If $X=\{a, b\}$ and $Y=\{c, d\}$ then: $$X\times Y=\{(a, c), (a, d), (b, c), (b, d)\}$$
## Power Set
The power set of a set $X$ is every possible subset of $X$. If $X=\{a, b, c\}$ then $$\mathcal{P}(X)=\{\emptyset, X, \{a\}, \{b\}, \{c\}, \{a, b\}, \{a, c\}, \{b, c\}\}$$


### Example
$A=\{a, b, c, d\}, B=\{a, d, e, f\}$, then the intersection would be $$A\cap B=\{a, d\}$$
# Cardinality
The cardinality of a set is the number of elements it contains. For example, the set $A=\{a, b, c\}$ has a cardinality $|A|=3$.
## Comparing Cardinalities
Sometimes we want to check if two sets have the same number of elements as another set. This becomes more complicated for sets with an infinite amount of elements such as $\mathbb{N}$ and $\mathbb{Z}$. Instead the definition for something having the same size as another set, is if there exists a [[Functions#Bijective|bijection]] between one set and another. 
# Vocabulary
##### Disjoint Sets
2 sets $A$ and $B$ are disjoint if $A \cap B=\emptyset$.
##### Partition of a set
let $X$ be an arbitrary set, a **partition of set $X$** would be a set of non-empty subsets of $X$ such that every element $x \in X$ is in exactly one of these subsets.  What this is saying is that the partition $P$ contains subsets of $X$, which could equal the set $X$ itself ($P=\{X\}$ is known as the ==trivial partition==) such that for all elements $x \in X$ there exists a disjoint subset $P \subseteq X$. A nice property of this is: $$\cup{P}=X$$
  An example of a partition of a set would be, given the set $A=\{a, b, c\}$, the a partition $P=\{\{a\}, \{b, c\}\}$.
# Absorbing Set
A set $A\subseteq X$ is an absorbing set if, for each $x\in X$ there is a positive number $s_x$ such that $x\in tA$ whenever $t > s_x$.
# Intervals
We're going to use the set $X= \mathbb{R}$ as an example in the following parts. An interval is a collection of objects with an order $<$ and or $\leq$ imposed on them. 
## Open Intervals
An open interval is an interval which does not include its end points. If we wanted to grab an open interval: $(a,b)\subseteq X$ then this would be the set: $$(a,b)\subseteq X=\{x\in X|a < x < b\}$$
## Closed Intervals
A closed interval is an interval which includes its end points. If we wanted to grab a closed interval: $[a,b]\subseteq X$ then this would be the set: $$[a,b]\subset X=\{x\in X|a \leq x \leq b\}$$
## Half Open Intervals
These are intervals of the form $[a,b)\subset X$ or $(a,b]\subset X$ wherein it contains one of the endpoints but not the other. These are of the form: $$[a,b)\subset X=\{x\in X| a\leq x<b\}$$$$(a,b]\subset X=\{x\in X| a< x\leq b\}$$
## Open Intervals as Countably Infinite Unions
We can represent open intervals as the union of [[Real Analysis#Countability and Uncountability|countably]] infinite sets by approaching the value at the open interval: $$(a,b)=\bigcup_{i=1}^\infty{[a+\frac{1}{n},b)}$$
This will union every element approaching $a$ but will never union $a$. We can do the same on the opposite side too: $$(a,b)=\bigcup_{i=1}^\infty{(a,b-\frac{1}{n}]}$$
# Ordered Pairs
Lots of definitions in math make use of ordered pairs, these are represented as $(a,b)$. These are occasionally also called a tuple of size 2. The only property we want from an ordered pair is one such that 
	$(a,b)=(c,d)\Leftrightarrow a=c,b=d$.
The initial definition of an ordered pair was the one by Felix Hausdorff in [Grundzüge der Mengenlehre](https://dn790002.ca.archive.org/0/items/grundzgedermen00hausuoft/grundzgedermen00hausuoft.pdf) page 32: $$(x,y)=\{\{x,1\}, \{y, 2\}\}$$
But it was later replaced by the ==**Kuratowski definition**==:
$$(x,y)=\{\{x\}, \{x, y\}\}$$
which many argue to be a more elegant form without the need of arbitrary markers such as $1$ and $2$.
# Cofiniteness
Given a $A\subset X$, then $A$ is cofinite if its complement is a finite set. The ==**co**== in cofinite is for complement.
# De Morgan's Laws
These laws are usually used for logic, but they also apply to sets:
* $(A\cup B)^C=A^C\cap B^C$
* $(A\cap B)^C=A^C\cup B^C$
Written differently, seeing as though $A^C=A-U$ where $U$ is the universal set, this turns to:
* $A-(B\cup C)=(A-B)\cap(A-C)$
* $A-(B\cap C)=(A-B)\cup(A-C)$
