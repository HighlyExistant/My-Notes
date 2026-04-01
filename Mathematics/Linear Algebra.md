Is the study of linear transformations and the spaces they lie in.
# Definitions
* ==**Orthogonal**==: Two vectors are orthogonal if their inner product is 0. One way to achieve this is if both vectors are perpendicular, or if they are both 0 vectors.
* ==**Orthonormal**==: Two vectors are orthonormal if they are orthogonal and have a magnitude of 1.
# Basis Vectors
A set of vectors that span the entire vector space which are linearly independent (meaning they cannot be written in terms of themselves) and can form every other vector in the vector space as a linear combination of said basis vectors. The basis of this vector defines the coordinate system. The standard basis vectors are $x=\begin{bmatrix}1 & 0\end{bmatrix}, y=\begin{bmatrix}0 & 1\end{bmatrix}$
# Linear Transformations
A linear transformation is usually denoted by a square matrix whose sides are equal to the dimension you are in.  A few properties of these linear transformations are that the origin is pinned in the same place and all the lines that were scaled from said linear transformation aren't curved. For more information I recommend you just watch [3blue1browns linear transformation videos.](https://www.youtube.com/watch?v=fNk_zzaMoSs&list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) which explain them really well.
# Direct-Sum
The direct sum is denoted by $\oplus$ and concatenates two vectors together. If we have a vector $\vec{u}=\begin{bmatrix} a & b\end{bmatrix}$ and another vector $\vec{w}=\begin{bmatrix} d & e & f\end{bmatrix}$  then their direct sum $\vec{u}\oplus \vec{w}=\begin{bmatrix}a & b & c & d & e & f\end{bmatrix}$.
# Tensor Product
The tensor product, denoted as $\otimes$, functions similar to a product of two sets, wherein every element will be multiplied with every other element in the set, as well as be concatenated. For $\vec{u}=\begin{bmatrix} a & b\end{bmatrix}$ and $\vec{w}=\begin{bmatrix} d & e & f\end{bmatrix}$ then $\vec{u} \otimes \vec{w}=\begin{bmatrix}a\cdot d & a \cdot e & a\cdot f & b\cdot d & b \cdot e & b\cdot f & c\cdot d & c\cdot e & c\cdot f\end{bmatrix}$ .
# Linear Form
Is a mapping $L$ between a vector space $V$ to a field $F$: $$L: V\rightarrow F$$
for all $V$. It also satisfies that the identity maps unto the field identity: $$L(0_{V})=0$$ as well as being a [[Category Theory#Homomorphisms|homeomorphism]]: $$L(\lambda\vec{u}+\vec{v})=\lambda L(\vec{u})+L(\vec{v})$$
# Bilinear Form
An upgraded form of linear form, which uses two vector spaces to a field $F$ $$B:V\times V\rightarrow F$$ where it satisfies:
$$B(u, \lambda w + v) = \lambda B(u, w) + B(u,v)$$
$$B(\lambda w + v, u) = \lambda B(w, u) + B(v,u)$$
