[[MATH317]]

##### Derivatives of Vector Valued Functions
the derivative of a vector function $\mathbf{r}$
$$
\mathbf{r}'(a) = \lim_{ \nabla t \to 0 } \frac{\mathbf{r}(a+\nabla t) - \mathbf{r}(a)}{\nabla t}
$$
if the limit exists then $\mathbf{r}$ is differentiable

for $\mathbf{r} =<f,g,h>$ where $f,g,h$ are functions of $t$ then
$$
\begin{align}
\mathbf{r'}(a)  & = \lim_{ \nabla t \to 0 } \frac{1}{\nabla t}  (<f(a+\nabla t), g(a+\nabla t), h(a +\nabla t)) > - <f(a),g(a),h(a)> \\
 & = \lim_{ \nabla t \to 0 } < \frac{f(a+\nabla t) - g(a)}{\nabla t},\frac{g(a+\nabla t) - g(a)}{\nabla t},\frac{h(a+\nabla t) - h(a)}{\nabla t}>
\end{align}
$$

so simply
$$
\mathbf{r'}(a) = <f'(a), g'(a), h'(a)>
$$
and you can just take that for higher derivatives

**Interpretation**
If $\mathbf{r}$ is the position function for a particle, then $\mathbf{r'}$ is the velocity. 
*intuition-proof:* let $\mathbf{r}$ be the position function for a particle then 
$$
|\mathbf{r}(t+\nabla t) - \mathbf{r}(t)| \approx \text{ the distance travelled in time $\nabla t$} 
$$
then
$$
|\mathbf{r}'(t)| = \lim_{ \nabla t \to 0 } \frac{|\mathbf{r}(t+\nabla t) - \mathbf{r}(t)|}{\nabla t} = \text{speed}
$$
direction is the direction being travelled. (i.e) the magnitude of $\mathbf{r'}$ is speed. Let
$$
\mathbf{v(t)} := \mathbf{r'}(t), \quad \mathbf{a}(t) := \mathbf{v'}(t) = \mathbf{r''}(t)
$$

**Properties:**
- addition/subtraction rule: $[\mathbf{u}(t) + \mathbf{v(t)}]' = <(u_{1}+v_{1})' , (u_{2}+v_{2})',(u_{3}+v_{3})'= \mathbf{u}' + \mathbf{v'}$
- scalar rule: $[c \mathbf{u}(t)]' =c \mathbf{u}(t)'$
- simple chain rule: $[f(t) \mathbf{u}(t)]' = f'(t) \mathbf{u}(t) + f(t)\mathbf{u'}(t)$ 
- dot prod: $[\mathbf{u(t)} \cdot \mathbf{v(t)}] = \mathbf{u}'(t)\cdot \mathbf{v}(t) + \mathbf{u}(t)\cdot \mathbf{v}(t)$
- cross prod: $[\mathbf{u}(t) \times \mathbf{v}(t)]= \mathbf{u}'(t) \times \mathbf{v}(t) + \mathbf{u}(t) \times \mathbf{v'}(t)$
- composition: $[\mathbf{u}(s(t))] = \mathbf{u}'(s(t))s'(t)$


