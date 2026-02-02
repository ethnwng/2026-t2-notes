[[MATH317]]

#### Vector Fields
A 2-D vector field is given by a $\mathbf{F}(x,y)$ where
$$
\mathbf{F}(x,y) = P(x,y)\mathbf{i} + Q(x,y)\mathbf{j}
$$
so at every point $(x,y)$ we draw some vector. In 3-D its just
$$
\mathbf{F}(x,y,z) = P(x,y,z)\mathbf{i} + Q(x,y,z)\mathbf{j} + R(x,y,z)\mathbf{j}
$$
2-d examples:
- water on lake surface
- motion of a particle in a plane

3-d examples:
- electric or magnetic field
- velocity of a fluid

*popular field* is
$$
\mathbf{\hat{r}} = \frac{\mathbf{r}}{\mathbf{|r|}} \quad e.g. \mathbf{\hat{r}}(x,y) = \frac{x}{\sqrt{ x^{2}+y^{2} }}\mathbf{i} + \frac{y}{\sqrt{ x^{2}+y^{2} }}\mathbf{j}
$$
which represents a field of vectors pointing away from the origin with one unit length.

*Gravitational Force Field example:*
we have that
$$
\mathbf{F}(x,y,z) = -\frac{GMm}{r^{2}} \mathbf{\hat{r}} = -\frac{GMm}{r^3}\mathbf{r} \to r = |\mathbf{r}|
$$
now consider $f= \frac{GMm}{r}$, taking the gradient 
$$
\nabla f = -\frac{GMm}{r^3}\mathbf{r} = \mathbf{F}
$$
which means that $\nabla f$ is the potential energy.


*gradients* are the most common vector field that is used 

*defn* We say that a vector field is *conservative* if it is a gradient. That is if $f$ is some continuously differentiable equation such that $\mathbf{F} = \nabla f$. We also call $f$ the *potential function* of $\mathbf{F}$.

*ex:* Show that $\mathbf{F}= (2xy)\mathbf{i} + (x^{2}-3y^{2})\mathbf{j}$ is a conservative vector field. 
i.e. find $f$ such that $\nabla f = \mathbf{F}$

so we just need to find
$$
\begin{align}
 & f_{x} = 2xy \implies f(x,y) = x^{2}y + g(y) \\
 & f_{y} = x^{2}-3y^{2} \implies f(x,y) = x^{2}y - y^3 + h(x)
\end{align}
$$

