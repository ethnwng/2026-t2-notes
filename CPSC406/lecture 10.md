[[CPSC406]]

##### Descent Methods
*motivation:* we want to minimize some function, just go in the direction that lowers the function value


**descent direction** which way do we walk (?)
given by
$$
f'(x;d) = \lim_{ \alpha \to 0^+ } \frac{f(x+\alpha d) - f(x)}{\alpha} = \nabla f^T d 
$$
where $d$ is a *descent direction* at $x$ if
$$
f'(x;d) < 0
$$

for a symmetric matrix $B$ if it is positive definite then we are descending (?)

###### Step size
some ways to pick step size $\alpha$
1. *find unique alpha* optimize some function $\phi(\alpha)$ which gives us the best step size,
2. *constant alpha* just pick some constant that will always decrease our function
3. *approximate* using back tracking

**constant alpha**
the sufficient condition is choosing $\alpha$ such that
$$
f(x^k + \alpha d^k) < f(x^k), \quad \forall k
$$
for *quadratic functions* pick
$$
\alpha \in \left( 0, \frac{2}{\lambda_{max} (H)} \right)
$$
where $f(x)$ is
$$
f(x) = \frac{1}{2 }x^T Hx + b^T x + \gamma, \text{ with H positive definite}
$$
**Lipschitz Smooth Functions**
For general smooth functions, the constant step size depends on the lipschitz constant of the gradient.

*defn*
A function $f$ is Lipschitz smooth if 
$$
|| \nabla f(x) - \nabla f(y) || \leq L ||x-y||
$$


*Claim* For quadratic functions $f$ defined same as above, $f$ is $\lambda_{max}(H)-$Lipschitz smooth because
*pf:* 
$$
\begin{align}
||\nabla f(x) - \nabla f(y) ||  & = ||Hx+b - (Hy+b)||\ \\
 & = ||H(x-y)||  \\
 & = ||\underbrace{ (U\Lambda U^T) }_{ \text{eigenvalue decomp.} } (x-y) || \to U\text{ orthogonal}\\
 & = || \Lambda \underbrace{ U^T (x-y) }_{ := v } ||  \\
 & = ||\Lambda v|| \to \Lambda \text{ is diagonal }\\
 &  = \sqrt{ \sum_{1}^n \lambda_{i}^{2} v_{i}^{2} } \\
 & \leq \lambda_{max}(H) ||v|| \\
 & = \lambda_{max}(H)||(x-y)||
\end{align}
$$
both $U$ and $U^T$ are orthogonal meaning they preserve the norm $||Ux|| = ||x||$. 