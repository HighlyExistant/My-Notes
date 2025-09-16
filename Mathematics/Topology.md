Is concerned with geometric objects, and continuous deformations between them. W
### Space
is just a set that defines relations with elements within the set. So depending on the objects within your set and the operations that govern those objects, they will define the space that your objects live in.
### Vector Space
vectors are written as $\vec{v}$ the arrow denoting it as a vector, or as $\mathbf{v}$ as a boldened letter.

the vector space needs to cover the following criteria:
* has a zero element also defined as $\vec{0} \in V$ where $V$ is a vector space.
* for all $\vec{u}, \vec{v} \in V$, then $\vec{u} + \vec{v} \in V$.
* For scalar $c$, then $c\vec{v} \in V$.
* There is no notion of distance, and no notion of angles between vectors
### Inner Product Space
* the product is written as $\langle\vec{v}, \vec{w}\rangle$
the inner product space needs to cover the following criteria:
* $\langle a\vec{u} + b\vec{v}, \vec{w}\rangle = a\langle\vec{u}, \vec{w}\rangle + b\langle\vec{v}, \vec{w}\rangle$
* $\langle\vec{v}, \vec{v}\rangle$ with $\langle\vec{v}, \vec{v}\rangle = 0 \Leftrightarrow \vec{v} = 0$
### Normed Vector Space
has the operation $\vert \vert \vec{v} \rvert \rvert := \sqrt{\langle\vec{v}, \vec{v}\rangle}$ which normalizes a vector. Not all norms are defined that way however, and norms are more generally known to have the following criteria:
* $\vert \vert \vec{v} \rvert \rvert \geq 0$ with $\vert \vert \vec{v} \rvert \rvert = 0 \Leftrightarrow \vec{v} = 0$
* $\vert \vert c\vec{v} \rvert \rvert := \vert c \vert \vert \vert \vec{v} \rvert \rvert$ for scalar $c$
* $\vert \vert \vec{u} + \vec{v} \rvert \rvert \leq \vert \vert \vec{u} \rvert \rvert + \vert \vert \vec{v} \rvert \rvert$
### Metric Space
have a concept of distance, and are defined as such for all $x, y, z$ in the space:
* $d(x,y)\geq 0$ and $d(x,y)=0 \text{ iff } x=y$.
* $d(x,y)=d(y,x)$
* $d(x,y)\leq d(x,z) + d(z,y)$ due to [[Geometry#Triangle inequality|the triangle axiom]].
Metric spaces can be defined as a pair $(X, d)$ where $X$ is a set and $d$ is a distance function. Due to this definition of distance, a distance function doesn't necessarily need to be the standard distance function we know $d(x,y)=|x-y|$, it can also be described be an entirely new ways.
#### Examples of alternate metric spaces on $\mathbb{R}$
1. The following metric gives a circular shape that describes distance.
$$d(x,y)=\sqrt{{\sum_{i=1}^{n}}{(x_i-y_i)^2}}$$
2. The following metric gives a square shape that describes distance
$$p(x,y)=\text{max}|x_i-y_i|$$
Every different metric creates a new metric space for some set $X$.
### Topological Space
Getting rid of distance we reach a topological space, which is purely defined in set theory. It works as a foundation for all mathematical spaces.
Say we have a set $X=\{ a,b,c \}$. To build a topology we must first see what are all the subsets of $X$. here it would be:
$$
\{\{a, b, c\}, \{a\}, \{b\}, \{c\}, \{a, b\}, \{a, c\}, \{b, c\}, \emptyset\}
$$
A topology on a set $X$ is a collection $\Large{\tau}$ of **subsets ([[Manifolds#What are Open Sets?|called open sets]])** of $X$ such that:
* $\emptyset, X \in \Large{\tau}$
* The union of subsets of $\Large{\tau}$ is in $\Large{\tau}$ $(\cup_{i}A_{i} \in \Large{\tau}$ for any $A_{i} \in \Large{\tau} \normalsize)$
* the finite intersection of subsets of $\Large{\tau}$ is in $\Large{\tau}$ $(\cap^{n}_{i=1}A_{i} \in \Large{\tau}$ for any $A_{i} \in \Large{\tau}\normalsize)$
More simply put: "$X$ is open, $\emptyset$ is open, the intersection of any two open sets is open, and the union of every collection of open sets is open"$^{(1)}$

The pair $(X, \Large{\tau}\normalsize)$ are called a topological space. Every set $X$ has 2 guaranteed topologies
* $\Large{\tau}_{\normalsize d}\normalsize = \mathcal{P}(X)$ where $\mathcal{P}$ is the powerset, is called the discrete topology
* $\Large{\tau}_{\normalsize i}\normalsize = \{ \emptyset, X \}$ is called the indiscrete or trivial topology.
#### Convergence in Topological Space
Let $(X, \Large\tau\normalsize)$ be a topological space and let $(a_{n})$ where $n \in \mathbb{N}$ be a [[Sequences|sequence]] in $X$.
as
$$
a_{n} \to a \textnormal{ as } n \to \infty: 
$$
$$
\Leftrightarrow 
$$
$$
\textnormal{ for each } U \in \Large\tau\normalsize \textnormal{ with } a \in U \textnormal{, there is } N \in \mathbb{N} \textnormal{ such that for all } n \geq N: a_{n} \in U
$$

$U$ is equal to a subset of $X$ that is also in topology $\Large{\tau}$. a is in subset $U$.
# Hausdorff Space
Is a topological space with a separation property. That is to say that for any distinct points $p \in U_{p}$ and $q \in U_{q}$ inside topological space $(X, \Large\tau\normalsize)$ the intersection between those 2 open sets is the empty set: $U_{p} \cap U_{q} = \emptyset$. In this manner we can make it so convergence can only go towards one value, unlike normal topological spaces. It is guaranteed for a discrete topology to be a valid Hausdorff Space.

# References
(1) Walter Rudin Functional Analysis Second Edition