# Quadric Surfaces
These are surfaces of the most general form: $$Ax^2+By^2+Cz^2+Dxy+Exz+Fyz+Gx+Hy+Iz+J$$
1. The terms with $A,B,C$ coefficients are called the degree 2 part
2. The terms with $D,E,F$ coefficients are called the cross product part
3. The terms with $G,H,I$ coefficients are called the degree 1 part
4. The final $J$ term is the constant term.
Through translations and rotations however, it can be brought to be either: $$Ax^2+By^2+Cz^2+J=0$$ or $$Ax^2+By^2+Iz=0$$
## Graphing Quadric Surfaces
To graph such equations, we can replace one of the variables, $x,y,z$ with a constant $k$, and trace through the line of the replaced variable. e.g. For the equation $z=4x^2+y^2$ we could replace $y=k$, and we can trace out the parabola $z=4x^2+k^2$ for increasing values of $k$ through the $y$ axis according to the substituted values of $k$. Alternatively you could graph $4x^2+y^2=k$ and trace circles around the $z$ axis.
# Contour Maps
When given a multivariable function, such as $z=f(x,y)$, it can be difficult to graph out, in 3 dimensions. Instead we can create a contour map, where we pick a specific height, or $z$ value, and map them unto a 2d map, with a specific id, call it $k$, corresponding to its height.
## Level Sets
Given a multivariable function $z=f(x,y)$ a level set is the set of all points which reside in a specific region $z=k$. You are basically grabbing the intersection of the function with the plane at height $k$ along the $z$ axis. It's important to note that the level set of a given multivariable function, will be one degree lower than the funciton, e.g. 
* If a function has 3 variables, the level set will be surface
* If a function has 2 variables, the level set will be a line
* If a function has 1 variable, the level set will be a set.
# Planes
Planes are the higher dimensional equivalent to lines. There are various ways of writing plane equations, such as the standard: $$Ax+By+Cz=0$$Which is just a series of linear equations, which could easily be representable by a matrix. That said a more useful way of writing them out, presents itself when we look at the original line equation. Usually we learn the standard line equation as $y=mx+b$, but we also learn about its other form, in terms of transformations: $y-y_0=m(x-x_0)$ where $m$ represents the slope of the line. Well we can do something similar with plane equations as well. Let $f(x,y,z)$ be some multivariable function, here listed with 3 variables, but which can take an arbitrary amount of parameters. Then, at some point $(x_0,y_0,z_0)$, its normal is given by $\nabla f(x_0,y_0,z_0)$. The plane equation can then be written out as: $$f_x(x_0,y_0,z_0)(x-x_0)+f_y(x_0,y_0,z_0)(y-y_0)+f_z(x_0,y_0,z_0)(z-z_0)$$
## Normal Line
The normal line to $S$ at point $P$ which is perpendicular to the tangent plane, is given by the intersections: $$\frac{x-x_0}{f_x(x_0,y_0,z_0)}=\frac{y-y_0}{f_y(x_0,y_0,z_0)}=\frac{z-z_0}{f_z(x_0,y_0,z_0)}$$
