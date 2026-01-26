[[MATH303]]

classifications

*defn* A (non-directed) graph $\Gamma = (V, E)$, where $V$ is the set of vertices and $E$ is the set of edges, with $V$ is a countable set and 
$$
E \subset \{  \{ x,y \} : x,y \in V, x \neq y\}
$$
and we say
- "$x$ is a neighbour of $y$" or "$x \sim y$" if $\{ x,y \} \in E$
- "degree of $x$" or $deg(x)$ = # $\{  y \in V : x \sim y \}$

$\Gamma=(V,E)$ is *locally finite* if the $deg(x)<\infty, \ \forall x \in V$. Assume that everything is locally finite.

##### Random Walks on Graphs
Define by: (some initial distribution) +
$$
P(x,y) = \begin{cases}
\frac{1}{deg(x)} : y \sim x \\
0 : y \not \sim x
\end{cases}
$$

```nomnoml
[1] -> [2]
[2] -> [3]
[3] -> [4]
[3] -> [5]
[3] -> [6]
[5] -> [6]
```
let this thing be our graph