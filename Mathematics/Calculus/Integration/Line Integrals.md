A line integral will integrate a surface $f(x,y)$ along a curve $C$. Similar to a normal integral the segment of a line integral is denoted as $dS$. This can be written as:
$$
\int_C{f(x,y)dS}
$$
A line integral constrains the two variables $x$ and $y$, and so can't be integrated separately. A line integral $C$ can be expressed with two functions $x(t)$ and $y(t)$, which define the curve for the respective axis. These functions are known as parametric equations, since they are defined based on a $t$ value.
$$
dS=\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2}dt
$$
where
$$
\frac{dx}{dt}=\frac{d}{dt}x(t) 
$$
$$
\frac{dy}{dt}=\frac{d}{dt}y(t) 
$$
$f(x,y)$ represents an arbitrary equation
$$
\Large{\int_{a}^{b}f(x,y)\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2}dt}
$$
to solve for, where $a$ and $b$ are the ranges the $t$ value goes to. **Important to note that these are not limited to 2 dimensions** if we wished to add another variable the equation above would change to:
$$
\Large{\int_{a}^{b}f(x,y, z)\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2+(\frac{dz}{dt})^2}dt}
$$
When it comes to vector fields we are integrating for the work done along a curve in a vector field.. It's written as:
$$
\int_C F \cdot dr
$$
where $F$ is a vector field and $d$r is the vector containing the derivatives of $F$. Finally the operation being performed is the dot product. When this is expanded it can be written as
$$
\Large{\int_C Pdx + Qdy + Rdz}
$$
This also being able to be expanded across dimensions.
