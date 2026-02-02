[[CPSC406]]

#### Second Order Optimality
##### positive/negative definite/semidefinite matrices
*defn* A matrix $H$ is *positive semidefinite* if
$$
x^THx \geq 0
$$
for all $x \in \mathbb{R}^n$ where $H$ is symmetric $H=H^T$

*defn* A matrix is *positive definite* if
$$
x^T Hx >0
$$
for all $x$ excluding $\mathbf{0}$

*defn* A matrix is *negative semidefinite* if $-H$ is positive semidefinite.
*defn* A matrix is *negative definite* if $-H$ is positive definite.


*ex:* The identity matrix
$$
\begin{bmatrix}
1 & 0  \\
0 & 1
\end{bmatrix}
$$
is positive definite because
$$
\begin{bmatrix}
x_{1} & x_{2}
\end{bmatrix} \begin{bmatrix}
1 & 0  \\
0 & 1
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix} = ||x||^2
$$
*ex:* Positive semidefinite example
$$
\begin{bmatrix}
1 & 1  \\
1 & 1
\end{bmatrix}
$$
because
$$
\begin{align}
\begin{bmatrix}
x_{1} & x_{2}
\end{bmatrix}\begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}  & = \\
 & = \begin{bmatrix}
x_{1} & x_{2}
\end{bmatrix} \begin{bmatrix}
x_{1}+x_{2} \\
x_{1}+x_{2}
\end{bmatrix}\\
 & = x_{1}^{2} + 2x_{1}x_{2} + x_{2}^{2} \\
 & = (x_{1}+x_{2})^{2} 
\end{align}
$$
*negative* is the same except everything is negative
- negate both matrices gives the negative versions


*defn* If it is neither positive or negative definite/semidefinite then the matrix is indefinite.

**aside:**
Given a *diagonal* matrix
$$
D = \begin{bmatrix}
d_{1} & 0 & \dots & 0 \\
0 & d_{2} & \dots & 0  \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 0
\end{bmatrix}
$$

*D* is positive definite $\iff d_{i} >0$ for all $d$
*D* is positive semi-definite $\iff d_{i} \geq0$ for all $d$

*Theorem:*
The eigenvalues of a symmetric matrix $H$ is 
$$
H X = X \Lambda
$$
where $X$ is a matrix of the eigenvectors of $H$ and $\Lambda$ is a diagonal matrix with the eigenvalues down the diagonal. 
- A *eigenvalue decomposition* always exists for symmetric matrices $H$.
- The *eigenvectors* are always *orthogonal* when $H$ is symmetric


*Theorem:* A matrix $H$ is positive (semi) definite if and only if all the eigenvalues are non negative, positive.

##### Hessian's
The *second order differential* for matrices 
$$
H(x) = \begin{bmatrix} 
\frac{ \partial^{2}f }{ \partial x_{1}^{2} }  & \frac{ \partial f }{ \partial x_{1} \partial x_{2} }  & \dots & \frac{ \partial^{2} f }{ \partial x_{1} \partial x_{n} }  \\
\vdots
\end{bmatrix}
$$
##### Quadratic functions
Quad functions over $\mathbb{R}^n$ have the form
$$
f(x) = \frac{1}{2} x^T H x + b^T x + \gamma
$$where $H$ is symmetric, for $n=2$ 
$$
f(x) = \frac{1}{2} \begin{bmatrix}
 x_{1} & x_{2} 
\end{bmatrix} \begin{bmatrix}
 h_{11}  & h_{12} \\
h_{21} & h_{22}
\end{bmatrix} \begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix} + \begin{bmatrix}
b_{1} & b_{2}
\end{bmatrix} \begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix} + \gamma
$$
in last lecture we already showed that
$$
\nabla f(x) = Hx + b
$$
and this time
$$
\nabla^{2}f(x) = H
$$
  