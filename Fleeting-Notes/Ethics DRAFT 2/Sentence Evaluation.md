Ultimately to understand any topic, especially one where the use of specific words can alter the meaning of a sentence entirely, it is important to note how one should go about evaluating their structure. It is also important to note that in doing so, we cannot possibly cover every edge case, since language evolves over time, and since that is the case, it is important to adjust the evaluation of sentences for new definitions which come along in the future. It is also important to note that due to sentences being language specific, we cannot possibly evaluate the same sentence similarly, and therefore must resort to an abstract understanding of sentences and their forms. Ultimately the most standard form of many sentences across many languages use the concepts of ==**subject**==, ==**predicate**== and ==**object**==. My ultimate goal with this document is:
- [x] Describe the set of all words, phrases and sentences, as a subset of strings.
- [x] Describe the set of Subjects, Predicates and Objects
- [x] Describe the adjunct
	- [x] Describe the adjunct functor and adjunct forgetful functor.
		- [x] Describe a method of acquiring a subject quotient space using the adjunct forgetful functor.
		- [x] Describe a method of acquiring a predicate quotient space using the adjunct forgetful functor.
		- [x] Describe a method of acquiring a object quotient space using the adjunct forgetful functor.
- [ ] Describe Quantifiers:
	- [ ] Generalizations and Universalized
		* A generalization is the removing of criteria to be met, while a universalization encapsulates a statement to apply $\forall x\in X$. we would say then that it has been universalized on $X$. Generally speaking a generalization would then be a universalization on some subset of $X$.
		* Simplified: generalization applies for some or all $x\in X$ while universalization applies only $\forall x\in X$.
- [ ] Describe the arbitrary subject set of a sentence.
- [ ] Describe the arbitrary predicate set of a sentence.
- [ ] Describe the arbitrary object set of a sentence.
- [ ] Describe Agents and Entities
	- [ ] Describe external entities and internal agents
	- [ ] Describe agent knowledge and A priori and A posteriori actions.
- [ ] Describe statements and propositions
- [ ] Describe interrogatives sentences
- [ ] Describe declarative and exclamatory sentences
- [ ] Describe imperative sentences
- [ ] Describe Modal Verbs
- [x] Describe Contexts
	- [x] Describe discrimination and tolerance
	- [ ] Describe language context
	- [x] Describe context variance and invariance
	- [ ] Polysemous and Amphibologies
	- [ ] Implicit Contexts
- [ ] Describe Situations
- [ ] Describe Cause and Effect
	- [ ] Necessary and Possibly consequence
# Notation
1. time $t$.
2. Grammer $G$
3. Set of all words in grammar $G$ is $W^*$.
4. Set of all sentences in grammar $G$ is $S^*$.
5. Set of all phrases in grammar $G$ is $P^*$.
6. Set of all clauses in grammar $G$ is $C^*$.
7. Set of all morphemes in grammar $G$ is $\mathbf{M}$.
8. Set of all lexemes in grammar $G$ is $\mathbf{L}$.
9. Set of all subjects in grammar $G$ is $\mathbf{S}$
10. subject covering $\{\mathbf{S}_{\text{noun}}, \mathbf{S}_{\text{pronoun}}, \mathbf{S}_{\text{noun phrase}}\}$.
11. Set of all reasonable agents, e.g. people $\mathscr{P}$.
12. Set of all signs $\mathfrak{S}$
13. Context set $\mathcal{C}$ (Contains all previously relevant signs, you can think of it as a person $p$'s memory).
# Assumptions
1. $\forall p,q\in\mathscr{P}$ a definition understood by $p$ called $D_p$, and a definition understood by $q$ called $D_q$, such that $D_p$ and $D_q$ describe similar concepts, and is not objective, cannot be assumed to be the same, e.g. $D_p\neq D_q$.
# The Language Context
In this document we will obviously be using standard english as our primary choice, but it is important to note that different languages have different rules, they might even divide the way sentences are phrased into further subcategories, this is then incomplete. That said, I will continue perfecting the document until it is satisfactory, and reaches a mathematical description of language, ethics, etc. ==**It is important to note that something becomes when it is understood to be**==, this means that if we understand the xenopronoun 'xi' is supposed to denote a particular subject, then it is in the set of pronouns. The language context $\mathcal{C}$,  is then dependent on time $t$, and so do all the sets which depend on the context. (The structure of context I've decided to leave very loosely).
## Grammar
$\mathcal{C}$ also holds the grammar set. Grammar is the syntax we will use. We want to think of these things as arbitrary, as long as one person can understand what another is saying. That said I know grammar is important in sentence evaluation, and therefore when we want to talk about a particular sentence, we must talk about it's grammar. A grammar can be described as a relation of strings where some relations are in the grammar or not. We will call $G$ the grammar. When we say a string $X$ is part of a grammar, we will say $X \sim G$.
# Sentences, Words, and Phrases
A ==**phrase**== is a valid statement within some grammar $G$. A phrase can either be a single ==**word**== or a ==**concatenation of multiple words with valid grammar**==. The specific grammar used in this document is an English grammar, but as long as the language utilized is not esoterically distinct from English grammar, it should also apply. We will also try and generalize the notion of English Grammar, to utilize a generalized version of language, which has the same basic components as English Grammar. We say a ==**sentence**== is then composed of two parts, a ==**subject**== and a ==**predicate**==. Let the sets $S^*$, $W^*$ and $P^*$ be the set of all sentences, words and phrases respectively. We would also like to distinguish ==**lexemes**==, ==**lemma**=='s, and ==**morphemes**==, within language. Even though such things could be considered arbitrary to some, it will be useful for differentiating between specific subjects and or predicates to form equivalence relations between root words and their variations. When talking about a particular subject-predicate portion of a sentence, we will refer to it as a ==**clause**==. The set of all clauses will be $C^*$.
* $S^*=(P^*)^*\text{ s.t. }(P^*)^*\sim G$.
* $P^*=(W^*)^*\text{ s.t. }(W^*)^*\sim G$.
## Lexemes, Lemmas and Morphemes
We say that a *morpheme* is an indivisible unit of language (think of it like the prime numbers of words). These are free of affixes (a type of morpheme called a ==**bound morpheme**== which represents either a suffix, infix, prefix, circumfix, and whatever other wacky affixes exist out in the world). We will represent these as $\mathbf{M}$.

We say that a *lexeme* (or a lexical item) is the minimal amount of words to create a new term which is unpredictable from its base parts, for example "rabbit hole" can of course mean rabbit hole literally, or researching a topic so intensely you reach a vast array of different topics. A lexeme in some way represents an implicit connection formed between words. A lexeme can of course also be a single word, but typically for lexemes, we assume that implicit context is being utilized. We will represent these as $\mathbf{L}$

A *lemma* can be thought of as a base word you will most likely find in a dictionary. Of course the arbitrariness of the dictionary used should most likely be taken into account, and due to this fact, it will go largely ignored in this document.

We will categorize the set of words $W^*$ as the concatenations of elements in $\mathbf{M}$ which satisfy some unit of language/meaning.
## Semiotics
Going too deeply into language, risks overcomplicating everything. That said we need to define methods of communication, to define answering functions. The largest answering function e.g. the answering function with the largest domain, receives a sign and returns a sign. Let $\mathfrak{S}$ be the set of all signs. Then $\mathbf{M}\subset\mathfrak{\mathfrak{S}}$.
# Subject
The subject of a particular sentence are the nouns, pronouns or noun phrase, also known as the nominal, which are in a particular sentence. Let $\mathbf{S}$ denote the set of all subjects and let $\mathbf{S}_{\text{noun}}, \mathbf{S}_{\text{pronoun}}, \mathbf{S}_{\text{noun phrase}}$, refer to the noun, pronoun and nominal subsets of $\mathbf{S}$, which constitute a covering over $\mathbf{S}$. Assume that operations such as the complement on these sets, will use $\mathbf{S}$ as the universal set.

All pronouns refer to some ==**referent**==. Let $*$ be the dereference operator such that: $$*:\mathbf{S}_\text{pronoun}\to\overline{\mathbf{S}_\text{pronoun}}$$
Let $s\in\mathbf{S}_\text{pronoun}$, then:
* $*s\neq \Lambda$ if there is enough context for who $s$ refers to.
* $*s=\Lambda$ if there is not enough context for who $s$ refers to.
# Predicate
The predicate of a particular sentence is the verb action being done by the subject, with or without *objects*. 
## Object
This is what the action verb in the predicate refers to.
# Answering Functions
Let's finally define a answering function:
$$\forall p\in\mathscr{P}, \exists A_p : U\to V$$
s.t. 
1. $U,V\subseteq\mathcal{P}(\mathfrak{S})$.
2. $A_p$ depends on some implicit time $t$.
3. $A_p$ depends on some implicit context $\mathcal{C}$ (Important to note every persons context is unique).
## Restrictions
When we want to deal with specific answers to questions, we will apply restrictions. In the real world, these restrictions are artificially made, such as restricting the answering function to only receive from the set $S^*$, or to only be able to answer in yes or no questions, in which case it would be restricted to the set. $\{\text{yes}, \text{no}\}$. These restrictions are very crudely done, if we do them like so. Instead, we should first use a quotient map to draw equivalences amongst our answers. To impose these restrictions, I will apply the notation as $X|_{A}$ or just $X_A$ when told explicitly.
# Adjuncts
When evaluating the truth value of a sentence, there are certain things, which act as "fluff", and unless a sentence has to do directly with this added context, it is unnecessary. These are called adjuncts, and when possible, we want to reduce a sentence to one without adjuncts. Wherever possible however, we might want to gauge whether someone is for, or against certain adjuncts, as it can give us a deeper view into their values. That is not to say all adjuncts are useless, but instead that by evaluating the ==**core clause**==, we can reach the core response. The set of adjuncts, which we will call $W_{A}^{*}$, is a subset of $W^*$. A core clause would again be a subject-predicate but which does not contain any $W_{A}^{*}$.
## Adjuncts to keep in mind
The reason adjunct would go like such for $S, P$ being subject and predicate respectively: $S P, \because A$. Here $\because A$ is an adjunct of reason. The symbol $\because$ means *because*, but we use it to denote any of its variants.
## Adjunct Functor
An adjunct functor, will attach a particular adjunct onto some part of the sentence.
1. "Bunny" $\to$ "Cute bunny" $\to$ "The cute bunny" $\to$ "The only cute bunny"
## Adjunct Forgetful Functor
A forgetful functor will get rid of a particular adjunct from some part of the sentence.
1. "The silly human" $\to$ "Silly human" or "The human" $\to$ "human".
## Examples
Let $C$ be the core clause "$A$ killed $B$", where $A$ is a predicate and $B$ is an object. We can personalize this to: "Jessie killed Petra". Personally if someone asked me whether or not this was a good action on Jessie's part, I would most likely answer that it was not. That said, if we perform an Adjunct Functor, this time the sentence could be "Jessie killed Petra, because Petra killed James". In this situation I could see maybe how Jessie could be justified, and therefore my answer changes. The adjunct in this case can be useful as a reason adjunct. In fact the preposition "because" is very useful as it will denote a reason adjunct, which often can change our response.

# Sentence Quotient Spaces
Let $X$ be some part of a sentence, be it a subject, object, predicate, adjunct, complement, etc. We can form a quotient space of like sentences, by using some relation on certain parts of the sentence. These can be things such as adjuncts, names, etc, and can be as general or as specific as one wishes. We write this as $X/R$ where $R$ is a relation which links certain adjuncts to $\Lambda$, and the other terms with themselves, basically stating that we do not care about these adjuncts. Given alternatively: $$(x,\Lambda)\in R\Leftrightarrow \text{cond(x)}$$
otherwise $$(x,x)\in R\Leftrightarrow \neg\text{cond}(x)$$
The conditions interpretation should be clear.  
### Example
For the condition, we can put: $$\text{cond}(x)=x\text{ is a persons name}$$
The relation $\equiv$ which depends on $\text{cond}$ would then not care for a persons name.
* "Jeffery went outside" $\equiv$ "Joshua went outside" $\not\equiv$ "Joshua went inside".
If we didn't care where a particular person went? We can modify our condition, let's say: $$\text{cond}'(x)=x \text{ denotes location }$$
The relation $\equiv'$ would then be:
* "Jeffery went outside" $\not\equiv'$ "Joshua went outside" $\equiv'$ "Joshua went inside".
If we wanted both, we would need a new relation which combines them: $\equiv''$ for $\text{cond}''(x)=\text{cond}(x) \text{ or }\text{cond}'(x)$. Then 
* "Jeffery went outside" $\equiv''$ "Joshua went outside" $\equiv''$ "Joshua went inside" $\not\equiv''$ "Jeffrey stayed outside".
We can see how it can be hard to generalize sentences, especially when such a tiny change can provoke them to no longer be equivalent. It is truly a fools errand to try and come up with a wholly equivalence relation which can cover every edge case, especially since Grammar, and new words, as well as a person $p$'s definition of the equivalence can destroy it. That is because ultimately, if "Jeffrey" denoted a dog, and a dog is not a person, then the first relation would not even be covered, in fact we used our own implicit context in that situation to assume it was a persons name, in reality the term "proper noun" would have better sufficed in that scenario. We need then Context. That said, I don't want to go through with the robotic scenario of cataloguing every edge case, so in some sections, you will just have to bare the edge cases, and use common sense to decipher what I mean. With that said, I will obviously try not to be so general as to have no one be able to understand what it means, and be just specific enough so that one can come to a similar conclusion.
# Polysemous and Amphibologies
==**When dealing with a polysemous, especially when it is an amphibology in an interrogative, additional context is a must**==. A malformed sentence, while their meaning could be deciphered, can ultimately be a form of trickery.
# Context
The context is all knowledge known. There is implicit and explicit context. The implicit context we usually bring to a topic is our life experience. We will usually denote any knowledge we get from the exercise as explicit and any knowledge we get outside the exercise as implicit. Important to note that words and definitions can be categorized as implicit, as a different upbringing could have brought about a different set of definitions for those words
## Context Variance
We previously talked about the answering function $A_p$ for a particular $p\in\mathscr{P}$. Here we will expand on its properties.

Given a sentence $S_i \in S^*$, and another string $S_j$ such that it is grammatically correct and contains the string to some capacity, the answering function $$A_p(S_i)=A_p(S_iS_j)$$means that the sentence $S_i$ is invariant under $S_j$ for answering function $A_p$. The opposite would mean that it is variant. The truth is that for most sentences, adding unto it another sentence will surely change the answer given. For that reason we will talking about specific portions of a sentence.
## Adjunct Variance
As the name suggests, these add adjuncts to sentences, and see if the answering function changes. 
### Discrimination and Tolerance
This is especially useful for adjectival adjuncts, whose variance we will denote as ==**discrimination**==, and whose invariance we will denote ==**tolerance**==.

# Metrics
## Agreement Characteristic Function
Let $A_p$ be an answering function for a particular person $p$ restricted on the codomain to some set with 2 elements either denoting, agreement or disagreement called $\mathbb{B}$ (The boolean set). Let $I$ be the interrogative and $\because A$ be the reasoning adjunct. For this specific case, let $0,1\in \mathbb{B}$. Then: $$A_p:S^*\to \mathbb{B}=A_p(S)=\begin{cases}p\text{ agrees with } S & 1\\p\text{ disagrees with } S & 0\end{cases}$$
This version of $A_p$ is a characteristic function of agreement, since we could, alternatively, have a set $\mathbf{A}_p$ which is all the statements a particular person $p$ agrees with, and see whether a sentence is within it.