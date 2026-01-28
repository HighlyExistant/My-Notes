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
# Outline of Geometric Algebra
* ==**Grade**==: Generalization of dimensions. Scalars are grade-0, vectors are grade-1 and bivectors are grade-2. We use $\langle\rangle_r$ to denote a chosen grade, so $\langle ab \rangle_2$ specifies a grade-2 (bivector) part of the geometric product $ab$. This is to say: $$\langle ab\rangle_2 = a\wedge b$$ $$\langle ab\rangle_0=a\cdot b$$
The geometric product can be extended to be associative $$a(bc)=(ab)c=abc$$ meaning that an arbitrary multi-vectors can be written as sums of products. The geometric product is also distributive over addition: $$A(B+C)=AB+AC$$
where $A, B, C$ are multi-vectors of arbitrary grade.
## Division with Vectors
given $C=ab$ we can obtain $$Cb=(ab)b=a(bb)=ab^2$$. We can then define $b^{-1}=b/b^2$. This will make it so that we can grab $a$ by saying $$a=Cb^{-1}$$
# Squaring Bivectors
Using the Axioms we can derive that the square of bivectors $$(a\wedge b)(a\wedge b)=(ab-a\cdot b)(a\cdot b-ba)$$ $$=-ab^2a-(a\cdot b)^2+a\cdot b(ab+ba)$$ $$= (a\cdot b)^2-a^2b^2$$ $$=-a^2b^2\text{sin}^2(\theta)$$
# Geometric Algebra of the Plane
Consider a two dimensional plane, spanned by two orthonormal vectors $e_1, e_2$ such that: $$e_1^2=e_2^2=1, e_1\cdot e_2=0$$
# Page 37