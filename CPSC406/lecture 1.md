[[CPSC406]]

### Least Squares and Regularization

##### Linear Least Squares
Given some amount of data points $(z_{i},y_{i}), i=1,\dots ,m$ our goal is to find a line $y=c+sz$ that best fits the data.

In Mathematical terms, solving the problem
$$
min_{c,s} = \sum_{i=1}^m (y_{i}-\bar{y_{i}})^{2}, \text{ st } \bar{y_{i}} = c +sz_{i}
$$
in matrix notation
$$
min_{\mathbf{x}} ||A\mathbf{x}-\mathbf{b}||^2_{2} 
$$
where
$$
A = \begin{bmatrix}
1  & z_{1} \\
\vdots & \vdots \\
1 &  z_{m}
\end{bmatrix}, \quad \mathbf{x} = \begin{bmatrix}
c \\
s 
\end{bmatrix}, \mathbf{b} = \begin{bmatrix}
y_{1} \\
\vdots \\
y_{m}
\end{bmatrix}
$$

##### Polynomial Data Fitting
does not only have to be linear there is also polynomial predictions. Instead of fitting a linear line we fit the polynomial
$$
p(t) = x_{0}+x_{1}t+\dots+x_{n-1}t^{n-1}
$$
In matrix form we fit this using
$$
A = \begin{bmatrix}
1 & t_{1} & t_{1}^{2} &  \dots  & t_{1}^{n-1} \\
1 & t_{2} & t_{2}^{2} & \dots & t_{2}^{n-1}  \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
1 & \dots & \dots & \dots & t_{m}^{n-1}
\end{bmatrix}, \quad \mathbf{x} = \begin{bmatrix}
x_{0} \\
\vdots \\
x_{n-1}
\end{bmatrix}, \quad \mathbf{y} = \begin{bmatrix}
y_{m} \\
\vdots \\
y_{1}
\end{bmatrix}
$$
where the goal is that each $p_{i}(t_{i}) = y_{i}$. 

*Recall* solving these linear systems depend on the dimension of $A$.

For $A$ is an $m \times n$ matrix, *m* rows, *n* columns. 
- if $m > n$ (*overdetermined*) there is possibly *no exact solution* (tall and skinny)
- if $m < n$ (*underdetermined*) there is possibly *infinitely many solutions* (short and wide)
- if $m=n$ (*square*) there is possibly a *unique solution*

##### Least Squares Optimality
Let $r:= Ax-b$ then 
$$
x^* = argmin_{x}\ f(x) := \frac{1}{2}||r||_{2}^2   = \frac{1}{2}\sum_{i=1}^m (a_{i}^Tx-b_{i})^{2}
$$
then define $f$ as
$$
f(x) = \frac{1}{2}(Ax-b)^T(Ax-b) = \frac{1}{2}x^TA^TAx-b^TAx+ \frac{1}{2}b^Tb
$$
the gradient of $f$ is just
$$
\nabla f = A^TAx - A^Tb
$$
set equal to zero and solve and we get
$$
A^TAx = A^Tb
$$
as the *normal equation*, if $A$ is invertible then
$$
x^* = (A^TA)^{-1}A^Tb
$$
