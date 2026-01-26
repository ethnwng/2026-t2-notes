[[MATH317]]

l6?

three formulas for curvature

$$
\kappa(s) = \left| \frac{d\mathbf{T}}{ds} \right|, \quad \kappa(t) = \frac{|\mathbf{T'}(t)|}{|\mathbf{r'}(t)|} , \quad \kappa(t) = \frac{|\mathbf{r'} \times \mathbf{r''}|}{|\mathbf{r'}|^3}
$$
The first one you use if you have the curve in arclength. Use the second if its easy to differentiate $\mathbf{T}$ and then the last can be used anytime, normally when its too hard to do the other two.

##### Principle Norm Vector
Recall: $|\mathbf{T}|= 1 \implies T'\perp T$

If $\kappa(s)\neq0$ we can divide $\frac{d\mathbf{T}}{ds}$ by its length, $\kappa(s)$ and obtain a unit vector $\mathbf{N}(s)$ in the same direction, called the *principle normal*
- the principle normal points in the direction of $T'$
$$
\mathbf{N}(s) = \frac{\mathbf{T'}(s)}{|\mathbf{T'}(s)|} = \frac{T'(s)}{\kappa(s)}
$$
i.e The rate $\mathbf{T}$ is turning (w.r.t. arclength) is $\kappa$ and the direction $\mathbf{T}$ is turning is $\mathbf{N}$

The plane made by the vectors $\mathbf{T}$ and $\mathbf{N}$ is called the *osculating plane* of $C$ at the point $P$. It is the plane that comes closest to containing the part of the curve near $P$.

The *osculating circle* is a circle with radius $\rho$ that lies in the osculating plane and lies on the concave side of $C$ (toward which $N$ points) and has the property that $\rho=\frac{1}{\kappa}$. 

i.e. 
The circle with radius $\frac{1}{\kappa}$, centered at $\Large\mathbf{P} +\frac{1}{\kappa} \mathbf{N}$, in the osculating plane

##### Binomial Vectors
The *binomial vector* is defined by
$$
\mathbf{B} = \mathbf{T} \times \mathbf{N}
$$
Note that at any point of the curve $C:$
- $\mathbf{B}$ is a unit vector orthogonal to both $\mathbf{T}$ and $\mathbf{N}$
- $\mathbf{B}$ is normal to the osculating plane at the point $P$

##### Torsion of a Curve
since $\mathbf{B}$ is a unit vector then
$$
|\mathbf{B}| = 1 \implies \mathbf{B'} \perp \mathbf{B}
$$
differentiating $\mathbf{B}$ with respect to arclength
$$
\frac{d\mathbf{B}}{ds} = \frac{d}{ds}(\mathbf{T}\times \mathbf{N}) = \frac{d\mathbf{T}}{ds} \times \mathbf{N} + \mathbf{T}\times \frac{d\mathbf{N}}{ds} 
$$
we know that $\frac{d\mathbf{T}}{ds} = \kappa(s)$ which is a constant so we are left with only
$$
\frac{d\mathbf{B}}{ds} = \mathbf{T}\times \frac{d\mathbf{N}}{ds} \implies \frac{d\mathbf{B}}{ds} \perp \mathbf{T}
$$

*defn* On any interval where $\kappa(s) \neq0$ there eixsts a function $\tau(s)$ called the *torsion* of $C$ at $\mathbf{r}(s)$ such that
$$
\frac{d\mathbf{B}}{ds} = -\tau \mathbf{N}
$$
- $\tau$ measures the rate of change of the angle of the normals $\mathbf{B}$ of the neighbouring osculating planes with the osculating planes at $\mathbf{r}(B)$

in other words, $\tau$ measures the rate $C$ twists out of the osculating plane.

*Q:* what about $\frac{d\mathbf{N}}{ds}$? 

We know the derivatives of $\mathbf{T}$ and $\mathbf{B}$ so $\mathbf{N}$ 
$$
\mathbf{B} = \mathbf{T}\times \mathbf{N}  \implies \mathbf{N} = \mathbf{B}\times \mathbf{T}
$$
so 
$$
\frac{d\mathbf{N}}{ds} = \frac{d\mathbf{B}}{ds} \times \mathbf{T} + \mathbf{B} \times \frac{d\mathbf{T}}{ds}
$$
doing some weird hand stuff to get direction or something
$$
\frac{d\mathbf{N}}{ds} = -\tau \mathbf{N}\times \mathbf{T}+\mathbf{B\times\kappa N} = \tau \mathbf{B-\kappa T}
$$
- we do not get anything different

In summary:
$$
\frac{d}{ds} \begin{pmatrix}
\mathbf{T} \\
\mathbf{N} \\
\mathbf{B}
\end{pmatrix} = \begin{pmatrix}
 0 & \kappa & 0 \\
-\kappa & 0 & \tau \\
0 & -\tau & 0
\end{pmatrix} \begin{pmatrix}
\mathbf{T} \\
\mathbf{N} \\
\mathbf{B}
\end{pmatrix}
$$
*The Fundamental Theorem of Curves*
Given $\kappa(s)>0$ and $\tau(s)$ both continuous, then there exists a unique curve $C$, (unique to rotation and translation) having $\kappa(s)$ and $\tau(s)$ as its curvature and torsion.

i.e the curvature and torsion uniquely determine a curve