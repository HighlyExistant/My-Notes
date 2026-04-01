# Gradients
## Of Scalar-Valued Multivariable Functions
Scalar-Valued Multivariable Functions are functions which are denoted as $f(x,y,...)=z$. Their gradient is denoted by the nabla symbol $\nabla$. It was introduced by **William Rowan Hamilton**, who you might know for being the creator of quaternions. We would say the gradient of $f$ as $\nabla f$. The gradient carries the [[Derivatives#Partial Derivatives|partial derivative]] information in a vector, meaning that the gradient is a vector: $$\large\nabla f=\begin{bmatrix}\frac{\partial f}{\partial x} \\\frac{\partial f}{\partial y}\\ \vdots\end{bmatrix}$$
The gradient would tell you:
* The direction to travel to increase the value of $f$ the fastest.
* The gradient $\nabla f$ is perpendicular to the [[Contours|contour lines]] of $f$.
# Directional Derivatives
When we talk about derivatives, we usually make the rate of change of the function, parallel to a particular axis and or [[Linear Algebra#Basis Vectors|basis vector]]. But what if we wanted to take it in any arbitrary direction?. The way we do this is by using direction derivatives. Their definition is provided by a limit, [[Derivatives#Derivative As a Function|similar to that of derivatives]]: $$\lim_{h\to0}{\frac{f(x+hv)-f(x)}{h||v||}}$$ where $||v||$ is the [[Topology#Normed Vector Space|magnitude]] of the vector, to make $v$ normed. We can alter this equation to transform it into: $$\frac{1}{||v||}\frac{d}{dt}f(x+tv){\Huge|}_{t=0}$$
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
