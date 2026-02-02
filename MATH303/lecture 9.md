[[MATH303]]

*Observation:*
- in the context of simple random walks in higher dimensions

Suppose we know that a simple random walk in $\mathbb{Z}^d$ is transient (we didnt do the proof). What can we say about a simple random walk in $\mathbb{Z}^{d+1}$? Is it also transient?

If we *ignore* the $d+1$ entry, meaning we do a *random walk* (not simple cause it could not move) on $\mathbb{Z}^d$ 
- So either it moves in $\mathbb{Z}^d$ or it "stays still"
- "staying still" means that its moving in our *ignored* $d+1$ direction. 
The probability that it stays still is $\frac{1}{d+1}$. *Call this a "Lazy Walk"*

Therefore
$$
\underbrace{ \mathbb{E^*}_{(0,0)} N_{0,0} }_{ \text{Lazy Walk} } = \frac{1}{1-\frac{1}{d+1}}U \underbrace{ \mathbb{E}_{0,0} N_{0,0} }_{ \text{Not lazy} }
$$
The lazy and 'normal' walk are both transient.