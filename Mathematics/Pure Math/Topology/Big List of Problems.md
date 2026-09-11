# Topologies
## Exercise 1.3
Fix a set $X$, and let ${\Large\tau}_{\text{co-finite}}$ and ${\Large\tau}_{\text{co-countable}}$ be the co-finite and co-countable topologies on $X$, respectively
### Co-Finite
Let ${\Large\tau}_{\text{co-finite}}=\{U\subseteq X|X\setminus U\text{ is finite}\}\cup \{\emptyset\}$
* $X$ and $\emptyset$ are in ${\Large\tau}_{\text{co-finite}}$ because when $U=X$ then $X\setminus X=\emptyset$, which is finite, and $\emptyset$ is there because we united it with the topology.
* Consider two sets $U, V\subseteq X$. Then we need to show that $(X\setminus U)\cup (X\setminus V)=X\setminus W$, and is finite. We can see then, that this is simply $X\setminus (U\cap V)$. If we make $W=U\cup V$, we have shown that $X\setminus W$ is in the topology, and $W$ must be finite, if $U$ and $W$ are finite, since the intersection of finite sets is finite.
* Consider two sets $U,V\subseteq X$. Then we need to show that $(X\setminus U)\cap (X\setminus V)=X\setminus W$. We can see then, that this is simply $X\setminus (U\cup V)$. If we make $W=U\cap V$ then we have shown that $X\setminus W$ is in the topology, and $W$ must be finite, if $U$ and $W$ are finite, since the union of finite sets is finite.
### Co-Countable
Let ${\Large\tau}_{\text{co-countable}}=\{U\subseteq X|X\setminus U\text{ is countable}\}\cup \{\emptyset\}$
* $X$ and $\emptyset$ are in ${\Large\tau}_{\text{co-countable}}$ because when $U=X$ then $X\setminus X= \emptyset$ and since $\emptyset$ is countable, then it is in the topology. $\emptyset$ is there because we united it with the topology.
We can prove this in a similar manner we did for the Co-Finite topology.
### Co-Finite Coarser than or equal to Co-Countable
Remember that $${\Large\tau}_{\text{co-finite}}=\{U\subseteq X|X\setminus U\text{ is finite}\}\cup \{\emptyset\}$$ and $${\Large\tau}_{\text{co-countable}}=\{U\subseteq X|X\setminus U\text{ is countable}\}\cup \{\emptyset\}$$
We can see that when $X$ is finite, then every complement is countable and finite, meaning that ${\Large\tau}_{\text{co-finite}}={\Large\tau}_{\text{co-countable}}$ when $X$ is finite. Not only that but every finite set must necessarily be countable, meaning that ${\Large\tau}_{\text{co-finite}}\subset{\Large\tau}_{\text{co-countable}}$, and considering we proved both, then ${\Large\tau}_{\text{co-finite}}\subseteq{\Large\tau}_{\text{co-countable}}$.
### When Co-Countable is Discrete?
$${\Large\tau}_{\text{co-countable}}=\{U\subseteq X|X\setminus U\text{ is countable}\}\cup \{\emptyset\}$$Is discrete when $X$ is countable, since every complement will also be countable.
## Exercise 1.4
Let $(X, {\Large\tau}_{\text{co-countable}})$ be an infinite set with the co-countable topology. Show that ${\Large\tau}_{\text{co-countable}}$ is closed under countable intersections. Give an example to show that it need not be closed under arbitrary intersections.
### Closed under Countable Intersections
Since $X\setminus U$ is open in ${\Large\tau}_{\text{co-countable}}$, then $U$ is closed in ${\Large\tau}_{\text{co-countable}}$. $$X\setminus\bigcap_{i\in I}{U_i}=\bigcup_{i\in I}{X\setminus U_i}$$
### Doesn't need to be closed under arbitrary intersections
Let $X$ be uncountable set under ${\Large\tau}_{\text{co-countable}}$, and consider the uncountable subset $U_x=X\setminus \{x\}$ with countable complement $\{x\}$. Write out $X$ as the union of two uncountable sets using the axiom of choice, and write $X=A\cup B$. Then we can index the intersection as $$B=\bigcap_{x\in A}{U_x}$$We can see that $B$ is equal to this since $B$ is the complement of $A$. The set $B$ even if it is the intersection of arbitrary $U_x$ is not open since it's complement is uncountable, it is also not closed because it cannot be expressed as the complement of an open set.
## Exercise 1.5
Let $X$ be a nonempty set, and fix an element $p\in X$. Recall that $${\Large\tau}_p:=\{U\subseteq X| p\in U\}\cup \{\emptyset\}$$
is called the particular point topology at $p$ on $X$. Show explicitly that ${\Large\tau}_p$ is a topology on $X$.
### Showing explicitly
1. Considering $p\in X$, then $X\in {\Large\tau}_p$. Also since $\emptyset$ was united into ${\Large\tau}_p$ it is also in ${\Large\tau}_p$.
2. Let $A, B\in {\Large\tau}_p$. Since $A, B$ contains $p$ then $A\cup \{p\}=A$ and $$B\cup \{p\}=B$$. Let $C=A\cup B$ This means that $A\cup \{p\}\cup B=C\cup\{p\}$. Considering that this set contains $p$, all unions are in ${\Large\tau}_p$.
3. We can make a similar argument to the one above. Let This means that $(A\cup \{p\})\cap (B\cup \{p\})$. Considering that both sets contains $p$, so does their intersection, therefore, all intersections are in ${\Large\tau}_p$.
## Exercise 1.6
Recall that the ray topology on $\mathbb{R}$ is $${\Large\tau}_\text{ray}:=\{(a,\infty)|a\in \mathbb{R}\}\cup \{\theta,\mathbb{R}\}$$
Show explicitly that ${\Large\tau}_\text{ray}$ is a topology on $\mathbb{R}$. Be sure to think carefully about unions.
### Showing Explicitly
1. $\mathbb{R}$ and $\emptyset$ are in ${\Large\tau}_\text{ray}$ since they are united together.
2. Checking to see if all unions are in the topology. Given two rays $A=(a,\infty)$ and $B=(b,\infty)$, we have 3 cases due to trichotomy where either $a>b$, $a=b$ or $a<b$.
	* Case 1 $a>b$: remember that an interval would have all numbers $a<x<\infty$. since $a>b$ then the ordering would go $b<a<x<\infty$. For this reason $A\cup B=B$. Considering that $B\in{\Large\tau}_\text{ray}$ the unions of such open sets are in ${\Large\tau}_\text{ray}$
	* Case 2 $a=b$: If $a=b$ then it is trivial to see that $A=B$ and both sets are in ${\Large\tau}_\text{ray}$.
	* Case 3 $a<b$. We do a similar conversion to what we did in Case 1, but with the variables interchanged, and we can then conclude it is in ${\Large\tau}_\text{ray}$.
   We can therefore conclude all unions of open sets are in the open set.
	3. Checking to see if all intersections are in the topology. Given two rays $A=(a,\infty)$ and $B=(b,\infty)$, we have 3 cases due to trichotomy where either $a>b$, $a=b$ or $a<b$.
		* Case 1 $a>b$: Remember again that $b<a<x<\infty$. we can see then that $a<x<\infty$ is contained in $b<x<\infty$ and therefore their intersection is $A$ which is in the topology.
		* Case 2 $a=b$: If $a=b$ then it is trivial to see that $A=B$ and both sets are in ${\Large\tau}_\text{ray}$.
		* Case 3 $a<b$. We do a similar conversion to what we did in Case 1, but with the variables interchanged, and we can then conclude it is in ${\Large\tau}_\text{ray}$.
   We can therefore conclude all intersections of open sets are in the open set.
## Exercise 1.7
Let $(X,{\Large\tau})$ be a topological space, and let $A\subseteq X$ be a set with the property that for every $x\in A$, there is an open set $U_x\in{\Large\tau}$ such that $x\in U_x\subseteq A$. Show that $A$ is open.

We need to show that $x\in U_x\subseteq A\in{\Large\tau}$. Consider then that there is $U_x$ for every $x\in A$. The union of all $U_x$ would be $A$, and since the union of open sets is an open set, then $A$ is an open set.
## Exercise 1.8
Let $(X,{\Large\tau})$ be a topological space, and let $f: X\to Y$ be an injective (but not necessarily surjective) function. Is ${\Large\tau}_f:=\{f(U): U\in {\Large\tau}\}$ necessarily a topology on $Y$? Is it necessarily a topology on the range of $f$?

For ${\Large\tau}_f$ to be a topology, then $f(U)\cup f(V)\in {\Large\tau}_f$ and $f(U)\cap f(V)\in{\Large\tau}_f$, as well as contain $f(X)$ and $\emptyset$.
1. Since the function is injective, every $U$ maps to a unique $f(U)$
2. $f(\emptyset)$ maps to $\emptyset$.
3. $f(X)$ maps to a subset $U$ of $Y$.
If we can prove that: $$f(U)\cup f(V)=f(U\cup V)$$then we would prove that every open union is in ${\Large\tau}$.