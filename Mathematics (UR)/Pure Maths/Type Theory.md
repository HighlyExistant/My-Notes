Used commonly in computer science to study the behavior of functions and whether or not they produce the correct types. It can be thought of as an extension of [[Lambda Calculus|Lambda Calculus]] where everything has a type associated:
# Definitions
* $a: \beta$ is a term $a$ with type $\beta$.
* $\alpha \to \beta$ where $\alpha$ and $\beta$ are types, is a type of a function from $\alpha$ to the type $\beta$, this is sometimes written as $\alpha \beta$.
* ==**Abstractions with types**==: If there is a function $\lambda x: \alpha .M$ such that $M$ has type $\beta$, then this function has type $\alpha \to \beta$.
* ==**Applications with types**==: If there is a function $M: \alpha \to \beta$ and $N: \beta$ then $(MN)$ has type $\beta$.
# Vocabulary
* ==**Predicates**==: Similar to how it functions in [[Rhetoric#^641e52|rhetoric]] the predicate will take an input and return a [[Rhetoric#^fb57f7|truth value]]. $F: \alpha \to \beta$ such that $\alpha$ is an argument and $\beta$ is a truth value.
* ==**Judgements**==: Are followed from assumptions, where we say "assuming $x: \text{bool}$ and $y: \text{nat}$, it follows that $(\text{if} x y y): \text{nat}$". These judgements are written as $\vdash$. Ej.$$x:\text{bool},y:\text{nat}\vdash (\text{if}xyy):\text{nat}$$ We can write these assumptions down onto a single symbol $\Gamma$, and say: $$\Gamma\vdash (\text{if}xyy):\text{nat}$$
# Relations to Lambda Calculus
Type theory is a way of adding syntactic sugar to the language of lambda calculus, now called ==**simply typed lambda calculus**==, although its primary focus is in studying types. For example we can define a function $\text{successor} : \text{nat} \to \text{nat}$ and call it using $(\text{successor})(1)$. What the function does, is not really of importance in type theory, only the type that it returns. ==**If we can assure that the correct output type goes into the correct input type, it assures our program retains coherence**==.