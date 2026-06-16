Integration is all about trying to find the area under the curve of a function $f(x)$. A way we we can estimate this, is by grabbing values at $x$, getting their values $f(x)$ and summing over a range by a certain change of $x$, also known as $\Delta x$. The value of $\Delta x$ is $\Delta x=\frac{b-a}{n}$, and summing over them. This makes it so an approximate solution is: $$\sum^n_{i=1}{f(x_i)\Delta x}$$
As $\Delta x$ gets infinitely small however, we can get a better and better value however. We can say that the area under a curve then, is: $$\lim_{n\to\infty}\sum^n_{i=1}{f(x_i)\Delta x}$$
The way we denote discrete integrals over a range $[a, b]$ is: $$\int_a^b{f(x)dx}$$which represents the area under the curve of a function $f(x)$ over a range $[a,b]$.
# Riemann Sums
Let's revise everything we just talked about. The integral of a function can be represented as the Riemann sum of a function, written as $$\lim_{n\to\infty}\sum^n_{i=1}{f(x_i)\Delta x}$$where every piece is:
1. $\Delta x$: this corresponds to the width of our tiny rectangles, which are supposed to be infinitesimally small. We can represent it as $\frac{b-a}{n}$.
2. $x_i$ represents every value inputted into the function $f$. In a Riemann sum we can represent this as: $x_i=x_0+\Delta x\cdot i$.
3. $x_0$ is the first value of the function, or just $x_0=a$.
Expanded out, this becomes $$\lim_{n\to\infty}\sum^n_{i=1}{f(a+\Delta x\cdot i)\Delta x}$$
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
## Examples
### Example 1
$$\frac{d}{dx}g(x)=\frac{d}{dx}\int_3^x{\frac{t^2-4}{t}}dt=\frac{x^2-4}{x}$$
### Example 2
$$\frac{d}{dx}g(x)=\frac{d}{dx}\int_x^4{\text{cos}(\sqrt{t})}dt=-\frac{d}{dx}\int_4^x{\text{cos}(\sqrt{t})dt}=-\text{cos}(\sqrt{x})$$
### Example 3
$$\frac{d}{dx}g(x)=\frac{d}{dx}\int_2^{x^2+4}{f(t)dt}=f(x^2+4)\cdot 2x$$
## Discrete Integration
==**This is the second part of the Fundamental Theorem of Calculus**==. If $f(x)$ is continuous over the range $[a,b]$, then $$F(x)=\int_a^b{f(x)}dx=F(b)-F(a)$$
This is because you first calculate the area from $[0, b]$, but since integration starts at $a$, you decide to subtract the area from $[0,a]$, thus giving you the area from $[a,b]$.
# Indefinite Integral
This is used for the most general form of the antiderivative: $$\int{f(x)dx=F(x)+C}$$
The $C$ represents an arbitrary constant. Thus the indefinite integral represents a family of functions.
# U Substitution
This is the inversion of the [[Derivatives#The Chain Rule|chain rule]], for use in integrals. When you have an indefinite integral: $$\int g'(x)f(g(x))dx$$we can use the reverse of the [[Derivatives#The Chain Rule|chain rule]] to evaluate it as $$\int{f(u)du}$$
where $du=g'(x)dx$.

For definite integrals, if $g'(x)$ is a continuous function on $[a,b]$ and $f$ is continuous in the range of $u=g(x)$ then:
$$\int_a^b{f(g(x))g'(x)dx}=\int_{g(a)}^{g(b)}{f(u)du}$$

## Examples
### Basic Application
Given a function we want to integrate: $$f(x)=2x\text{cos}(x^2)$$if we make $u=x^2$ then $\frac{du}{dx}=2x$. Solving for the [[Derivatives#Differentials|differential]] we get $du=2xdx$. We can now turn the integral of $f(x)$ into: $$\int2x\text{cos}(x^2)dx=\int \text{cos(u)du}$$
we can then solve this integral and replace the original values: $$\int{\text{cos}(u)du}=\text{sin}(u)=\text{sin}(x^2)$$
### Derivative is not present?
Given a function we want to integrate: $$f(x)=\text{cos}(\frac{1}{3}x)$$we can see the derivative is not on the outside. This doesn't mean we can't use u substitution however. Instead we can view the function as $$f(x)=\frac{1}{3}3\text{cos}(\frac{1}{3}x)$$thus the $\frac{1}{3}3=1$ gets ignored and we can evaluate this integral instead making $u=\frac{1}{3}x$ then $du=\frac{1}{3}dx$ which would allow us to evaluate the integral: $$\int{\frac{1}{3}3\text{cos}(\frac{1}{3}x)dx}=\int{3\text{cos}(u)du}=3\text{sin}(u)=3\text{sin}(\frac{1}{3}x)$$
# Trig Substitution
This is a way of replacing square coordinates with polar coordinates using the trigonometric identities.
# Integrals of Absolute Values
$$\int{|x|dx}=-\frac{|x|}{x}\frac{x^2}{2}$$
# Integral between Curves
The area between two curves is $$A=\int_a^b{[f(x)-g(x)]dx}$$
where $f(x)$ is the upper curve and $g(x)$ is the lower curve.

There might be a possibility that when finding the area between two functions $f(x)$ and $g(x)$, that there exists some $f(x)\leq g(x)$ and that there exists some $f(x)\geq g(x)$. In this case, we can instead get $$A=\int_a^b{|f(x)-g(x)|dx}$$
## In terms of $y$
Sometimes it's easier to grab the integral between a curve by using a function in terms of $y$ instead of $x$. Given $x=f(y)$ and $x=g(y)$, such that $y=c$ and $y=d$ respectively, where $f$ and $g$ are continuous and $f(y)\geq g(y)$ for $c\leq y \leq d$ then the area is: $$A=\int_c^d[f(y)-g(y)]dy$$
