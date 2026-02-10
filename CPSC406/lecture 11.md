[[CPSC406]]

##### Least Squares Descent
For an objective function
$$
f(x) = \frac{1}{2} ||Ax-b||
$$
we have
$$
\nabla f = A^T(Ax-b), \quad \nabla^{2}f = A^TA \text{ positive definite}
$$
Lipschitz smoothness is
$$
L = max_{\lambda}(A^TA)= ||A||^2_{2} 
$$
so pick $\alpha$ constant to be 
$$
\alpha \in \left( 0, \frac{2}{L} \right)
$$

##### Exact Linesearch
To find an *exact value* of $\alpha$ is only possible for *quadratic* functions
$$
f(x) = \frac{1}{2} x^T H x + b^Tx + \gamma
$$
exact line search solves the 1-d optimization problem with $d$ descent direction
$$
\min_{\alpha \geq 0} \phi(\alpha) := f(x+\alpha d)
$$
the exact computation is
$$
\phi(\alpha) = \frac{1}{2}(x+\alpha d)^T H (x+\alpha d) + b^T(x+\alpha d) + \gamma
$$
$$
\phi'(\alpha) = \alpha d^T H d + \nabla f(x)^T d
$$
thus
$$
\phi'(\alpha) = 0 \iff \alpha = - \frac{\nabla f^Td}{d^T Hd}
$$
##### Backtracking Linesearch
Pull back on some descent direction $d$ until we find a sufficient decrease in $f$
i.e.
$$
f'(x^k; d^k) < 0 
$$
with sufficient descent parameter
$$
\mu \in (0,1)
$$
for each iteration we are looking to satisfy
$$
f(x+\alpha d) < f(x) + \mu \alpha \cdot \nabla f(x)d 
$$