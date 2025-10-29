
## Linear Velocity
* $x(t)$ is the position at some time $t$.
* $v(t)$ is the rate of change of position, also known as velocity, at some time $t$.
* $a(t)$ is the rate of change of velocity, also known as acceleration, at some time $t$.
Using the **Euler Method** the formula for integration is: 
$$
	x(t + \Delta t) = x(t) + v(t) \Delta t
$$
This same derivation of integration also applies to $v(t)$:
$$
	v(t + \Delta t)=v(t)+a(t)\Delta t
$$
This derivation is however not practical when it comes to simulation accuracy and we'd rather use a different method like the Runge-Kutta.
### Solving linear velocity equations
The linear velocity of an object is equal to distance traveled over time. This can be described as $\frac{dx}{dt}$.
## Angular Velocity
### 2D representation
