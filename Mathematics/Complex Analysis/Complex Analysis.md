The definition of a complex number is: $$\mathbb{C}=\{a+bi|a,b\in\mathbb{R}, i^2=-1\}$$
## Conjugate
The conjugate of a complex number $z=a+bi$ is expressed as: $$\overline{z}=a-bi$$it has the unique property that: $$z\overline{z}\in\mathbb{R}$$Which can make it useful for cancelling out the imaginary part in equations where the imaginary portion is in the denominator. In the above case $$(a+bi)(a-bi)=a^2+b^2$$
## Operations
Important to note that [[Algebraic Structures#Associativity|associativity]], commutativity and distributivity apply to complex numbers as they do in reals. ==**Addition and subtraction**== on complex numbers is fairly similar to vector addition, you simply add like terms. $$(a\pm bi)\pm(c\pm di)=(a\pm c)\pm(b\pm d)i$$Where things spice up is ==**multiplication**==: $$\begin{matrix}(a+bi)(c+di)=a(c+di)+bi(c+di)\\=ac+adi+bci-bd=\\(ac-bd)+(ad+bc)i\end{matrix}$$Which is fairly similar to the inner product but with subtraction on the reals, and a cross product but with addition in the imaginary. ==**Division**== comes naturally from multiplication: $$\begin{matrix}(a+bi)\frac{1}{c+di}=(a+bi)\frac{1}{c+di}\frac{c-di}{c-di}\\=(a+bi)\frac{c-di}{c^2+d^2}\\=\frac{(ac+bd)+(cb-ad)i}{c^2+d^2}\end{matrix}$$
Simplifying with complex conjugates utilizing $z_0=a+bi$ and $z_1=c+di$ this is: $$\frac{z_0\overline{z_1}}{z_1\overline{z_1}}$$You will quickly notice that the terms $\overline{z_1}$ would cancel to give us $\frac{z_0}{z_1}$.
## Modulus
Written as $|z|$ the modulus of a number is kind of like the absolute value of $z$. it is expressed as the norm of $\mathbb{C}$ which is: $$|z|=\sqrt{a^2+b^2}$$We can also ==**calculate distance**== between two complex numbers $z_0,z_1$ using this modulus as a metric: $$d(z_0,z_1)=|z_0-z_1|$$
## Polar Coordinates
We can express these values as polar coordinates (via magnitudes and angles) as follows: $$a+bi=r(\text{cos}(\theta)+\text{sin}(\theta)i)$$where $r$ is the distance from the origin $$r=(a^2+b^2)^{\frac{1}{2}}$$
and $\theta$ is the angle between $a$ and $b$, which if you want to be specific, can be obtained from $\text{atan}(\frac{b}{a})$. We can alternatively rewrite this using the Euler identity: $$re^{\theta i}=r(\text{cos}(\theta)+\text{sin}(\theta)i)$$which heavily compresses the writing.
## Exponents and Roots
Expressing the complex number as a polar coordinate we can express a root as: $$\sqrt[n]{re^{\theta i}}=r^{\frac{1}{n}}e^{\frac{\theta i}{n}}$$
If we translate this back to polar coordinates, this becomes: $$r^{\frac{1}{n}}(\text{cos}(\frac{\theta}{n})+\text{sin}(\frac{\theta}{n})i)$$
You can see how this can be generalized into simply exponents as: $$re^{\theta ni}=r^{n}e^{\theta ni}$$
## Topology on Complex Numbers
A [[Topology|topology]] on complex numbers that we utilize in complex analysis can be defined using its metric, and acquiring a function to obtain its open balls: $$B_d(z,\epsilon)=\{w|d(z,w)<\epsilon\}$$We can then utilize this to impose a basis on the complex numbers: $$\mathscr{B}=\{B_d(z,\epsilon)|z\in\mathbb{Z},\epsilon>0\}$$And then get the topology induced by the basis.
## Iteration
An iteration can be thought of as repeated composition. The notation used for it is $f^n(z)$ not to be confused with powers of $f$. A quick example of how this looks for $f^3$ would be $$f^3(z)=f(f(f(z)))$$
## Quadratic Polynomials
Unlike real quadratic polynomials, which are of the form $ax^2+bx+c$, containing 3 constants, it is possible to find a constant $c$ in complex polynomials $z^2+c$ such that they correspond to $a$ and $b$. 

Given $a,b$ and $d$ in $\mathbb{C}$ we can define $c=ad+\frac{b}{2}-(\frac{b}{2})^2$, and by letting $\varphi(z)=az+\frac{b}{2}$ one can check that $p(z)=\varphi^{-1}(f(\varphi(z)))$ for all $z$.
### Julia Set
Named after Gaston Julia, it is all points $z\in\mathbb{C}$ of $f(z)=z^2+c$ in which the behavior of iterates is "==**chaotic**==" in a [[Topology#Neighborhoods|neighborhood]]. A chaotic point is sensitive to change, so nearby points will travel to entirely different directions.
### Fatou Set
Named after Pierre Fatou, it is all points $z\in\mathbb{C}$ of $f(z)=z^2+c$ in which the behavior of iterates is "==**normally**==" in a [[Topology#Neighborhoods|neighborhood]]. A normal point is relatively predictable, meaning nearby points travel to similar directions.
#### Examples
This example is taken from [The following youtube video](https://www.youtube.com/watch?v=eqNdkbHF93Y&list=PLi7yHjesblV0sSfZzWdSUXGO683n_nJdQ&index=8):

Let $f(z)=z^2$, then $f^n(z)=z^{2^n}$
1. For points $|z|<1$ the iterate $|f^n(z)|\to 0$ as $n\to \infty$ therefore: $\lim_{n\to\infty}f^n(z)=0$. 
2. For points $|z|>1$ the iterate $|f^n(z)|\to \infty$ as $n\to \infty$ therefore: $\lim_{n\to\infty}f^n(z)=\infty$. 
3. If $|z|=1$ then $f^n(z)=1$ for all $n$
If we grab a neighborhood for a point for which $|z|=1$ there will be points that shoot off to $\infty$ and others which converge to $0$. We then conclude that: $$J(f)=\{z||z|=1\}$$is the locus of chaotic behaviour, and $$F(f)=\{z||z|>1\}\cup\{z||z|<1\}$$form the locus of normal behaviour.
### Basin of Attraction to Infinity
The set $$A(\infty)=\{z|f^n(z)\to \infty\}$$is the basin of attraction to infinity. It is a:

#### Theorem
The set $A(\infty)$ is open, connected and unbounded. It is contained in the Fatou set of $f$. The Julia set of $f$ coincides with the boundary of $A(\infty)$, which is closed and bounded subset of $\mathbb{C}$.
1. Julia Set is closed and bounded (and is the boundary of $A(\infty)$)
2. Fatour set is open and unbounded, and contains $A(\infty)$
3. $J(f)\cap F(f)=\emptyset$
4. Both Julia and Fatou sets are completely invariant under $f$ meaning $f(J)=J$ and $f(F)=F$.
### Fixed Points
A fixed point is such a point where $f(x)=x$, meaning that no matter how iterated the function is $f^n(x)=x$. We can find such fixed points by solving the equation $f(x)=x$.
#### Example
Let $f(x)=x^2-2$. If we solve the equation $$\begin{matrix}f(x)=x\\\Rightarrow x^2-2=x\\\Rightarrow x^2-2-x=0\\\Rightarrow (x-2)(x+1)\end{matrix}$$Meaning that $f$ has two fixed points which are $-1$ and $2$.
### Orbits
#### Periodic Orbits
A periodic orbit corresponds to multiple values which loop unto one another. 
##### Example
Take for example: $f(z)=z^2-1$. If we put the values for example:
1. $f(0)=-1$
2. $f(-1)=0$
So we say the orbit of $f$ at that point is $0, -1, 0, ...$ of period 2 since there are 2 values in the orbit.  The point $1$ we call ==**pre-periodic**== since it follows the trajectory: 
3. $f(1)=0$
4. $f(0)=-1$
5. $f(-1)=0$
to which it then repeats. If we select $\phi=\frac{1+\sqrt{5}}{2}$ we actually obtain back the same number. This is then a fixed point. We can show that for any point outside the range (of this particular function) $[-\phi,\phi]$ it will be in the basin of attraction to infinity. 

We represent the orbit of a value in the set as: $\{f^n(z)\}$
#### Theorem
Let $f(z)=z^2+c$, and let $R=\frac{1+\sqrt{1+4|c|}}{2}$, let $z_0\in\mathbb{C}$, if for some $n>0$ we have that $|f^n(z_0)|>R$, then $f^n(z_0)\to\infty$, i.e. $z_0\in A(\infty)$, so $z_0\not\in K(f)$. ($K(f)$ ==**is the filled in Julia Set**==).
#### Algorithm to Find Filled in Julia Set
1. Given $c$ calculate the radius $R=\frac{1+\sqrt{1+4|c|}}{2}$
2. Choose a window of $z$ values you want to check, namely: $W=\{x+yi|a\leq x \leq b, c\leq y \leq d\}$
3. Pick a large $n$ for it to check, the larger the number, the more accurate the picture.
4. $\forall z\in W$ choose a pixel for that $z$.
5. Calculate the iterates of $z$ e.g. $f^n(z)$, and if one of the iterates satisfies $|f^n(z)|>R$ then color it white since it is not in the filled in julia set.
6. If $n$ is reached in the iterates and hasn't left then color it black, since it is likely that it is in the filled in julia set.
### The Mandelbrot Set
Let $J$ be the Julia Set. The Mandelbrot set is: $$M=\{c\in\mathbb{C}|J(z^2+c)\text{ is connected}\}$$
We can check this using the following theorem:
#### Theorem
Let $f(z)=z^2+c$. Then $J(f)$ is connected if and only if $0\not\in A(\infty)$ e.g. the orbit $\{f^n(0)\}$ is bounded under iteration.

Another theorem is:

$$c\in M\Leftrightarrow \forall n\geq 1,|f^n(0)|\leq 2\text{ s.t. }f(z)=z^2+c$$
# Derivatives
The [[Derivatives#Derivative As a Function|derivative]] is analogous to the real number case, except now it's with complex numbers.
# Exponential
Not to be confused by raising a complex number to a power $z^n$ the complex exponential will take a $e^z$. We define it as $$e^z=e^x\cdot e^{iy}=e^{x+iy}$$
The modulus of $$|e^z|=|e^x||e^{iy}|=e^x$$ since $e^{iy}$ lies on the unit circle and $e^x$ is always positive and we're simply retrieving the absolute value.

The exponential is periodic, meaning that $$e^{z+2\pi i}=e^z$$The angle formed is: $$\text{arg}(e^z)=\text{arg}(e^xe^{iy})=y + 2\pi k\text{ s.t. }k\in\mathbb{z}$$
Other properties of the exponential hold:
1. $e^z e^w=e^{z+w}$
2. $\frac{1}{e^z}=e^{-z}$
## Derivative of Exponential
Remembering the [[Derivatives#Exponential|exponential derivative]] we can see that $$e^z=e^x\text{cos}(\theta)+e^x\text{sin}(\theta)i$$Considering we are differentiating in terms of $x$, and $\theta$ is constant, there is no difference and therefore: $$\frac{d}{dz}e^z=e^z$$
For $$\frac{d}{dz}e^{az}=a\cdot e^{az}$$
by [[Derivatives#The Chain Rule|chain rule]].
# Trig Functions
Using the identities we can also find that: $$\begin{matrix}\text{cos(z)}=\frac{e^{iz}+e^{-iz}}{2} & & \text{sin(z)}=\frac{e^{iz}-e^{-iz}}{2i}\end{matrix}$$
1. Properties of [[Angles#Formulas for the Sum and Difference of Angles|addition of angles]] holds.
2. Periodicity of trig functions hold.
3. [[Unit Circle#Trigonometric Identities|Trig identity]] holds.
4. $$\text{sin}(z+\frac{\pi}{2})=\text{cos}(z)$$
## Trig Functions
Derivative of the functions: $$\frac{d}{dz}\text{sin}(z)=\text{cos(z)}$$
Similarly: $$\frac{d}{dz}\text{cos}(z)=-\text{sin(z)}$$
### Simplifying Complex Trig Functions
$$\text{sin}(x+iy)=\text{sin}(x)\text{cosh}(y)+i\text{cos}(x)\text{sinh}(y)$$
$$\text{cos}(x+iy)=\text{cos}(x)\text{cosh}(y)-i\text{sin}(x)\text{sinh}(y)$$
# Natural Logarithm
We can retrieve the natural log as follows: $$\begin{matrix}z=re^{i\theta}\\\Rightarrow \text{ln}(z)=\text{ln}(r)+i\theta\end{matrix}$$converting back we can remember that $r=|z|$ and $\theta=\text{arg}(z)$. This means that the complex logarithm, titled $\text{Log}$ the principal logarithm is: $$\text{Log}(z)=\text{ln}|z|+\text{arg}(z)i$$
1. Its domain is: $\mathbb{C}\setminus \{0\}$.
2. It is continuous and analytic on $\mathbb{C}\setminus (-\infty,0]$.