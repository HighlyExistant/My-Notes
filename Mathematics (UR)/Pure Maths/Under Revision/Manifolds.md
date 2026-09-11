### Types of points in a topology 
Say we have a topological space $(X, \Large\tau\normalsize)$ where $S \subseteq X, p \in X$
* An interior point $p$ of $S\Leftrightarrow p \in U$ and $U \subseteq S$ where $U \in \Large\tau$. Translated, this means an interior point $p$ of $S$ means that it's in the interior of $S$.
* An exterior point $p$ of $S\Leftrightarrow p \in U$ and $U \subseteq X \setminus S$ where $U \in \Large\tau$
* $p$ is a boundary point of $S$ if it is neither an interior nor exterior point. This can also be defined as $p$ boundary point of $S \Leftrightarrow U \cap S \neq \emptyset$ and $U \cap (X \setminus S) \neq \emptyset$ where $U \in \Large\tau$
* $p$ accumulation point of $S$ simply means that the point $p$ is not isolated from $S$.
	* For all open sets $U \in \Large\tau\normalsize$ with $p \in U: U \setminus\{p\}\cap S \neq \emptyset$

When we want to denote the set of all **interior points** in $S$ we use $S^{\circ}$ which is defined as:
$$
S^{\circ} := \{ p \in X \mid p \text{ is an interior point of } S \}
$$
When we want to denote the set of all **exterior points** in $S$ we use $Ext(S)$ which is defined as:
$$
Ext(S) := \{ p \in X \mid p \text{ is an exterior point of } S \}
$$
When we want to denote the set of all **boundary points** in $S$ we use $\partial S$ which is defined as:
$$
\partial S := \{ p \in X \mid p \text{ is a boundary point of } S \}
$$
When we want to denote the set of all **accumulation points** in $S$ we use $S'$ which is defined as:
$$
S' := \{ p \in X \mid p \text{ is an accumulation point of } S \}
$$
Some call $S'$ the derivative of set $S$ also called the derived set of $S$.
The final one is the closure of set $S$ which is $\overline{S}$ defined as: 
$$
\overline{S} := S \cup \partial S
$$
or where $A \subseteq X$
$$
	\overline{S} := S \cap\{C|C\subseteq \text{closed under} A\subseteq C\}
$$ This is the smallest closed set that includes $A$, that is the intersection of all closed sets that include $A$.
A manifold is defined as a topological space that resembles a Euclidean Space near each point (like $\mathbb{R}^2$ ).

#### What are Open Sets?
Is a generalization of an open interval $(a, b)$. In the context of topological spaces an **open set** on some topology $\Large{\tau}$ on set $X$, is each member of $\Large{\tau}$.
#### What are Closed Sets?
Is a generalization of a closed interval $[a, b]$. In the context of topological spaces a set $E \subset X$ is closed if and only if its complement (the set of all subsets not in the original topology) is open. We can form a closed set through the union of the boundary set $\partial X$ and the open set $X$. We can denote this as $$\overline{X}:=X\cup \partial X$$
##### Example:
Say we have a topological space $(X, \Large{\tau}\normalsize)$ where $X=\{a, b, c\}$ and $\Large{\tau}$$=\{X, \emptyset, \{a\}, \{a, b\}\}$. 
* The closed set of the subset $\{a\}$ would be $\{b, c\}$.
* The closed set of the subset $\{a, b\}$ would be $\{c\}$.
* The closed set of the subset $X$ would be $\emptyset$ and vice versa.

Another important detail about closed sets is that they contain all their limit points. That is to say that if you had an infinite sequence within some closed set, its limit would be found inside that closed set.
#### What are Convex Sets?
A set $C \in X$ where $X$ is a vector space is said to be convex if 
$$
	tC + (1-t)C \subset C
$$ where $0 \leq t \leq 1$$.
What this is basically saying is that for any 2 points in set $C$, the points in-between are also included in that set. This goes for the usual definition of convexity, because a concave shape does not contain all the points in-between 2 points.
#### What are Balanced Sets?
A set $B \in X$ is balanced if for each $x \in B$ $xt \in B$ where $0 \leq t \leq 1$. This is similar to the convex set, except this time it covers all points from the origin until the value $x$.
#### What is a neighborhood?
In the context of topological spaces, a neighborhood of $p \in X$ on a topological space $X$ is a subset $V$ of $X$ that includes an open set $U$ containing $p$, more formally defined:
$$
	p \in U \subseteq V \subseteq X.
$$
#### What is an Open Cover?
An open cover $C$ on a [[Topology OLD#Topological Space|topological space]] $(X, \Large{\tau})$ is a collection of open sets (subsets) of $X$ with the following properties:
* The union of all subsets of $C$ equals $X$, that is to say $X=\cup C$
* The elements of $C$ are also found in the topology $\Large{\tau}$, that is to say: $c \in \Large{\tau}$ and $c \in C \Rightarrow C$ is an open cover$^{(1)}$
#### What is a Closed Cover?
A closed cover $C$ on a [[Topology OLD#Topological Space|topological space]] $X$ is a collection of closed subsets of $X$ where:
* The union of all subsets of $C$ equals $X$, that is to say $X=\cup C$
* The elements of $C$ are also found in the topology $\Large{\tau}$, that is to say: $c \in \Large{\tau}$ and $c \in C \Rightarrow C$ is an open cover$^{(2)}$
It is very similar to an **open cover**, except for closed subsets.
#### What is a Subcover?
A subcover is a subset of a cover on some topological space $X$, that still covers $X$.
An example of a subcover is: Say you have some topology $\Large{\tau}$ on some set $X$, with some open cover $C$. The subcover would be a subset of $C$ which still covers $X$.
#### Boundedness
When a set is bounded, it means that it is not infinitely big or elongated.
#### Completeness
When a set is complete, it means that it's not missing a gap in the interior of the set, or a boundary. There should be no missing points.
#### Compactness
A topological space $X$ is said to be compact if each open cover of $X$ contains a finite part (subcover) that also covers $X$.$^{(3)}$
#### Extreme Value Theorem
If a function is continuous under a closed interval $[a, b]$, then the function must have a maximum and a minimum on the interval.$^{(4)}$
### Quotient Spaces
Are spaces formed by gluing points based on an [[Relations#Equivalence|equivalence relation]]. This term is known as **identifying** as all these points are now identified by a single coordinate. A good example of this can be a ==mobius strip==, or ==modulus arithmetic==. These types of mappings from one set to another are considered quotient spaces.
* These spaces have the nice property that ==**equivalence is now equality**==.
### Banach Spaces
Are **Complete [[Topology OLD#Normed Vector Space|normed spaces]]**.
### Fréchet space / F-space
It's a **Complete [[Topology OLD#Vector Space|topological vector space]]**. An **F-space** does not need the **local convexity**, Although some mathematical literature might define them to require local convexity.
# References
(1) [E-Academy](https://www.youtube.com/watch?v=auc9CBxi5jM)
(2) [ncatlab](https://ncatlab.org/nlab/show/closed+cover)
(3) [webhomes](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/viro.pdf)'
(4) [khan academy](https://www.khanacademy.org/math/ap-calculus-ab/ab-diff-analytical-applications-new/ab-5-2/v/extreme-value-theorem#:~:text=The%20Extreme%20value%20theorem%20states,a%20minimum%20on%20the%20interval.)
