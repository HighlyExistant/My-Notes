The derivative of a function is the change of the function over time. It has a few different notations that I'll list out here: 
* $\large{\frac{dy}{dx}f(x)}$ in **Leibnitz notation**
* $\large{f'(x)}$ in **Lagrange notation**
* $\large{D_x f}$ in **Euler notation**
* $\large{\dot{f}}$ in **Newtons notation**
### Computation
The equation for computing derivatives is: 
$$
	\lim_{h\to0} \frac{f(x+h)-f(x)}{h}
$$
where $h$ is some infinitesimal value as expressed in the limit $h\to0$. This is very similar to the way you get a line intersecting two points using the equation:
$$\large{\frac{p_y-q_y}{p_x=q_x}}$$
And that is not a coincidence. What the derivative function is doing is changing the function $f$ by an infinitesimal amount and subtracting it by the previous value. After that it is dividing it by $h$. An easier way of computing derivatives is via the power rule where:
$$
	\large{\frac{d}{dx}x^n=nx^{n-1}}
$$
# Partial Derivatives
The partial derivative of a function denotes the **change over time** of a **multivariable function**. The reason why it's called a partial derivative is because you only care about one of those variables in the multivariable function, and treat any other variable as a constant.

### Example
Lets say we have some function $f(x, y)=x^2 + xsin(y)$  and we want to compute its partial derivative with respect to $y$. The variables $x$ are treated as constants with derivatives equal to $0$ so if they don't share a term with $y$, they can be ignored. Instead the term we care about is $xsin(y)$ who's derivative is $xcos(y)$. Therefore the answer is $xcos(y)$.
# Gradients
A gradient is a vector valued function containing the partial derivatives of a function. The symbol for the gradient is nabla: $\nabla$. A useful property of the gradient is that it points to the **direction of steepest ascent**, while the length of the vector field shows the steepness of the graph.
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
This matrix is very similar to the gradient from earlier, except that the gradient is for multivariable functions that produce a scalar value, while the Jacobian is for multivariable functions that produce a vector value.
### Example
This example comes from the following [khan academy video](https://www.youtube.com/watch?v=CGbBbH1e7Yw&list=PLEZWS2fT1672lJI7FT5OXHJU6cTgkSzV2&index=3).
Lets say $f(x,y)=\begin{bmatrix} x + sin(y) \\ y + sin(x) \end{bmatrix}$ . The Jacobian of $f$ usually denoted $J$ is the partial derivative of the 1st component with respect to $x$ and the partial derivative of the 2nd component with respect to $x$ for the first column. Then you take the partial derivative of the 1st component with respect to $y$ followed by the partial derivative of the 2nd component with respect to $y$ for the second column:
$$
	\begin{bmatrix}
		1 & cos(y)\\
		cos(x) & 1
	\end{bmatrix}
$$
