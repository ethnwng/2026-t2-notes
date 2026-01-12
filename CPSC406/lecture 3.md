[[CPSC406]]

*QR recap:*
Can either do regular QR factorization for $m\times n$ matrix $A$ where $m > n$ (long skinny) or *Reduced* QR factorization.

Regular
$$
A=\hat{Q} \bar{Q} R
$$
$\bar{Q}$ is a $m-n\times m-n$ ``matrix``, $\hat{Q}$ is a $n\times n$ matrix. $R$ is upper triangular with entries in the first $n$ rows and $0$'s in $m-n$ rows

Reduced there is no $\bar{Q}$

*how do we use to solve systems?*
For $A$ with full rank
$$
A \mathbf{x} = \mathbf{b}
$$
and $A = QR$, with $QQ^T=I$ so
$$
x = A^{-1}b = (QR)^{-1} = R^{-1}Q^{-1}b = R^{-1}Q^T b
$$
$R^{-1}$ is easy to compute. 

```Julia
using LinearAlgebra
Q, R = qr(A) # O(n^3)  dominant cost
y = Q’b      # O(n^2)  matrix-vector multiply
x = R \ y    # O(n^2)  triangular solve
```


