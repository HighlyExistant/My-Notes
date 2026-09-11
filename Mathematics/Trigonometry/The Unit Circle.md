The unit circle is represented by the equation $x^2+y^2=1$. You can think of it as either
* The circle of radius 1 centered at the origin
* The set of all points with distance 1 from the origin
We utilize the unit circle because we can generalize other circles in basis of this one. The circle of radius $r$ for example which would be represented by $x^2+y^2=r^2$ can be thought of as a scaled version of the unit circle: $$\frac{x^2}{r^2}+\frac{y^2}{r^2}=1$$From this generalized equation of a circle, we can derive the trigonometric functions.
# Trigonometric Functions
## Vocabulary
1. $r$: Radius of the circle
2. $\theta$: Angle between the unit vector pointing to a point on the circle $p=(x,y)$ and the basis vector $\langle 1,0\rangle$.
3. $x$: horizontal position in the circle given an angle $\theta$
4. $y$: vertical position in the circle given an angle $\theta$
## Definitions
The standard trigonometric functions are the ==**cosine**== and ==**sine**== functions, which are defined as the $x$ and $y$ positions of the unit circle respectively, given an angle $\theta$. We write these functions as:
* $\cos(\theta):\mathbb{R}\to [-1,1]=\frac{x}{r}$
* $\sin(\theta):\mathbb{R}\to [-1,1]=\frac{y}{r}$
The ==**tangent**== function, $\tan(\theta)$ can be seen as:
* The ratio between the $x$ and $y$ positions, e.g. $\tan(\theta)=\frac{\sin(\theta)}{\cos(\theta)}=\frac{y}{x}$.
* The slope towards the point $(\cos(\theta), \sin(\theta))$ from the origin.
These functions each have their own reciprocal functions:
1. ==**secant**== is defined as $(\cos(\theta))^{-1}=\sec(\theta)=\frac{r}{x}$.
2. ==**cosecant**== is defined as $(\sin(\theta))^{-1}=\csc(\theta)=\frac{r}{y}$.
3. ==**cotangent**== is defined as $(\tan(\theta))^{-1}=\cot(\theta)=\frac{x}{y}$.
# Trigonometric Identities
## Relation between Sine, Cosine and Radius
From the definition of the unit circle, as well as the definition of the trigonometric functions, or even simply the Pythagorean theorem, we can arrive at the conclusion that: $$\cos^2(\theta)+\sin^2(\theta)=1$$
## Relation between Tangent, Secant and Radius
From the previous identity, if we divide it all by $\cos^2(\theta)$ we can obtain $$1+\tan^2(\theta)=\sec^2(\theta)$$
## Relation between Cotangent, Cosecant and Radius
If alternatively we divide by $\sin^2(\theta)$ we obtain $$\cot^2(\theta)+1=\csc(\theta)$$
# Law of Sines
This is a useful law to for when ==**dealing with triangles with unknown sides and or angles**==. It simply states that given a triangle with angles $\alpha, \beta,\gamma$ and respective opposing sides, lengths $a, b, c$ then: $$\frac{\sin({\alpha})}{a}=\frac{\sin{\beta}}{b}=\frac{sin{\gamma}}{c}$$
We can see that for two distinct values this can be translated to: $$\begin{matrix}\sin{(\alpha})=\frac{a}{r}, \sin(\beta)=\frac{b}{r},\sin(\gamma)=\frac{c}{r}\end{matrix}$$ so when you are dividing them by their side lengths, what you are getting is the reciprocal of the radius. e.g. $r^{-1}$.
# Law of Cosines
This is another useful law for dealing with triangles with unknown side lengths, and can be seen as a ==**generalized version of the quadratic equation for arbitrary triangles**==. Given a triangle with a known angle $\gamma$, two known side lengths $a,b$ and an unknown opposing side length $c$, we can obtain that unknown side length through: $$a^2+b^2-2ab\cos(\gamma)=c^2$$
# Properties
## Summation and Difference Rules
Adding angles in $\cos$ function has the following rules: $$\begin{matrix}\cos(\alpha+\beta)=\cos(\alpha)\cos(\beta)-\sin(\alpha)\sin(\beta) \\ \cos(\alpha-\beta)=\cos(\alpha)\cos(\beta)+\sin(\alpha)\sin(\beta) \\ \sin(\alpha+\beta)=\sin(\alpha)\cos(\beta)+\cos(\alpha)\sin(\beta) \\ \sin(\alpha-\beta)=\sin(\alpha)\cos(\beta)-\cos(\alpha)\sin(\beta)\end{matrix}$$
It looks similar to the inner and wedge products respectively between vectors: $$\cos(\alpha+\beta)=\langle\cos(\beta),-\sin(\beta)\rangle\cdot \langle\cos(\alpha),\sin(\alpha)\rangle$$ $$\sin(\alpha+\beta)=\langle\cos(\beta),-\sin(\beta)\rangle\wedge \langle\cos(\alpha),\sin(\alpha)\rangle$$
## Double, Reduction and Half Angle Rules
If you were to multiply two angles, e.g: $\cos(2\alpha)$ then $\cos(2\alpha)=\cos(\alpha+\alpha)$ Solving using the summation rules, it gives you: $$\cos(2\alpha)=\text{cos}^2(\alpha)-\text{sin}^2(\alpha)$$
Similarly with $\sin(2\alpha)$: $$\sin(2\alpha)=2\text{sin}(\alpha)\text{cos}(\alpha)$$
We can use these formulas to help simplify squares of trigonometric functions, such as: $$\begin{matrix}\sin^2(\alpha)=\frac{1-\cos(2\alpha)}{2} \\ \cos^2(2\alpha)=\frac{1+\cos(2\alpha)}{2}\end{matrix}$$
Finally we can derive the half angle formulas to obtain: $$\begin{matrix}\cos(\frac{\alpha}{2})=\pm \sqrt{\frac{1+\cos(\alpha)}{2}} \\ \sin(\frac{\alpha}{2})=\pm \sqrt{\frac{1-\cos(\alpha)}{2}}\end{matrix}$$
