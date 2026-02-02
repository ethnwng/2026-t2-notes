[[CPSC406]]

#### Generalized Second Order Optimizations

*directional second derivatives*
$$
f'(x;d) = d^T \nabla f
$$

the directional second derivative 
$$
f''(x;d) = d^T \nabla^{2} f(x)d
$$
*Theorems:*
*Linear Approximation:*
$$
f(y) = f(x) + \nabla f(x)^T (y-x) + \frac{1}{2}(y-x)^T \nabla^{2}f(z)(y-z)
$$

*Quadratic Approximation:*
$$
f(x+d) = f(x) \nabla f(x)^T d + \frac{1}{2} d^T \nabla^{2}f(x)d + o(||d||^2)
$$
no idea what $o$ is 

