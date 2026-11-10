# Chudnovsky
The algorithm that computes $\pi$ to arbitrary decimals is $$\frac{1}{\pi}=12\sum_{k=0}^\infty{\frac{(-1)^k(6k)!(545140134k+13591409)}{(3k)!(k!)^3(640320)^{3k+3/2}}}$$This is basically the Ramanujan series for $\pi$ $$\frac{1}{\pi}=12\sum_{k=0}^\infty{\frac{(-1)^k(6k)!(A+Bk)}{(3k)!(k!)^3C^{3k}}}$$
For 
* $A=13591409$
* $B=545140134$
* $C=640320$
# Binary Splitting
We can achieve good performance by performing recursive splits to the algorithm. The following technique holds for any linearly convergent series of the form: $$S=\sum_{n_1<n<n_2}{\frac{a(n)p(n_1)\dotsb p(n)}{b(n)q(n_1)\dotsb q(n)}}$$
Instead of computing the series directly, we compute the integers 
* $P=p(n_1)\dotsb p(n_2-1)$
* $Q=q(n_1)\dotsb q(n_2-1)$
* $B=b(n_1)\dotsb b(n_2-1)$
* $T=BQS$
Where The original algorithm proposes to compute directly if $n_2-n_1< 5$ and split otherwise, but the implementations I've seen make due when $n=1$. I suppose the $n_2-n_1<5$ restriction in the paper was due to needing more splits for bounds of lesser radius.
## How to perform a split
Choose some index $n_m$ in the middle of the interval $[n_1,n_2]$. We then compute the above mentioned components for both sides of this split, keeping in mind the rules for splitting and evaluating directly. The components $P_l, Q_l, B_l, T_l$ are computed using the terms in the interval $[a,n_m]$ where $a$ is the first element of the previous split. The components $P_r,Q_r,B_r,T_r$ are instead computed in the interval $[n_m, b]$ where $b$ is the final element of the previous split. The algorithm is applied on $n_1=0$ and $n_2=n_\text{max}$. Once we return from the split, we set 
* $P=P_lP_r$
* $Q=Q_lQ_r$
* $B=B_lB_r$
* $T=B_rQ_rT_l+B_lP_lT_r$.
The final operation is a floating point division: $$S=\frac{T}{BQ}$$

# References
1. [Nick Craig-Wood](https://www.craig-wood.com/nick/articles/pi-chudnovsky/)
2. [Bin Split Article](https://www.ginac.de/CLN/binsplit.pdf)
