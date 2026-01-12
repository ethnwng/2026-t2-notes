[[MATH317]]

looking at lengths of curves

what is the length of the space curve $C$ described by the vector function $\mathbf{r}(t)$

*idea:* approximate the length by dividing the curve into segments

**Process:**
- Take derivative of $\mathbf{r}(t)$ 
- Find $|\mathbf{r}(t)|$ 
- Integrate over the interval of the curve

**Arclength Function**
Suppose $\mathbf{r}(t) t_0 < t < t_1$ paramaterizes a curve $C$

Define $s(t)$ = the length of $C$ from $\mathbf{r}(t_{0})$ to $\mathbf{r}(t)$, then

$$
s(t) = \int_{t_{0}}^t |\mathbf{r}'(u)| du
$$
and 
$$
\frac{ds}{dt} = |\mathbf{r'}(t)|
$$
by the fundamental theorem of calc (?)

**Parameterization by Arclenth**
There are infinitely many different parametrizations of any given curve. What is the best?

We say that $\mathbf{r}(t)$ is *parametrized by arclength* if the aprameter $t$ is the arclength from some point
$$
t= \int_{t_{0}}^t |\mathbf{r}'(u)|du
$$
differentiate the above 
$$
1 = |\mathbf{r}'(t)|
$$or in other words $\mathbf{r}$ has *constant speed*. Thus the "nicest way" to parametrize a curve is to just say that the object moves at constant speed across the path.

**Reparametrize a curve by arclength**

Solve for $t$ in terms of $s$
$$
S(t)= \text{ some formula involving $t$} \to t(s) = \text{ some formula involving s}
$$
*ex:* Re-param $\mathbf{r}(t)=3\sin t\mathbf{i}+4t\mathbf{j}+3\cos t\mathbf{k}$ in terms of arclength measured from $(0,0,3)$. 
- find $\mathbf{r'}$ 
$$
\mathbf{r}'(t) = < 3\cos t, 4, -3\sin t>
$$
- find magnitude
$$
|\mathbf{r}'(t)| = \sqrt{ 9\cos ^{2}t + 16+9\sin ^{2}t } = \sqrt{ 25 } = 5
$$
- now write arclength function
$$
s(t) = \int_{0}^t |\mathbf{r'}(u)|du = \int_{0}^t 5 du = 5t
$$
- now just rearrange to be in terms of $s$
$$
t = \frac{1}{5}s
$$
- replace all $t$ with $s$ in $\mathbf{r}(t)$
$$
\mathbf{r}(s) = < 3\sin\left( \frac{1}{5}s \right), \frac{4}{5}s, 3\cos\left( \frac{1}{5}s \right)>
$$
