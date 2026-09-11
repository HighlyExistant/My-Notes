When we are trying to approximate an integral $F(b)-F(a)$ we will assume that we are given the function $f(x)$. Reviewing the definition of the integral, the simplest way to integrate a value via approximation is using the 
# Different Integration Methods
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
# Runge-Kutta Integration
## Forward-Euler (FE) or RK1
This is a review of [[Derivatives#Linear Approximations|linear approximations]]. Given $\dot{x}=f(x,t)$ and $x=F(x,t)$, then we can consider our current position to be $x_k=F(x,k)$ and we can approximate our next position as $$x_{k+1}=x_k+ f(x_k,t_k)\Delta t$$
## 2nd Order Runge-Kutta
This method of continuous linear approximation Grabs the midpoint t value of integration, then does the linear approximation, before adding it unto the original positional value. $$x_{k+1}=x_k+f(x_k+\frac{\Delta t}{2}f(x_k,t_k), t_k+\frac{\Delta t}{2})$$
alternatively we can write $f_1$ to be the original forward Euler integration: $$f_1=f(x_k,t_k)$$ and $f_2$ to be the midpoint $$f_2=f(x_k+\frac{\Delta t}{2}f_1,t_k=\frac{\Delta t}{2})$$
to then write $$x_{k+1}=x_k+f_2\Delta t$$
### Geometric Intuition
In a usual linear approximation, we would grab the slope $f(x_k,t_k)$ and move $\Delta t$ forward by that slope. Alternatively, what we do in RK2, we grab the slope of the midpoint between $x_k$ and $f(x_k,t_k)$. to grab that slope, obtain the midpoint and input it into $f$, so: $$f(x_k+\frac{1}{2}f(x_k,t_k)\Delta t,\frac{1}{2}\Delta t)$$
