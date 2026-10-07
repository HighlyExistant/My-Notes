# What is a Proposition
A proposition is a declarative sentence which has a truth value.
## Examples
1. $2+3=5$ is a proposition which is true
2. $2+3=6$ is a proposition which is false
3. $2+x=5$ is not a proposition yet, but once we assign a value to $x$ it becomes a proposition
4. "The earth is flat", is a proposition which is false.
## Notation
We can simplify the calculation of truth values by assigning variables to these propositions, such as $P:$  "It is raining".
# Propositional Function
Is an expression $P(x)$ which maps $X$ to a truth value. Examples include: $$P(x): x^2>2$$
# Quantifiers
Are used to denote how many elements something applies to.
## Universal Quantifier
==**For all**==: $\forall$. The way we use it would be $$\forall x\in X, P(x)$$where $P(x)$ is a propositional function. It states that for all $x\in X$, it satisfies $P(x)$.
## Existential Quantifiers
* ==**There Exists**==: $\exists$ 
* ==**There Exists a Unique**==: $\exists!$
The way we use it would be $$\exists x\in X, P(x)$$where $P(x)$ is a propositional function. It states that there exists $x\in X$, which satisfies $P(x)$. The unique version $\exists !$ means that there is only a single $x\in X$ which satisfies $P(x)$.
## Properties
* $\neg (\forall x P(x))\equiv \exists x,\neg P(x)$
* $\neg (\exists x P(x))\equiv \forall x,\neg P(x)$
* $\exists x (P(x)\Rightarrow Q(x))\equiv  \forall x, P(x)\Rightarrow \exists x, Q(x)$
* $\exists x(P(x)\vee Q(x))\equiv \exists x P(x)\vee (\exists x Q(x))$
* $\forall x (P(x)\wedge Q(x))\equiv \forall x P(x)\wedge \forall x Q(x)$
* $\forall x P(x)\vee \forall xQ(x)\Rightarrow \forall x(P(x)\vee Q(x))$
* $\exists x(P(x)\wedge Q(x))\Rightarrow \exists x (x)\wedge \exists x Q(x)$

## Logical Negation
==**Not**==: $\neg$, $\sim$ $A'$, $A^C$ or $\overline{A}$. Is known as the complement of a set or the opposite of a given value. If we wanted to draw a truth table

| A     | Output |
| ----- | ------ |
| True  | False  |
| False | True   |

## Logical Conjunction
==**And**== $\wedge$ or $\cap$. Is known as the intersection between the two statements. If we wanted to draw a truth table 

| A     | B     | Output |
| ----- | ----- | ------ |
| False | False | False  |
| True  | False | False  |
| False | True  | False  |
| True  | True  | True   |
### Properties
* [[Algebraic Structures#Associativity|Associative]]
* [[Algebraic Structures#Commutativity|Commutative]]
* [[Algebraic Structures#Distributivity|Distributive]] along $\vee$.
* [[Algebraic Structures#Idempotency|Idempotent]] for all propositions
## Logical Disjunction
 ==**Or**== $\vee$ or $\cup$. Is known as the union between the two statements. If we wanted to draw a truth table 

| A     | B     | Output |
| ----- | ----- | ------ |
| False | False | False  |
| True  | False | True   |
| False | True  | True   |
| True  | True  | True   |
### Properties
* [[Algebraic Structures#Associativity|Associative]]
* [[Algebraic Structures#Commutativity|Commutative]]
* [[Algebraic Structures#Distributivity|Distributive]] along $\wedge$.
* [[Algebraic Structures#Idempotency|Idempotent]] for all propositions
## Conditional
==**If**==, ==**Implies**== $\rightarrow$ or more commonly $\Rightarrow$, represents a conditional statement if $p$ then $q$. 

| A     | B     | Output |
| ----- | ----- | ------ |
| False | False | True   |
| True  | False | False  |
| False | True  | True   |
| True  | True  | True   |
In a statement $p\Rightarrow q$: 
* the $p$ is known as either the antecedent, condition or hypothesis
* the $q$ is known as either consequent or conclusion.
### Converse and Contrapositive
* If $p\Rightarrow q$, then the converse would be $q\Rightarrow p$.
* If $p\Rightarrow q$ then the contrapositive would be $\neg q \Rightarrow \neg p$.
### Example
The truth table might look odd, but my discrete math teacher has given me the following example:
Let $p(f)$ denote that $f$ is differentiable and $q(f)$ denote that $f$ is continuous. We can say that $p(f)\Rightarrow q(f)$ which would be true, but $q(f)\Rightarrow p(f)$ would be false.

## Biconditional
==**Iff**== $\leftrightarrow$ or more commonly $\Leftrightarrow$.

| A     | B     | Output |
| ----- | ----- | ------ |
| False | False | True   |
| True  | False | False  |
| False | True  | False  |
| True  | True  | True   |
## Tautology, Contradiction and Contingent
A ==**tautology**== is a propositional statement which is true for any values given in the proposition, while ==**contradiction**== is where any given value is false. The classical tautology is $p\vee \neg p$ and the classical contradiction is $p \wedge \neg p$. A ==**contingent**== proposition is one which can have either true or false outputs.
### Other examples of Tautologies
1. $p\wedge q\Rightarrow p$. Since $p\wedge q$ contains $p$ then implies $p$ must be true. The opposite $p\vee q\Rightarrow p$ is not guaranteed, since it might not contain $p$.
2. $p\Rightarrow (p\vee q)$
3. $\neg p\Rightarrow (p\Rightarrow q)$ and their contrapositive $\neg (p\Rightarrow q)\Rightarrow p$ are tautologies
4. $(p\wedge (p\Rightarrow q))\Rightarrow q$
5. $(\neg p \wedge (p\vee q))\Rightarrow q$ Modus Tollendo Ponens. It basically describes that if it is either $p$ or $q$ and it is not $p$ then it must be $q$.
6. $(\neg p\wedge (p\Rightarrow q))\Rightarrow \neg p$
7. $(p\Rightarrow q)\wedge (p\Rightarrow r)\Rightarrow (p\Rightarrow r)$ [[Mathematics/Pure Math/Relations/Relations#Transitive|transitivity]]
## Equivalence
If a given biconditional $p\Leftrightarrow q$ is a tautology, then we can write $p\equiv q$ which means that these are [[Mathematics/Pure Math/Relations/Relations#Equivalence|equivalent]].
## Theorem Listing
1. $p\Rightarrow q \equiv \neg p \vee q$.
2. $p\Rightarrow q\equiv \neg q \Rightarrow \neg p$ (==**Contrapositivo**==)
3. $p\Leftrightarrow q\equiv p\Rightarrow q\wedge p\Rightarrow q$
4. $\neg (p\Rightarrow q)\equiv p\wedge \neg q$ (==**Reducto ad absurdum**==)
5. $\neg (p\Leftrightarrow q)\equiv (p\neg q)\vee (q\wedge \neg p)$
