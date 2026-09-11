# Ring (of Sets)
Given a nonempty family of [[Set Theory|sets]] $\mathcal{R}\subseteq\mathcal{P}(X)$ it is called a ring if it satisfies the following statements:
1. $A, B\in \mathcal{R}\Rightarrow A\cup B\in \mathcal{R}$
2. $A, B\in \mathcal{R}\Rightarrow A\cap B\in \mathcal{R}$
# $\delta$ Rings
Given a nonempty family of sets $\mathcal{R}\subseteq\mathcal{P}(X)$ it is called a delta ring if it satisfies the following statements:
1. Closed under finite unions: $A,B\in\mathcal{R}\Rightarrow A\cup B\in \mathcal{R}$
2. Closed under relative complement ([[Set Theory#Difference|set difference]]): $A,B\in\mathcal{R}\Rightarrow A\setminus B\in\mathcal{R}$.
3. Closed under countable intersections: $A_n \in \mathcal{R}\Rightarrow\bigcap_{n=1}^\infty{A_n}\in\mathcal{R}$
Unlike sigma rings, these do not necessarily allow a countably infinite amount of sets to be united.
# $\sigma$ Rings
Given a nonempty family of sets $\mathcal{R}\subseteq\mathcal{P}(X)$ it is called a sigma ring if it satisfies the following statements:
1. Closed under countable unions: for $A\subseteq\mathcal{R}$ $A_n \in \mathcal{R}\Rightarrow\bigcup_{n=1}^\infty{A_n}\in\mathcal{R}$
2. Closed under relative complement ([[Set Theory#Difference|set difference]]): $A,B\in\mathcal{R}\Rightarrow A\setminus B\in\mathcal{R}$.
These two properties also imply that it is closed under countable intersections: $A_n \in \mathcal{R}\Rightarrow\bigcap_{n=1}^\infty{A_n}\in\mathcal{R}$ ==**which make the sigma ring a ring of sets**== as well as a delta ring.
