# Prerequisite
## On Polynomial Representations
### Value Representation
A polynomial of degree $n$ can be uniquely represented by $(n+1)$ points, e.g. linear by 2 points, quadratic by 3 points, etc. For a polynomial $P(x)$ we can represent it as a set: $$\{(x_0,P(x_0)), (x_1,P(x_1)), ..., (x_n,P(x_n))\}$$
### Coefficient Representation
For a polynomial $a_0+a_1x^1+a_2x^2+...+a_nx^n$, we can represent it as: $$[a_0,a_1,a_2,...,a_n]$$
## Multiplication using the Value Representation
Let $A(x)$ and $B(x)$ be polynomials of degree $n$. Their product $C(x)=A(x)\cdot B(x)$ will be a polynomial of degree $2n$ meaning that their value representation will be uniquely represented by $2n+1$ points. What we can do is take $n+1$ points from $A(x)$ and $B(x)$ respectively from some subset of their domain, and multiply them linearly, to get back the $n+1$ points of our $C(x)$, and since only 1 polynomial exists with such points, $C(x)$ can be solved using the points in the value representation to the coefficient representation, which reduces the operations from $O(n^2)\to O(n)$.
# The Discrete Fast Fourier Transform
The coefficient representation will now be detailed by powers of $\omega$ where $\omega = e^\frac{2\pi i}{n}$. 

The FFT is defined as: $$\mathcal{F\{}x\mathcal{\}}=\sum_{x=0}^{n-1}f(x){\omega^{nxu}}$$
The Cooley–Tukey FFT, also called the radix-2 decimation-in-time or DIT, alters this, to split it on even and odd numbers. Let $f_e(x)$ and $f_o(x)$ denote the even and odd number coefficients respectively. Then: $$\mathcal{F\{}x\mathcal{\}}=\sum_{x=0}^{N/2-1}f_e(x)\omega^{n(2x)u}+\sum_{x=0}^{N/2-1}f_o(x)\omega^{n(2x+1)u}$$Ultimately all of this simplifies to a recursive algorithm: $$\mathcal{F\{}x\mathcal{\}}=\mathcal{F_e\{}x\mathcal{\}}+\mathcal{F_o\{}x\mathcal{\}}$$The Fourier transform simplifies into the sum of the even and odd Fourier transforms.
# Pseudocode provided by Reducible
``` python
def FFT(P): # P is the coefficient representation
	n = len(P) # n is power of 2
	if n == 1:
		return P;
	omega = exp((2*PI* i)/n);
	P_e = [p_0, p_2, ..., p_n_minus_2]
	P_o = [p_1, p_3, ..., p_n_minus_1]
	y_e, y_o = FFT(P_e), FFT(P_o)
	y = [0]*n
	for j in range(n/2):
		y[j] = y_e[j] + (omega**j)*y_o[j]
		y[j+n/2] = y_e[j] - (omega**j)*y_o[j]
		
	return y
```

# To Read
R. C. Gonzalez and P. Wintz, Digital Image Processing. Addison Wesley, (1983). ISBN 0-201- 03045-4.

C. L. Phillips and J. M. Parr, Signals, Systems, and Transforms. Englewood Cliffs, New Jersey: Prentice Hall, (1995). ISBN 0-13-795253-8.

J. W. Cooley, P. A. W. Lewis, and P. D. Welch, “Application of the fast fourier transform to computation of fourier integrals, fourier series, and convolution integrals”, IEEE Transactions on Audio and Electroacoustics, AU-15(2), pp. 79–84 (1967).

S. J. Orfandis, Introduction to Signal Processing. Upper Saddle River, New Jersey: Prentice Hall, (1996). ISBN 0-13-209172-0.
# References
1. [Reducible](https://www.youtube.com/watch?v=h7apO7q16V0)
