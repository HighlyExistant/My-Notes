# The Basics
The derivative is the equation $d(x)$ which is tangential to the curve $f(x)$. To start out, the equation for the slope, which will help us derive derivatives, is that of the secant line: $$m_{PQ}=\frac{f(x)-f(a)}{x-a}$$
# Rates of Change
 Suppose $y$ depends on a quantity $x$. We write this function as $$y=f(x)$$If $x$ changes from $x_1$ to $x_2$ then the rate of change would be $$\Delta x=x_2-x_1$$
The quotient of change (or the rate of change) would then be represented by the slope equation: $$\frac{\Delta y}{\Delta x}=\frac{f(x_2)-f(x_1)}{x_2-x_1}$$Which gives us an average rate of change with respect to $x$ and $y$. Similarly we can reach instantaneous rate of change (misnomer) using limits: $$\lim_{\Delta x\to 0}\frac{\Delta y}{\Delta x}=\frac{f(x_2)-f(x_1)}{x_2-x_1}$$
# Derivative As a Function
The following uses Lagrange notation, as is listed in the Notations section. $$f'(x)=\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}$$
where $h$ is some infinitesimal value as expressed in the limit $h\to0$.
# When is a Function Differentiable
If the function $f$ is differentiable in $a$ then $f$ is continuous in $a$. The converse is not necessarily true however, if $a$ is continuous it does not men that $f$ is differentiable in $a$.
## Example
$f(x)=|x|$
$$\lim_{h\to 0}\frac{|x+h|-|x|}{h}$$if we take the limit from the lefthand side we get $-1$ while if we look for it in the righthand side we get $1$, meaning that the limit does not exist, and therefore the derivative doesn't exist. A 
## Ways a function can stop being differentiable
1. If the graph of the function contains a jagged turn. If the function doesn't have a tangent, then it doesn't have a slope, and therefore doesn't have a derivative.
2. If the function is discontinuous in $a$ then it has no derivative in $a$.
3. If the tangent of the function $f$ is vertical, then its limit doesn't exist as it would be a division by $0$.
# Notations
The derivative of a function is the change of the function over time. It has a few different notations that I'll list out here: 
* $\large{\frac{d}{dx}f(x)}$ in **Leibnitz notation**
* $\large{f'(x)}$ in **Lagrange notation**
* $\large{D_x f}$ in **Euler notation**
* $\large{\dot{f}}$ in **Newtons notation**
# Derivatives of Higher Order
The notation for this is also dependent on the notation:
* $\frac{d}{dx}\frac{dy}{dx}=\frac{d^2y}{dx^2}$.
* $(f'(x))'=f''(x)$
* $D_x^2 f$
* $\frac{d}{dt}\dot{f}=\ddot{f}$. 
# Derivative Laws
* The derivative of a constant function $f(x)=c$ is $0$. $\frac{d}{dx}f(x)=0$
# Unique Derivatives
### Exponential
$$\Large\frac{d}{dx}e^x=e^x$$

# Difference Between Notations
* $\frac{dy}{dx}$ tells you that this is the derivative of a function. For example, if you have the variable $y=x^3$, then the derivative $\frac{dy}{dx}=3x^2$.
* $\frac{d}{dx}f(x)$ tells you to differentiate $f(x)\to f'(x)$.
### Summation and Difference Rules
$$\frac{d}{dx}(f(x)+g(x))=\frac{d}{dx}f(x)+\frac{d}{dx}g(x)$$
$$\frac{d}{dx}(f(x)-g(x))=\frac{d}{dx}f(x)-\frac{d}{dx}g(x)$$
### Power Rule
Given a polynomial $x^n$ is $$\frac{d}{dx}x^n=nx^{n-1}$$
### Product Rule
When getting the derivative of the product of two functions $f(x)g(x)$, their derivative is defined as: $$f(x)g'(x)+g(x)f'(x)$$
### Quotient Rule
$$\frac{d}{dx}(\frac{f(x)}{g(x)})=\frac{g(x)f'(x)-f(x)g'(x)}{g(x)^2}$$
### Constant Product Rule
Given a constant function $f(x)=c$ then the product rule becomes: $$cg'(x)$$
### The Chain Rule
This rule applies for derivatives of composite functions (functions of the form $f(g(x))$ or $f(x)^n$). The way we calculate the derivatives of these two functions is as follows.
$$
	\frac{d}{dx}f(g(x))=f'(g(x))\cdot g'(x)
$$
and for the case of $f(x)^n$ it's calculated:
$$
	\frac{d}{dx}f(x)^n=n(f(x))^{n-1}\cdot f'(x)
$$
the chain rule can also apply to functions with just a basic variable such as $f(x)$, but since the derivative of $x=1$, then it gets simplified to just $f'(x)$. This changes however for $f(2x)$ where it would then be $2f'(x)$. As a more generalized result, such that $y=f(u)$ and $u=g(x)$: $$\frac{dy}{dx}=\frac{dy}{du}\cdot\frac{du}{dx}$$ 
# Implicit Differentiation
## Steps
1. Derive both sides with respect to $x$, remembering that $y=f(x)$, using the chain rule.
2. Isolate $y'$.
### Example
$$\begin{matrix}x^2+y^2=4\\2x+2y(y')=0\\2y(y')=-2x\\y'=-\frac{2x}{2y}\\y'=-\frac{x}{y}\end{matrix}$$
When differentiating between variables that are not present, like say $\frac{d}{dx}y^2$ then what you have to do is multiply by its derivative with respect to $x$, that is: $$\frac{d}{dx}y^2=2y\cdot\frac{dy}{dx}$$
# Derivatives of Inverse Trigonometric Functions
## Derivative of $\textbf{sin}^{-1}(x)$ and $\textbf{cos}^{-1}(x)$
$$\large\begin{matrix}\frac{d}{dx}y=\text{sin}^{-1}(x)\\\Rightarrow\frac{d}{dx}\text{sin}(y)=x\\\Rightarrow\text{cos}(y)y'=1\\\Rightarrow y'=\frac{1}{\text{cos(y)}}\\\Rightarrow y'=\frac{1}{\sqrt{1-x^2}}=\frac{d}{dx}\text{sin}^{-1}(x)\end{matrix}$$
cosine is the same except that it's negative: $$\frac{d}{dx}\text{cos}^{-1}(x)=-\frac{1}{\sqrt{1-x^2}}$$
## Derivative of $\textbf{tan}^{-1}(x)$ and $\textbf{cot}^{-1}(x)$
$$\frac{d}{dx}\text{tan}(y)=x\Rightarrow\frac{1}{1+\text{tan}^2(y)}=\frac{1}{1+x^2}=\frac{d}{dx}\text{tan}^{-1}(x)$$
$$\frac{d}{dx}\text{cot}(y)=x\Rightarrow-\frac{1}{1+x^2}=\frac{d}{dx}\text{cot}^{-1}(x)$$
## Derivative of $\textbf{sec}^{-1}(x)$ and $\textbf{csc}^{-1}(x)$
$$\frac{d}{dx}\text{sec}(y)=x\Rightarrow \frac{1}{|x|\sqrt{1-x^2}}=\frac{d}{dx}\text{sec}^{-1}(x)$$
$$\frac{d}{dx}\text{csc}(y)=x\Rightarrow -\frac{1}{|x|\sqrt{1-x^2}}=\frac{d}{dx}\text{csc}^{-1}(x)$$
### Time Derivatives
Some equations relating to physics correspond variables of position such as  and  as functions over time, that is $x=x(t)$. This leads to these positions being differentiable over time, written as:
$$
	\frac{dx}{dt}x(t)=\dot{x}
$$
which is used for velocity. The second derivative $\frac{d^2x}{d^2t}=\ddot{x}$ being acceleration. These $\dot{x}$ and $\ddot{x}$ are also called newtons notation.
# Partial Derivatives
The partial derivative of a function denotes the **change over time** of a **multivariable function**. The reason why it's called a partial derivative is because you only care about one of those variables in the multivariable function, and treat any other variable as a constant.
### Example
Lets say we have some function $f(x, y)=x^2 + xsin(y)$  and we want to compute its partial derivative with respect to $y$. The variables $x$ are treated as constants with derivatives equal to $0$ so if they don't share a term with $y$, they can be ignored. Instead the term we care about is $xsin(y)$ who's derivative is $xcos(y)$. Therefore the answer is $xcos(y)$.
# Gradients
==A gradient is a vector valued function containing the partial derivatives of a function that produces a scalar value==. The symbol for the gradient is **nabla**: $\nabla$. A useful property of the gradient is that it points to the **direction of steepest ascent**, or where the functions value increases, while the length of the vector field shows the steepness of the graph.
### Example
Lets say we have some function $f(x, y)=x^2 + xsin(y)$, similar to the last example, and we want to get its gradient. First we'll need to get the partial derivatives of $x$ and $y$.
$$
		\large{\frac{\partial f}{\partial x} x^2+xsin(y) = 2x+sin(y)}
$$
$$
		\large{\frac{\partial f}{\partial y} x^2+xsin(y) = xcos(y)}
$$
Now that we have both partial derivatives for the multivariable function, we can say that the gradient of this function is
$$
	\begin{bmatrix}
		2x+sin(y) \\
		xcos(y)
	\end{bmatrix}
$$
# Jacobian
Before starting to talk about the Jacobian, read a refresher on [[Linear Algebra#Linear Transformations |what a linear transformation is]]. The Jacobian is a way to encode the derivatives of a vector valued function. Even when the transformation that we're dealing with is not linear, it still has local linearity, where if you zoom in enough, the neighborhood of points around it look linear. **By computing the partial derivatives of that nonlinear function we can figure out what that linear transformation is at that point**.
### Computation
The way you compute the Jacobian in 2 dimensions (But should work in any n dimensional space) for some vector valued function $f(x, y)$ is through the matrix:
$$
	\begin{bmatrix}
		\partial f_1 / \partial x & \partial f_1 / \partial y \\
		\partial f_2 / \partial x & \partial f_2 / \partial y \\
	\end{bmatrix}
$$
This matrix is very similar to the gradient from earlier, except that the gradient is for multivariable functions that produce a scalar value, while ==the Jacobian is for multivariable functions that produce a vector value==.
### Example
This example comes from the following [khan academy video](https://www.youtube.com/watch?v=CGbBbH1e7Yw&list=PLEZWS2fT1672lJI7FT5OXHJU6cTgkSzV2&index=3).
Lets say $f(x,y)=\begin{bmatrix} x + sin(y) \\ y + sin(x) \end{bmatrix}$ . The Jacobian of $f$ usually denoted $J$ is the partial derivative of the 1st component with respect to $x$ and the partial derivative of the 2nd component with respect to $x$ for the first column. Then you take the partial derivative of the 1st component with respect to $y$ followed by the partial derivative of the 2nd component with respect to $y$ for the second column:
$$
	\begin{bmatrix}
		1 & cos(y)\\
		cos(x) & 1
	\end{bmatrix}
$$
# ==**Exercises**==
## Chain Rule Exercises
### Exercise 1
 $(2x+3)^2=4(2x+3)=8x+12$
### Exercise 2
$$\frac{1}{(1+sec(x))^2}$$
$$f(u)=\frac{1}{u^2}, u=1+sec(x)$$
$$f'(u)\Rightarrow u^{-2}=-2u^{-3}, u'\Rightarrow 1+sec(x)=sec(x)tan(x)$$
$$(-2(1+sec(x))^{-3})(sec(x)tan(x))$$
