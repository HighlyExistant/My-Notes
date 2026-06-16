# Derivation
We represent the neck area where the head will go through the chest area is larger than the side area. The circumference, should then also equal 2$\cdot$chest + 2$\cdot$shoulder = *circumference*.
#### Example
Let *count*=19 and *spacing*=4. then the *circumference*=96. therefore we can choose the two values *chest* and *shoulder* such that it satisfies the equations 2$\cdot$chest + 2$\cdot$shoulder = *circumference* and *chest* > *shoulder* such that *chest*, *shoulder* $\in\mathbb{N}$. We can solve for this and get that $$c+s=48$$ and so $c$ is $48-s$. If we add an arbitrary ratio of $\frac{1}{4}$ then $c=36$ and $s=12$.
## Sets
* Let $\mathbb{N}$ be the set of all natural numbers.
* Let $C$ be the set of all possible values of the circumference: $$C=\{n\in\mathbb{N}|n=\textit{spacing}+2+(\textit{spacing}+1)\cdot (\textit{count}-1)\}$$
# Variables
* let *spacing*: $\mathbb{N}$.
* let *count*: $\mathbb{N}$
* let *chest*: $\mathbb{N}$ (length of chest)
* let *shoulder*: $\mathbb{N}$ (length of shoulders)
* let *height shoulder*: $\mathbb{N}$ (height of shoulders)
* let ratio: $\mathbb{Q}$ (the chest, shoulder ratio)
* let *arm*: $\mathbb{N}$ (circumference of arms)
* let *circumference*: $C=\{n\in\mathbb{N}|n=\textit{spacing}+2+(\textit{spacing}+1)\cdot (\textit{count}-1)\}$.
Some testing suggests that this should be *spacing*=4 and *count*=16 or 18.
### Rnd 1
* ch-sc-*circumference* (We do this to add neckspace so the top can fit)
* ss-*start* (We stitch it to the start to form a circle)
### Rnd 2 
* 1 dtr
* ch-sp-*spacing* with sc 
* rep *count* (to finish the stitch on the circle)
* rep *height shoulder* (repeat the circle till shoulder height is reached)
### Rnd 3
