[[MATH303]]

*recall:* stochastic process is a random thing that changes with time

*markov examples.*
- coin flipping
- drunk person walking in a direction
- drunk bird walking in a direction
- branching system where each branch has some probability

*non markov example.*
- a *less drunk person* self avoiding walker (they do not backtrack $\implies$ they have memory)

both are stochastic processes but one is *markov* because they *do not remember the past/future*

*defn:* **markov chains**
Let $S$ be a countable set ($\{ on,off \},\{ 1,2,\dots,N \},\{ 1,2,\dots \}$) (can be infinite but must be countable) that represent the states of the system. And let 
$$
(\text{rand. var})\ x_{n} := \text{ the state of the system at time $n$}
$$
The sequence $\{ x_{n} \}_{n\geq 0}$ is a *discrete time* Markov chain with state-space $S$ if:
- *Markov Property (Memoryless)* For every $m \geq 0$ and $i_{0},i_{1},\dots, i_{m+1} \in S$ such that 
$$
\mathbb{P} (x_{0}=i_{0}, x_{1}=x_{1},\dots, x_{m+1}=i_{m+1}) > 0
$$
	in english, the probability that a certain "sequence of states" has a probable chance of happening. This is the memoryless property in math form
$$
\mathbb{P} (x_{m+1} = i_{m+1} | x_{0}=i_{0}, \dots x_{m}=i_{m}) = \mathbb{P}(x_{m+1}=i_{m+1} | x_{m} = i_{m}) 
$$
- *Stationary Property* There exists some function $P : S\times S \to [0,1]$ such that for all $m\geq 0, \ z,y\in S$
$$
\mathbb{P} (x_{m+1} = y | x_{m} = z) = P(x,y) = P_{x,y}
$$
	$P$ is the set that represents the transition probability of going from one state to the next state. 

for the light on off example:
$$
P(on,on) = 1-p, \quad P(on, off) = p, \quad P(off,on) = q, \quad P(off, off) = 1-q
$$
we define a *Transition matrix*
$$
P = \begin{bmatrix}
1-p & p \\
q & 1-p
\end{bmatrix}
$$
where $P$ is a *stochastic matrix*
- the rows sum to $1$
	- each row represents a state and it has to do something in each state
- all entries are non-negative (each are a probability)

*question:* suppose $\mathbb{P}(x_{0}=i_{0})= x_{i}$ for $i$ is one of the states. What is the distribution of $X_{1}$
