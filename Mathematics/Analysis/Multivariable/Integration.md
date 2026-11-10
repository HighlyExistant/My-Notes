# Integrals
Extending the [[Integrals#Fundamental Theorem of Calculus|fundamental theorem of calculus]] to vectors: $$\int_a^b\textbf{r}(t)dt=\textbf{R}(t)|_a^b$$
Generalized this is: $$\int\textbf{r}(t)dt=\langle\int f(t)dt, \int g(t)dt, \int h(t)dt\rangle$$
# Double Integrals
Double integrals are of the form $$\int_Df(x,y)dA=\int_a^b\int_{g(y)}^{h(y)}f(x,y)dxdy$$
Where $dA=dxdy$ and is meant to represent an area. 
# Square Coordinates
There are two types of integrals. In the textbook I am using these are called type 1 and 2 but here they will be called type $x$ and $y$ respectively:
## Type $x$
These are double integrals of the form: $$\int_a^b\int_{g(x)}^{h(x)}f(x,y)dydx$$We can tell them apart because the outer integral is an integral over $x$. Similarly you can also see that the $h(x)$ and $g(x)$ functions of the inner integrals use $x$ as their variable of choice. Integrals over $x$ you can also view them as being areas with constant valued $x\in [a,b]$ while $y\in [g(x),h(x)]$.
# Type $y$
These are double integrals of the form: $$\int_a^b\int_{g(y)}^{h(y)}f(x,y)dxdy$$You can use a similar intuition for type $y$ as you do with type $x$.
# Polar Coordinates
Doing the translation between square and polar coordinates the $dA$ changes: $$dA=dxdy\to dA=rdrd\theta$$Apart from that, similar intuitions arise from the other types.
# Type $r$
$$\int_a^b\int_{g(r)}^{h(r)}f(x,y)d\theta dr$$
# Type $\theta$
$$\int_a^b\int_{g(\theta)}^{h(\theta)}f(x,y)drd\theta$$
# Turning Paraboloids to Polar Coordinate Integrals
Given some paraboloid $z = ax^2+ay^2+c$ we can turn it into polar coordinates $z=ar^2+c$. Afterwards if the problem tells us to integrate from a plane $z=d$ then we just integrate from the radius of the circle at $d=ar^2+c$ which would be $r=\sqrt{\frac{d-c}{a}}=$. The integral would then look like: $$\int_0^{2\pi}\int_D{r(ar^2+c)drd\theta}$$Where $D$ is the start and end radius of the circle.
# Spherical Coordinates
This replaces $z$ with the angle $\phi$ which represents the angle between the $z$-axis towards the $xy$ plane. You can view it as starting at $z=1$ and ending at $z=-1$. This is to say that $\phi\in[0,\pi]$. The coordinates now look like: 
1. $x=\rho\sin(\phi)\cos(\theta)$
2. $y=\rho\sin(\phi)\sin(\theta)$
3. $z=\rho\cos(\theta)$
Integrating over spherical coordinates makes it so that: $$dV=\rho^2\sin(\phi)d\rho d\theta d\phi$$
So a standard integral will usually look like: $$\int_\alpha^\beta\int_{h_1(\phi)}^{h_2(\phi)}\int_{f_1(\phi,\theta)}^{f_2(\phi,\theta)}f(\rho,\theta,\phi)\rho^2\sin(\theta)d\rho d\theta d\phi$$
