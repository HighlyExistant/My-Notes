One of the most fundamental theories of modern mathematics, a set is simply an abstract mathematical object that contains ==**elements**==. The way we write sets is using open and closed brackets:
$$
	\{\}
$$
The following is what's known as an empty set, and can be rewritten as:
$$
	\{\}=\emptyset
$$
Sets are obviously however supposed to contain elements, and these elements can be anything ==except the set itself==. That means that $a=\{a\}$ is not a valid set. That said however we can put anything in a set such as numbers $\{1, 2, 3, ...\}$, letters $\{x, y, z\}$ or even just emojis $\{🤓\}$. Important to note however that a set does not have duplicate elements, meaning that $\{a, a\}=\{a\}$. There's multiple ways of writing a set, one of them we have already seen, where we discretely write the elements of the set. the other way is by defining rules for our set:
$$
	\{x|x>0\}
$$
the $|$ should be read as, "such that", therefore the way we read this set is "the set of all $x$ such that $x$ is larger than $0$". To denote that an element is part of some set $X$ we can use $\in$ symbol and say: $$x\in X$$
# Operations
## In
We say an element $a$ is inside a set $A$ using the $\in$ symbol and $\not\in$ it it is not in the set.
### Example
given a set $A=\{a, b, c, d\}$, then $a\in A$, but $e\not\in A$.  
## Complements
Given a set $A$ which is a subset of a universal set $U$, so $A\subseteq U$, we say that the complement of $A$, written as either $A'$, $A^C$ or $\overline{A}$, is everything not in $A$ and in $U$. If we were thinking of this in terms of logic, this would be the [[General Logic#Logical Negation|logical not]].
### Example
Given a set $A=\{a, b, c, d\}$ and a universal set $U=\{a, b, c, d, e, f, g, h\}$. the compliment of $A$ would be: $$A^C=\{e, f, g, h\}$$
## Union
Given a set $A$ and a set $B$ the union of a set $A\cup B$ combines the elements in both sets. If we were thinking of this in terms of logic, this would be the [[General Logic#Logical Disjunction|logical or]]
### Example
$A=\{a, b, c, d\}, B=\{a, d, e, f\}$, then the union would be $$A\cup B=\{a, b, c, d, e, f\}$$
## Intersection
Given a set $A$ and a set $B$ the intersection $A\cap B$ would be the set containing all the values they have in common. If we were thinking of this in terms of logic, this would be the [[General Logic#Logical Conjunction|logical and]].
### Example
$A=\{a, b, c, d\}, B=\{a, d, e, f\}$, then the intersection would be $$A\cap B=\{a, d\}$$
# Vocabulary
* **Disjoint Sets**: 2 sets $A$ and $B$ are disjoint if $A \cap B=\emptyset$.
* **Partition of a set**: let $X$ be an arbitrary set, a **partition of set $X$** would be a set of non-empty subsets of $X$ such that every element $x \in X$ is in exactly one of these subsets.  What this is saying is that the partition $P$ contains subsets of $X$, which could equal the set $X$ itself ($P=\{X\}$ is known as the ==trivial partition==) such that for all elements $x \in X$ there exists a disjoint subset $P \subseteq X$. A nice property of this is: $$\cup{P}=X$$
  An example of a partition of a set would be, given the set $A=\{a, b, c\}$, the a partition $P=\{\{a\}, \{b, c\}\}$.
# Absorbing Set
A set $A\subseteq X$ is an absorbing set if, for each $x\in X$ there is a positive number $s_x$ such that $x\in tA$ whenever $t > s_x$.
