[[CPSC406]]

#### SVD
Decomposition of a *non-square* matrix into its eigenvalue decomposition

*recall:*

A matrix $A$'s, *rank* is the maximum number of linearly independent *columns* of $A$. It indicates the dimension of the subspace spanned by its columns (or rows)

**Theorem (Existence)**
Let $A$ be a $m\times n$ matrix (real or complex) with rank $r$. Then there exists orthonormal matrices 
$$
U \in \mathbb{R}^{m\times m}, \quad V \in \mathbb{R}^{n\times n}
$$
and a diagonal matrix
$$
\Sigma \in \mathbb{R}^{m\times n}
$$
such that
$$
A = U \Sigma V^T
$$
The first $r$ diagonal entries $\sigma_{1} > \sigma_{2}> \dots \sigma_{r} > 0$ of $\Sigma$ are called the *singular values*.
- If $A$ is real then $U$ and $V$ are orthogonal 
- If $A$ is complex then $A=U\Sigma V^*$ where $U$ and $V$ are unitary

*column and row bases*
The left- and right- singular vectors constitute orthogonal bases for the four fundamental subspaces of $A$
$$
\begin{align}
 & proj(range(A^T)) = VV^T \\

 & proj(n ull(A^T)) = I_{n} - VV^T \\ \\

 & proj(range(A)) = U U^T \\

 & proj(n ull(A)) = I_{n} - UU^T \\
\end{align}
$$


