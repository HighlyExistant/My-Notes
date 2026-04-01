# Round Robin
This is a very simple scheduling algorithm, where every task is performed after one another. Lets say you wanted to repeat the tasks $T_0, T_1, T_2$. A round robin algorithm would make it so that they go in consecutive order:
```  tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
	& T_0 \arrow[dr, bend left] \\
	\arrow[ur, bend left] T_1 & & \arrow[ll, bend left] T_2
\end{tikzcd}
\end{document}
```
This is also why it's called the round robin algorithm.