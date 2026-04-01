# Central Nervous System
Composed of:
* ==**The Brain (Encephalon)**== 
* ==**Spinal Cord**==
## Encephalon
Composed of the brain, cerebellum, the trunk of the encephalon and the diencephalon.
### Parts of the Brain
1.  <mark style="background: #FF5582A6;">Cerebrum</mark>:
	1. ==**Occipital Lobe**==: From the word **occiput**, meaning rear of the skull (back of skull). ==**In charge of sight**==.
	2. ==**Parietal Lobe**==: **Parietal** meaning relating to wall, located between the frontal and occipital lobe. ==**In charge of sensation and reasoning**==.
	3. ==**Frontal Lobe**==: Located at the front of the head. In charge of ==**movement, problem solving, behavior and speech**==.
	4. ==**Temporal Lobe**==: In this case, temporal does not mean time, but ==**temple of the head**==, which composes near the side of the head. ==**In charge of memory, hearing, language and emotions**==.
2. <mark style="background: #FFB86CA6;">Brain Stem</mark> (Encephalon Trunk): Stem which connects the brain to the spinal cord. ==**in charge of breathing and swallowing**==.
3. <mark style="background: #BBFABBA6;">Cerebellum</mark>: Bottom rear part of the brain, below the cerebrum and next to the brain stem. ==**In charge of balance and muscle control**==.
![[Pasted image 20260224112549.png]]
Is the connecting point between the spinal cord and the brain.
4. ==**Gray Matter**== is composed of large bodies of dendrites and axons, that aren't myelinated (Don't contain large amounts of Myelin Sheaths).
5. ==**White Matter**==: Is composed of large fibers which are myelinated, giving it the distinct whitish pink look. These myelinated fibers help send signals quickly and efficiently across the interneurons.
6. ==**Cerebrospinal Fluid**==: This fluid is here to give the brain nutrients and diminish the force of any force which affects the brain.
# Peripheral Nervous System
Composes every other part of the nervous system.
# Neurons
The parts of a neuron are as follows
![](Neuron-Parts.png)

![[Neuron-Types.png]]
1. ==**Soma**==: Comes from the Greek word for body, which is ==**somas**== or ==**somata**==. This is meant to represent the cell body
2. ==**Nucleus**==: Where the reproductive information is stored.
3. ==**Dendrite**==: Is a crystalline mass with a branching treelike structure. It is meant to represent the tree like outer parts of the neuron.
4. ==**Axon (Nerve Fiber)**==: From the Greek word for ==**axis**==. It is the long threadlike part of the nerve cell where impulses are conducted to other cells.
5. ==**Myelin Sheath**==: Myelin is a mixture of proteins and phospholipids which increases the speed in which impulses are conducted, which appear pinkish white under a microscope.
6. ==**Axon Terminal (Terminal Boutons, Synaptic Boutons)**==: Terminal meaning end, It is where the neurons release their neurotransmitters rapidly through exocytosis.
## Classifications
1. Sensory: Has long dendrites and short axons. Their job is to send messages from sensory organs to the central nervous system. Sensory organs include
	1. Eyes
	2. Ears
	3. Tongue
	4. Skin
   These sensory organs basically send signals to interneurons which then send signals to motor neurons, or directly to the spinal cord for quick reflex actions.
2. Motor: Large axon and small dendrites, their job is to receive messages from the central nervous system and send them to muscle fibers and glands.
3. Interneuron: ==**Only found in the central nervous system**==, their job is to transmit messages throughout the central nervous system, such as.
	* $\text{Brain}\to \text{Spinal Cord}$
	* $\text{Spinal Cord}\to \text{Brain}$
	* $\text{Brain Region A}\to\text{Brain Region B}$
	* $\text{Spinal Cord Region A}\to\text{Spinal Cord Region B}$
   They can be further split into two different groups:
	* Local Interneurons: These have short axons and form circuits with other nearby neurons.
	* Relay Interneurons: Contain long axons to form circuits between one region of the brain, and another region of the brain.
## Math Translation
1. The Nervous system$= \text{NT}$ is composed of the Central Nervous System ($\text{CNS}$) and the Peripheral Nervous System ($\text{PNS}$) $$\text{NT}=\text{CNS }\cup \text{ PNS}$$ which contains motor neurons $N_m$, sensory neurons $N_s$ and interneurons $N_i$, therefore $N_m \cup N_s \cup N_i=NS$.
2. $\text{CNS}$ is composed of the Encephalon and the Spinal Cord
3. $\text{PNS}$ is composed of the Sensory Nervous System ($\text{SNS}$) and the Motor Nervous System ($\text{MNS}$) $$\text{}PNS=\text{SNS}\cup\text{MNS}$$
4. The $\text{NS}$ is the set of all neurons present in the body.
5. $S_i(x)$ will be the synapse function between interneurons. $x$ will be over the domain of all interneurons, and outputs a set of all connecting neurons over the set of all neurons. $$S_i:N_i\to NS$$
6. $S_m(x)$ and $S_s(x)$ will be the synapse function between motor and sensory neurons respectively, which share similar ranges over the set of interneurons. $$\begin{matrix}S_m: N_m\to N_i\\S_s: N_m\to N_i\end{matrix}$$
7. 