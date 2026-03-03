Diferencia de cuadrados: $a^{2}-b^{2}=(a-b)(a+b)$
* Cuadrado perfecto: $a^2 + 2ab + b^2=(a+b)^2$
* Cuadrado perfecto: $a^2-2ab+b^2=(a-b)^2$
* Diferencia de cubos: $a^3-b^3=(a-b)(a^2+ab+b^2)$
* Suma de cubos: $a^3+b^3=(a+b)(a^2-ab+b^2)$
# Synthetic Division
Given a polynomial $ax^n+bx^{n-1}+cx^{n-2}...$ which for this example we'll just use the cubic polynomial $ax^3+bx^2+cx+d$, we can perform synthetic division to factor out certain expressions.
## Steps
We're going to be using the equation $x^3-4x^2-7x+10$
1. Write out the coefficients of the expression in descending order according to the grade (exponent): $$\begin{bmatrix}1 & -4 & -7 & 10\end{bmatrix}$$
2. We're going to place our root on the side, as that will be what we will be dividing our equation by. For example if our root was $-2$ then we would be dividing by $(x+2)$, due to the fact that if we substitute $x$ by $-2$, we would get $0$. $$-2\begin{bmatrix}1 & -4 & -7 & 10\end{bmatrix}$$
3. We will now sum the coefficients sequentially, whilst multiplying it by our root. 
$$
\begin{matrix}
	-2\begin{bmatrix}
		1 & -4 & -7 & 10 \\0 & -2 & 12 & -10
	\end{bmatrix} \\
	\begin{matrix}1 & -6 & 5 & 0\end{matrix}
\end{matrix}
$$
4. The final number will be our remainder. If the remainder is $0$, then the number we divided it by is a root. Otherwise it is not. We can then use the numbers that are left, to write out our new equation, which would be $$(x^2-6x+5)(x+2)$$
