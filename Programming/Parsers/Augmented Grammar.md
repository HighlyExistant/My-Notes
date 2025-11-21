> *If $G$ is a grammar with start symbol $S$ then $G'$, the augmented grammar for $G$, is the grammar with new start symbol $S'$ and a production value $S'\to S$. The purpose of this new production is to indicate to the parser when it should stop parsing and announce acceptance of input. The ' . ' before S indicates the left side of ' . '  has been read by a compiler and the right side of ' . ' is yet to be read by a compiler. - [geeksforgeeks.org](https://www.geeksforgeeks.org/compiler-design/problem-on-lr0-parser/)*

# Vocabulary
* ==**Production**==: Are the rules of combining symbols to create other symbols ej. $S' \to S$.
* ==**Starting Symbol**==: Is the symbol at which the parser should stop parsing.
* ==**Terminals**==: Terminals are the building blocks of the grammar, or the [[Abstract Rewriting System#Normal Forms (Irreducibles)|irreducibles]]. 
* ==**[[Backus–Naur form#^4a6c9d|Non-terminals]]**==: Are the composite of terminals. In notation, as stated above, adding the ' . ' as a prefix means we need to write all its production and add ' . ' as a prefix to all those sub productions.
## Example
Given a grammar:
* $S\to A A$ 
* $A \to aA$ or $b$ 
The augmented grammar would be.
* $S'\to .S$
* $S\to .AA$
* $A\to .aA$
* $A \to .b$

# Action-Goto Tables
With a given grammar you can use these rules to constructo a table. In the table, the accepted state is written as `$`. 
* ==**State**==: Is a numbered index of all of the action-goto pairs.
* ==**The Goto Portion**==: Tells the parser where to go when it finds a reducible element in the stack.
* ==**The Action Portion**==: Tells the parser where to go when it finds an irreducible element in the stack.