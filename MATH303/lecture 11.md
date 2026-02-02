[[MATH303]]

continuation from last on **limiting probabilities**
*proposition 2*
Let $X_{n}$ be a irreducible Markov chain and $\lambda$ be an invariant function with $\lambda_{j} \geq 0 \forall j$ and $\lambda_{n}=1$

then
$$
\lambda_{j} \geq \gamma_{j}^{(k)} \quad \forall j \in S
$$
If $X_{n}$ is recurrent then
$$
\lambda_{j} = \gamma_{j}^{(k)}, \quad \forall j \in S
$$

*proposition 3*
$X_{n}$ is a irreducible. The following are equivalent statements
1. Every state is positive recurrent
2. Some state is positive Recurrent
3. $X_{n}$ has an invariant distribution call it $\pi_{i}$
- each of these statements imply one another

Moreover, when these hold, 
$$
\pi_{i} = \frac{1}{m_{i}} = \frac{1}{\mathbb{E}_{i}{T_{i}^+}}
$$
*pf:*
- claim: $1. \implies 2.$ which is obvious (?)
- claim $2. \implies 3.$ 
	- $i$ is positive recurrent, $\implies i$ is recurrent $X_{n}$ is recurrent
	by prop 1. $\gamma^{(i)}$ is an invariant function
$$
\begin{align}
\sum_{j \in S} \gamma_{j}^{(i)}  & = \sum_{j\in S} \mathbb{E}_{i} \sum_{n=0}^{T_{k}^+ -1} \mathbb{1}_{X_{n}=j} \\
 & = \mathbb{E}_{i} \sum_{j \in S} ^{T_{k}^+ -1} \underbrace{ \sum_{j\in S} \mathbb{1}_{X_{n}=j} }_{ =1 } \\
 & = \mathbb{E}_{i}T_{i}^+ = m_{i} < \infty
\end{align}
$$
thus
$$
\pi_{j} = \frac{1}{m_{i}} \gamma_{j}^{(i)}
$$
