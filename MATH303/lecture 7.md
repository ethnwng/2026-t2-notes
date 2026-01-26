[[MATH303]]

Very confused.

Consequences of Last Lec
$$
i\text{ is } \begin{cases}
recurrent\text{ if } \sum_{n=0}^\infty P_{n(i,i)} = \infty \\
transient\text{ if } \sum_{n=0}^\infty P_{n(i,i)} < \infty
\end{cases}
$$
4) If $i$ is recurrennt, and $i \leftrightarrow j$ then $j$ is recurrent
$pf$
$i\leftrightarrow j$ therefore $\exists m,k$ such that $\mathbb{P}_{k}(i,j) >0, \mathbb{P}_{m}(i,j)>0$, using chapman-k equations
$$
\begin{align}
P_{m+n+k}(j,j) = \sum_{s \in S} P_{m}(j,s) P_{n+k}()
\end{align}
$$