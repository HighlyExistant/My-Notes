# Formal Definitions
## Axioms
These are horn clauses, which are of the form $$\neg p_0\vee \neg p_1\vee \ldots \vee p_n$$It is basically a series of disjunctions with at most one positive clause, here being $p_n$. If theres exactly one positive literal, then it is called a ==**definite clause**==, while if there is no positive literal at all, it is called a ==**goal clause**==.

Horn clauses are [[Algebraic Structures#Closure|closed under resolution]], meaning that resolving two horn clauses, gives another horn clause.

Horn clauses can also be written as implications, because they are in the form of modus ponens.
## Operators
An operator is an expression `(:operator h D A)`, where: 
* `h` is the primitive task to be performed (denoted `h` for head). Primitive tasks in SHOP are denoted by the bang symbol `!` before the actual task name. Variables can be denoted using `?`.
* `D` and `A` are the Deletions and Additions respectively, containing no variables except those specified in `h`.
Alternatively it can be expressed as a triplet $(h, D, A)$. These are written in a lisp style syntax as: 
```
(:operator (!putdown ?block) ; primitive task
	((holding ?block)) ; deletions
	((ontable ?block) (handempty)) ; additions
)
```
## Methods
A method is an expression `(:method h C T)` where: 
* `h` is a compound task (denoted `h` for head)
* `C` are the preconditions
* `T` is a task list to perform.
Alternatively it can be expressed as a triplet $(h, C, T)$.
# Planning Problem
A planning problem is defined as a triplet $(S, T, D)$ where:
* $S$ is the state
* $T$ is a task list
* $D$ is the domain, which is a set of axioms, operators and methods.
# References
1. [SHOP-1999](https://www.cs.umd.edu/~nau/papers/nau1999shop.pdf)
2. [Vaskar Raychoudhury Lec 54: Horn Clause](https://www.youtube.com/watch?v=IZPpNA2FFGI)
3. [Vaskar Raychoudhury Lec 55: Forward and Bckward Chaining](https://www.youtube.com/watch?v=glZMMGBa9MU)
4. [Exploring HTN Planners through Example](https://www.gameaipro.com/GameAIPro/GameAIPro_Chapter12_Exploring_HTN_Planners_through_Example.pdf)
