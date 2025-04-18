Firstly category theory is not about categorization, it is a mathematical theory about mathematical structure.

### Category
A category is usually denoted as a short capitalized word or an abbreviation in bold or italics, such as ***$C$***. It consists of: 
* Objects, 
* Morphisms
* Composition
* Identities
subject to 2 requirements:
* Identity Law
* Associativity law

### Objects
In principle it can be anything, usually a number or a set or another mathematical structure.
### Morphisms
For any two objects $A, B$ the category has morphisms from $A \to B$. Which can be denoted as:
$$\textbf{C}(A, B)=\{f, g, \dots\}$$They can be thought of as relations. There is a morphism from $A \to B$ if there is a relation to $B$. Such can be written as:
$$
f: A \to B
$$
$B$ in this case does not necessarily need to be related to $A$ though. It can be a one way connection. There can also be an empty set of relations from $A \to B$ or there can be more than one relation. Morphisms are commonly described as functions, although they don't have to be.
#### Example of a commutative diagram

<center>
<img src="https://i.upmath.me/svg/%0A%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%5Ctextcolor%7Bwhite%7D%7BA%7D%20%26%26%20%5Ctextcolor%7Bwhite%7D%7BB%7D%0A%09%5Carrow%5B%22f%22%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D1-3%5D%0A%5Cend%7Btikzcd%7D%5C%5D%0A" alt="
\[\begin{tikzcd}
	\textcolor{white}{A} &amp;&amp; \textcolor{white}{B}
	\arrow[&quot;f&quot;, color=white, from=1-1, to=1-3]
\end{tikzcd}\]
" />
</center>
Here we can see a morphism $f$ that turns $A \to B$. Now lets say we had another morphism

<center>
<img src="https://i.upmath.me/svg/%0A%5C%0A%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%5Ctextcolor%7Bwhite%7D%7BB%7D%20%26%20%5Cbullet%20%26%20%5Ctextcolor%7Bwhite%7D%7BC%7D%0A%09%5Carrow%5B%22g%22%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D1-3%5D%0A%5Cend%7Btikzcd%7D%5C%5D%0A" alt="
\
\[\begin{tikzcd}
	\textcolor{white}{B} &amp; \bullet &amp; \textcolor{white}{C}
	\arrow[&quot;g&quot;, color=white, from=1-1, to=1-3]
\end{tikzcd}\]
" />
</center>
this means that there is a morphism, say $h$, that allows us to go from $A \to C$.
<center>

<img src="https://i.upmath.me/svg/%0A%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%5Ctextcolor%7Bwhite%7D%7BA%7D%20%26%26%20%5Ctextcolor%7Bwhite%7D%7BC%7D%0A%09%5Carrow%5B%22%7Bf%20%5Ccirc%20g%7D%22%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D1-3%5D%0A%5Cend%7Btikzcd%7D%5C%5D%0A" alt="
\[\begin{tikzcd}
	\textcolor{white}{A} &amp;&amp; \textcolor{white}{C}
	\arrow[&quot;{f \circ g}&quot;, color=white, from=1-1, to=1-3]
\end{tikzcd}\]
" />
</center>
If such composition does not exist, then it is not a category
### Identities
are morphisms from an object to itself

<center>
<img src="https://i.upmath.me/svg/%0A%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%5Ctextcolor%7Bwhite%7D%7B1_A%3AA%7D%20%26%26%20%5Ctextcolor%7Bwhite%7D%7BA%7D%0A%09%5Carrow%5Bcolor%3Dwhite%2C%20from%3D1-1%2C%20to%3D1-3%5D%0A%5Cend%7Btikzcd%7D%5C%5D%0A" alt="
\[\begin{tikzcd}
	\textcolor{white}{1_A:A} &amp;&amp; \textcolor{white}{A}
	\arrow[color=white, from=1-1, to=1-3]
\end{tikzcd}\]
" />

</center>

We need to have 1 morphism from the object to itself

# Types of Categories

### Homomorphisms
Are categories that satisfy the property $f(a \cdot b) = f(a) \cdot f(b)$. 
### Isomorphisms
are morphisms with inverses. If there exists an isomorphism between 2 objects, then those objects are isomorphic, $A \cong B$. It is said that two structures are isomorphic if there is an isomorphism from one space onto another space. 

# Functors
are a translation between categories. It lets us change the priority of the category. To have a functor $F: C \to D$ we need the following:
* Function on objects
* Function on morphisms
As long as they respect:
* Identity preservation $F(1_A) = 1_{F(A)}$
* Composition preservation $F(g \circ f) = F(g) \circ F(f)$
