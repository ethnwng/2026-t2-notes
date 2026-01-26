[[CPSC406]]

Connecting SVD to Least-Squares Minimizations

If $A$ is $m\times n$ with $rank(A) = r<n$ (not full rank) then infinitely many least squares solutions exist
$$
\chi = \{ x \in \mathbb{R}^n | A^TAx = A^Tb \}
$$
SVD provides the *minimum norm* solution $\bar{x}=min\{ ||x|| | x \in \chi \}$

