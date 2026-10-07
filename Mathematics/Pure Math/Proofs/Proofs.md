Proofs are the way we show that things are true in math. There are various types of proofs, and depending on which axioms you are working with, there are different ways of proving things logically.
# Pigeonhole Principle
Given a number of "holes" $m$ and a number of "pigeons" which will enter the holes $n$, such that $n>m$, the pigeonhole principle states that at least one hole will have more than 1 pigeon.
# Proof by Contrapositive
If $p\Rightarrow q$ then $\neg q \Rightarrow \neg p$. Instead of proving that one true statement leads to another true statement, we prove that a false statement leads to another false statement.
# Proof by Contradiction
This uses the assumption that a statement is either true or false. Given a statement $p$ which we want to prove, we first assume that $p$ is already true to begin with and show how that leads to a contradiction. These are usually of the form $p\wedge \neg p$ 
## Example: Proof that $\sqrt{2}$ is irrational
* Let $p,q\in \mathbb{Z}$ and $\frac{p}{q}\in\mathbb{Q}$. 
* We assume that $(\frac{p}{q})=\sqrt{2}$ and therefore $(\frac{p}{q})^2=\frac{p^2}{q^2}=2$.
* We assume that $p$ and $q$ ==**share no common factors**== since if they did, we could cancel them out into a new $p$ and $q$.
* Passing $q^2$ onto the other side, we reach: $p^2=2q^2$
* This tells us that $p^2$ is an even number and so $p$ must be even because the square of an odd number is odd. Therefore $p=2r$ where $r\in \mathbb{Z}$.
* $4r^2=2q^2$ cancelling out the $2$ we reach $2r^2=q^2$. 
* With the same logic as before we can conclude that $q$ is also even.
* $p$ and $q$ cannot both be even, since they share no common factors, but here we can see they share $2$ as a common factor, and therefore this cannot hold for any rational numbers.
# Proof by Logical Equivalency
Here we use the rules of [[General Logic|logic]] to manipulate the statement we want to prove into a sepárate statement. 
#### Example
$$[P\to(Q \vee R )\equiv [(P \wedge \neg Q ) \to R $$
# Proof by Induction
Given some ==**hypothesis**== we prove its ==**base case**== to show that it applies $\forall x\in X$, by showcasing that the previous case implies the next case. It has the following structure:
1. Base Case: Prove the property for $n=k$.
2. Induction Hypothesis: Set up the equation with the previous case, the current case implying the next case.
3. With the base case $P(k+1)$ is satisfied.
## Example: Proof of sums of numbers
$$\sum_{i=1}^n{i}=\frac{n(n+1)}{2}$$
### Base Case
for $i=1$ then $\frac{1(1+1)}{2}=1$, which is the sum of $1$ term.
### Hypothesis of Induction
assume $$\sum_{i=1}^n{i}=\frac{n(n+1)}{2}$$
### Inductive Pass
Then $$\frac{n(n+1)}{2}+(n+1)=\frac{(n+1)(n+2)}{2}$$
If the lefthand side reaches the righthand side, the proof is complete.