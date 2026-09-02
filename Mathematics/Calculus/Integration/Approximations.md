When we are trying to approximate an integral $F(b)-F(a)$ we will assume that we are given the function $f(x)$. Reviewing the definition of the integral, the simplest way to integrate a value via approximation is using the 
# Runge-Kutta Integration
## Forward-Euler (FE) or RK1
This is a review of [[Derivatives#Linear Approximations|linear approximations]]. Given $\dot{x}=f(x,t)$ and $x=F(x,t)$, then we can consider our current position to be $x_k=F(x,k)$ and we can approximate our next position as $$x_{k+1}=x_k+ f(x_k,t_k)\Delta t$$
## 2nd Order Runge-Kutta
This method of continuous linear approximation Grabs the midpoint t value of integration, then does the linear approximation, before adding it unto the original positional value. $$x_{k+1}=x_k+f(x_k+\frac{\Delta t}{2}f(x_k,t_k), t_k+\frac{\Delta t}{2})$$
alternatively we can write $f_1$ to be the original forward Euler integration: $$f_1=f(x_k,t_k)$$ and $f_2$ to be the midpoint $$f_2=f(x_k+\frac{\Delta t}{2}f_1,t_k=\frac{\Delta t}{2})$$
to then write $$x_{k+1}=x_k+f_2\Delta t$$
### Geometric Intuition
In a usual linear approximation, we would grab the slope $f(x_k,t_k)$ and move $\Delta t$ forward by that slope. Alternatively, what we do in RK2, we grab the slope of the midpoint between $x_k$ and $f(x_k,t_k)$. to grab that slope, obtain the midpoint and input it into $f$, so: $$f(x_k+\frac{1}{2}f(x_k,t_k)\Delta t,\frac{1}{2}\Delta t)$$