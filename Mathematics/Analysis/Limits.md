The limit is one of the fundamental building blocks of Calculus, as it adds a notion of being able to approach values, which is important for when you are dealing with undefined values. We write out the limit of a given function $f(x)$ as $$\lim_{x\to a}f(x)$$
It's important to note that $f(a)\neq \lim_{x\to a}f(x)$, as the function $f(x)$ can be undefined at $x=a$, but the limit can still exist. For example, the function: $$f(x)=\frac{x-1}{x-1}$$ yields $1$ for all $x\in\mathbb{R}$, except for $x=1$, as it gives a indeterminate form of $\frac{0}{0}$. That said we could assume that if we were to approach $x\to 1$ the value would reach $1$ at $x=1$. We write out this expression as: $$\lim_{x\to 1}{\frac{x-1}{x-1}}$$ in which case we could perform simplifications such as dividing out common factors, reaching the expression: $$\lim_{x\to 1}1=1$$
Now theres various definitions of limits for each mathematical structure, which generalizes upon the notion of approaching a value, which we will explore in future sections.

## Unilateral Limits
Limits can also come from various directions. If you are coming from the left to right side, you write it as such: $$\lim_{a\to n^{-}}$$
If you are coming from the right side, and travelling left, you write it as: $$\lim_{a\to n^{+}}$$
# Limits unto Infinity
What makes limits interesting, is that you can reach numbers, that would generally be regarded as impossible to reach. We can replace the $n$ in the previous limits to $\infty$, and these limits would be able to reach unto the value at infinity.
# Limit Laws
1. $$\lim_{x\to a}f(x)+g(x)=\lim_{x\to a}f(x)+\lim_{x\to a}g(x)$$
2. $$\lim_{x\to a}f(x)-g(x)=\lim_{x\to a}f(x)-\lim_{x\to a}g(x)$$
3. $$\lim_{x\to a} cf(x)=c \lim_{x\to a}f(x)$$
4. $$\lim_{x\to a} f(x)\cdot g(x)=\lim_{x\to a}f(x)\cdot \lim_{x\to a} g(x)$$
5. $$\lim_{x\to a}\frac{f(x)}{g(x)}=\frac{\lim_{x\to a} f(x)}{\lim_{x\to a}g(x)}\text{ s.t. }g(x)\neq 0$$
6. $$\lim_{x\to a}(f(x)^n)=(\lim_{x\to a}f(x))^n\text{ s.t. } n>0$$
7. $$\lim_{x\to a}\sqrt[n]{f(x)}=\sqrt[n]{\lim_{x\to a}f(x)}\text{ s.t. } n>0$$
8. $$\lim_{x\to a}c=c$$
# Finding Limits Approaching Infinity
## Rational Functions
We can find an equation to find the limits of horizontal asymptote by simply getting the inverse of the function. Take the function $$\begin{matrix}f(x)=\frac{3x-2}{x+1}\\\Rightarrow x=\frac{3y-2}{y+1}\\\Rightarrow x(y+1)=3y-2\\\Rightarrow xy+x=3y-2\\\Rightarrow xy+x-3y=-2\\\Rightarrow y(x-3)+x=-2\\\Rightarrow y(x-3)=-2-x\\\Rightarrow y=\frac{-x-2}{x-3}\end{matrix}$$
We can now clearly see that the asymptote of the inverse function 3 because of the $x-3$ term of the denominator. We could also identify that the term which caused this was the coefficient of the $x$ term in the numerator of the original function.

When we're evaluating asymptotes on infinity (horizontal asymptotes), we can note that any number divided by an infinitely large number is $0$. Therefore $$\lim_{x\to\infty}\frac{a}{x}=0$$ The way we can change the asymptote is by summing an $x$ term, as we did previously.
### Using the Limit Laws
There's another way of solving these limits, by simply using the limit laws. Lets use $$\lim_{x\to \infty}\frac{6x-2}{2x+1}$$ We can divide by $x$ on the numerator and denominator to get $$\lim_{x\to\infty}\frac{6-\frac{2}{x}}{2+\frac{1}{x}}$$ We can then use the limit laws to realize that $\lim_{x\to\infty}\frac{2}{x}=\lim_{x\to\infty}\frac{1}{x}=\lim_{x\to\infty}\frac{a}{x}=0$. This simplifies it to $$\frac{6}{2}=3$$ therefore the limit is $3$.
In fact for any polynomial equation $a_0x+a_1x^2+...+a_nx^n$ we take into account the highest exponent. If we use: $f(x)=a_0x+a_1x^2+...+a_nx^n$ and $g(x)=b_0x+b_1x^2+...+b_nx^n$, the limit of the equation: $$\lim_{x\to\infty}\frac{f(x)}{g(x)}=\frac{a_n}{b_n}$$
# Definitions
* ==**Continuity**==: A function is continuous if $$\lim_{x\to a}f(x)=f(a)$$
### L'Hôpital's Rule
For a limit of the form: $$\lim_{x\to c}\frac{f(x)}{g(x)}=\frac{0}{0}\text{ or }\frac{\infty}{\infty}\text{ etc}$$such that 
* $f, g$  are differentiable
* $\lim_{x\to c}f(x)=0\text{ or }\infty$ and $\lim_{x\to c} g(x)=0\text{ or }\infty$ 
* $f'(x)\neq0\text{ or }\infty$, $g'(x)\neq 0\text{ or }\infty$, and $\lim_{x\to c}\frac{f'(x)}{g'(x)}=L$ 
then: $$\lim_{x\to c}\frac{f(x)}{g(x)}=L$$
Useful trick for when the limit approaches $\infty$ and you get an indefinite form of $\frac{\infty}{\infty}$ is to derive the functions multiple times, until the variables cancel out.
#### Indefinite Products
These are of the form $f(x)\cdot g(x)=0\cdot\infty$. We can rewrite this as a quotient to use L'Hôpital's Rule by making it $\frac{f(x)}{(g(x))^{-1}}$ or $\frac{g(x)}{(f(x))^{-1}}$.
#### Indefinite Exponentials
These are of the form $\lim_{x\to c}f(x)^{g(x)}=0^0\text{ or }\infty^0\text{ or }1^\infty$. We can resolve these by applying ==**logarithmic differentiation**==: 
1. Grab your indefinite exponential and turn it into a logarithm:
$$y=f(x)^{g(x)}$$
$$\text{ln}(y)=g(x)\text{ln}(f(x))$$
2. Resolve the limit and check if it gives you a value: $$\lim_{x\to a}\text{ln}(y)=L$$
3. If the previous step gives you $L$ then: $$\lim_{x\to a}f(x)^{g(x)}=e^{L}$$
#### Indefinite Difference
These are of the form $\lim_{x\to c}\frac{f(x)}{a(x)}-\frac{g(x)}{b(x)}=\infty-\infty$. The way we can resolve these is by:
1. Finding a common denominator: $$\frac{f(x)b(x)-g(x)a(x)}{a(x)b(x)}$$
2. Resolving with L'Hôpital's.