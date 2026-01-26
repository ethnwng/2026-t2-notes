[[MATH303]]

in [[MATH303/lecture 5]] talked about graphs and stuff, pretty much all markov chain diagrams can be thought of as a graph.

recall:
- two points on a graph *communicate* if there is a path that connects them both ways $i \leftrightarrow j$
- $j$ is *accessible* from $i$ if there is a path from $i$ to $j$ but not vice versa $i \to j$

**Gambler's Ruin Problem**
The diagram in *l6* notes have three cases:
1. *Absorbing Boundaries:* $p \in (0,1)$ 
	- the states at $0$ and $N$ have arrows that point back to them with $p=1$ which means that once you reach those states you *never leave*.
	- the states in between $\{1,2,\dots,N-1\}$ all *communicate* with each other 
	- states $\{ 0 \},\{ N \}$ form *closed communications* with themselves
2. *Forward/Backwards Only:* $p \in \{ 0,1 \}$ 
	- the arrows pretty much point one way and you can only go up. The last state must be absorbing by some rules of Markov
3. *Reflecting Boundaries:* 
	- if states $0$ and $N$ have a pathway backwards with prob $1$ then the chain is *reflecting*
	- you hit a 'wall' and 'bounce' back into the chain.
	- every state here is communicative therefore the entire thing is a *communicative class*

*defn* A state space $S$ is *irreducible* if if it is a communicative class
- case 1 is reducible since the entire thing is not a communicative class (the endings $0$ and $N$ act like roadblocks)
- case 2 is irreducible since the entire thing is a communicative class (everything is connected, no roadblocks)

*defn* $i \in S$ has a period $d$ if 
$$
P_{n}(i,i) = 0 \text{ when } n \text{ does not divide } d
$$
and $d$ is the largest such integer. Equivalently
$$
\tau(i) = \{ n\geq 1: P_{n}(i,i)>0 \}, \quad d = gcd(\tau(i))
$$
where $i$ is called *aperiodic* for $d=1$

*in english:* The *period* just counts the number of steps needed to take yourself back to the original position. 
- $P_{n}(i,i)$ is the probability of being back where you started in $n$ steps, this is zero when $n$ is not divisible by the period
- $\tau(i)$ is a set that describes any number of steps to get back to where you started, $d$ is the greatest common divisor of the set. 
 ![[Pasted image 20260122233736.png]]
 for this graph, the point $\{ 1 \}$ has period $d=1$, this is because you can either take the paths
$$
\begin{align}
 & 1 \to 2 \to 3 \to 1  \\
 & 1 \to 2 \to 1 
\end{align}
$$
the first path has length 3 and the second length 2, thus 
$$
\tau(1) = \{ 2, 3 \}, \quad gcd(2, 3) =1
$$
the point $4$ has period $d=3$ since
$$
4 \to 5 \to 6
$$
so
$$
\tau(3) = \{ 3,6,9,12,\dots \}, \quad gcd = 3
$$

*defn* Let $f_{i} = \mathbb{P}(X_{n}=i \text{ for some } n\geq 1)$ (call this the return probability)
- $i$ is *recurrent* if $f_{i}=1$
- $i$ is *transient* if $f_{i} < 1$
*in english:* being *recurrent* means that we will always return to that state at some point, but it will always happen. being *transient* means that we may never return to a state ever, we might return a couple of times but after an infinite steps, we may never reach it again.

**properties**
Let $N_{i} = \# \{ n\geq 0: X_{n}=i \}$, the number of times we are in state $i$. 

1. claim: if $i$ is recurrent then $\mathbb{P}_{i}(N_{i}=\infty)=1$, pretty much what we said above, if a state is recurrent we are going to return to that state infinite times always. 

2. claim: if $i$ is transient then $\mathbb{P}_{i}(N_{i}=m)=f_{i}^{m-1}(1-f_{i})$ for $m\geq 1$. In other words, $N_{i}$ follows a geometric distribution with $p= 1-f_{i}$ and 
$$
\mathbb{E}[N_{i}] = \frac{1}{1-f_{i}} \text{ and } \mathbb{P}_{i}(N_{i}=\infty)=0
$$
*consequences of 1. and 2.*
i) 
$$
\mathbb{E}[N_{i}] = \begin{cases}
\infty : i\text{ recurrent} \\
\frac{1}{1-f_{i}} : i \text{ transient}
\end{cases}
 $$
ii) if $S$ is finite then at least $1$ state is recurrent. 	 

*pf.* Being *transient* means that at some point we never go to that state again, if we have finite states then at some point we will run out of states to be in, thus at least one of the states has to be recurrent (a state that we can return to)

3. For $n \geq 0$ let $I_{n} = \begin{cases} 1 : X_{n}=i \\ 0 : X_{n} \neq i\end{cases}$ then $N_{i} = \sum_{0}^\infty I_{n}$ is the total number of times you return to state $i$. 
$$
\begin{align}
\mathbb{E}[N_{i}] = \mathbb{E}\left[ \sum_{n=0}^\infty I_{n} \right]  & = \sum_{i=0}^\infty \mathbb{E}[I_{n}] \\
 & = \sum_{i=0}^\infty \mathbb{P}_{i}(X_{n}=i) \\
 & = \sum_{i=0}^\infty P_{n}(i,i)
\end{align}
$$
ngl idk how this algebra worked out but we can use this to say two things
$$
i \text{ is } \begin{cases}
\text{ recurrent if } \sum P_{n}(i,i) = \infty \\
\text{ transient if } \sum P_{n}(i,i) < \infty
\end{cases}
$$
4. if $i$ is recurrent and $i\leftrightarrow j$, ($i$ communicates with $j$) then $j$ is also recurrent.
*pf* ngl this shit makes no sense but.

if $i\leftrightarrow j$ then $\exists m,k$ such that $P_{k}(i,j) >0$ and $P_{m}(j,i)>0$. 
*english* 
- there exists a path from $j\to i$ in $m$ steps with prob. $P_{m}(j,i)>0$
- there exists a path from $i \to j$ in $k$ steps with prob. $P_{k}(i,j)>0$
- 
using *Chapman-Kolmogorov (C-K) Equations* (i think this just used to split transitions into steps)
$$
\begin{align}
P_{m+n+k} (j,j)  & = \sum_{s \in S} P_{m}(j,s) P_{n+k} (s,j) \\
 & = \sum_{s \in S} \sum_{t \in S} P_{m} (j,s) P_{n}(s,t) P_{k}(t,j) \\
 & \geq \underbrace{ P_{m}(j,i) }_{ >0 } P_{n}(i,i) \underbrace{ P_{k}(i,j) }_{ >0 } \\
\end{align}
$$
*english* the *C-K* equations are used to look at the probability of starting at $j$ and returning to $j$ after a long time $(m+n+k)$ steps. What it pretty much is saying that **one** way to go from $j \to j$ is
- start at $j$ and take a path to $i$ (in $m$ steps), $P_{m}(j,i)$
- waffle around in state $i$ for $n$ times, $P_{n}(i,i)$ 
- finally go from $i$ to $j$ in $k$ steps, $P_{k}(j,i)$
since this is only **one** of the paths that could be taken the prob. of this is less than the **total** prob. for **all** paths to go from $j\to j$. 

The next part of this is to show that $j$ is recurrent, which just means we need to show
$$
\sum_{i=0}^\infty P_{i}(j,j)=\infty
$$
we have that
$$
\begin{align}
\sum_{n=0}^\infty P_{m+n+k}(j,j) & \geq \sum_{n=0}^\infty (P_{m}(j,i)\cdot P_{n}(i,i) \cdot P_{k}(j,i)) \\
 &  \geq P_{m}(j,i) \cdot P_{k}(i,j) \underbrace{\sum_{n=0 }^\infty P_{n}(i,i) }_{ =\infty } \\
\end{align}
$$
we were able to pull out the $P_{m}$ and $P_{k}$ terms since those are finite, and we know the last summation is infinite since $i$ is recurrent.

