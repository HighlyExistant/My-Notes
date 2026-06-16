Is an applied branch of mathematics, which provides us methods on how to reason about statistics and data. For this reason, although we will still try to focus on rigor, it will deal mostly with estimation techniques and possible generalizations.
# Relationships
A relationship between two variables, is a certain trend dependent variables data follows, when given certain independent variable.
## Linear
These are trends which follow a general linear growth in the graph.
## Nonlinear
These are trends which follow a general nonlinear growth in the graph, e.g. quadratics.
## Monotonic
The variables in a monotonic relationship move in the same relative direction, but not necessarily at a constant rate, e.g. cubic functions.
# Vocabulary
* ==**Resampling**==: Taking another random sample from the distribution.
* ==**Population**==: Pool from which samples are drawn.
# Hypothesis Testing
The hypothesis is one of the steps of the scientific method. This is the assumption that is made before the experiment is done. To test our hypothesis we run an experiment which would either prove or reject the hypothesis. The more experiments we do, the more accurate the results will be.
# Null Hypothesis
This is the hypothesis which states that there is no difference between things. An example would be that given two drugs $A$ and $B$, there is no difference in recovery times for either drug.
# Bootstrapping
Is a technique for estimating an estimator through ==**resampling**==. Let $X$ be the random sample you obtained from the population $\mathcal{X}$, but it would be difficult to obtain another sample from the population. Bootstrapping says that instead of sampling from the population $\mathcal{X}$, we instead resample the population $X$ randomly, making a new sample with the same size. This resampled list of items would be known as our ==**bootstrapped dataset**==. The steps for bootstrapping are then:
1. Making a bootstrapped dataset
2. Calculating something from that new set (be it the [[What is Probability and Statistics#Mean or Average|mean]], [[What is Probability and Statistics#Median|median]], [[What is Probability and Statistics#Standard Deviation|standard deviation]], etc).
3. Keep track of said calculation in a histogram, or some other method.
4. Repeat steps 1 through 3 however long one wishes.
