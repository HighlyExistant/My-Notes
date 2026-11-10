# Prerequisites
1. [[Multivariable#Vector-Valued Functions|What are vector functions]]
2. [[Multivariable#Gradients|Gradients]]
# Definition
A vector field is the assignment of a vector to every point in a space. Consider a function $$F:D\to\mathbb{R}^n$$where $D$ is some arbitrary domain. Technically if we explore broader spaces such as [[Algebraic Structures#Vector Spaces|vector spaces]] this applies to much more than just $\mathbb{R}^n$ but for calculus, we just work with this.
# Properties of Gradients in Vector Fields
When we have some surface $f(x,y,z)$ and we grab its gradient $\nabla f$, we're obtaining a vector field which is ==**perpendicular**== to the surface $f$, or grabbing the normal of the surface $f$. 
## Why the normal? Why not the tangent?
Consider the function $$y=x^2+2x$$See how $x$, being an independent variable, changes linearly without change. It could be expressed as $x=t$. If we were to change this function to be a pair of coordinates $(x,y)$, we would describe it as: $$\begin{matrix}x=t\\y=t^2+2t\end{matrix}$$The vector formed by this is then $$v(t)=\langle t,t^2+2t\rangle$$
If we were to derive this vector component wise, it would indeed give us the tangent vector, that being: $$v'(t)=\langle 1,2t+2\rangle$$If we were to obtain the gradient of the function, keeping it as a function of two variables, then we would need to add a new value $z$ and treat it as the level curve constant. $y=x^2+2x$ would then turn into $$z=x^2+2x-y$$The gradient of $z$ would then be: $$\nabla z=\langle2x+2,-1\rangle$$e.g. its normal.
### Expanding Dimensions
Let $z=x^2+y^2-2xy$ be a function on 2 variables $x,y$. Then $x$ and $y$ are independent variables where $x=t$ and $y=u$. The function can be represented then as $$f(t,u)=\langle t,u,t^2+u^2-2tu\rangle$$We can represent its tangent by deriving component wise: $$f'(u,t)=\langle 1, 1, \frac{\partial z}{\partial x}\frac{\partial x}{\partial t}+\frac{\partial z}{\partial y}\frac{\partial y}{\partial u} \rangle$$Which would be: $$f'(u,t)=\langle 1, 1, 0\rangle$$So the tangent appears to be constant. Now the gradient, which will be the normal, will again add a new component $w$ to be the level curve, and denote the new curve as: $w=t^2+u^2-2tu-z$ so the normal will be: $$\nabla w=\langle 2t-2u,2u-2t,-1\rangle$$
# Curl
The curl of a vector field is denoted by the symbol $\nabla\times$. The symbol $\nabla$ is the symbol for the gradient, but it does not seem to be the gradient of a function. Instead we will be abusing notation! $\nabla$ will instead denote a vector of operators, specifically the partial derivatives: $$\nabla=\begin{bmatrix}\frac{\partial}{\partial x} \\ \frac{\partial}{\partial y} \\ \vdots\end{bmatrix}$$The $\times$ will denote the [[Algebraic Structures#Grassman Algebra (Exterior Algebra)|cross product]], which for an operation $a\times b$ can be expressed as the determinant $$\begin{vmatrix}i & j & k \\ a_0 & a_1 & a_2\\b_1 & b_2 & b_3\end{vmatrix}$$where $i, j, k$ are the basis vectors. Therefore the curl of some vector field $F=\langle f_1,f_2,f_3\rangle$ denoted $\nabla\times F$ is:
$$\begin{vmatrix}i & j & k \\\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z}\\f_1 & f_2 & f_3\end{vmatrix}$$where you would originally have multiplied together the components of the second row with the third, you will instead apply their derivative. That is: $\frac{\partial}{\partial x}\cdot f_2\equiv \frac{\partial f_2}{\partial x}$.
# Divergence
The divergence of a vector field is denoted by $\nabla \cdot$ which similar to the curl, we can abuse the notation to get what it's trying to tell us. The $\nabla$ is a vector of operators while the $\cdot$ denotes the dot product, or scalar product. Therefore the divergence of some vector field $F=\langle f_1,f_2,f_3\rangle$ denoted $\nabla\cdot F$ is: $$\frac{\partial f_1}{\partial x}+\frac{\partial f_2}{\partial y}+\frac{\partial f_3}{\partial z}$$Once again, where you would originally have multiplied together the components on similar positions, you will instead apply their derivative.
# Flow Lines
A flow line $\vec{x}(t)$ is a path traced by a vector field $\vec{F}$.
## Definition
A more formal definition goes as follows:

Let $X\subseteq \mathbb{R}^n$. Then a flow line of a vector field $\vec{F}:X\to\mathbb{R}^n$ is a differentiable path $\vec{x}: I\to \mathbb{R}^n$ with the property that $$\forall t\in I(\vec{x}'(t)=\vec{F}(\vec{x}(t)))$$
## Properties
1. The flow lines of some gradient field $\nabla F$ are perpendicular to $F$. This is due to the fact that $\nabla F$ is perpendicular to $F$, and the flow lines simply follow the path of $\nabla F$.