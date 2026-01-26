[[MATH317]]

*skipped part of initial recap in slides*

If a curve is parameterized by arclength i.e $\mathbf{r}(s)$ then 
$$
\frac{ds}{ds} = 1 = |\mathbf{r'}(t)|
$$
Saying that the curve is traced at *unit speed*

To reparametrize by arclength, find $s(t)$ = expression involving $t$ and solve for $t(s)$.

Unit tangent to a curve
Let $C$ be a space curve described by the vector function $\mathbf{r}(t)$

Recall: geometrically, $\mathbf{r'}(t)$ is a vector tangent to $C$ at $\mathbf{r}(t)$

The *unit tangent* vector $\mathbf{T}$ is
$$
\mathbf{T}(t) = \frac{\mathbf{r'}(t)}{|\mathbf{r'}(t)|}
$$
pointing in the direction of movement ($\mathbf{r'}$)

Q: Suppose we have another curve $C$ what is the *curvature* of the curve?

*Curvature* of a curve $C$ at a point is a measure of how quickly the curve changes direction at that point. Defined to be the magnitude of the rate of change of the unit tangent vector with *respect to arclength*

Let $\kappa$ denote the curvature then
$$
\boxed{\kappa = \left| \frac{d\mathbf{T}}{ds} \right|} 
$$
*Note:* If $\mathbf{r}$ is parametrized by arclength $\mathbf{T}(s) = \mathbf{r}'(s)$ so
$$
\boxed{\kappa(s)= |\mathbf{r}''(s)|}
$$
What if we dont want to re-paramaterize $\mathbf{r}(t)$, then using the chain rule
$$
\frac{d\mathbf{T}}{dt} = \frac{d\mathbf{T}}{ds} \cdot \frac{ds}{dt} \leftarrow \frac{ds}{dt}=|\mathbf{r}'(t)|
$$
then take the magnitude and solve
$$
\left| \frac{d\mathbf{T}}{ds}  \right| = \frac{\large\left| \frac{d\mathbf{T}}{dt} \right|}{|\mathbf{r'}(t)|}
$$
therefore
$$
\boxed{\kappa = \frac{|\mathbf{T}'(t)|}{|\mathbf{r}'(t)|}}
$$

Now what if we just want a formula for $\kappa$ which does not involve $\mathbf{T}$ and we do not need to parameterize. For *any general parameter* which is called $t$ in this case.

*derivation*
we have
$$
\mathbf{T} = \frac{\mathbf{r'}}{|\mathbf{r'}|},  \quad |\mathbf{r'}| = \frac{ds}{dt}
$$
then 
$$
\begin{align}
 & \implies\mathbf{r'} = \frac{ds}{dt} \mathbf{T} \\
 & \implies\mathbf{r''} = \frac{d^2s}{dt^2} T + \frac{ds}{dt} T' \\ \\

 & \implies \mathbf{r' \times r''} = \left( \frac{ds}{dt} \mathbf{T} \right) \times\left( \frac{d^2s}{dt^2} \mathbf{T} + \frac{ds}{dt}\mathbf{T'} \right)
\end{align}
$$
recall that cross product is communicative and that the cross product of $a\mathbf{T} \times b\mathbf{T} =0$ so,
$$
\begin{align}
 & \implies |\mathbf{r' \times r''}| = \left( \frac{ds}{dt} \mathbf{T} \right) \times\left( \frac{ds}{dt}\mathbf{T'} \right) \\
 & \implies |\mathbf{r' \times r''}| = \left( \frac{ds}{dt} \right)^2 |\mathbf{T|} |\mathbf{T'}| \sin \theta
\end{align}
$$
*fact:* any unit vector is orthogonal to its derivative 
$$
\mathbf{T}' \perp \mathbf{T}
$$
so 
$$
|\mathbf{T'}| = \frac{|\mathbf{r'\times r''}|}{|\mathbf{r'}|^2}
$$
using $\frac{ds}{dt}=|\mathbf{r'}|$, therefore the final expression
$$
\kappa = \frac{|\mathbf{T'(t)}|}{|\mathbf{r'(t)}|} = \frac{|\mathbf{r' \times r''}|}{|\mathbf{r'}|^3}
$$
*defn* a *unit normal* is
$$
\mathbf{N}(t) = \frac{\mathbf{T'(t)}}{|\mathbf{T}'(t)|}
$$


