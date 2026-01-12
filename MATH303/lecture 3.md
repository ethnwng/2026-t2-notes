[[MATH303]]
below is assuming our example for $\{ on,off \}$ states with $p,q$ as the probabilities.

**TLDR:**
- The distribution of each *next-step* in a Markov sequence is
$$
(\alpha \underline{P})_{i}
$$
- $\pi_{i}:= \lim_{ n \to \infty }\mathbb{P}(X_{n}= i)$ depends on a couple of things but in general
	- $\mathbb{P}(X_{n}=i)$ converges to a steady state for $0<p+q<2$ given by $\frac{q}{p+q}$ or $\frac{p}{p+q}$
	- If $p=q=0$ then the state of the system never changes $\mathbb{P}(X_{n}=i)=\mathbb{P}(X_{n}=i)$
	- If $p=q=1$ then the system oscillates and the limit does not exist (except for when $\mathbb{P}(X_{0}=i)=0.5$)

**from last:** we want to know what is the *distribution* of $X_1$ (or any next step). 
	(i.e) What is the probability of being in either the on or off state given we know what the first state was?

*recall:*
- $P$ to be the *transition matrix* which defines all the probabilities of moving between states.
	- each entry of $P$ represents $\mathbb{P}(X_{n+1}=i | X_{n} = k)$, i.e. the conditional probability of moving from one state to another
- $\mathbb{P}(X_{0} = i)$ for $i \in \{ \text{on,off} \}$ is the probability that the $0th$ "step" is in the state $i$.
- $\alpha_{i} := \mathbb{P}(X_{0}=i)$ for $i \in \{ {on,off} \}$ and is a tuple. 
	- ex: if the light started *on* then $\alpha=(1,0)$.
	- ex: if the light starting *on* is *fifty-fifty* then $\alpha=(0.5,0.5)$
##### Distribution of the Next Step:
By Law of Total Probability:
$$
\mathbb{P}(X_{1}=i) = \mathbb{P}(X_{1}=i|X_{0}=on)\mathbb{P}(X_{0}=on)+\mathbb{P}(X_{1}=i|X_{0}=off)\mathbb{P}(X_{0}=off)
$$
- the probability you started *on* and moved to $i$ *plus* the probability you started *off* and moved to $i$

Using the definitions above we can replace the formula with
$$
\mathbb{P}(X_{1}=i) = P_{on,i} \ \alpha_{on} + P_{off,i}\ \alpha_{off} = (\alpha \underline{P})_{i}
$$
- the $ith$ entry of $(\alpha \underline{P})$
- *aside:* my algebra is bad but to see why the above holds true
$$
\alpha \underline{P} = \begin{pmatrix}
\alpha_{on} & \alpha_{off}
\end{pmatrix} \begin{pmatrix}
P_{on,on} & P_{on,off} \\
P_{off,on}  &  P_{off,off}
\end{pmatrix} = \alpha_{on}P_{on,on} +\alpha_{on}P_{on,off} + \alpha_{off}P_{off,on} + \alpha_{off} P_{off,off}
$$
	$i$ in this case is being used as a place holder, $i=on$ then we just take the first column else use second.

*Note:* We have that $\mathbb{P}(X_{1}=on)+\mathbb{P}(X_{1}=off)=1$ then
$$
\begin{align}
\mathbb{P}(X_{1}=on)+\mathbb{P}(X_{1}=off)  & = \\
 & =\alpha_{on}P_{on,on} + \alpha_{on}P_{on,off} + \alpha_{off}P_{off,off} + \alpha_{off}P_{off,on} \\
 & =\alpha_{on} \cancel{(P_{on,on} + P_{on,off})} + \alpha_{off}\cancel{(P_{off,off} + P_{off,on})} \to P_{i,k} + P_{i, j} = 1 \\
 & = \alpha_{on} + \alpha_{off} = 1
\end{align}
$$
in simple words $(\alpha \underline{P})$ is a distribution or tuple with states $\{ on,off \}$.

*in english:* what we just showed is that every "next-step" distribution in a sequence is found by just taking the last $\alpha$ and multiplying it by the transition matrix. So 
$$
\mathbb{P}(X_{n} = i) = (\alpha \underline{P}^n)_{i} \to \alpha P \dots P
$$

##### Limit of the Sequence
*Q:* What is $\pi_{i} := \lim_{ n \to \infty }P(X_{n}=i)$?

*Initial Attempt:* For simplicity look at the probability the $n+1$ step is $on$. Similar to the first attempt by law of total probability
$$
\begin{align}
\mathbb{P}(X_{n+1} = on)  & = P_{on,on} \mathbb{P}(X_{n} = on) + P_{off, on} \mathbb{P}(X_{n} = off)  \\
 & =(1-p) \mathbb{P}(X_{n}=on) + q(1-\mathbb{P}(X_{n}=on))  \\ \\

 & \text{ using } \mathbb{P}(X_{n}=off)^C = 1-\mathbb{P}(X_{n}=on)
\end{align}
$$
Now take $n \to \infty$ and solve
$$
\lim_{ n \to \infty } \mathbb{P}(X_{n+1} = on) = \pi_{on} = (1-p) \pi_{on} + q(1-\pi_{on})
$$
- distribute the limit and then replace notation. 
$$
\pi_{on} = \frac{q}{p+q} \quad \pi_{off} = \frac{p}{p+q}
$$
- But what happens if $p=q=0$? 
	- division by zero
- Does this limit always exist?
	- not always if $p=q=1$ then we are always switching on/off forever so there is no convergence.

*Proper (?) Attempt:*
Define (if we used $A_{n}=\mathbb{P}(X_n=off)$ then $b=p$ instead of $q$)
$$
A_{n} = \mathbb{P}(X_{n}=on), \quad a = 1-p-q, \quad b=q
$$
then using the law of total probability formula in the first attempt we get the $n+1$ step as
$$
A_{n+1} = a A_{n} + b,
$$
Let $x$ be the value such that *if the probability gets to that point it stays there forever* 
$$
x = ax+b \implies x = \frac{b}{1-a}
$$
substituting back values we get
$$
x = \frac{q}{p+q}
$$
*in english:* If the probability for $A_{n}$ is $x$, then the probability $A_{n+1}$ is also $x$. $x$ is the converged solution


Now we introduce $B_{n}$ to represent the *distance from the steady state* 
$$
B_{n} = A_{n} - x \implies B_{n} = A_{n} - \frac{b}{1-a}
$$
We have that
$$
A_{n} = B_{n} + \frac{b}{1-a}, \quad A_{n+1} = a A_{n}  + b 
$$
Sub one into the other and simplify
$$
\begin{align}
B_{n+1} + \frac{b}{1-a}  & = a\left( B_{n} + \frac{b}{1-a} \right) + b  \\
 B_{n+1}& = aB_{n} + \cancel{\frac{ab}{1-a} + b - \frac{b}{1-a}} \\
  B_{n+1} & = aB_{n} \\
\end{align}
$$
Since $B_{n+1}$ is just matrix multiplication of $a$ with $B_{n}$ we can "unroll" and get it in terms of $B_{0}$
$$
B_{n} = a^n B_{0}
$$
sub back in to be in terms of $A$ to get
$$
\begin{align}
A_{n} - \frac{b}{1-a}  & = a^nA_{0} - \frac{a^nb}{1-a}  \\
\end{align}
$$
and then back in terms of $\mathbb{P},q,$ and $p$
$$
\boxed{\mathbb{P}(X_{n}=on)  = \frac{q}{p+q} +(1-p-q)^n \left( \mathbb{P}(X_{0}=on) -\frac{q}{p+q} \right)} 
$$
the $(1-p-q)^n$ term controls the output of the limit as $n\to \infty$. 
1. if $0 < p+q < 2$ then $(1-p-q)^n \to 0$ and the *limit exists* and converges to the point $\large \frac{q}{p+q}$ 
2. if $p=q=0$ then $(1-p-q)^n = 1$ and $\mathbb{P}(X_{n}=on)=\mathbb{P}(X_{0}=on)$ meaning that the *state never changes* and stays that state forever
3. if $p=q=1$ then $(1-p-q)^n= (-1)^n$ which makes the *probability oscillate* and thus the limit does not exist 

theres an edge case for *3.* if $p=q=1$ and $\mathbb{P}(X_{0}=on)=0.5$ then there is a stable solution to the  since you are *starting on the only stable solution* available and the oscillations never get a chance to start
$$
\mathbb{P}(X_{n}=on) = \frac{1}{1+1} + (-1)^n(0.5-0.5) \implies \mathbb{P}(X_{n}=on)=0.5 + (-1)^n ( 0)= 0.5
$$
*In General:*
- $(\pi_{on}, \pi_{off})$ is independent of $(\alpha_{on}, \alpha_{off})$
- If $(\alpha_{on}, \alpha_{off}) \neq (\pi_{on}, \pi_{off})$, then $|\mathbb{P}(X_{n}=i) - \pi_{i}|\to0$ exponentially fast
- if $(\alpha_{on},\alpha_{off})=(\pi_{on},\pi_{off})$ then $\mathbb{P}(X_{n}=i)$ is constant

We call $(\pi_{on},\pi_{onff})$ the *invariant, equilibrium, stationary, or steady-state* distribution