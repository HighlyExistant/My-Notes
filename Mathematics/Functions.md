A function $f$ simply maps a set called the ==**domain**== $X$ onto some other set called the ==**codomain**== $Y$, such that for all $x \in X$ there is assigned one element $y\in Y$. We can express this as a mapping $f: X \to Y$. It is possible that not all values of $Y$ are in the functions outputs. The set of all possible outputs of $f$ is called the ==**range**==.
## Surjective
As we mentioned previously, a function is a mapping from a domain $X$ to a codomain $Y$. Every possible output value that $f$ can produce is called the **range**. If $\text{Range}(f)=Y$ then the function is surjective, because the range of possible values covers the set $Y$. for example the function $f: \mathbb{R} \to \mathbb{R} \text{ where } f(x)=x^{2}$ is not surjective because it does not include negative numbers in its range, while the codomain $\mathbb{R}$ does contain negative numbers. We say then that functions that are surjective are like maps from $X$ onto $Y$.
### Example
The function $f(x)=x^3$ is surjective, because every value in the domain $\mathbb{R}$ is mapped unto the codomain $\mathbb{R}$. A function does not necessarily need to have unique outputs however. If we choose our domain and codomains carefully, we can make lots of functions surjective. If we needed a mapping $$F:\mathbb{R}\to \mathbb{Z}$$
then the function $\text{floor}(x)$ would be such a surjective function from $\mathbb{R}$ to $\mathbb{Z}$. We can see then that there can be repeated outputs.
## Injective
This property means that a functions inputs each correspond to a unique output. That is to say that there is no repeating outputs. We say this is a one to one relation. These are called ==**embeddings**==, and depending on authors, they will utilize $\hookrightarrow$ to denote it, instead of the normal $\to$, so it would be written as: $$f:X\hookrightarrow Y$$
### Inclusion Maps
(Sometimes called canonical injections, insertions or insertion functions) This is a one to one mapping which sends a subset $A\subset X$ to $X$ in the same elements, basically mapping a subset as the domain, to its superset in its codomain: $$f:A\to X$$
this is usually denoted using $\iota$, and utilizing $\hookrightarrow$ instead of $\to$ to show that it is an embedding (but the notation depends). It is written as $$\begin{matrix}\iota(x)=x & & \iota: A\hookrightarrow X\end{matrix}$$
### Example
The function $f(x)=2x$ has a one to one mapping where each number in the domain corresponds to another unique number in the codomain. The function $g(x)=\sqrt{x}$ is also injective, even if the domain does not cover the entire codomain of $\mathbb{R}$.
# Bijective
Means that it is both ==**Injective**== and ==**Surjective**==. We call this a one to one and onto relation.
## Invertible and Bijective
An ==**invertible function**== is a function which contains an inverse. This means that the function $f: X \to Y$ needs to have another function $g: Y \to X$. In simpler terms, a function $f(x)$ must have an inverse $f^{-1}(x)$ such that $(f^{-1}\circ f)(x)=(f \circ f^{-1})(x)=x$.

Through the same reasoning a function is bijective if there is a one-to-one correspondence between the codomain and the domain. For this reason a function is bijective if it is **invertible** (**injective**) and it is **surjective**.
# Images
An image is similar to a function, except it receives a set of values instead of a single value. Let $X, Y$ be nonempty sets and let $f: X\to Y$, and then let $E\subset X$. The image of $E$ under $f$ is the set $$f(E)=\{f(x)|x\in E\}$$
## Preimage (Inverse Image)
Let $X, Y$ be nonempty sets, and $f: X\to Y$. Then let $G\subset Y$. The preimage of $G$ under $f$ is the set: $$f^{-1}(G)=\{x\in X|f(x)\in G\}$$The preimage is the function that maps the set $Y$ back to $X$. It is important to note that $f^{-1}$ ==**is not the inverse**==, it is the preimage. The preimage will get all the values in the domain of $f$ that will give the values in the range.
#### Example
Given an image $f(x):\mathbb{R}\to \mathbb{R}$ s.t. $f(x)=x^2$, the image for a subset $[0,1]\in \mathbb{R}$ would map values $f([0,1])=[0,1]$. That is because the range of possible values is between $[0,1]$. The preimage however would map values in the range to the domain as $f^{-1}([0,1])=[-1,1]$ because the quadratic function has vertical symmetry.
# Projections
## Flattening Projections
A mapping which takes a product space, and extracts specific information from that space. Given a product set $X\times \dotsb \times Z$ A projection space only grabs a portion of the tuples.
#### Example
Given a set $\mathbb{R}^n$ where $n\in\mathbb{N}$, one possible projection is: $$F:\mathbb{R}^n\to\mathbb{R}^{n-1}$$
or it could even be $$G_i:\mathbb{R}^n\to\mathbb{R}$$where $i$ denotes the index of the component to extract. All of these in some way flatten the space.
