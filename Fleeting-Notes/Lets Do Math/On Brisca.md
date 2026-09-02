Brisca is a card game containing 52 cards, ranging in the range from $[1,13]\in \mathbb{N}$, with 4 types of cards. The rules will now be explained, generalized mathematically.
## Cards Definitions
Let $I$ be an arbitrary index set, and let $\mathscr{C}$ be a nonempty collection of disjoint sets of size $|I|$, then the set $$B=\bigcup_{c\in \mathscr{C}}{\{c_i\}_{i\in I}}=\bigcup_{c\in\mathscr{C}}{c}$$
is the set of all cards in the game. 
## Card Value Order Relation
There exists an order relation $\overset{h}{<}_\ell$ which denotes whether a given card holds more value than another card. The relation is:
1. [[Relations#Transitive|Transitive]]
2. [[Relations#Antireflexive|Antireflexive]], which is not something to worry about, given no two players can hold the same cards (will be explained in the axioms)
3. [[Relations#Asymmetric|Asymmetric]]
For such a reason, the relation satisfies being a [[Relations#Strict Order|strict order relation]]. The relation is defined as follows:
* Let $a,b, h\in\mathscr{C}$ s.t. $a\neq b\neq c$ then $\forall a_i\in a,\forall b_j\in b,\forall h_k\in h\Rightarrow a_i \overset{h}{<}_b b_j \overset{h}{<}_b h_k$.
* Let $a,b\in\mathscr{C}$ then $\forall a_i, a_j\in a\wedge i<j\Rightarrow a_i\overset{h}{<}_b a_j$
## Game Step Function
We will not be utilizing the card value order relation directly. Instead we will utilize this relation to define the game step function, which takes two cards $x,y\in B$ such that $x\neq y$, and produces a Boolean value given by the order relation. It is as follows: $$G_h:B\times B\setminus \{(x,x)|x\in B\}\to\mathbb{B}$$where $\mathbb{B}$ is a set denoting boolean values. The set is defined as follows: $$G_h(x,y)=x\overset{h}{<}_x y$$
$x$ is the first card thrown in the game step, while $y$ is the second card thrown. The card type $h$ is predefined before the game starts, and is constant.
## Drawing Mechanic
The original set of cards is $B$. Drawing is without replacement, and the probability of receiving given cards is $\mu (X)=\frac{|X|}{|B|}$. at the start of the game, players will draw $3$ cards each. Let $n$ be the amount of players, the amount of cards left in the start of the game would then be $|B'|=|B|-3n$, with probabilities adjusted for $B'$. Every round, each player will place a single card and draw from the deck, therefore each round, the amount of cards in the deck would be $|B'|=|B|-n$.
## Card Knowledge
There are two sets $K,U\subseteq B$ of known cards $K$ and unknown cards $U$. The set of known cards is $K=B\setminus U$ and the set of unknown cards is $U=B\setminus K$, meaning that $K\cup U=B$. A card becomes known when it is thrown, or in your possession. Let's then make two sets $B_\text{thrown}$  and $P_i$ be the cards in someone's possession. Then $K=B_\text{thrown}\cup P_i$ for that particular player $P_i$. Considering every player has their known and unknown cards, then this becomes $K_i, U_i$ for player $P_i$.
## Standard Game Variables
1. $n$ amount of players in the game.
2. arbitrary index set $I$ for the amount of cards.
3. collection of disjoint sets $\mathscr{C}$, each of size $|I|$.
### Induced Variables
1. Set of all cards $B=\bigcup_{c\in \mathscr{C}}{c}$
2. 