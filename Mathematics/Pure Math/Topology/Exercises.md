## Exercises in James R. Munkres Book
#### Exercise 16.1
Show that if $Y$ is a subspace of $X$, and $A$ is a subset of $Y$, then the topology $А$ inherits as a subspace of $Y$ is the same as the topology it inherits as a subspace of $X$.
We are given that:
* $A\subset Y\subset X$
We want to prove that 
* ${\Large\tau}_A \subset {\Large\tau}_Y \subset {\Large\tau}_X$
Proof:
1. We know that an arbitrary set $X$ and its topology ${\Large\tau}_X$ contains all its intersections and unions as well as $\emptyset$ and $X$.
2. The subspace topology on $X$ is ${\Large\tau}_Y=\{U\cap Y|U\in {\Large\tau}_X\}$
3. The subspace topology on $A$ is $${\Large\tau}_A=\{U\cap A|U\in{\Large\tau}_Y\}$$We also know that that $A=A\cap Y$, since it is a subset of $Y$.
4. alternatively then, the subspace can be rewritten as  $${\Large\tau}_A=\{U\cap Y\cap A|U\in{\Large\tau}_X\}$$
5. The term $U\cap Y$ generates elements of ${\Large\tau}_Y$ therefore $U\cap Y\cap A$ would generate elements of ${\Large\tau}_A$. Given that $Y\cap A=A$ this simplifies to: $${\Large\tau}_A=\{U\cap A|U\in{\Large\tau}_X\}$$which is the subspace topology of $X$ with subset $A$.
#### Exercise 16.2
If ${\Large\tau}$ and ${\Large\tau}'$ are topologies on $X$ and ${\Large\tau}'$ is strictly finer than ${\Large\tau}$, what can you say about the corresponding subspace topologies on the subset $Y$ of $Х$?

We are given that
* ${\Large\tau}\subset {\Large\tau}'$
* $Y\subset X$
The corresponding subspace topologies on $Y$ would be: $${\Large\tau}_Y=\{U\cap Y|U\in {\Large\tau}\}$$$${\Large\tau}_Y'=\{U\cap Y|U\in {\Large\tau}'\}$$
If we consider an indiscrete topology on $X=\{1,2,3\}$ such that $${\Large\tau}=\{\emptyset, X\}$$ and a strictly finer topology $${\Large\tau}'=\{\emptyset,X,\{1,2\}\}$$as well as a subset $Y\subset X=\{3\}$ we reach that their subspace topologies are equal. This showcases that their subspaces are not necessarily finer. Considering however that any element in ${\Large\tau}$ is an element of ${\Large\tau}'$, we can conclude that a subspace of ${\Large\tau}$ on $X$ could never be larger than ${\Large\tau}'$ but could be equal. This means that a subspace ${\Large\tau}_Y'$ is ==**finer**== than ${\Large\tau}_Y$.
#### Exercise 16.3
Consider the set $Y = [-1, 1]$ as a subspace of $\mathbb{R}$. Which of the following sets are open in $Y$? Which are open in $\mathbb{R}$? $$\begin{matrix}A=\{x|\frac{1}{2}<|x|<1\}\\B=\{x|\frac{1}{2}<|x|\leq1\}\\C=\{x|\frac{1}{2}\leq|x|<1\}\\D=\{x|\frac{1}{2}\leq|x|\leq1\}\\E=\{x|0<|x|<1\text{ and }\frac{1}{x}\not\in\mathbb{Z}_+\}\end{matrix}$$
Assuming that $\mathbb{R}$ is under the standard topology, then the set $A$ would be
#### Exercise 17.1
Let $\mathcal{C}$ be a collection of subsets of the set $X$. Suppose that $\emptyset$and $X$ are in $\mathcal{C}$, and that finite unions and arbitrary intersections of elements of $\mathcal{C}$ are in $\mathcal{C}$. Show that the collection: $${\Large\tau}=\{X\setminus C|C\in\mathcal{C}\}$$ 
is a topology on $X$.
#### Exercise 17.2
Show that if $A$ is closed in $Y$ and $Y$ is closed in $X$, then $A$ is closed in $X$.

* If $A$ is closed in $Y$ then $A=B\cap Y$, and $Y-A$ is open.
* If $Y$ is closed in $X$ then $Y=C\cap X$, and $X-Y$ is open.
* For $A$ to be closed in $X$ we must prove either that $A=D\cap X$ or that $X-A$ is open.
* We need to prove then that $X-(B\cap Y)$ is open.