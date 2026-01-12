[[MATH303]]

*Proposition:* Let $(X_{n})_{n \geq 0}$ be a Markov Chain with state space $S$. Let $m\geq 1$, and $i_{0},i_{1},\dots,i_{m} \in S$ be a bunch of different states. Then
1. if
$$
\mathbb{P}(X_{0}=i, X_{1}=i_{1}, \dots, X_{m}=i_{m}) > 0
$$
	then 
$$
\mathbb{P}(X_{0}=i, X_{1}=i_{1}, \dots, X_{m}=i_{m}) = \mathbb{P}(X_{0}=i_{0})P_{i_{0},i_{1}} P_{i_{1},i_{2}}\dots P_{i_{m-1},i_{m}}
$$
	describes a path of a markov chain
2. *(1)* is also true if $\mathbb{P}(X_{0}=i_{0} \dots X_{m}=i_{m})= 0$ 

3. if
$$
\mathbb{P}(X_{0}=i_{0})>0
$$
	then 
	$$
\mathbb{P}(X_{1}=i_{1}, \dots, X_{m}=i_{m}|X_{0}=i_{0}) = P_{i_{0},i_{1}}P_{i_{1},i_{2}}\dots P_{i_{m-1},i_{m}}  
$$
*prf:* handwritn

*Theorem: Chapman-Kolmogorovovo Equations*
Let $(X_{n)})_{n\geq 0}$ be a Markov Chain on a possibly infinite state space $S$. Then $\forall m,n \geq 0$, with $x,y \in S$. 
$$
\mathbb{P}(X_{n+m} = y | X_{0}=x) = \sum_{z\in S} \mathbb{P}(X_{n}=y | X_{0}=z)\mathbb{P}(X_{m} =z | X_{0}=z) 
$$
*in english:* it states that the probability of going from state $i$ to $j$ in $m+n$ steps is equal to the sum of the probability of going from state $i$ to state $k$ in $m$ steps and then from state $k$ to state $j$ in $n$ steps.
- able to use this to combine previous steps together to get an overall probability for a sequence.

*prf:* handwrtn
