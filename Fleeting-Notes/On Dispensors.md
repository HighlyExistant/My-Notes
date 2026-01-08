A dispenser is simply a producer of some item. We can denote a dispenser as $\bar{a}$, such that $\bar{a}$ produces $a$. These dispensers are connected over belts $\bar{a}\to\bar{b}$.
# Operations on Dispensers
A dispenser is defined as $\bar{a}=\{a,r\}$ such that $a$ is the item being produced and $r$ is the rate of production.
## Parallel
When two dispensers are running in parallel it is denoted as $\bar{a} | \bar{b}$, similar to the [[Process Calculus#Entering $ pi$-Calculus|pi-calculus]].
## Fork
Denoted by the symbol $\top$ which represents a single lane splitting in two. The unary operator has the following properties:
1. $\top(\bar{ab})=\top(\bar{ba})=\bar{a}|\bar{b}$
