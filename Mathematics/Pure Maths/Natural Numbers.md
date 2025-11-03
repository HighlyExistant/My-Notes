# Peano Axioms
These axioms are applied for all natural numbers:
1. $0$ is a natural number. Occasionally this $0$ is exchanged for a $1$ and is usually just up to definition.
2. Natural numbers are [[Relations#Reflexive|reflexive]], [[Relations#Reflexive|symmetric]] [[Relations#Reflexive|transitive]] and [[Relations#Closure|closed]] under equality.
3. $\forall n\in\mathbb{N} (S(n) \in \mathbb{N})$
4. $\forall m, n \in \mathbb{N} (S(m)=S(n)\Rightarrow m=n)$
5. $\forall n\in \mathbb{N} (S(n)\neq0)$ that is to say there is no successor equal to 0.
The function $S(n)$ we've been seeing so far is called the successor equivalent to $S(n)=n+1$, with the properties that:
* $a + 0 = a$
* $a + S(b) = S(a+b)$

This is useful for the following axioms: ==**The axioms of induction**==:
1. If $K$ is a set such that $0 \in K$ and for $n \in \mathbb{N}\Rightarrow S(n) \in \mathbb{N} \Rightarrow \mathbb{N} \subseteq K$.
2. If $\phi$ is a unary predicate $s.t. \phi(0)=true$ and for every $n \in \mathbb{N}, \phi(n)=true \Rightarrow \phi(S(n))=true \Rightarrow \phi(n)=true \forall n \in \mathbb{N}$
3. v