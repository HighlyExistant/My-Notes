This is a simple syntax to allow for the creation of grammars by defining simple building blocks.
# Notation
* ==**non-terminal**==: `<symbol>` which creates a category^4a6c9d
* ==**Definition**== `::=` Is a meta symbol which means "is replaced by".
* ==**Or**== `|` defines that it can be replaced by any of the following symbols.
## Additional Notation
* ==**Optional Items**==: `[<item-x>]`
* ==**0 or more times**==: `<item>*` or `{<item>}` ej. ``
* ==**1 or more times**==: `<item>+`
* ==**Range**==: `[start-end]`
* ==**Terminals**== are written in bold.
# Example
An example would be [[Lambda Calculus|lambda calculus]] which has a BNF of:
```
<expr> ::= <variable> | <abstraction> | <application>

<variable> ::= [a-z]+
<abstraction> ::= \ <variable> . <expr>
<application> ::= (<expr> <expr>) | 
				  (<expr>) <expr> | 
				  <expr> (<expr>)
```

