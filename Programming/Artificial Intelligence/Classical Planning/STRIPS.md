The Stanford Research Institute Problem Solver, is a method of modelling complex problems to reach goals, through actions. In STRIPS we use:
1. ==**Facts**==: Which is the set of all facts/predicates
2. ==**Operators**==: Which are the actions we can perform
3. ==**Initial State**==: Which is how the problem is at the beginning.
4. ==**Goal**==: The state we want to achieve.

When detailing out a problem in STRIPS we need to list out the:

1. ==**Constants/Objects**==: Which will serve as the elements that are used in the problem, e.g. blocks.
2. ==**Variables**==: Which are wildcard objects, e.g. can be any element from constants
3. ==**Predicates**==: Which are the facts which are true at any given state.
4. ==**Operators**==: Which are the actions we can take. Each operator comes with it:
	* ==**Preconditions**==: The predicates which must be true to be able to run the operator. It's important to note that at any given time the preconditions could be considered false, in which case the operation must be cancelled. Usually you will see this denoted as $\text{PRE}$
	* ==**Effects**==: The state which will change upon completing the operation. This is hopeful and it's entirely possible for it to fail. Effects are composed of 
		* $\text{ADD}$: Facts to add upon completion
		* $\text{DEL}$: Facts to delete upon completion
# References
1. [Video from Thomas Nobles](https://www.youtube.com/watch?v=uFPx6yoXz1k)