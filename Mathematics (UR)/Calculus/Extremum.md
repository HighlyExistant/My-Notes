The extremum of a function is just an extreme point, like a ==minimum== or a ==maximum==. An example of this can be the formation of a parabola, as every parabola has a maximum or a minimum point. To find these local maxima's and minima's we should find the point at which the [[Derivatives#Computation|derivative]] of the parabola is $0$, as that is when it is neither increasing nor decreasing. 

To provide an example, the function $-x^2+2x$ is graphed like such. 
``` desmos-graph
top=5;
bottom=-5;
left=-5;
right=5;
---
y=-x^2+4x
```
You'll notice that at the extreme maximum point, there exists a place where the function is neither ascending or descending. If we find the derivative of this function: $$\frac{dy}{dx}=-2x+2$$ the point will lie at the very point where the slope equals zero, or $-2x+2=0$.
``` desmos-graph
top=5;
bottom=-5;
left=-5;
right=5;
---
y=-x^2+4x
-2x+4=0
```
This does not work for every function however, like cubic functions that don't exude this parabolic behavior, Although it is possible to find some local maxima and minima.