Going along with my plans of making a GPU programming language which has GPU debugging capabilities, that I don't think are suboptimal, as well as ensuring that there is no accidental data racing, I'm going to detail the language, its syntax and a general set of ideas on what this language should capture. First of all, it should capture all the features present in modern GPU programming languages such as GLSL and HLSL. I'm also taking inspiration from languages like rust which take safety very seriously through the borrow checker. In this case since there aren't really any references (unless you account for the device address extension) We'll instead be disallowing data races from happening. It shares a lot of similarities with the WGSL syntax, except I have a deep hatred for `@` so I avoid it entirely in favor of more concise keywords.
# What the Language Contains
1. ==**Shared Memory**==
2. ==**Specifically designed for Compute Shaders in mind**==, therefore no support for graphics shaders like vertex, fragment or tessalation. Also no support for raytracing. If I take it more seriously theres a possibility that I'll focus more on those features, but to simplify the project, it will only focus on Compute Shaders.
3. ==**Macros**==: I feel as though the macros in GLSL and HLSL are rather subpar, and very simple C Style macros. Instead I'll replace these with function style macros.
4. ==**Const Keyword**==: Instead of having to use C Style macros for const expressions, there will be a specific keyword for it.
5. ==**Let syntax for variable declaration**==: This is `let <value>: <type> = <expr>`.
6. ==**Intermediate Representation**==: Before turning code into SPIR-V, it will go through an intermediate phase, which will allow for debugging and optimization.
### Keywords
* ==**let**==: Variable Declaration. `let <ident-name>: <ident-type> = <expr>` or `let mut <ident-name>: <ident-type> = <expr>` 
* ==**const**==: Constant value declaration. `const <ident-name>: <ident-type> = <expr>`
* ==**shared**==: Marks something as shared memory. `shared <ident-name>: <ident-type> = <expr>` or `shared mut <ident-name>: <ident-type> = <expr>`.
* ==**layout**==: Marks something as an external input. I was questioning whether to make this an input to a function, but in this way, there will be no need to pass these values between functions to get what is needed. `layout <ident-name>: <ident-type>`.
* ==**struct**==: Object oriented structure. 
  ``` 
  struct <ident-type> {
	  <ident-name>: <ident-type>,
  } 
  ```
  * ==**impl**==: Taking from rust, the impl blocks
  ```
  impl <ident-type> {
	  <functions>
  }
  impl <ident-trait> for <ident-type> {
	  <function>
  }
  ```
  * ==**function**==: I like specific langauge, therefore I use the full term function, instead of a nickname like ==**fn**==, ==**func**== or ==**def**==. That said those keywords could also make sense. For now no generics.
  ```
  function <ident-name>(<list-comma-punctuated>) -> <ident-type> {
	  <statements>
  }
  ```
  * ==**function calls**==: Calling a function syntax is familiar `<ident-name>(<list-comma-punctuated>)`
* ==**trait**==:  A set of functions for implementing. Unlike rust however, this will not have dyn types, only impl types.
  ``` 
  trait <ident-type> {
	  <function-declarations> | <functions>
  } 
  ```
* ==**for**==: creates a loop, like any other language. This language however does have iterators using traits:
```
for <ident> in <iterator-trait> {

}
```
* ==**while**==: loops while it is true:
```
while <boolean-expr> {

}
```
## BNS Format
* Such that `$()*` stands for repeating syntax inside the brackets no times or more.
* `$` is a macro token.
* Such that `?` stands for optional token. and `$?()` denotes that everything in the bracket is optional.
* Such that `//` is a comment
```
<statement> ::= <function> | <struct> | <trait> | <impl> | <const> | <shared> | <layout>

<expr> ::= <binary-expr> | <unary-expr> | <function-call> | <const> | <shared> | <ident>

<binary-expr> ::= <expr> <binop> <expr>
<unary-expr> ::= <uniop> <expr>
<function-call> ::= <ident> ( <expr-list-input> ) ;

<let> ::= let ?mut <ident>: <ident> = <expr> ;

<const> ::= const <ident>: <ident> = <const-expr>; // <const-expr> is just expr but will be checked later to only contain const expressions which can be evaluated in compile time

<shared> ::= shared <ident>: <ident> $?(= <const-expr>) ;

<layout> ::= layout(<modifier-list>) <ident>: <ident> ;

<struct> ::= struct <ident> { <ident-list> }

<trait> ::= trait <ident> { <function-decleration-list> }

<impl> ::= impl $?(<ident> for) <ident> { <function-list> }

<modifier> ::= buffer | sampler | uniform | input | output | set(<literal>) | binding(<literal>) | push_constant | offset(<literal>)

<function> ::= function <ident>(<ident-list>) { $(expr) }
<$macro-list> ::= $(<$macro>: <$macro>),*
<$macro-list-input> ::= $(<$macro>),*
<ident> ::= primitive
```
For the primitive types that exist there are: `i32, i64, u32, u64, f32, f64, bool` as well as their vector and matrix counterparts: `bvecn, ivecn, uvecn, vecn, dvecn, matn, matnxm`. There's also the atomic counter type `atomic_u32` which can only be used in layouts.
# Project Overview
For the project to start we need:
1. ==**A Good Parser**==. I will be using my repositories `gelato_parser` as well as of course adding features and better documentation for ease of use.
2. ==**A good intermediate language**==: I'll be making my own virtual machine for the SPIR-V Language for debugging, or maybe my own bytecode inspired by it. With this there will also be a ==**config file**== supplying the buffers for debugging.
## Parsing Processs
1. Tokenization: Parse the text into tokens
2. Abstract Syntax Tree: Turn those tokens into a list of statements. The root node will be the program. We'll also perform syntax checking to see if there are any violations in the code. Providing as well, a list of scoped variables.
3. Bytecode: Using the Abstract Syntax Tree, turn it into an intermediate bytecode representation. The Virtual Machine, being based on SPIR-V, will be register based. Here the  program could be done, since in this state it is debuggable. That said if you want it out of the debug phase, then it would be useful to have the 4th step.
4. Translation: Translate the bytecode into its SPIR-V representation to actually run it in Vulkan.
## Syntax Rules for Safety
The main goal of this language is to be a safe alternative to GLSL while still retaining good speed. For this reason there will be restrictions on the language and what you can do, while still keeping safety. These rules are: