Is the study of functions and a formal system of studying computations. Lambda Calculus is separate from [[Type Theory|Type Theory]] but we will occasionally use it to describe certain operations.
## Definitions
* ==**Variables**==: things such as $x, y, z$ are terms
* ==**Constants**==: things such as $a, b, c$ are terms
* ==**Abstractions**==: The lambda abstract of a term is a form of creating functions, which receive an input $x$ and produce an output as $\lambda x.M$. This is basically a <mark style="background: #ABF7F7A6;">function definition</mark>.
* ==**Application**==: Is a combination of these terms, like $xy$, which applies a function $x$ on $y$. A much more explicit version would be $(\lambda x.x)(y)$. This is a way of calling functions, also known as a <mark style="background: #FF5582A6;">function application</mark>. Applying a function is associative.
## Currying
When writing a function that has two inputs, such as an addition function $+: (\text{nat} \times \text{nat})\to \text{nat}$ (this is using [[Type Theory|type theory]] syntax) we can rewrite this into its curried form $$+:\text{nat} \to (\text{nat} \to \text{nat})$$ This can be thought of as taking a natural number, and producing a function from natural numbers to natural numbers. Heres an example of currying:
$$
	\lambda x.\lambda y.xy
$$
here the function $\lambda x$ creates a function $\lambda y.xy$. If we wanted to call this function we could say:
$$
	(\lambda x.\lambda y.xy)(a)(b)
$$
which would first call $(\lambda x.\lambda y.xy)(a)=\lambda y.ay$ then call that using $(\lambda y.ay)(b)=ab$

## Lambda Calculus and Stacks
You'll notice that the way these operations work is via a stack.
* <mark style="background: #ABF7F7A6;">When a function consumes a variable it pops the stack</mark>.
* <mark style="background: #FF5582A6;">When a function is called it pushes onto the stack</mark>.
$$
	{\color{cyan}\lambda x.x x}{\color{#ff2596be} a} = {\color{#ff2596be} a a}
$$
You can notice that the stack used to contain only 1 $a$ but after getting consumed by the function it got pushed twice onto the stack for the final answer $a a$.
## Truth Values
Similar to how truth values work in Boolean algebra, they have two states ==**true**== or ==**false**==. In lambda calculus these values must be defined in terms of functions
* ==**True**==: Also known as $\top$ can be represented as $\lambda x. \lambda y.x$, which takes the first value it sees $x$ and ignore the second value $y$, returning only $x$.
* ==**False**==: Also known as $\perp$ can be represented as $\lambda x. \lambda y.y$, which ignores the first value $x$ and takes the last value $y$.
* ==**Booleans**==: The similarity of these true and false values can not be dismissed, as this is how we construct Booleans. By being able to interchange the values $x$ and $y$ at the end, we can put these all under the term Boolean.
## If Statements
These are [[Critique of Pure Reason#^a34345|hypothetical statements]] together with a disjunction between whether it is true or false. In total these are 3 inputs.
This can be defined as $$\lambda {\color{blue}b} . \lambda {\color{lightgreen}t} . \lambda {\color{red}f}.{\color{blue}b} {\color{lightgreen}t} {\color{red}f}
$$Where:
* $\color{blue}b$: Is a Boolean value.
* $\color{lightgreen} t$: Is the statement that will be called if the Boolean value is true. 
* $\color{red} f$: Is the statement that will be called if the Boolean value is false. 
We will denote this operation as $\text{IF}$.
## Unary Logical Operators
### Logical Not
``` pseudo
\begin{algorithm}
\caption{Not}
	\begin{algorithmic}
		\Procedure{Not}{$A$}
			\If{$A$}
				\State false
				\Else
				\State true
			\EndIf
		\EndProcedure
	\end{algorithmic}
\end{algorithm}
```
Can be expressed as: $$\lambda a.\text{IF}(a)(\text{false})(\text{true})$$
## Binary Logical Operators
utilizes two Boolean values and produces a Boolean value. $$
\text{F}: (\text{bool} \times \text{bool}) \to \text{bool}$$Due to the cartesian product, we already know we should curry it into $\lambda a.\lambda b$ at the very beginning.
### Logical And
Lets analyze [[General Logic#Logical Conjunction|truth table]] for $\text{AND}$ 
``` pseudo
\begin{algorithm}
\caption{And}
	\begin{algorithmic}
		\Procedure{And}{$A, B$}
			\If{$A$}
				\If{$B$}
					\State true
				\Else
					\State false
				\EndIf
				\Else
				\State false
			\EndIf
		\EndProcedure
	\end{algorithmic}
\end{algorithm}
```
We can see that only when $A$ and $B$  are true then it is true, but every thing else is false. This can be represented as:
$$
\lambda a.\lambda b.\text{IF} (a)(\text{IF}(b)(\text{true})(\text{false}))(\text{false})
$$
There's a lot of repetition here however. For example if $B$ is true then we return true, and if its false then we return false. This can be simplified to just be 
``` pseudo
\begin{algorithm}
\caption{And}
	\begin{algorithmic}
		\Procedure{And}{$A, B$}
			\If{$A$}
				\State B
				\Else
				\State false
			\EndIf
		\EndProcedure
	\end{algorithmic}
\end{algorithm}
```
This simplifies it to: $$\lambda a. \lambda b. \text{IF}(a)(b)(\text{false})$$
### Logical Or
Lets analyze [[General Logic#Logical Disjunction|truth table]] for $\text{OR}$. 
``` pseudo
\begin{algorithm}
\caption{Or}
	\begin{algorithmic}
		\Procedure{And}{$A, B$}
			\If{$A$}
				\State true
				\Else
				\If{$B$}
					\State true
				\Else
					\State false
				\EndIf
			\EndIf
		\EndProcedure
	\end{algorithmic}
\end{algorithm}
```
We can notice the same logic as last time and simplify to:
``` pseudo
\begin{algorithm}
\caption{Or}
	\begin{algorithmic}
		\Procedure{And}{$A, B$}
			\If{$A$}
				\State true
				\Else
				\State $B$
			\EndIf
		\EndProcedure
	\end{algorithmic}
\end{algorithm}
```

This becomes: $$\lambda a. \lambda b. \text{IF}(a)(\text{true})(b)$$
### Logical Implication
``` pseudo
\begin{algorithm}
\caption{Implies}
	\begin{algorithmic}
		\Procedure{Implies}{$A, B$}
			\If{$A$}
				\State $B$
			\Else
				\State true
			\EndIf
		\EndProcedure
	\end{algorithmic}
\end{algorithm}
```
This becomes: $$\lambda a. \lambda b. \text{IF}(a)(b)(\text{true})$$
# Records
A record is a set of ==**fields**== where each field consists of a unique label and a type. For example: $$\text{person}=\begin{bmatrix}\text{age}: \text{nat} \\ \text{name}:\text{string}\end{bmatrix}$$
We can then create an object as: $$\text{Object}=\begin{bmatrix}\text{age}=12 \\ \text{name}=\text{"Fulano"}\end{bmatrix}
$$
or $$\text{Object}=\begin{bmatrix}\text{age}=a \\ \text{name}=b\end{bmatrix}
$$

