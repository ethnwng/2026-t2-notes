[[MATH317]]

##### Independence of Path
by the fundamental theorem of line integrals the line integral $\int_{C} Fc\cdot dr$ of a conservative field is completely defined by the values of $f$ (potential function) at the endpoints and is independent of the path taken between the endpoints

*defn* We say $\int_{C} \mathbf{F} \cdot d\mathbf{r}$ is independent of path if
$$
\int_{C_{1}} \mathbf{F}d\mathbf{r} = \int_{C_{2}} \mathbf{F} \cdot d\mathbf{r}
$$

equivalently
$$
\int_{C} \mathbf{F} \cdot d\mathbf{r} \text{ is independent of path }\iff \int_{C} \mathbf{F} \cdot d\mathbf{r} = 0
$$
for every closed curve $C$. 
*pf:* 
$\implies$
Assume $\int_{C} \mathbf{F} \cdot d\mathbf{r}$ is independent of path, if you pick any two points $p_{1},p_{2}$ on $C$ then
$$
\begin{align}
\int_{C_{1}} \mathbf{F} \cdot d\mathbf{r}  & = \int_{C_{2}} \mathbf{F} \cdot d\mathbf{r} \\
\int_{C} \mathbf{F} \cdot d\mathbf{r}  & = \int_{C_{1}} \mathbf{F} \cdot d\mathbf{r} + \int_{-C_{2}} \mathbf{F} \cdot d\mathbf{r} = 0
\end{align}
$$

converse
Assume $\int_{C} F dr=0$ for any closed curve $C$. Let $C_{1}$ and $C_{2}$ be any two curves with the same initial and terminal points. We need to show
$$
\int_{C_{1}} F dr = \int_{C_{2}} F dr
$$
Notice if you take $C_{1} \cup (-C_{2})$ then that is a closed curve. 
$$
0 = \int_{C} F dr = \int_{C_{1}} Fdr - \int_{C_{2}} Fdr
$$
So we have
$$
\mathbf{F} \text{ is conservative} \implies \mathbf{F} \text{ is path independent } \iff \int_{C}\mathbf{F} d \mathbf{r} = 0 \text{ for any closed curve}
$$
turns out the converse is also true so we get
$$
\mathbf{F} \text{ is conservative } \iff \mathbf{F} \text{ is path independent}
$$
**notation:** call $\kappa := \int_{C}\mathbf{F}d\mathbf{r}$

*Theorem:* Let $D$ be an open and connected region and let $\mathbf{F}$ be a continuous vector field on $D$. If $\kappa$ is independent of path on $D$ then $\mathbf{F}$ is conservative. In other words, $\mathbf{F}=\nabla f$

*pf:* 2d case: $\mathbf{F}=<P,Q>$
We must find $f(x,y)$ such that $\nabla f=\mathbf{F}$. Let
$$
f(x,y) = \int_{(a,b)}^{(x,y)} \mathbf{F} \cdot d\mathbf{r}
$$
now choose some random point $(a,b) \in D$ and $(x,y)$ is also some point in $D$. 