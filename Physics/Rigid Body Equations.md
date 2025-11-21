
## <mark style="background: #F7A51C;">Linear Force</mark>
* $p$, $x$ or $x(t)$ is the position at some time $t$.
* $v$, $\dot{x}$, $v(t)$ is the rate of change of position, also known as velocity, at some time $t$.
* $a$, $\ddot{x}$, $a(t)$ is the rate of change of velocity, also known as acceleration, at some time $t$.
Using the **Euler Method** the formula for integration is: 
$$
	x(t + \Delta t) = x(t) + v(t) \Delta t
$$
This same derivation of integration also applies to $v(t)$:
$$
	v(t + \Delta t)=v(t)+a(t)\Delta t
$$
This derivation is however not practical when it comes to simulation accuracy and we'd rather use a different method like the Runge-Kutta.
## Net Force
Is the total sum of forces in your problem. It's usually represented by the symbol $F_{net}$.
### Solving linear velocity equations
The linear velocity of an object is equal to distance traveled over time. This can be described as $\frac{dx}{dt}$.
## <mark style="background: #971f21;">Angular Force</mark>
* $r(t)$ is the rotation at some time $t$.
* $\omega(t)$ is the angular velocity at some time $t$.
* $\alpha(t)$ is the symbol for angular acceleration at some time $t$.
The angular force, is represented as ==**torque**== or $\tau$. The way we calculate torque is using the perpendicular force of linear velocity is:
$$
	\tau=r\times F
$$
where $\times$ is the cross product of the vectors, This however doesn't truly capture the intent of the equation which is to get the perpendicular force of the $F$ so instead we can replace it as just:
$$
	\tau = rF_{\perp}=rFsin(\theta)
$$
where $\theta$ is the angle between the force vector and the lever arm vector.
### 2D representation
