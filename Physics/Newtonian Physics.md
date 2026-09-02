# Force
The standard equation for force in physics was derived by newton: $$F=ma$$Where $m$ is mass and $a$ is acceleration which is the 2nd [[Derivatives|derivative]] of position in the problem. Force is worked in newtons $N$.
# Work
The concept of **work**, denoted as $W$. It's used when a force acts through a distance. The definition of work is $$W=Fd=mad$$
Where $d$ is the distance. The work is worked in newtons times meter ($N\cdot m$), or **jules** $J$.
## Non Constant Work
When work is non constant, we need to integrate with respect to a given variable, meaning that work suddenly becomes an integral. Suppose an object is moving in an axis $x$ from $x=a$ to $x=b$. Then the function of force $f(x)$ is continuous on $[a,b]$. We sum all timesteps of $\Delta x$, and we get that $$W_i\approx F(x_i^*)\Delta x$$We can convert this into an integral: $$\int_a^bf(x)dx$$
## Hooke's Law
This is a law in relation to springs to find the work in contracting springs:

The force $f(x)$ required to contract or stretch a spring in the spring $x$ units, more than its resting state, also known as its ==**equilibrium length**==, is given by $f(x)=kx$ such that $k$ is the ==**spring constant**==. This basically states that the force is proportional to the distance $x$ of the stretched spring:
### Work for Hooke's Law
Let $\ell$ be the equilibrium length, and $f(x)=kx$. The work produced by the spring would be: $$\int_{a-\ell}^{b-\ell}{f(x)}dx$$If we consider the origin to not be at the equilibrium length. Whenever obtaining the integral, assume the equilibrium length is the origin, to then obtain just: $$\int_{a}^{b}{f(x)}dx$$
### Notation for Hooke's Law
* ==**Equilibrium Length**==: Is the length of the spring with no spring force, usually denoted $\ell$.
* ==**Spring Force**==: Is the force that a spring exerts when it is stretched by some amount $x$. The force the spring exerts is directly proportional to $x$ by some proportionality constant $k$, also known as the spring constant. Basically $F_p=kx$.
* ==**Restoring Force**==: Is the force that a spring exerts when it is being pulled which is **equal in magnitude to the spring force $F_p$**, but opposite in direction. $F_s=-F_p$ or $F_s=-kx$.
* ==**Spring Constant**==: Also known as $k$, is the proportionality constant of the spring. If we were for example to have some force $F_p$ exerted unto a spring which moves it some $x$ amount, then $k=\frac{F_p}{x}$. The spring constant, basically tells you **how much force needs to be exerted to stretch the spring by some amount**. The larger the spring constant, the stiffer a spring.
* ==**Spring Length**==: The total length of a spring, which is $\ell+x$ where $\ell$ is the equilibrium length and $x$ is the amount stretched. When working with forces on these springs, we need to keep track of the $x$ component as it changes over time. For example in a spring pendulums we need to keep track of the mass at the end with the pendulums rotation which is $(\ell+x)\dot{\theta}$, and the changing spring length $\dot{x}$.