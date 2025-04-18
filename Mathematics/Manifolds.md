### Types of points in a topology 
Say we have a topological space $(X, \Large\tau\normalsize)$ where $S \subseteq X, p \in X$
* An interior point $p$ of $S\Leftrightarrow p \in U$ and $U \subseteq S$ where $U \in \Large\tau$
* An exterior point $p$ of $S\Leftrightarrow p \in U$ and $U \subseteq X \setminus S$ where $U \in \Large\tau$
* $p$ is a boundary point of $S$ if it is neither an interior nor exterior point. This can also be defined as $p$ boundary point of $S \Leftrightarrow U \cap S \neq \emptyset$ and $U \cap (X \setminus S) \neq \emptyset$ where $U \in \Large\tau$
* $p$ accumulation point of $S$ simply means that the point $p$ is not isolated from $S$.
	* For all open sets $U \in \Large\tau\normalsize$ with $p \in U: U \setminus\{p\}\cap S \neq \emptyset$

When we want to denote the set of all interior points in $S$ we use $S^{\circ}$ which is defined as:
$$
S^{\circ} := \{ p \in X \mid p \text{ is an interior point of } S \}
$$
When we want to denote the set of all exterior points in $S$ we use $Ext(S)$ which is defined as:
$$
Ext(S) := \{ p \in X \mid p \text{ is an exterior point of } S \}
$$
When we want to denote the set of all boundary points in $S$ we use $\partial S$ which is defined as:
$$
\partial S := \{ p \in X \mid p \text{ is a boundary point of } S \}
$$
When we want to denote the set of all accumulation points in $S$ we use $S'$ which is defined as:
$$
S' := \{ p \in X \mid p \text{ is an accumulation point of } S \}
$$
Some call $S'$ the derivative of set $S$ also called the derived set of $S$.
The final one is the closure of set $S$ which is $\overline{S}$ defined as:
$$
\overline{S} := S \cup \partial S
$$
A manifold is defined as a topological space that resembles a Euclidean Space near each point (like $\mathbb{R}^2$ ).
### Quotient Spaces
Are spaces formed by gluing points based on an **equivalence relation**. This term is known as **identifying** as all these points are now identified by a single coordinate. A good example of this can be the intersecting lines of a circle that intersect the origin. These types mappings from one set to another are considered quotient spaces.