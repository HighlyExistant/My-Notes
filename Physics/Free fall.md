The equation for free fall is:
$$
	v_0t+\frac{1}{2}gt^2
$$
Analyzing every component of the equation:
* $v_0$ is the ==initial velocity==. Gravity takes time to build up, so this initial velocity term can denote the velocity at the moment which you throw a ball in the air. 
* $g$ is the constant for gravity usually denoted as $9.80665 \text{m/}\text{s}^2$, often simplified to just $9.8\text{m/}\text{s}^2$. ==Gravity is dependent on where you are==.
* $t$ is our independent variable time. We can look at the state of our system over time, through this variable.
## Derivation: Newtonian Mechanics
Using the equation $F=ma$, we can derive the equation of free fall, using a free body diagram.
![[free_fall_2.svg|center]]
We can write all the forces acting on the system. We can see that $g$ is a vector acting on $m$ over time $t$. All together the acceleration we get $F=mgt$, considering we only want the acceleration we can just remove the $m$ and focus on $gt$. If we now want to integrate to get a vector of velocity we get $\frac{1}{2}gt^2 + C$, where the constant of integration $C$ is the initial velocity which we can also get to act over time $v_0t$. 
## Derivation: Lagrangian Mechanics
Listing out kinetic energy $T=\frac{1}{2}m\dot{y}^2$ and the potential energy $U=mgy$. We now get the equation $L=\frac{1}{2}m\dot{y}^2-mgy$. Writing out the Euler-Lagrange equation we get 
$$
	\frac{\partial L}{\partial\dot{y}}=m\dot{y}\ddot{y}
$$
$$
	\frac{\partial L}{\partial y}=mg\dot{y}
$$
Now we can organize this into the equation:
$$
	m\dot{y}\ddot{y}=mg\dot{y}
$$
cancelling out for acceleration we get
$$
	\ddot{y}=g
$$
If we now integrate this over time we get the velocity:
$$
	\dot{y}=\frac{1}{2}gt^2+C
$$
