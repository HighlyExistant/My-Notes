A function $f$ simply maps a set called the domain $X$ onto some other set called the codomain $Y$, such that for all $x \in X$ there is assigned one element $y\in Y$. We can express this as a mapping $f: X \to Y$.
## Surjective
As we mentioned previously, a function is a mapping from a domain $X$ to a codomain $Y$. Every possible output value that $f$ can produce is called the **range**. If $Range(f)=Y$ then the function is surjective, because the range of possible values covers the set $Y$. for example the function $f: \mathbb{R} \to \mathbb{R} \text{ where } f(x)=x^{2}$ is not surjective because it does not include negative numbers in its range, while the codomain $\mathbb{R}$ does contain negative numbers.
## Injective
This property means that a functions inputs each correspond to a unique output. That is to say that there is no repeating outputs.
# Bijective
Means that it is both ==**Injective**== and ==**Surjective**==.
## Invertible and Bijective
An ==**invertible function**== is a function which contains an inverse. This means that the function $f: X \to Y$ needs to have another function $g: Y \to X$. In simpler terms, a function $f(x)$ must have an inverse $f^{-1}(x)$ such that $(f^{-1}\circ f)(x)=(f \circ f^{-1})(x)=x$.

Through the same reasoning a function is bijective if there is a one-to-one correspondence between the codomain and the domain. For this reason a function is bijective if it is **invertible** (**injective**) and it is **surjective**.
