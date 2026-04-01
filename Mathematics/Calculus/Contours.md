The contour is the ==**outline of a shape**==.
# Contour Maps
When given a multivariable function, such as $z=f(x,y)$, it can be difficult to graph out, in 3 dimensions. Instead we can create a contour map, where we pick a specific height, or $z$ value, and map them unto a 2d map, with a specific id corresponding to its height.
## Example
Lets take the multivariable function $f(x,y)=x^2 + y^2$:

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}

\begin{document}

\begin{tikzpicture}
\begin{axis}[colormap/viridis]

\addplot3[
	surf,
	samples=18,
	domain=-3:3
]
{x^2+y^2};

\end{axis}
\end{tikzpicture}

\end{document}
```
