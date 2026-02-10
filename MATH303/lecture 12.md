[[MATH303]]

##### Branching Parameters
also called (Galton-Watson processes, Biegenyue ??)

Population Modle:
- Population evolves in discrete generations.
- Each individual has independent identically distributed number of offspring

Call the number of offspring is $\zeta$, $\mathbb{P}(\zeta=j) = p_{0}$ and assume $p_{0}>0$ and
$$
Z_{n} := \text{ \# of individuals in generation }n
$$
assume $Z_{0}=1$ (only one node at the very beginning)


questions we can ask:
- does the population die off (with what probability?)

$(Z_{n})$ is a Markov chain with $S := \{ 0,1,2,\dots \}$. The transition probabilities are messy, they depend on the distribution of the offspring $\{ p_{j} \}$. 

- For $i >0$, currently more than zero children, $P(i,0)= (p_{0})^i >0$. i.e. The transition prob. that every single one of the nodes does not have any more children.
- state $0$ is absorbing
- $i>0$ is transient
- there is a finite number of transient states

There are two cases for these branching processes.
- The population dies off
- The population grows to infinity

Which one is it?

Use Generating Functions:
Define
$$
G(s) = \mathbb{E}s^\zeta = \sum_{i=1}^{\infty} s^i p_{i}
$$
