# Countability of the Rationals
## Lemas Utilized
1. $A\subseteq B\Rightarrow |A|\leq B$.
2. $f:C\to D$ is bijective $\Leftrightarrow a\leq b$ or $a\geq b$.
## Proof
Remember $\mathbb{N}\subseteq \mathbb{Q}$, by lemma (1) $|\mathbb{N}\leq \mathbb{Q}|$, we then proceed to show 

Define $f:\mathbb{Q_+}\to\mathbb{N}$ as $f(\frac{a}{b})=2^a3^b$ (2 and 3 being arbitrary primes) we can see we have a bijection between the two values. By doing the same for $\mathbb{Q}_-$ we can see both sets are countable. The union of countable sets is countable, and then we union it with $\{0\}$ which is finite and therefore countable, and we obtain that $\mathbb{Q}$ is countable.
# Countability of the Integers
Given $\mathbb{Z}\subseteq \mathbb{Q}$, then $|\mathbb{Z}|\leq |\mathbb{Q}|$ by lemma 1, and $\mathbb{Q}$ is countable, then $\mathbb{Z}$ is countable.