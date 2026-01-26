[[CPSC406]]

#### Gradients cont.
**Quadratic** least squares.
For *least squares* we only have an *optimal minimum* when $\nabla f(x)=0$.
- in worksheet we showed that for $\nabla f(x) = x^TQx = 2Qx$ so
$$
f(x) = \frac{1}{2}x^THx -c^Tx+ \gamma
$$
where in least squares
$$
\begin{align}
f(x) = \frac{1}{2} ||Ax-b||^2  & = \frac{1}{2}(Ax-b)^T(Ax-b) \\
 & = \frac{1}{2}x^T \underbrace{ (A^TA) }_{ =H }x - \underbrace{ (b^TA) }_{ c^T } + \underbrace{ \frac{1}{2}b^Tb }_{ \gamma }
\end{align}
$$
take the gradient of this thing and set to zero and we will end up getting
$$
0 = \nabla f(x) = Hx^* - c \implies Hx^* =c \iff A^TAx = A^Tb
$$
which gives us the normal equations again.


*rqrmts:* 
- $H=H^T \in \mathbb{R}^{n\times n}$
- $c \in \mathbb{R}^n$

There is also the property that
$$
\nabla f(x) = J(x)^T r(x)
$$
where $r(x)$ is some non-linear function?

in general for *non-linear least squares*
$$
f(x) = \frac{1}{2}||r(x)||^2 = \frac{1}{2}r(x)^T r(x) = \frac{1}{2}\sum_{i=1}^m r(x)^2
$$
where for *linear* $r(x) = Ax-b$ but here it could be anything.

The gradient of this is then
$$
\begin{align}
\nabla f(x) = \nabla \left[ \frac{1}{2}\sum_{rows} r_{i}(x)^2 \right]  & = \sum_{rows} \nabla r_{i}(x)r_{i}(x) \\
 & = \underbrace{ \begin{bmatrix}
\nabla r_{1}  &  \nabla r_{2}  & \dots  & \nabla r_{m}
\end{bmatrix} }_{ \equiv J(x)^T} \begin{bmatrix}
r_{1} \\
r_{2} \\
\vdots  \\
r_{m}
\end{bmatrix} = J(x)^T r(x)
\end{align}
$$

#### Second Order Optimality
