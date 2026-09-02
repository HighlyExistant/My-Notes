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
# Volumes
Volumes can be represented as integrals over area. We sum over infinitesimal areas of surfaces which compose the volume, similar to how we would in a Riemann sum. We can represent this as: $$\int_a^b A(x)dx$$
Some things to know are:
1. Area is invariant to translation
## Revolution Volumes
If we wanted to gain the volume of a function, which revolves, say $f(x)=x^2$ and $y=3$ 
```tikz
\begin{document}
  \begin{tikzpicture}[domain=0:4]
    \draw[very thin,color=gray] (-0.1,-1.1) grid (3.9,3.9);
    \draw[->] (-0.2,0) -- (4.2,0) node[right] {$x$};
    \draw[->] (0,-1.2) -- (0,4.2) node[above] {$f(x)$};
    \draw[color=red]    plot (\x,{\x * \x * 0.25})             node[right] {$f(x) =x$};
    \draw[color=red]    plot (\x,{3})             node[right] {$y=3$};
    
  \end{tikzpicture}
\end{document}
```
we can revolve it around one of the axis (say the $y$ axis) to obtain a new function, which will revolve around itself. This new function will have an area of the form: $$A=\pi r^2$$where the radius is given by the function being evaluated. In this case since we're rotating around the $y$ axis, we will utilize the distance from the $y$ axis, which would be $\sqrt{x}$ since it is the inverse of $x^2$. It would then be: $$A=\pi x$$
We then remember that the volume can be represented as the integral over area, giving us: $$\int_a^b A dx=\int_0^3\pi x=\frac{9\pi}{2}$$
If instead the volume is represented with a hole in them (form of a donut), you can use the following formula instead: $$A=\pi (r_\text{ext})^2-\pi(r_\text{in})^2$$
## Volumes using Cylindrical Cuts
Occasionally it might be hard to calculate a function from a specific side being revolved,  such as a cubic around the $y$ axis as it would require you to solve for $x$ which is hard to do. Instead we can use cylindrical cuts. Remember that the volume of a cylinder is: $$V=2\pi r^2 h$$It's circumference is $$C=2\pi r$$
We can then find the area of revolution of $f(x)$ by using: $$\int_a^b {2\pi x f(x)}dx$$
* $2\pi x$ being its circumference
* $f(x)$ being height
* $dx$ being thickness
#### Example
The area between $y=2x^2-x^3$ and $y=0$ rotating around the $y$ axis.
* Its circumference would remain $2\pi x$.
* Its height would be $f(x)=2x^2-x^3$
* Its bounds would be $[0,2]$.
The integral would then be: $$\int_0^2{2\pi x(2x^2-x^3)}dx=\int_0^2{2\pi(2x^3-x^4)}$$
Which would result in: $$F(x)=2\pi(\frac{x^4}{2}-\frac{x^5}{5})$$which you then solve as $$F(2)-F(0)=16\pi-\frac{32\pi}{5}$$
# Average Values
## Mean Value Theorem
Assume $f(x)$ is continuous on the interval $[a,b]$. Then $\exists c\in[a,b]$ such that $$f(c)(b-a)=\int_a^b{f(x)}dx$$It just so happens that this value is: $$f(c)=\frac{1}{b-a}\int_a^b{f(x)}dx$$which is the mean of the function on that interval. The geometric intuition is that the product $f(c)(b-a)$ forms a rectangle with the same area as the area under the curve of $f(x)$.
# Solving Trigonometric Integrals
If we have an integral $$\int{\text{sin}^n(x)dx}$$such that $n$ is odd, we can use trig identities to resolve it: $$\int{(1-\text{cos}^2(x))^{n-1}(x)dx}$$and then resolve it using u substitution. We can follow a similar path when integrating for $\text{cos}^n(x)$.

When $n$ is even, we need to use the half angle identities, which are: $$\begin{matrix}\text{cos}^2(x)=\frac{1+\text{cos}(2x)}{2}\\ \text{sin}^2(x)=\frac{1-\text{cos}(2x)}{2}\end{matrix}$$
# Integrals of Rational Functions
We use partial fractions to solve these. The cases are, for a function $$f(x)=\frac{P(x)}{Q(x)}$$
## Product of Linear Factors which don't repeat
$$Q(x)=(a_1x+b_1)...(a_n x+b_n)$$
Then we can rewrite it as $$\frac{A_1}{a_1+b_1}+...+v\frac{A_n}{a_n+b_n}$$
### Example:
$$\int\frac{13x+17}{x^3+2x^2-x-2}dx$$This is a proper rational function, therefore we can use this method: We can then factor the denominator: $$x^3+2x^2-x-2\Rightarrow x^2(x+2)-(x+2)\Rightarrow(x+1)(x-1)(x+2)$$
therefore: $$\frac{13x+17}{(x-1)(x+1)(x+2)}$$
We can see then that it can be rewritten as: $$\frac{A}{x-1}+\frac{B}{x+1}+\frac{C}{x+2}$$
We can rewrite the previous value using the sum rule of fractions: $$\tiny\frac{13x+17}{(x-1)(x+1)(x+2)}=\frac{A(x+1)(x+2)+B(x-1)(x+2)+C(x-1)(x+1)}{(x-1)(x+1)(x+2)}$$
we then expand the values: $${A(x^2+3x+2)+B(x^2+x-2)+C(x^2-1)}$$and group values: $$13x+17=(A+B+C)x^2+(3A+B)x+(2A-2B-C)$$
We then need to solve: $$\begin{matrix}A+B+C=0\\3A + B + 0C=13\\2A-2b-C=17\end{matrix}$$And solve the system of equations. Solving we get: $$\begin{matrix}A=5\\B=-2\\C=-3\end{matrix}$$
Asique nuestra ecuacion final es: $$\frac{5}{x-1}-\frac{2}{x+1}-\frac{3}{x+2}$$
Ahora podemos resolver la integral: $$\int{\frac{5}{x-1}-\frac{2}{x+1}-\frac{3}{x+2}}dx=5\text{ln}(|x-1|)-2\text{ln}(|x+1|)-3\text{ln}(|x+2|)$$
which simplifies to: $$\text{ln}(|\frac{(x-1)^5}{(x+1)^2(x+2)^3}|)$$
## Product of Linear Factors which repeat
### Example
$$\int{\frac{3x^2-x-3}{x^2(x-1)}}$$
## Integral Formulas:
$$\int{\frac{1}{x^2+a^2}}dx=\frac{1}{a}\text{tan}^{-1}(\frac{x}{a})$$
$$\int{\frac{1}{\sqrt{a^2-x^2}}}dx=\text{sin}^{-1}(\frac{x}{a}), a>0$$
## Trapezoid Rule
A way of approximating integrals by grabbing the average using the leftmost and rightmost Riemann sums $L_n, S_n$ respectively:
$$\frac{1}{2}[\sum^n_{i=1}{f(x_{i-1})\Delta x} + \sum^n_{i=1}{f(x_{i})\Delta x} ]=\frac{\Delta x}{2}[\sum^n_{i=1}(f(x_{i-1})+f(x_i))]$$
Due to the of all values apart from the bounds, we can write: $$\frac{\Delta x}{2}[f(x_0 + 2f(x_1) + ... + 2f(x_{n-1})+f(x_n))]$$
The final rules states: $$\int_a^b{f(x)dx\approx \frac{\Delta x}{2}[f(x_0) + 2\sum_{i=1}^{n-1}f(x_i)}+f(x_n)]$$
The area of a trapezoid is: $$A=\frac{1}{2}{h}(a+b)$$where $a, b$ are the bounds and $h$ is height.
### Error
Suppose $|f''(x)|\leq K$ for $a\leq x \leq b$. If $E_T$ and $E_M$ are errors for the trapezoid and middle point rules respectively, then: $$|E_T|\leq \frac{K(b-a)^3}{12n^2}$$
$$|E_M|\leq \frac{K(b-a)^3}{24^2}$$
## Simpson's Rule
Instead of rectangles and triangles, we will utilize parabolas. We take 3 points $P_0 = (x_0,y_0), P_1 = (x_1,y_1), P_2 = (x_2,y_2)$
We then form a system of equations: $$\begin{matrix}y_0=ax_0^2+bx_0+c\\y_1=ax_1^2+bx_1+c\\y_2=ax_2^2+bx_2+c\end{matrix}$$
and we then resolve for $a, b, c$.
# Improper Integrals
these are integrals which have infinity in one of their bounds, e.g.: $\int_a^\infty{f(x)}dx$ or $\int^b_{-\infty}$. This is another way of saying: $$\lim_{t\to\infty}\int_a^\infty{f(x)}dx$$
So we can just resolve the integral up until $$\lim_{t\to\infty}F(t)-F(a)$$
The same logic goes for integrals of the other form $\int^b_{-\infty}$. Another function with infinity as its bounds would be: $$\int_{-\infty}^\infty{f(x)}dx=\lim_{t_1\to\infty}\int_{t_1}^c{f(x)dx}+\lim_{t_1\to\infty}\int_c^{t_2}{f(x)dx}$$
Which would basically cut the area between two arbitrary constants $c$ and sum them up. ==**There is however always the possibility that the limit does not exist, so keep this in mind for all cases**==. If the limit of these exist, we call it a convergent integral, while if it doesn't exist, we call it divergent integral.
## Discontinuous Integrals
Let $\int_a^b{f(x)}dx$ be the integral of a function which is continuous over $[a,b)$, and therefore discontinuous in $b$, then: $$\int_a^b{f(x)}dx=\lim_{t\to b^-}\int_a^t{f(x)dx}$$conversely if $f(x)$ is defined on $(a,b]$ then: $$\int_a^b{f(x)}dx=\lim_{t\to a^+}\int_t^b{f(x)dx}$$
==**As long as the limits exist on both examples**==. Let's then consider another function $f(x)$ which is continuous on $[a,b]\setminus \{c\}$ such that $c\in[a,b]$. Then we need to partition the integral and resolve according to the limits: $$\lim_{t\to c^-}\int_a^t{f(x)}dx+\lim_{t\to c^+}\int_t^b{f(x)}dx$$
# Integrals of Parametric Curves
Parametric curves can be viewed as scalar valued functions which produce vectors, e.g. $f(t)=(x(t),y(t))$. We obtain their integral as follows: $$\int{y(t)x'(t)dt}$$ or more simply: $$\int{ydx}$$
## Line Integrals of Parametric Curves
The line integral of a parametric curve is: $$\int{\sqrt{x'(x)^2+y'(x)^2}}dt$$
