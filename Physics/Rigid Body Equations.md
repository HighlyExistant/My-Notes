
## <mark style="background: #F7A51C;">Linear Force</mark>
* $p$, $x$ or $x(t)$ is the position at some time $t$.
* $v$, $\dot{x}$, $v(t)$ is the [[Derivatives#Rates of Change|rate of change]] of position, also known as velocity, at some time $t$.
* $a$, $\ddot{x}$, $a(t)$ is the [[Derivatives#Rates of Change|rate of change]] of velocity, also known as acceleration, at some time $t$.
The equation for linear force is the famous: $$F=ma$$
force equals mass times acceleration.
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
	\tau=a\times F
$$
where $\times$ is the cross product of the vectors. $F$ is the force being applied and $a$ is the axis to the point from the center of mass, This however doesn't truly capture the intent of the equation which is to get the perpendicular force of the $F$ so instead we can replace it as just:
$$
	\tau = aF_{\perp}=aFsin(\theta)
$$
where $\theta$ is the angle between the force vector and the lever arm vector.
## Moment of Inertia
Is defined as the sum of the points of mass $m_i$ times the distance to the axis of rotation $r_i$. This can be portrayed as:$$\sum_{i=0}^n{m_ir_i^2}$$
For an arbitrary object however, this becomes (==**This is the preferred equation**==): $$\int{r_i^2dm}$$where $dm$ is the mass per unit length, or the differential of the volume we're trying to get inertia for. We denote inertia by $I$. 

How do we find $dm$? Well we need to remember that $m=\ \sigma v$, where $\sigma$ is density and $v$ is volume, area, etc. By deriving by $r$ we reach the equation (assuming constant density): $$\frac{dm}{dr}=\sigma\frac{dv}{dr}$$
  And when we [[Derivatives#Differentials|differentiate]] we get that $$dm=\sigma\frac{dv}{dr}dr $$ The full equation then (assuming constant density) is: $$\sigma\int{r^2\frac{dv}{dr}dr}$$

## Angular Momentum
The equation for angular momentum, now that we have all the previous context, is similar to the one for linear force. If the position is equal to $p=mv$, then the angular momentum is: $$L=I\omega$$where $I$ is inertia and $\omega$ is angular velocity.
