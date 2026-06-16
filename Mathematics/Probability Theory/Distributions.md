# Probability Density Function (PDF)
A probability density function over a given range of values gives the continuous probability of a random variable giving a specific value. 
# Probability Mass Function (PMF)
Also known as the Discrete Probability Density Function, which functions similarly to a PDF but for discrete cases.
## Cumulative Distribution Function (CDF)
Let $f(x)$ be a probability density function. The CDF is the probability of a variable $X\sim f(x)$ such that $X\leq x$. This is usually denoted as $$F_X(x)=P(X\leq x)\text{ }\forall x\in\mathbb{R}$$
This value is actually just the integral of our pdf over $x$, that is $$F_X(x)=\int_{-\infty}^{x}{f(x)dx}$$
If we wanted to get it within a semi closed interval, that is $P(a \lt X \leq b)$, is $$P(a \lt X \leq b)=F_X(b)-F_X(a)$$==**The CDF is simply the integral of the PDF and the PDF is the derivative of the CDF**==.
## Sampling from the PDF using the CDF (inverse transform sampling)
We can restrict the CDF of $f(x)$ within an interval $[a,b]$
by dividing by the proportionality constant $c=F_X(b)-F_X(a)$ giving the following PDF and CDF respectively: $$p_X(x)=\frac{f(x)}{c}$$$$P_X(x)=\frac{F_X(x)-F(a)}{c}$$
Thus ensuring that $$\int_a^b{p_X(x)dx}=1$$
Which makes it a valid pdf.

Afterwards we can get the inverse of $P_X(x)$, and this function will have the same distribution as $f(x)$ which can generate random values between $[a,b]$. That is to say that since the domain of $P_X(x)$ is $[a,b]$ then the range of $P_X^{-1}(x)$ is $[a,b]$. And also, since we ensured that $P_X(b)=1$ and $P_X(a)=0$ we also ensure that $P_X^{-1}(a)=0$ and $P_X^{-1}(b)=1$.
### Excerpt from Rendering Lecture 06 - Importance Sampling by Computer Graphics at TU Wien
You can find the video [here](https://web.archive.org/web/20260414211949/https://www.youtube.com/watch?v=c6NvZ74LAhE&t).
For a random uniform variable $\xi\in [0,1]$.
#### The Inversion Method, Completed
- Find a candidate function $f(x)$ with the desired distribution shape
- Choose the range $[a,b]$ in $f(x)$ you want your variable to imitate
- Determine the indefinite integral $F(x)=\int{f(x)dx}$
- Compute the proportionality constant $c=F(b)-F(a)$
- The CDF for the new variable $X$ is $P_X(x)=\frac{F(x)-F(a)}{c}$
- Compute the inverse of the CDF $P_X^{-1}(\xi)$
- Use $P_X^{-1}(\xi)$ to warp the samples of a canonic random variable so that they are distributed with $p(x)=\frac{f(x)}{c}$ in the range $[a,b)$
Also to include unto the lecture notes, the pdf of $f(x)$ is $p(x)=\frac{f(x)}{c}$.
# Normalization Constant
The [[What is Probability and Statistics#Probability Distributions|characteristics of a probability distribution]] make it so that the area of a probability distribution needs to be $1$. This can be hard when you want to have very distinct probability distributions. However we can still achieve this as long as it is nonnegative and has a finite integral.
# Uniform Distribution
This is a distribution where the probability of any given value is constant. For example, a probability distribution of $10$ distinct values appearing, would have a $p(x)=\frac{1}{10}$ uniform distribution. We can denote these types of distributions as $\mathcal{U}(a, b)$ where $a, b$ are the bounds of the randomly generated values.
# The Gaussian Function
This is a function of the form $$f(x)=\text{exp}(-x^2)=e^{-x^2}$$
Which looks like a bell curve.
## [[Integrals|Gaussian Integral]]
The integral of the gaussian function over the whole real numbers is: $$\int_{-\infty}^\infty{\text{exp}(x^{-2})dx}=\sqrt{\pi}$$
## The Normal Distribution
This is a special case of the gaussian function, except we have normalized it by dividing it by its integral. $$\frac{1}{\sqrt{2\pi}}e^{-x^2/2}$$
We can control where the [[What is Probability and Statistics#Mean or Average|mean]] $\mu$ of the normal distribution is located through horizontal translations: $$\large \frac{1}{\sqrt{2\pi}}e^{\frac{-(x-\mu)^2}{2}}$$
and finally we can change its standard deviation through its denominator in the exponent, which changes the normalizing constant a bit: $$\large \frac{1}{\sigma\sqrt{2\pi}}e^{\frac{-(x-\mu)^2}{2\sigma^2}}$$
