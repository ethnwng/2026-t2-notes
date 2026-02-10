[[MATH303]]
(non-examinable for mt1)
##### Time Reversal 

Suppose we have a fixed time $N$ and a Markov Chain $(X_{n})_{0\leq n\leq N}$ What can we say about $Y_{n}=X_{N-n}$
- Markov property("past and future are independent given the present") is symmetric under the time reversal
	- The *Convergence Theorem* complicates things in time reversal
		- convergence theorem assumes we start from a large number of distributions and converge to some *stable* one $\pi$
		- time reversal says we start at the converged solution and spread out?
	- At start: lots of information about the initial state (low entropy)
	- At future: little information (high entropy)

*Theorem:* Suppose $(X_{n})_{0\leq n\leq N}$ is a markov chain with invariant distribution $\pi$ and initial distribution also $\pi$
Define
$$
Y_{n} := X_{N-n} \quad \forall 0\leq n \leq N
$$
Then $Y(_{n})_{0\leq n \leq N}$ is a markov chain with initial distribution $\pi$, invariant distribution $\pi$ and transition probability
$$
Q(i,j) = \frac{\pi_{i}}{\pi_{j}} P(j,i) \quad \forall i,j \in S
$$
*english:* $Y_{0}=X_{N}$ so the first state in $Y$ is the *last* state in $X$. $Y$ is a sequence that goes *backwards* on the sequence $(X_n)$. 

*pf:* book

*defn* We call a markov chain *time reversible* if
$$
\underbrace{ Q(i,j) }_{ \text{transition of reversed} }  = \underbrace{ P(i,j) }_{ \text{transition of forward} } \quad \forall i,j \in S
$$
A function $(\lambda)_{i \in S}$ with transition probabilities $P(i,j)$ are *in detailed balance* if
$$
\lambda_{i}P(i,j) = \lambda_{j}P(j,i) \quad \forall i,j \in S
$$

*interpretation:* if you start in an invariant distribution $\pi$, then
$$
\begin{align}
\pi_{i} P(i,j)  & = \mathbb{P}(X_{n}=i)\mathbb{P}(X_{n+1}=j| X_{n}=i) \\
 & =  \mathbb{P}(X_{n+1}=j, X_{n}=i)
\end{align}
$$
what is the rate that i go from $i$ to $j$? 
$$
\pi_{j}P(j,i) = \mathbb{P}(X_{n+1}=i, X_{n}=j)
$$
and, what is the rate that i go from $j$ to $i$? 

a *detailed* balance means the likelihood of going either direction is the same

*Proposition.* Let $(X_{n})$ be irreducible and positive recurrent, with transition probabilities $P(i,j)$. If $(x_{i})_{i \in S}$ and $P(i,j)$ are in detailed balance, $\sum x_{i}=1$ and $x_{i}\geq 0$, then $(x_{i})$ is an invariant distribution and $(X_{n})$ is reversible.

