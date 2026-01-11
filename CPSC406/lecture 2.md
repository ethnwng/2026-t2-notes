[[CPSC406]]

##### QR Factorization
*recap:*

the *cosine identity is*
$$
\mathbf{x^T y} = ||x||_{2}||y||_{2} \cos(\theta)  
$$
$||x||_{2}$ is the 2-norm

Two vectors are *orthogonal* if
$$
\mathbf{x^T y} = 0 \implies \cos(\theta) = 0
$$
Two vectors are *orthonormal* if
$$
\mathbf{x^T y} =0, \quad \mathbf{x^T x} = \mathbf{1}, \mathbf{y^T y} = \mathbf{1}
$$
A $n\times r$ matrix $Q$ is *orthonormal* if its columns are pairwise orthonormal

if $Q$ is square then $Q$ is *orthogonal*. With the properties
- $||x||_{2}=||Qx||_{2}$
- $x^Ty=x^T Q^T QY= (Qx)^T(Qy)$
- $\det(Q) = \pm 1$
