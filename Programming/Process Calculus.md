# Introduction
Multithreading is a way in which computers can achieve running multiple computations at once. While this might sound amazing (and it is), it comes with its own slew of problems that need to be solved. Before that lets set a few rules so you know what exactly will happen in multithreading, and define these things mathematically. I will be discussing multiple process calculi by order of history, and taking note of new concepts, and transformations of old concepts.
# Dijkstra and GCL
Introduced **Guarded Command Language (GCL)** and the concept of guards in his paper, "Guarded Commands, Nondeterminacy and Formal Derivation of Programs", in 1975. A ==**guarded command**== is a statement of the form $P\to S$ where:
* $P$ is a [[Rhetoric#^726ebd|proposition]], called a guard.
* $S$ is a statement.
These are also known as ==**preconditions**==. 
If $P$ is true then $S$ can be executed.
* <mark style="background: #CACFD9A6;">Skip</mark> Is a NOP instruction which does nothing.
* ==**Abort**== Is an undefined instruction which can do anything, and is used to describe a failure in a proof usually.
# Tony Hoare and CSP
Extends on Dijkstra's **GCL** and their guarded commands in 1978. Tony Hoare's philosophy in making CSP is that a fundamental part of programming is the input and output. He went about describing a language that could use these operations for sequential processing on channels.
## Primitives
* ==**Processes**==: Statements, operations etc.
* ==**Channels**==: How processes communicate (ej. bytes, text). You can pass data structures, but values aren't shared. It can be:
	* ==**One-to-One**==: Post a piece of data for one other channel on a different process.
	* ==**One-to-Many**==: Multiple processes are grabbing off a work queue, where the first one to receive it is the one that works off of it.
	* ==**Many-To-One**==: Multiple channels pushing data onto one process to use.
	* ==**Many-To-Many**==: Multiple channels sending to multiple channels.
## Synchronization
Given two process $A, B$:
* <mark style="background: #FF5582A6;">Output</mark>: To output a value from $A$ to $B$ you use $B!y$ where $y$ is the output value.
* <mark style="background: #BBFABBA6;">Input</mark>: To receive the output from $A$ you use $A?x$ where $x$ is the value the output value $y$ will go to. If $A$ does not output onto $A$, then $B$ will simply <mark style="background: #ADCCFFA6;">wait</mark> for $A$. 
The idea is very similar if not equivalent to pipes.
## Operators 
Introduced **Communicating sequential processes (CSC)**. Some operators and constants:
* $p;q$ is a ==**sequential composition**==, meaning that $p$ is executed then $q$ is executed.
* $p \textbf{ u } q$ means that there is a choice between $p$ and $q$, and only one of them will be executed.
* $1$ is execute by doing nothing, making no change. This can be viewed as equivalent to Dijkstra's skip.
## Refinement Ordering
* ==**The Below Operator**==: Represented as $\leq$, is used to denote that an execution $p$ is also an execution of $q$. Ej. $p \leq q$.
# Calculus of Communicating Systems
Created by Robin Milner around 1980, it models communications between two processes specifically ==**One-to-One**==. The syntax is given by BNF grammar as:$$P::= 0\;|\;a.P_1\;|\;ref A\;|\;P_1+P_2\;|\;P_1|P_2\;|P_1[b/a]\;|\;P_1\setminus a$$
* <mark style="background: #CACFD9A6;">Inactive Process</mark>: Represented as $0$, it does nothing and is equivalent to a NOP. It marks the end of execution.
* ==**Action**==: $a.P_1$ performs action $a$ then continues as the process $P_1$.
* ==**PID**==: works as a reference of a process. by defining $A\overset{\text{def}}{=}P_1$. Using this reference you can allow recursive definitions.
* ==**Choice (Sum)**==: $P_1+P_2$ can proceed exclusively as either $P_1$ or $P_2$.
* ==**Parallel Composition (Concurrency)**==: Is the act of two processes running at the same time. Ej. Let $P, Q$ be processes. We say that $P$ and $Q$ are running concurrently by saying: $P|Q$.
* ==**Renaming**==: $P_1[b/a]$ Is a process $P_1$ where all actions named $a$ will be renamed as $b$.
* ==**Restriction**==: $P_1\setminus a$ is a process $P_1$ without $a$.
# Entering $\pi$-Calculus
Created in 1992 it presents a few basic operations for basic concurrency modeling.
## Definitions
* ==**Free Names**==: Represented as a set $N$, which contains a list (possibly infinite) of elements called free names, which will be passed as communication channels or values.
* ==**Bound Names**==: These names mean nothing outside of the process it is running in. Ej. $a(x).\bar{x}y.0$, what this will do is bind the input from $a$ onto $x$ and then output $y$ on $x$.
* <mark style="background: #CACFD9A6;">Nil Process</mark>: Functions as an identity $0$ where it is a process that has already finished execution. Basically a NOP instruction. 
* ==**Communication**==: Represents communication channels in which two processes can talk to one another.
	* <mark style="background: #FF5582A6;">Output Prefixing</mark>: $\bar{c}\langle y \rangle.P$ or $\bar{c}y .P$ is a name $y$ emitted on channel $c$ before proceeding as $P$.  It could also represent a label $c$ usable only once by $\text{goto } c$. 
	* <mark style="background: #BBFABBA6;">Input Prefixes</mark>: $c(x).P$ is a process $P$ <mark style="background: #ADCCFFA6;">waiting</mark> on a communication channel $c$ and binding the name received on $x$. It could also represent a $\text{goto } c$ operation.
  If we wanted to represent these mathematically then it would be a function $$f:N^2\times P\to P$$ as it takes two inputs of free names and one process. Where $f$ is either output  $\bar{ }$  or inpu.t $()$. A simple program that represents these two functions is $$\bar{a}b.P|a(x).Q$$ which will output $b$ on channel $a$ then on the other process, receive  $b$ and ==**bind it**== to $x$, therefore $x=b$, then continue running process $Q$. Which can be reduced to: $$\bar{a}b.P|a(x).Q\Rightarrow P|Q\{b/x\}$$
* ==**Restriction**==: Represented as $(vx)P$ represents an allocation of a new constant $x$ which is always a communication channel with scope $P$. 
* ==**Concurrency**==: $P|Q$ Is the act of two processes running at the same time. Is both commutative and associative.
* ==**Abstract, Sequential**==: $P.Q$ represents a sequential operation which finishes $P$ then continues to $Q$. The operation has right distributivity of any $+$ operations.
* ==**Replication**==: Written as $!P$ is a process which can always create a new copy of $P$. It is equivalent to $P|!P$. This operation is also distributive among processes, example: $!(P|Q)=!P|!Q$. This operation is lazily evaluated, that is, it is only evaluated once an operation involving it is executed, in which case it will then duplicate the process. This is to avoid there being actual infinite amount of processes when calculating programs.
* ==**Choice (Sum)**==: $P + Q$ does exclusively either $P$ or $Q$.
* ==**Binding**==: The binding syntax above written as $Q\{b/x\}$ simply says that all $x$ in $Q$ shall know be $b$'s.
### Example of the Non-Deterministic nature of $\pi$-Calculus
Given a program $$\bar{a}y|a(x).\bar{x}w|\bar{a}z$$ We can see the two processes $\bar{a}y$ and $\bar{a}z$ racing to output onto channel $a$. There are two possibilities to this program, either: $$\bar{a}y|\bar{z}w$$ if the channel $\bar{a}z$ wins, or  $$\bar{y}w|\bar{a}z$$ if the channel $\bar{a}y$ wins.
### Example of Bound Names within $\pi$-Calculus
There are 2 ways to create bound names, these are <mark style="background: #BBFABBA6;">positive prefixes also known as inputs</mark>, or ==**restrictions**==. When we start a program, we'll start with a restriction to be able to allocate a new channel. The scope of that channel, or the processes that know of the existence of that channel, are contained within the scope of the restriction. 
##### Scope Intrusion
When 2 variables have the same name, due to one being passed and another being restricted, the restricted variable, such as $x$ can be renamed to $x'$ as many times as needed. This renaming of $x \to x'$ is done using the rewrite semantic $\{x'/x\}$.
##### Scope Extrusion
When a process with a private variable (a variable within a scope defined by a restriction) wants to pass that variable to another process without that variable in its scope, it will make an extrusion in which that process now belongs to that variable.
* If the process has no name bounded defined $x$ in its scope, it will just define $x$ of that restriction that is now within its scope.
* If instead the process already has a channel defined $x$ bounded within its scope, it will redefine the passed down variable to $x'$.
* After sending a private channel $x$ in a public channel $y$ (e.g. $y\langle x\rangle$) then it will be extruded to all the process becoming a public channel. In contrast if its sent on a private channel, then it will only extrude until that private channel.
# Synchronous $\pi$-Calculus
In this version of the calculus, outputs and inputs synchronize with each other, producing silent actions $\tau$. If a pair $\bar{x}y$ does not find its respective $x(y)$, it will wait.