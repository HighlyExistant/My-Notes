We will be using the standard definitions for dilemas, agents, and whatnot. This document focuses more on a proposed method of thought
# On the Construction of Dilemas and Hypotheticals
Of course a simple definition of dilemas would propose that an ethical dilema is a situation in which one has to choose between two outcomes, neither of which are clearly right or wrong, but this construction in words, and the subjectivity of the words 'clearly', as in it is obvious, or in this case, it is not obvious, would be rather subjective given the person. That would suggest that depending on the person, something is either a dilema or not. For that reason I will propose an alternative way of constructing dilemas.
### Situations and Agents
Every situation should have ==**agents**==, which are the entities in the situation. An entity is either 
* ==**External**==, meaning that you have no control over their actions.
* ==**Internal**==, meaning that you are in direct control over their actions. These agents usually have an interrogative sentence correlating them, suggesting you to choose the action for them.
A dilema should have both ==**external entities**==, and an ==**internal agent**==. The external entity can propose the problem, be it a trolley or a person, while the internal agent allows us to place ourselves in the situation and choose an outcome.
#### Examples
1. ==**Charlie**== has murdered a ==**man**==.
	* In this example, both Charlie and the man are external agents, as you have no control over their actions.
2. ==**Charlie**== is about to murder ==**Jessie**==, *should Jessie defend themselves*?
	* In this example, Charlie is an external agent, as you have no control in whether they will murder Jessie, but Jessie is an Internal agent, as you are given the choice on whether Jessie should defend themselves or not.
	* A very crude dilema, as Jessie
3. ==**Charlie**== has asked ==**Jessie**== to help them with an assignment. *Is it necessary for Jessie  to help Charlie*?
	* Charlie is external, Jessie is internal
	* Oddly enough this could be considered a very crude dilema. Although the choice seems easy enough, one could make the argument that the choice is in whether time should be spent helping Charlie or doing other things. You are torn between spending time or doing what you want.
The difference between an external agent and an internal 
agent is, whether the words 'should' or 'must' are used, or not. 
### Choices
Every dilema comes with either a ==**finite**== set of choices, or an ==**infinite**== amount of choices, each with a unique ==**consequence**==. ==**If a problem has no choice, then there is no dilema**==. Internal agents are the only ones with a choice.
#### Examples
1. A trolley's brakes are broken and is heading towards 5 people tied to the tracks. You can flick a lever and bring it to an alternate track, where it will hit a single person. Should you flick the lever?
	* This problem has a finite set of choices (specifically 2), as you can either flick or not flick the lever.
2. Jessie has been convicted of attempting to murder Petra, what should their punishment be?
	* Here you have an infinite amount of choices, as you can choose any punishment, or even none.
3. Jessie has been caught attempting to murder Petra, should they be punished?
	* Here you have an 2 choices, as you can choose to either punish or not punish them, wherein the punishment is abstract (It could be a light punishment or a strict one).
4. Jessie has been convicted of attempting to murder Petra.
	* There is no choice here, and therefore no dilema

### Outcomes
An outcome is representable as an "if $A$ then $B$" statement, such as $A\Rightarrow B$, where $A$ is the choice and $B$ is the consequence. Every dilema has atleast one situation that goes: $$A\Rightarrow B \vee \neg A\Rightarrow C$$written out as If $A$ then $B$ else not $A$ then $C$. If a situation goes $$A\Rightarrow B \vee \neg A\Rightarrow B$$then the consequence $B$ is invariant to the choice $A$, and therefore not really a choice. Every dilema should have at least 2 outcomes (Here $B$ and $C$).
#### Necessarily and Possibly Consequence
In a necessary consequence, the consequence is neatly defined in the problem scenario, and therefore you can be certain that the situation will occur. In a possibly scenario, there is a set of possibilities which could occur, perhaps even defined with probabilities, so you can not be certain of the scenarios consequence and will need to base your decision on the details given alone.
* In front of you theres 1 red button and 1 green button as well as a curtain concealing a person. Pressing the red button will allow you to earn $100 but the person behind the curtain will lose $100, while choosing the green button will split the money. The person who is concealed is given the same choice. If both of you press the red button, you will both lose $100.
	* In this scenario you are not given the other persons actions, and therefore this consequence is a possibility.
* Jessie will let you decide whether they kill you or Petra, which do you choose?
	* In this scenario you are given that the actions will occur with what will happen if those actions take place, and therefore this consequence is necessarily.
#### Finite and Infinite Outcomes, as well as rewriting scenarios
Given a set of outcomes $A_i\Rightarrow B_j$ such that $i,j\in I$ (where $I$ is an index set, not to be confused by an interrogative), then there are $|I|$ possible scenarios. That said there can be scenarios in which the consequence $B_j$ repeats, and depending on how you frame the problem these can be equivalent. For example, consider the scenario:
    Jessie is planning on killing Petra at a time of your choosing, but Petra will move away in 1 week, wherein Jessie will be unable to kill them, that said if Jessie doesn't kill Petra, they will kill you, and you will be unable to get away due to the fact you are in house arrest. 
    * Putting aside the fact this dilema is utterly ridiculous, it is important to note that since time $t\in \mathbb{R}$, which is continuous and technically infinite, you have an infinite amount of scenarios you could choose, that said the outcomes of either you will die, or Petra will die remain the same. Let $t$ represent days, then 
		* $t\in [0,7)\Rightarrow \text{Petra will die}$
		* $t\in [7,\infty)\Rightarrow \text{You will die}$. (Ignore the fact that you can choose infinity as a date)
	* This means that, under an [[Mathematics/Pure Math/Relations/Relations#Equivalence|equivalence relation]] there is technically a finite amount of scenarios and we can rewrite it as: "Jessie will let you decide whether they kill you or Petra, which do you choose?", in which case there are only two outcomes.
#### Examples
1. Jessie is about to kill Petra, should you get ice cream?
	* The choice $A$ is whether you should get ice cream. If you decide to get ice cream, Petra will die, but if you decide not to get ice cream, Petra will still die. This is in fact a choice, but it will not affect the consequence, and therefore this situation cannot be a dilema.
2. Jessie is about to kill Petra, if you choose to step in you could save Petra but will die in the process, or you can spare your life and let Petra die.
	* Here you are given a choice $A$ where 
		* $A\Rightarrow\text{Petra lives but you will die}$
		* $\neg A\Rightarrow\text{Petra dies but you will live}$
	Both outcomes are different, and directly affect the situation, therefore this can be considered a dilema.

## Constructing Dilemas
Given a situation $S=\text{Jessie killed Petra}$, and the interrogative $I=\text{Should Jessie be punished}$. It's concatenation (keeping the grammar intact) $$S,I=\text{Jessie Killed Petra, Should Jessie be punished}$$Forms an entirely new context. In $S$, both Jessie and Petra are external agents, and therefore no dilema can be thought out, and in $I$ the answer is meaningless, as there is no context on who Jessie even is, or why they should be punished. You could answer yes or no, but ultimately the reason wouldn't matter. When these sentences are combined a new agent is formed implicitly, which is ==**you**==, as you are now the judge who will decide whether Jessie gets punished and why. There is then 2 external agents and 1 internal agent, with both a situation and a finite set of choices. This would still however, not qualify as a dilema, as there are no clear consequences, if anything this is a hypothetical. However if we then concatenate the outcomes $O=\text{If Jessie is punished then their child will not have a parent}$, offers 2 outcomes. The dilema would then be $S,I,O$, a **situation**, an **interrogative** and a set of **outcomes**. If a string can be represented in these pieces with the same information, it is a dilema. Here we have somewhat generalized away the concept of difficulty, of course a good dilema would be difficult to choose from, but since difficulty is subjective, here it does not matter.
## Constructing Hypotheticals
A hypothetical can be constructed as a "if $S I$" (correcting for grammar) where $S$ is a situation, and $I$ is an interrogative. for example "if Jessie killed Petra, should Jessie be punished". A hypotheticals answer would then be the natural construction of an outcome $S\Rightarrow B\vee S\Rightarrow \neg B$. ==**A hypothetical allows the reader to construct their own outcome, or perceived outcome**==. It is important to note that the natural construction does not need to be followed, for example, the answer could instead be "If Jessie killed Petra, then Jessie should get ice cream", which wouldn't make much sense, but is what the reader could perceive as the hypothetical consequence which should follow.