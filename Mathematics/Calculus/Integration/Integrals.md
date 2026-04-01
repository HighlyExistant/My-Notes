Integration is all about trying to find the area under the curve of a function $f(x)$. A way we we can estimate this, is by grabbing values at $x$, getting their values $f(x)$ and summing over a range by a certain change of $x$, also known as $\Delta x$, and summing over them. This makes it so an approximate solution is: $$\sum^n_{i=1}{f(x_i)\Delta x}$$
As $\Delta x$ gets infinitely small however, we can get a better and better value however. We can say that the area under a curve then, is: $$\lim_{n\to\infty}\sum^n_{i=1}{f(x_i)\Delta x}$$
The way we denote discrete integrals over a range $[a, b]$ is: $$\int_a^b{f(x)dx}$$which represents the area under the curve of a function $f(x)$ over a range $[a,b]$.
## Discrete Integration
If $f(x)$ is continuous over the range $[a,b]$, then $$F(x)=\int_a^b{f(x)}dx=F(b)-F(a)$$
This is because you first calculate the area from $[0, b]$, but since integration starts at $a$, you decide to subtract the area from $[0,a]$, thus giving you the area from $[a,b]$.
# Integral Laws
### Summation and Difference Rules
$$\int{f(x)\pm g(x)dx}=\int{f(x)dx}\pm\int{g(x)dx}$$
### Power Rule
Given a polynomial $x^n$, when integrated it would be:$$\int x^n=\frac{x^{n+1}}{n+1}$$
### Integration by Parts (Reverse Product Rule)
$$
\large
\begin{matrix}
	\frac{d}{dx}f(x)g(x)=f'(x)g(x)+g'(x)f(x) \\
	\int\frac{d}{dx}f(x)g(x)dx=\int f'(x)g(x)dx+\int g'(x)f(x)dx \\
	f(x)g(x)=\int f'(x)g(x)dx + \int g'(x) f(x)dx \\
	\int f(x)g'(x)dx=f(x)g(x)-\int f'(x)g(x)dx \\ \Rightarrow \int \mathbf{u} d\mathbf{v} = \mathbf{u}\mathbf{v} - \int \mathbf{v}d\mathbf{u}
\end{matrix}
$$
### Constant Product Rule
$$\int{cf(x)dx}=c\int{f(x)dx}$$
# Fundamental Theorem of Calculus
States that the integral, is the antiderivative. That is to say that the integral is the inverse of the derivative: $$\frac{d}{dx}\int_a^xf(t)dt=f(x)$$
