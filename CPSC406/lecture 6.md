[[CPSC406]]

### Gradients, Linearizations, and Optimality

**Optimality**
$$
\min_{x} f(x) \text{ where } f: \mathbb{R}^n \to \mathbb{R}
$$
we say that $x^* \in \mathbb{R}$ is
- *global minimizer* if $f(x^*)\leq f(x)$ for all $x$
- *strict global minimizer* if $f(x^*) < f(x)$ for all $x$
- *local minimizer* if $f(x^*) \leq f(x)$ for all $x \in \epsilon$ where $\epsilon$ is some region ball of points
- *strict local minimizer* if $f(x^*) < f(x)$ for all $x \in \epsilon$

an *optimal value* may not be *attained*
$$
inf_{x} \exp(-x) \text{ no attainable value}
$$
an *optimal value* may not *exist*
$$
\min_{x} -x^{2} \text{ unbounded so no minimum value}
$$
the global solution set can be *empty, infinite,* or contain exactly *one solution*

*Theorem: Coercivity Implies a Global Min*
- implies bowl shaped like functions therefore there has to be a min
If $f:\mathbb{R}^n \to \mathbb{R}$ is continuous and $\lim_{ ||x|| \to \infty }f(x)=\infty$ then $\min_{x} f(x)$ has a global minimizer 

