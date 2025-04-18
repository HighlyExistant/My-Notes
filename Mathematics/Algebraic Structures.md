An algebraic structure is a collection of objects with one or more operations that can be performed on those objects:
### Example
* Addition
* Multiplication
* Subtraction
* Division

### Why use them?
- We use them to draw connections among all the number systems
- We can prove theorems using systems with the same properties

## Groups
A group is a collection of objects usually denoted by a capital letter. Here our basic group will be known as **G**. operations on these groups are denoted using any abstract symbol such as $\oplus$. The reasoning behind this is that operation $\oplus$ can be multiplication, subtraction, addition, division, etc. Here we can find unique properties:
* Associativity: $a \oplus (b \oplus c) = (a \oplus b) \oplus c$
* Identity: $e \oplus g = g \oplus e = g$ $\forall g \in G$
* Inverse: For every $g \in G$ there exists $g^{-1}$ such that $g \oplus g^{-1} = g^{-1} \oplus g = e$
##  Abelian Groups
Are groups that have the added property of commutativity, that is $a \oplus b = b \oplus a$.

## Rings
A ring is a set also denoted by a capital letter. Here our ring is **$R$** with 2 operations than can be denoted with $\oplus$ an $*$, where they have the following properties:
* $R$ is a commutative group (also known as an Abelian Group) under $\oplus$
* $R$ is associative under $*$
* Multiplicative identity: There is an element 1 such that $r * 1 = 1 * r = r \forall r \in R$ 
* The operation $*$ distributes over $\oplus$
$$
a*(b\oplus c)=(a*b)\oplus(a*c)
$$
$$
(a\oplus b)*c=(a*c)\oplus(b*c)
$$
## RNG or Rong's
Have the same properties as a ring without the multiplicative identity

## Fields
A field is a set again denoted by a capital letter. Here our Field is **$F$**. A field is similar to a ring as it has 2 operations $\oplus$ and $*$ except that it has the following additional properties:
* $F$ is a commutative ring under $\oplus$ and $*$ (that is to say that both $\oplus$ and $*$ are commutative)
* Every nonzero $f \in F$ has a multiplicative inverse, that is, some element $g \in F$ for which $f * g = g * f = 1$
## Vector Spaces
A vector space is composed of a set of vectors **$V$** and a set of scalars **$F$** with the following properties:
* $V$ is a commutative group under vector addition
* $F$ is a field under multiplication (specifically scalar multiplication, scalar times vector)
* for each $s \in F$ and $v \in V$, scalar multiplication gives a unique element $s \cdot v \in V$ 
$$
1v=v
$$
$$
a(bv) = (ab)v
$$
$$
a(u+v) = au+av
$$
$$
(a+b)v=av+bv
$$

