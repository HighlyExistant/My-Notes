These heuristics simplify problems, by erasing key details in a problem. Some ethical schools of thought will use these heuristics when deciding whether something is good or not.
# Notation
1. Sets of sentences are denoted using *mathscr*.
2. Sets of phrases and or words are denoted using *mathbf*
# Equivalent Consequence
When given a set of outcomes $O\subseteq\{A\Rightarrow B\}$, then given two outcomes $A\Rightarrow B, C\Rightarrow D\in O$ then $A\Rightarrow B=C\Rightarrow D\Leftrightarrow B=D$. In simpler words, An outcome is equivalent if the consequence is the same. This is to say that it doesn't matter how you reach that outcome.
## Example
1. Jessie believes that praying to their god will kill Petra. If Jessie prays, Petra will live, if Jessie does not pray, Petra will live. Regardless of the action, Petra will live, and according to equivalent consequence, there is nothing bad about doing this, since Petra will not die. That said, we could say Jessie believing something will happen, makes them a bad person.
# The Language Context
In this document we will obviously be using standard english as our primary choice, but it is important to note that different languages have different rules, they might even divide the way sentences are phrased into further subcategories, this is then incomplete. That said, I will continue perfecting the document until it is satisfactory, and reaches a mathematical description of language, ethics, etc. ==**It is important to note that something becomes when it is understood to be**==, this means that if we understand the xenopronoun 'xi' is supposed to denote a particular subject, then it is in the set of pronouns.
# Sentence Functions
## Subject
The set of all subjects is $\mathbf{S}$, and is the union of the set of all nouns, pronouns and nominals (noun phrase). 
Noun phrases can have optional information added unto them:
* Nominals = (Determiner or Adjectivals)* + Noun
I'm under the assumption that some determiners are language specific, so of course only use what is within a language, that said, the important part of determiners are the quantifiers:
* $\forall$, $\exists$, $\exists!$, and of course the set or element it corresponds to.
Meanwhile the adjectival is just added structure unto the word. For all subjects, we can use a forgetful function, which forgets a particular determiner or adjectival. We denote this similar to a forgetful functor, mapping the nominal, unto the nominal without that structure e.g:
### Adjunct Forgetful Functor
1. "The silly human" $\to$ "Silly human" or "The human" $\to$ "human".
Repeated application of the forgetful functor until all structure has been stripped will yield a noun for which it is referring to.
### Adjunct Functor
We have another function which can add structure by concatenating adjectives and determiners (adjusting for grammer) called the ==**adjunct**==.
1. "Bunny" $\to$ "Cute bunny" $\to$ "The cute bunny" $\to$ "The only cute bunny"
## Predicate
This is the action done on a particular object. Some definitions make predicate = verb + optional object, while others just make it use verb. Similar to the subject this also has an adjunct forgetful functor and adjunct functor. We can map the predicate unto an ordered pair containing the action
## Declarative/Exclamatory Sentences
A declarative and or exclamatory sentence, declares a property onto another, e.g. makes a statement about a particular subject. We will denote the set of all declaratives by the set $\mathscr{D}$ and the set of all exclamatory sentences as $\mathscr{E}$, both of which are subsets on the set of all sentences. Their union will be known as the normal declarative set $\overline{\mathscr{D}}$. It is composed of 2 parts, similar to other sentences, which are:
* The Subject
* The Predicate
The third part, which is the punctuation, turns it into either a declarative or exclamatory sentence. Now the punctuation is very general, and depends on language, therefore we will be working purely with the normal declarative set. There exists then two bijections unto either the declarative and exclamatory sentences, from the neutral declarative:
$$\pi_{\mathscr{D}}:\overline{\mathscr{D}}\to\mathscr{D}=\pi(S)=S.$$
$$\pi_{\mathscr{E}}:\overline{\mathscr{D}}\to\mathscr{E}=\pi(S)=S!$$
the preimage of both of these functions is the neutral declarative, and it simply removes the punctuation. By consequence we also find that there is an equal amount of exclamatory sentences, as there are declarative as there are neutral declaratives.
## Interrogatives
An interrogative is a sentence which asks a question. It naturally expects an answer in return. We will call $\mathscr{I}$ the set of all interrogatives, which will be a subset of all sentences.
## Imperatives
These are commands, which tell you to do something. These are formed by a verb and an object to direct the verb at.
# Answering Functions
Every person $p\in\mathscr{P}$ has an answering function which maps strings onto other strings, denoted: $$f_p: \mathscr{S}\to\mathscr{S}$$
Basically you are given a sentence, and you answer with a sentence. 
## Properties of Answering Functions
* Time dependence: Depending at what time $t$ you ask $S\in\mathscr{S}$, $f_p(S)\neq f_p'(S)$.
* Sporadic answer: The answering function for $f_p(\Lambda)$ grabs a pseudo-random sentence from $\mathscr{S}$.
## Communication
Given two answering functions $f_p$ and $f_q$, a communication is denoted as the iteration of the new function formed $$f_{pq}(S)=f_p(f_q(S))$$ending with either $f_p$ or $f_q$. A communication is then:
$$(f_{pq}^n\circ (f_p\vee f_q))(S)$$
The basin of attraction for all communications is $\Lambda$.
## Sentence Quotient Space
In standard language, we divide sentences in 4 categories:
* Declarative
* Interrogative
* Exclamatory
* Imperative
The sentence quotient space is then just the general categorization of these questions in these respective categories. Any nonsense statements can be made to not be part of the set of sentences for which we take the quotient space for.
## Context Variance/Invariance
Given an answering function $f$, an interrogative $I$, and a sentence $S$:
1. Your answer $f$ with interrogative $I$ is invariant under $S$ if $f(I)=f(IS)$.
2. Your answer $f$ with interrogative $I$ is variant under $S$ if $f(I)\neq f(IS)$.
Invariance suggests that adding that context, does not change your answer, while variance suggests that the added context does change your answer.
## Implicit Context
History, cultural and social standards, shape the way we view the world, and we apply implicit contexts to everything. For example if:
1. Jessie was not hired
2. Jessie is a woman and was not hired
The sentence does not implicate Jessie was not hired because they were a woman, nonetheless our implicit context could make that connection. That said in my ethical writings I would like to keep implicit contexts out, as to not cause confusion, unless I explicitly state it.
## Discrimination and Tolerance
Given a characteristic/modifier $C$ towards an agent $A$ then if a sentence without the characteristic, called $S$ and the sentence with the characteristic $S_C$ are variant, then it is considered discriminatory towards that characteristic:
1. $f(S)\neq f(S_C)$ e.g. is variant.
If the opposite is true, then it is considered tolerant:
2. $f(S)=f(S_C)$ e.g. is invariant.
### Fallacies
It's important to note that discrimination isn't necessarily bad, nor is tolerance necessarily good. If I say "Jessie killed Petra, is this racist?" we cannot conclude from the given information if this is racist. If we instead added the context, "Petra is black", we can still not conclude that the action is racist, but if we modify the sentence to "Jessie killed Petra, because they were black", then we can conclude that such an act is racist, because the reasoning was because they were black. If however, we modified, not the reasoning, but who Jessie is: "Jessie is a KKK member", and remove the previous modification, it becomes: "Jessie is a KKK member. Jessie killed Petra. Petra is black", we could conclude through implicit context, that Jessie killed Petra, because they were black, since implicitly we know, "Members of the KKK kill black people because they are black". 
Utilizing implicit context:
* If I say "I invited Jessie and Petra", the action is neutral.
* If I say "I invited Jessie, who is white and Petra, who is black", the action is neutral.
* If I say "I invited Jessie, who is a member of the KKK and Petra, who is black", the action is negative.
	* My definition states that this is discriminatory towards KKK members, and it is true, I am discriminatory towards KKK, but discrimination towards terrible people is not bad, since being a KKK member says something about that person, while being black does not.
	* if instead I viewed this as neutral again, I would consider myself a bad person
### Agreement Quotient Space
Given the set of interrogatives $\mathscr{I}\subset\mathscr{S}$, and an answering function $f_p$, and a boolean set $B$, mapping all answers which agree with a particular statement, e.g. "Yes" or "I agree", etc to one value of $a\in B$, and the rest of the answers to some $b\in B$ (s.t. $a\neq b$) Then this is the agreement quotient of interrogatives.
### Agreement and Disagreement
Given a set of interrogatives $\mathscr{I}$ and a boolean answer which we will denote as $B=\{0,1\}$, the agreement function for a particular person $p$ is: $$A_p:\mathscr{I}\to B$$
The agreement function is an answering function which has been restricted on interrogatives, and whose range has a quotient space induced. 

Given 2 answering functions $A_p$ and $A_q$, and an interrogative $S$: 
* agreement is formed if: $A_p(S) = A_q(S)$
* disagreement is formed if: $A_p(S)\neq A_q(S)$
We can form a new agreement function denoted $$A_{pq}(S)=A_p(S)A_q(S)$$
The agreement function can be seen as the characteristic function on the subset of opinions on a person in particular, with the universal set being the set of all opinions, therefore the new agreement function would be equivalent to the characteristic function of their intersection. Disagreement would simply be the complement of this: $$A_\overline{pq}(S)=1-A_p(S)A_q(S)$$
#### Jaccard Metric on Agreements
Given a set of interrogatives $\mathscr{I}=\{S_j\}_{j\in J}$, the Jaccard metric formed is: $$d(p,q)=1-\frac{\sum_{S\in\mathscr{I}}{A_{pq}(S)}}{\sum_{S\in\mathscr{I}}{(A_p(S)+A_q(S)-A_{pq}(S))}}$$
and denotes how much a person $p$'s opinion is similar to a person $q$'s opinion, using the axioms of metric spaces.
#### Topology induced by the Jaccard Metric
Given the Jaccard Metric on Agreements $(\mathscr{I}, d)$ we can derive a topology on people who agree $\Large\tau$ by describing their open balls: $${B(p,\epsilon)}=\{q|d(p,q)<\epsilon\}$$
then the topology is induced by the following basis:
$$\mathscr{B}=\{B(p,\epsilon)|p\in\mathscr{P},\epsilon>0\}$$
### Assignment
A neutral declarative sentence assigns characteristics unto objects. We 
### Agreement In Declaratives
The agreement function $A_p$ on declaratives works a similar way to how it does in interrogatives, except that it 
# Problems
## Example 1
Grab 3 interrogatives:
1. $I_0=$"Do minorities deserve rights"
2. $I_1=$"Do foreigners deserve rights"
3. $I_2=$"Do left handed people deserve rights"
Then grab 2 people $p,q$. Their respective answering functions said:
* $A_p(I_0)=0$
* $A_p(I_1)=1$
* $A_p(I_2)=1$
* $A_q(I_0)=1$
* $A_q(I_1)=0$
* $A_q(I_2)=1$
The Jaccard metric would then give: $$d(p,q)=1-\frac{1}{3}=\frac{2}{3}$$
This denotes that they have very disimilar opinions, but at least agree on one thing. If they were to agree on all opinions $d(p,q)=0$ and if they were to disagree on all opinions $d(p,q)=1$.
# Reasoning
For every answer you give to a dilema, there is a reason for that answer, the way we know this reason is because of the subordinating conjunction of reason. Words like "because", "since", "so that", "in order (to)", "as". We can obtain the reason from a sentence, using again a forgetful functor on everything except the subordinating conjunction of reason. Let $f$ be such a forgetful functor, and $S$ be the answer to a dilema, then:
1. $f(S)=\Lambda$, then $S$ is arbitrary.
2. $f(S)\neq \Lambda$, then $S$ is rationalized.
