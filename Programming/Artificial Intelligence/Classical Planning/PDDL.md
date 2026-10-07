Known as Planning Domain Definition Language, is the modern equivalent of [[STRIPS]], which builds on top of it, and therefore it is recommended to read that document beforehand. PDDL Also has its own syntax, which will be explained below. The entire syntax however can be found in this [website](https://planning.wiki/ref/pddl/):
# Comments
The way we write comments in PDDL is through `;`, so: 
```
; These would be comments
```
# Variables
1.  ==**Variables**==: We denote variables in PDDL with `?x`.
2. ==**Predicates**==: We denote predicates in PDDL with `cond()` and optionally a variable `cond(?x)`.
# Actions in PDDL
We can use in precondition's and effect's boolean symbols like
* `and()`
In effects, to add an effect you add it simply as you would in a precondition, and to remove the precondition you use `not()`
```
(:action pickup
	:parameters (?x ?y)
	:precondition (and(cond ?x)(cond2 ?y)
	:effect (and(cond3 ?x)(not (cond4 ?y)))
)
```
# Domain Files
These contain the information space that you will be dealing with. We define the domain like:
``` PDDL
(define (domain NAME)
	(:requirements:strips:typing)
	(:predicates
		(cond ?x)
		(cond5 ?x ?y)
	)
)
```
You can look more into [requirements here](https://planning.wiki/ref/pddl/requirements).