[[MATH317]]

*Continuation of Vector Field integration over curve*

In general
$$
\int_{C_{1}} \mathbf{F}d\mathbf{r} \neq \int_{C_{2}} \mathbf{F} d\mathbf{r}
$$
where $C_{1},C_{2}$ are two different paths to the points $p_{1},p_{2}$

There is no reason for them to be equal; the field $\mathbf{F}$ near $\mathbf{C_{1}}$ has nothing to do with $\mathbf{F}$ near $C_{2}$

##### The Fundamental Theorem of Line Integrals
Suppose $\mathbf{F}$ is conservative (i.e. $\mathbf{F} = \nabla f$) and $C$ is a path from $p_{1}$ to $p_{2}$ then
$$
\int_{C} \mathbf{F} \cdot d\mathbf{r} = f(p_{2}) - f(p_{1})
$$
line integral version of the fundamental theorem of calculus
$$
\int_{C} \nabla f d\mathbf{r} = f(p_{2}) - f(p_{1})
$$

being conservative is a *local condition* but the statement above is true *globally*

Thus,
$$
\mathbf{F} \text{ conservative } \implies \int_{C} \mathbf{F} \cdot d\mathbf{r} \text{ is independent of the path of C}
$$
called the *path independent property*

Many of the fundamental vector fields of nature are independent of path; e.g. gravitational field and electric field. So for example, the work done by gravity when an object moves depends only on the starting and ending points and not on the path taken.