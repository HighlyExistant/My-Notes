Geometric algebra allows us to express scalars, vectors, matrices, quaternions and a whole host of other mathematical structures in one unified manner, to make it easier to deal with. Before starting it is important to introduce a few concepts. This is based off of ==**Doran and Lasenby's Geometric Algebra for Physicists**==.
# Definitions
* ==**Frame**==, which serves as a generalization of a basis vector. These frames will be expressed as $e_i$.
* ==**Geometric (Clifford) Algebras**==: For a vector space with signature $(p, q)$ are expressed as $\mathcal{G}(p,q)$.
* Outer (Exterior) product is written as $A\wedge B$.
* ==**Linear Space**==: Different wording for vector space.
* ==**Orthogonal vectors**==: Two vectors whos scalar products equal 0
* $\delta_{ij}$: Kronecker delta function, defined as: $$\delta_{ij}=\begin{cases}1 \text{ if }i=j \\ 0 \text{ if }i\neq j\end{cases}$$
* ==**Orthonormal basis**==: Normalized basis vectors, defined as $e_i\cdot e_j=\delta_{ij}$
* ==**Einstein summation convention**==: Introduced by Einstein to physics in 1916, this notation simplifies vectors by employing summation notation $$\sum_{i=1}^n{a_ie_i}$$
* ==**Scalar product**==: Also known as dot product, can be derived now as $$a\cdot b=(a_ie_i)\cdot(b_je_j)=a_ib_ie_i\cdot e_j=a_ib_j\delta_{ij}=a_ib_i$$
* ==**Magnitude**==: Denoted as $|a|$, expresses the length or area of something.
# Bases and Dimensions Axioms
1. A vector $b$ is said to be a linear combination of the vectors $a_1, ..., a_n$ if scalars $\lambda_1, ..., \lambda_n$ can be found such that $$b=\lambda_1a_1 + ... + \lambda_na_n=\sum_{i=1}^n\lambda_ia_i$$
2. A set of vectors $\{a_1, ..., a_n\}$ is said to be linearly dependent if scalars $\lambda_1,...,\lambda_n$ (not all zero) can be found such that $$\lambda_1a_1+...+\lambda_na_n=0$$ If such a set of scalars cannot be found, the vectors are said to be linearly independent
3. A set of vectors $\{a_1,...,a_n\}$ is said to span a vector space $V$ if every element of $V$ can be expressed as a linear combination of the set.
4. A set of vectors which are both linearly independent and span the space $V$ are said to form a basis for $V$.
# Quaternion Rules
1. $i^2=j^2=k^2=-1$
2. $ij=-ij=k$
3. $jk=-kj=i$
4. $ki=-ik=j$
# The Outer Product
Also known as the exterior product or the wedge product. Using two vectors the wedge product, written as $A\wedge B$ returns a bivector, which forms a directed plane. A few algebraic properties are that:
![[Topology#Grassman Algebra (Exterior Algebra)]]
# Bivectors
A bivector is given by the wedge product, where it contains both a magnitude and orientation. We can denote bivectors as $\overset{\Rightarrow}{a}$. A way to visualize bivectors, are as oriented planes. The way
# The Geometric Product
Is a combination of the symmetric interior product and the antisymmetric exterior product (outer or wedge product). It is defined as: $$ab=a\cdot  b+a\wedge b$$
which is composed of two different objects summed together, a scalar formed by the inner product, and a bivector formed by the wedge product. Due to the wedge product being antisymmetric: $$ba=a\cdot b + b\wedge a=a\cdot b-a\wedge b$$ Using this identity, it follows that: $$a\cdot b=\frac{1}{2}(ab+ba)$$ and $$a\wedge b=\frac{1}{2}(ab-ba)$$
# Identities
1. $ab=2a\cdot b- ba$ Proof: $$\begin{matrix}ab=2a\cdot b-ba\\=2a\cdot b-(b\cdot a+ b\wedge a)\\=2a\cdot b-(a\cdot b-a\wedge b)\\=2a\cdot b- a\cdot b + a\wedge b\\=a\cdot b + a\wedge b \\= ab \end{matrix}$$
2. $ab=2a\wedge b+ ba$ via the same reason as the previous.
3. Inner Product Identity: $a\cdot b=\frac{1}{2}(ab+ba)$
4. Exterior Product Identity: $a\wedge b=\frac{1}{2}(ab-ba)$
# Outline of Geometric Algebra
* ==**Grade**==: Generalization of dimensions. Scalars are grade-0, vectors are grade-1 and bivectors are grade-2. We use $\langle\rangle_r$ to denote a chosen grade, so $\langle ab \rangle_2$ specifies a grade-2 (bivector) part of the geometric product $ab$. This is to say: $$\langle ab\rangle_2 = a\wedge b$$ $$\langle ab\rangle_0=a\cdot b$$
The geometric product can be extended to be associative $$a(bc)=(ab)c=abc$$ meaning that an arbitrary multi-vectors can be written as sums of products. The geometric product is also distributive over addition: $$A(B+C)=AB+AC$$
where $A, B, C$ are multi-vectors of arbitrary grade.
## Division with Vectors
given $C=ab$ we can obtain $$Cb=(ab)b=a(bb)=ab^2$$. We can then define $b^{-1}=b/b^2$. This will make it so that we can grab $a$ by saying $$a=Cb^{-1}$$
# Squaring Bivectors
Using the Axioms we can derive that the square of bivectors $$(a\wedge b)(a\wedge b)=(ab-a\cdot b)(a\cdot b-ba)$$ $$=-ab^2a-(a\cdot b)^2+a\cdot b(ab+ba)$$ $$= (a\cdot b)^2-a^2b^2$$ $$=-a^2b^2\text{sin}^2(\theta)$$
# Vector times a Bivector
## Inner Product
By multiplying a vector $a$ with bivector $B$ you get $aB=(a_{||}+a_\perp)B$ such that $a_{||}$ is on the plane formed by the bivector $B$ and $a_\perp$ is the part of the vector $a$ perpendicular to $B$. 
Derivation of $a(b\wedge c)$:
$$
\begin{matrix}
	a(b\wedge c)= a\frac{1}{2}(bc-cb) \\
	= \frac{1}{2}(abc-acb) \\
	= \frac{1}{2}((2a\cdot b - ba)c - (2(a\cdot c)-ca)b) \\
	= (a\cdot b)c-(a\cdot c)b+\frac{1}{2}(-bac+cab) \\
	=(a\cdot b)c-(a\cdot c)b-\frac{1}{2}(bac-cab) \\
	=(a\cdot b)c-(a\cdot c)b-\frac{1}{2}((2(b\cdot a)-ab)c-(2(c\cdot a)-ac)b) \\
	=2(a\cdot b)c-2(a\cdot c)b-\frac{1}{2}(-abc+acb) \\
	=2(a\cdot b)c-2(a\cdot c)b+\frac{1}{2}(abc-acb) \\
	=2(a\cdot b)c-2(a\cdot c)b+\frac{1}{2}(bca-cba) \\
	=2(a\cdot b)c-2(a\cdot c)b+\frac{1}{2}(bc-cb)a \\
	=2(a\cdot b)c-2(a\cdot c)b+(b\wedge c)a \\
\end{matrix}
$$
It's taken a long time to get to this result, but now we have the equality $$a(b\wedge c)=2(a\cdot b)c-2(a\cdot c)b+(b\wedge c)a$$
Taking the wedge from the right hand side and placing it into the lefthand side we get the final equation: 
$$
\begin{matrix}
a(b\wedge c)-(b\wedge c)a=2(a\cdot b)c-2(a\cdot c)b \\
= 2a(b\wedge c)=2(a\cdot b)c-2(a\cdot c)b \\
=a(b\wedge c)=(a\cdot b)c-(a\cdot c)b
\end{matrix}
$$
we can see that the righthand side is a vector, meaning that a multiplication between a vector and a bivector is grade lowering. Since the multiplication between a vector and a bivector is grade lowering we will use the dot notation $a\cdot(b\wedge c)=a\cdot b c-a\cdot cb$. This operation with an arbitrary bivector $B$ can be denoted as $$a\cdot B=\frac{1}{2}(aB-Ba)$$
## Wedge Product
The effect of taking the wedge product $a\wedge (b\wedge c)$ is grade raising, giving the identity: $$\begin{matrix}a\wedge (b\wedge c)=\frac{1}{2}(a(b\wedge c)+(b\wedge c)a)\end{matrix}$$
Which is Associative.
## Full Product
we now have the dot product between a vector and a bivector: $$a\cdot B=\frac{1}{2}(aB-Ba)$$ and the wedge product: $$a\wedge  B=\frac{1}{2}(aB+Ba)$$
We can now write the full product as $$aB=a\cdot B+ a\wedge B$$
# What is a Basis Set
A basis was defined above, but basically a basis set contains the number of scalars, vectors, bivectors, which can be classified as a basis. A pseudo scalar represents the highest grade element in a given algebra, which coincides with the dimension of the underlying vector space.
# Geometric Algebra of the Plane
Consider a two dimensional plane, spanned by two orthonormal vectors $e_1, e_2$ such that: $$e_1^2=e_2^2=1, e_1\cdot e_2=0$$
Here the basis set is:
* Scalar Count 1: $1$
* Vector Count 2: $e_1, e_2$
* Bivector Count: 1: $e_1\wedge e_2$
We denote this algebra as $\mathcal{G}_2$. We can now compose multivectors for this basis like:
$$\begin{matrix}A= \alpha_0 + \alpha_1e_1+\alpha_2e_2+\alpha_3e_1\wedge e_2 \\ B=\beta_0 + \beta_1e_1+\beta_2e_2+\beta_3e_1\wedge e_2  \end{matrix}$$
their sum $S=A+B$ is: $$S=(\alpha_0+\beta_0) + (\alpha_1+\beta_1)e_1 + (\alpha_2+\beta_2)e_2 + (\alpha_3+\beta_3)e_1\wedge e_2$$

# Final Operations

This is the final list of operations in geometric algebra. Here we use $\vec{u}, \vec{v} \in V$, where $V$ is a vector space over a field of scalars $F$.  We also consider the bivector $B$.
* Wedge Product:
	* Vector times Vector: $\vec{u}\wedge\vec{v}=\frac{1}{2}(\vec{u}\vec{v}-\vec{u}\vec{v})$.
	* Vector times Bivector: $\vec{u}\wedge\vec{B}=\frac{1}{2}(\vec{u}B-B\vec{u})$.
* Inner Product:
	* Vector times Vector: $\vec{u}\wedge\vec{v}=\frac{1}{2}(\vec{u}\vec{v}+\vec{u}\vec{v})$.
	* Vector times Bivector: $\vec{u}\wedge\vec{B}=\frac{1}{2}(\vec{u}B+B\vec{u})$.

# Page 37