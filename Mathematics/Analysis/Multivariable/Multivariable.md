# Vector-Valued Functions
## Limits
Given a vector $\textbf{r}(t)=\langle f(t), g(t), h(t)\rangle$ the limit of $\textbf{r}(t)$ is: $$\lim_{t\to a}\textbf{r}(t)=(\lim_{t\to a} f(t), \lim_{t\to a} g(t), \lim_{t\to a} h(t))$$ 
## Calculating Domain
When getting the domain of a vector valued function $\textbf{r}(t)$ it is the intersection of the domains of each component.
# Partial Derivatives
For a multivariable function $f(x,y,...)$ the partial derivative of a function is it's derivative with respect to a single variable. We write it as: $\frac{\partial f}{\partial x}$ and this would be the partial derivative of $f$ with respect to $x$. It's defined as: $$\frac{\partial f}{\partial x}=\lim_{h\to 0}\frac{f(x+h, y,...)-f(x,y,...)}{h}$$
We can alternatively write this in a different notation: $$\frac{\partial f}{\partial x}=f_x(x,y,...)$$
## Derivate
The derivative of a vector valued function is calculated much the same way as the standard derivative: $$\frac{d\textbf{r}}{dt}=\textbf{r}'(t)=\lim_{h\to 0}\frac{\textbf{r}(t+h)-\textbf{r}(t)}{h}$$
So for a vector $\textbf{r}(t)=\langle f(t), g(t), h(t)\rangle$ the derivative is $\textbf{r}'(t)=\langle f'(t), g'(t), h'(t)\rangle$.
## Linear Approximations
The higher dimension version of a line equation $y=mx+b$ is the plane equation $z=m_1 x+m_2 y + h$. Remember that in the line equation $m$ represents the slope, which can be represented by the derivative $m=\frac{df}{dx}$. We could therefore represent the linearization of a particular function $f(x)$ as $L(x)=f(a)+f'(a)(x-a)$. The linearization of a higher dimensional function works in a similar fashion, but using partial derivatives. For some higher dimensional function $f(w_1,w_2,...)$, the linear approximation can be represented as: $$L(w_1,w_2,...)=f(a_1,a_2,...)+f_x(a_1,a_2,...)(w_1-a_1)+f_y(a_1,a_2,...)(w_2-a_2)+...$$
### The Unit Tangent Vector 
Normalizing the derivative of a vector gives you the unit tangent vector, which represents the unit direction of the curve, represented as: $$T(t)=\frac{\textbf{r}'(t)}{|\textbf{r}'(t)|}$$
## Differentiation
Looking back to the single variable case, we defined a function $f$ to be differentiable at $x_0$ if $$f'(x_0)=\lim_{h\to 0}\frac{f(x_0+h)-f(x_0)}{h}$$
where the limiting term denotes a secant line as the distance between the two points on the $x$ axis, $h$ approaches 0. While this is fine, it can be rewritten in terms of error values. Let $E(h)$ be a function denoting the given error between the $y$ values of the actual derivative $f'(x_0)$ and the secant line $\frac{f(x_0+h)-f(x_0)}{h}$, in a given $h$ value, such that $\lim_{h\to 0}\frac{E(h)}{h}=0$. We can rewrite the terms as: $$\begin{matrix}f'(x_0)=\frac{f(x_0+h)-f(x_0)}{h}\\f'(x_0)h=f(x_0+h)-f(x_0)\\f'(x_0)h=f(x_0+h)-f(x_0)\color{green}+E(h)\end{matrix}$$
Here the added $E(h)$ will go away as $h\to 0$, which is when we want the derivative, and not the secant line, then again it also adjusts it to be the derivative when it is not $0$, so here we have a different way of writing the derivative, but this time in terms of the secant and its error value.

We will utilize the previous conclusion to provide the definition when it comes to the multivariable case. Here since we are dealing with multiple variables, instead of $h$, we will utilize $\Delta x$ and $\Delta y$ to represent that change in a particular variable. We say that a multivariable function is differentiable at $(x_0,y_0)$ if: $$f_x(x_0,y_0)\Delta x+f_y(x_0,y_0)\Delta y+E_1(\Delta x)+E_2(\Delta y)$$where $$\lim_{\Delta x\to 0}\frac{E_1(\Delta x)}{\Delta x}=0, \lim_{\Delta x\to 0}\frac{E_2(\Delta y)}{\Delta y}=0$$This can of course be extended into higher dimensions with more error functions, delta terms and their respective partial derivatives.
### Differentiation Rules
#### Summation Rules
The derivative of the sum/difference of vectors are the sum/difference of the derivatives of the individual vectors, similar to scalar valued functions: $$\frac{d}{dt}[\textbf{u}(t)\pm\textbf{v}(t)]=\textbf{u}'(t)\pm\textbf{v}'(t)$$ 

#### Product Rule
The product rules for both vector products, work the same way as the product rule for scalar valued functions:
$$\frac{d}{dt}[\textbf{u}(t)\cdot \textbf{v}(t)]=\textbf{u}'(t)\cdot\textbf{v}(t)+\textbf{u}(t)\cdot\textbf{v}'(t)$$
$$\frac{d}{dt}[\textbf{u}(t)\wedge \textbf{v}(t)]=\textbf{u}'(t)\wedge\textbf{v}(t)+\textbf{u}(t)\wedge\textbf{v}'(t)$$ $$\frac{d}{dt}[c\textbf{u}(t)]=c\textbf{u}'(t)$$
#### Chain Rule
Given a scalar valued function $f(t)$.
$$\frac{d}{dt}[\textbf{u}(f(t))]=f'(t)\textbf{u}'(f(t))$$
#### Clairaut's Theorem
Suppose $f$ is defined on a disk $D$ that contains the point $(a,b)$. If the functions $f_{xy}$ and $f_{yx}$ are both continuous on $D$ then $$f_{xy}(a,b)=f_{yx}(a,b)$$
Important to note that this applies for higher order partially differentiated functions, as long as we differentiate $f$ by the same variables the same number of times, e.g. $$f_{xyyzy}=f_{yxzyy}$$
## Integrals
Extending the [[Integrals#Fundamental Theorem of Calculus|fundamental theorem of calculus]] to vectors: $$\int_a^b\textbf{r}(t)dt=\textbf{R}(t)|_a^b$$
Generalized this is: $$\int\textbf{r}(t)dt=\langle\int f(t)dt, \int g(t)dt, \int h(t)dt\rangle$$
# Partial Derivatives
The partial derivative of a function denotes the **change over time** of a **multivariable function**. The reason why it's called a partial derivative is because you only care about one of those variables in the multivariable function, and treat any other variable as a constant.
### Example
Lets say we have some function $f(x, y)=x^2 + xsin(y)$  and we want to compute its partial derivative with respect to $y$. The variables $x$ are treated as constants with derivatives equal to $0$ so if they don't share a term with $y$, they can be ignored. Instead the term we care about is $xsin(y)$ who's derivative is $xcos(y)$. Therefore the answer is $xcos(y)$.
## Definition
The definition of a partial derivative, is similar to that of a regular derivative: $$\frac{\partial f}{\partial x}=\lim_{h\to0}{\frac{f(x+h,y)-f(x,y)}{h}}=f_x$$
## Partial Chain Rule
The chain rule for multivariable functions must be generalized for composite functions of any variable to any variable to a single variable. Given a function $h=f\circ g$ then $$\frac{d}{dt}f(g(t))=\frac{df}{dg}\frac{dg}{dt}=f'(g(t))g'(t)$$
For multivariable functions, we can derive a more generalized version of this, wherein given a function $h=f\circ g$ where $f:\mathbb{R}^m\to\mathbb{R}$ and $x,y,...:\mathbb{R}^n\to\mathbb{R}^m$, then let $$h(x,y,...)=f(x(t),y(t),...)$$Then the partial derivative will have $n$ terms and be represented by: $$\frac{\partial h}{\partial t}=\sum_{j=1}^n\frac{\partial f}{\partial x}\cdot\frac{\partial x}{\partial t}$$
The partial derivative will then have $n$ terms.
# Gradients
## Of Scalar-Valued Multivariable Functions
Scalar-Valued Multivariable Functions are functions which are denoted as $f(x,y,...)=z$. Their gradient is denoted by the nabla symbol $\nabla$. It was introduced by **William Rowan Hamilton**, who you might know for being the creator of quaternions. We would say the gradient of $f$ as $\nabla f$. The gradient carries the [[Derivatives#Partial Derivatives|partial derivative]] information in a vector, meaning that the gradient is a vector: $$\large\nabla f=\begin{bmatrix}\frac{\partial f}{\partial x} \\\frac{\partial f}{\partial y}\\ \vdots\end{bmatrix}$$
The gradient would tell you:
* The direction to travel to increase the value of $f$ the fastest.
* The gradient $\nabla f$ is perpendicular to the [[Contours|contour lines]] of $f$.
# Directional Derivatives
When we talk about derivatives, we usually make the rate of change of the function, parallel to a particular axis and or [[Linear Algebra#Basis Vectors|basis vector]]. But what if we wanted to take it in any arbitrary direction?. The way we do this is by using direction derivatives. Their definition is provided by a limit, [[Derivatives#Derivative As a Function|similar to that of derivatives]]: $$\lim_{h\to0}{\frac{f(x+hv)-f(x)}{h||v||}}$$where $||v||$ is the [[Topology OLD#Normed Vector Space|magnitude]] of the vector, to make $v$ normed. We can alter this equation to transform it into: $$\frac{1}{||v||}\frac{d}{dt}f(x+tv){\Huge|}_{t=0}$$
The notation for directional derivatives is [[Derivatives#Notations|similar to that of regular derivatives]], except it has the vector $\vec{\mathbf{v}}$ as its subscript:
* $\nabla_{\vec{\mathbf{v}}}f$
* $\frac{\partial f}{\partial \vec{\mathbf{v}}}$
* $f'_\vec{\mathbf{v}}$
* $D_{\vec{\mathbf{v}}}f$
* $\partial_{\vec{\mathbf{v}}}f$
I will take an excerpt from khan academy to explain some intuition to have:
> *One very helpful way to think about this is to picture a point in the input space moving with velocity $\vec{\textbf{v}}$. The directional derivative of $f$ along $\vec{\textbf{v}}$ is the resulting rate of change in the output of the function. So, for example, multiplying the vector $\vec{\textbf{v}}$ by two would double the value of the directional derivative since all changes would be happening twice as fast.*
## Computation
For the following section, the vectors $\hat{\mathbf{i}}$ and $\hat{\mathbf{j}}$ will be defined as $\hat{\mathbf{i}}=\begin{bmatrix}1 & 0\end{bmatrix}, \hat{\mathbf{j}}=\begin{bmatrix}0 & 1\end{bmatrix}$, and the vector $\vec{\mathbf{v}}$ will be an arbitrary variable.

For $\vec{\mathbf{v}}=\hat{\mathbf{j}}$ it would point upwards. The partial derivative $\frac{\partial f}{\partial y}$ would then tell us the rate of change as we move along the $y$ axis, so as we move along the $\hat{\mathbf{j}}$ direction. We could write this as: $$\frac{\partial f}{\partial y}=\nabla_{\hat{\mathbf{j}}}f$$ If we have a vector then, of $\hat{\mathbf{i}}$ and $\hat{\mathbf{j}}$ components, such that $\vec{\mathbf{v}}=\hat{\mathbf{i}}+\hat{\mathbf{j}}$ the directional derivative would be $$\nabla_{\vec{\mathbf{v}}}f=\frac{\partial f}{\partial x} + \frac{\partial f}{\partial y}$$
The way we compute partial derivatives, we can see it as a weighted sum of their partial derivatives multiplied by the vector components. Take a vector $\vec{\mathbf{v}}=\begin{bmatrix}v_1, v_2, v_2\end{bmatrix}$ and a multivariable function $f(x, y, z)$. their directional derivative would be $$\nabla_{\vec{\mathbf{v}}}f=v_1\frac{\partial f}{\partial x}+v_2\frac{\partial f}{\partial y}+v_3\frac{\partial f}{\partial z}$$
We can also compute this as the dot product of the gradient $\nabla f\cdot \vec{\mathbf{v}}$, which I personally think to be the most compact way of defining it: $$\nabla_\vec{\mathbf{v}}f=\nabla f\cdot \vec{\mathbf{v}}$$
## When Finding the Slope
It is important to note that when you are trying to find the slope of the directional derivative, the vector $\vec{\mathbf{v}}$ must be normalized.
# Local Maximum, Minimum and Saddle Point
We're trying to find the local maximum and minimum of a multivariable function. Lets first define what the local maximum and minimum is for multivariable functions. 
## Definition
Given a function $f: \mathbb{R}^n\to \mathbb{R}$, the point $p=(t_1,t_2,...,t_n)$ is considered the local minimum if: 
1. The point $p$ is in the [[Topology#Interior of a Set|interior]] of the domain $\text{Dom}(f)$.
2. at some small disk $D$ around $p$ inside $\text{Dom}(f)$, the point $p$ pertains to the least valued point.
## How to Find it

Given a point $(t_1,t_2,...,t_n)\in\mathbb{R}^n$ we consider $p$ to be either a local maximum, minimum, or saddle point if at $f(t_1,t_2,...,t_n)$: $$\nabla f(t_1,t_2,...,t_n)=\langle0,0,...,0\rangle$$
Better said, ==**if the gradient is the zero vector**==. We can consider this as a generalization of the local maximum and minimum being found when the derivative is $0$ in a single variable function.
