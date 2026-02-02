[[MATH303]]

##### Limiting Probabilities
For $i$ is some state in $S$, define
$$
T_{i}^+ := inf \{ n >0: X_{n}=i \}
$$
- the first time you return to state $i$ 
- the "length of time the first cycle takes"
- is equal to infinity if the sequence never returns to $i$

*recall:*
$$
f_{i} = \mathbb{P}_{i} (T_{i}^+ < \infty), \quad f_{i} = 1 \iff i \text{ is recurrent}
$$
Let $m_{i}:= \mathbb{E}_{i}T_{i}^+$ then,
- $i$ is positive recurrent when $m_{i} < \infty$
- i is null recurrent when $m_{i} = \infty$ and $i$ is recurrent
*in english:* 
- something is *null recurrent* means that the sequence will return to some state in the long future but after *infinite* time. 
- something is *pos. recurrent* if it returns to that state in *finite* time.

*example:* SRW on $\mathbb{Z}$ where we want to know if it is null or positive recurrent.
no clue 

**Facts:**
1. Positive recurrence and null recurrence are *class properties*
	- if one is null/positive recurrent then they all are 
2. If state space is finite, then all recurrent states are positive recurrent.

*Theorem:* For an irreducible, aperiodic, positive recurrent markov chain. Then 
$$
\pi_{j} := \lim_{  n \to \infty }  \mathbb{P}(X_{n}=j) \text{ exists } \forall j \in S \text{ indp. of initial distribution}
$$
further the row vector $\pi$
1. $\pi$ is the unique solution to
$$
\pi_{j} = \begin{cases}
\sum_{\text{states}} \pi_{i} P(i,j) \quad \forall j \\
\sum_{\text{states}} \pi_{j} = 1
\end{cases}
$$
2. $$\pi_j = \frac{1}{m_j} \quad ( m_{j}< \infty \implies \pi_{j} > 0)$$
3. how fast does it diverge 
$$
\pi_{j}=\lim_{ n \to \infty } \frac{\text{\# of visits to j by time n}}{n}
$$
We call a function $f$ *invariant* if 
$$
f_{j} = \sum_{states} f_{i} P(i,j)
$$
if also, $\sum f_{i}=1$ and $f_{j}>0$ we call $f$ an invariant distribution


Given $k,i \in S$ define
$$
\gamma_{i}^k = \mathbb{E}_{k} \left[ \sum_{n=0}^{\large T_{k}^+ -1} ??_{X_{n}=i} \right] 
$$
the "expected time spent in state $i$ between visits to $k$"

*Propositions:*
Suppose $X_{n}$ is irreducible and recurrent. Then 
1. $$\gamma_{k}^k = 1$$
2. $$
\gamma^k \text{ is an invariant function}
$$
3. for all states $i$ $$
0 < \gamma_{i}^{(k)} < \infty
$$
*pfs:*
- for (1) just plug into definition
- for (2) handwrtn but idk
- for (3) given that $\gamma$ is invariant, then
$$
\gamma_{j}^{(k)} = \sum \gamma_{i}^{k} P(i,j)
$$
to show that its always positive, then use some other thing to show that it is finite.

