Random process wherein the probability of events depends on the current state. 
# Markov Property (Memorylessness)
Denotes a variable whose future state does not depend on any previous state. We denote this as: $$P(X>t + s| X>s)=P(X>t)$$
This is the probability of $X$ larger than time step $t$ plus the state $s$ such that $X$ is larger than $s$ is equal to the probability of $X$ larger than time step $t$.

This is all to say that the probability of the next trials are independent of those of future trials.
# Discrete-Time 
We can represent these events as nodes, and the probability of the next event occurring is given by the directed graph.
``` tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
    A \arrow[from=1-1, to=1-1, loop, in=240, out=120, distance=10mm, "0.75"'] \arrow[r, bend left, "0.25"] & B \arrow[from=1-2, to=1-2, loop, in=-60, out=60, distance=10mm, "0.6"] \arrow[l, bend left, "0.4"]
\end{tikzcd}
\end{document}
```
We can also represent these as matrices: $$S_0=\begin{bmatrix}1 \\ 0\end{bmatrix}$$where each element corresponds to the probability of the next event occuring. If the first element is the probability of event $A$ and the 2nd is the probability of event $B$ then it will be set to $A$ initially. The $S_0$ denotes the initial state. If the probability of $A$ staying the same is $0.75$ and the probability of it changing to $B$ is $0.25$ then $S_1$ will be $$S_1=\begin{bmatrix}0.75 \\ 0.25\end{bmatrix}$$
When you're at state $B$ however, there's a chance of $0.6$ it will stay at $B$ or $0.4$ it will go to $A$. We represent all these probabilities as: $$P=\begin{bmatrix}0.75 & 0.4\\ 0.25 & 0.6\end{bmatrix}$$
When going through the probability of something being at a specific place at timestep $1$ we can simply denote it by the matrix multiplication: $$S_1=PS_0$$
And if we wanted to denote it for timestep $n$ we would say it's $$S_n=P^nS_0$$
