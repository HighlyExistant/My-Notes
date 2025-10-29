# Work
Work $W$ is the energy exerted by an object when it applies a force $F$ to move it some distance $d$, and is proportional to $F$.
$$
	W = Fd
$$
This formula only applies if the force is constant, because work is the area under the curve of the two values $F$ and $d$. If we look at a graph where $y=F$ and $d=x$ then we can see the area under the curve is $Fd$.
```desmos-graph
	left=0;
	right = 10;
	top=10;
	bottom=0;
	---
	y=5
	0<y<5
```
However for a variable $F$ whose force depends on $x$ this will change.
### Example of variable $F$
if we have a force $F=mx$ then $F$ is proportional to $x$ by some constant $m$ giving us a linear graph:
``` desmos-graph
left=0;
right = 10;
top=10;
bottom=0;
---
y=x
y<x
```
The area under this curve is no longer $Fx$ but a rectangular triangle. By using this knowledge we can figure out that the area is $\frac{1}{2}Fx$. We also know that $F=mx$ so we can further extend this to be $W=\frac{1}{2}mx^2$ (keeping in mind that $x$ is supposed to represent some delta time meaning it's $W=\frac{1}{2}m\Delta x^2$).
## Conservative Force and Potential Energy
To denote work done by [[Types of Forces#Conservative Forces|conservative force]] we use $W_c$.
# Weight
You might see work denoted as $\mathbf{W}$ or just a simple $W$, but to differentiate it from work which is also $W$, it is better to say that weight is $F_g$ where the subscript $g$ stands for gravity.

Weight $F_g=mg$ where $m$ is mass and $g$ is gravity. It is equal to the force of gravity acting on an objects mass. Depending on where you are, whether it be the moon or on earth, gravity will change and objects will become lighter or heavier according to that change.
# Energy
There are two types of energies, **kinetic energy** and **potential energy**. 
* ==**Kinetic energy**== denoted as $KE$. Has to do with motion. Anything that moves has kinetic energy. A mass at rest has no kinetic energy. The equation for kinetic energy is 
$$
	\frac{1}{2}\sum_{k=1}^{N}{{m_kv_k^2}}
$$
* ==**Potential energy**== denoted as $PE$. This energy is due to position. The energy is equal to the work done against any restoring forces (conservative forces). If we wanted to use a spring as an example $S_p=kx$, then the **work done by this spring would be its integral**, equal to: $$ \int kx=\frac{1}{2}kx^2$$ The potential energy is a theoretical energy, as it has the potential to become kinetic energy.
