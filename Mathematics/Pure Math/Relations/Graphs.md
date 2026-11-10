# Associating Matrices to Relations
If $A=\{a_1, ..., a_m\}$ and $B=\{b_1,...b_n\}$ then for $R\subseteq A\times B$ the matrix $M_R$ is defined as: $$r_{ij}=\begin{cases}{1:   (a_i,b_j)\in R\\0:   (a_i,b_j)\not\in R}\end{cases}$$
Given an example matrix for the set $A=\{1,2,3\}$ and $B=\{a,b\}$ with [[Types of Orders|order]] $a_1=1,a_2=2.a_3=3$ and $b_1 = a, b_2 = b$, and a relation $R=\{(1,a), (1,b), (3,b)\}$, then the matrix is: $$M_R=\begin{bmatrix}1 & 1 \\ 0 & 0 \\ 0 & 1\end{bmatrix}$$

# Associating Digraphs to Relations
A directed graph is a relation $R\subseteq A\times A$ where $A$ contains the ==**vertices**== and the relation $R$ are the ==**directional edges**==. 
## Definitions
1. We say $a\to b$ when $(a,b)\in R$.
2. A loop is formed when $a\to a$.
3. The adjacency matrix of the graph is the matrix formed by the relation $M_R$.
# Degrees of a Graph
For a vertex $a$, the degree of output $d^+(a)$ is the number of directed edges leading out to some other vertex. The degree of input $d^-(a)$ is the number of directed edges leading towards $a$.
# Weights in Graphs
We can add weights to graphs as: $$\text{wt}(a\to b)=f(a,b)$$
## Matriz de Transferencia
According to my discrete math professor, a useful weight to use is: $$\text{wt}(a\to b)=(-1)^{a+b}$$This matrix is just the matrix of adjacency with weights instead of $1$.
### Example with de Bruijin's Graph
The graph: $$\mathbb{F}^3=\{(a,b,c)|a,b,c\in\{0,1\}\}$$
Consider the relation: $\sim$ where $$(a_1,b_1,c_1)\sim (a_2,b_2,c_2)\Leftrightarrow (b_1=a_2\wedge c_1=b_2)$$The  matrix formed by this graph, using lexicographical order is: $$\begin{bmatrix}1 & 1 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 1 & 0 & 0 & 0 & 0 \\ 0 &0 &0 &0 & 1 & 1 &0 &0  \\0 &0 &0 &0 &0 &0 & 1& 1\\1 & 1 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 1 & 0 & 0 & 0 & 0 \\ 0 &0 &0 &0 & 1 & 1 &0 &0  \\0 &0 &0 &0 &0 &0 & 1& 1\end{bmatrix}$$
This type of matrix is called (matriz 2-circulante) 
## Counting Degrees Theorem
In a finite digraph: $$\sum_{a\in A}{d^+(A)}=\sum_{a\in A}{d^-(a)}$$
### Using Matrices
We can count $d^+(a)$ of a vertex in a graph by counting the $1$'s in the row of a matrix, and $d^-(a)$ by counting the columns. Considering that the sum of all $1$'s is the same regardless of how you sum them, it gives the proof to the theorem above.
# Walks
A walk of length $k$ of $a, b$ is $$a\to x_1\to x_2\to ...\to x_{k-1}\to b$$ e.g. the number of arrows it took to reach $b$. It is also just the number of relations used in $R$, we can denote walks of $k$ length as $$a R^k b$$
The set of all walks is
$$R^\infty =\bigcup_{k=1}^\infty{R^k}$$
Another definition to note is reachability. Consider: $$\Delta_A = \{(a,a)| a\in A\}$$
A vertex is reachable if it is in: $$R^*=\Delta_A\cup R^\infty$$
## Product of Matrices with Walks
Consider the new matrix product $M_R^2=M_R\odot M_R$. We treat products as $\wedge$ and sums as $\vee$ so we write this as just the matrix multiplication with those operations replaced.