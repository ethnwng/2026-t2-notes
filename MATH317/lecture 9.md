[[MATH317]]

##### Line Integrals of Vector Fields
To define the line integral of a vector field $\mathbf{F}$ along a curve $C$ we use the concept of "work". Recall:
$$
\text{Work} = \text{Force} \times \text{Distance}
$$
In general, we will follow the idea of splitting the curve into segments, computing the "work" at each segment and the summing that. Taking the number of summations to infinity gives the definition for the total "work" which is 
$$
\int_{C} \mathbf{F} \cdot d\mathbf{r} = \int_{C} \mathbf{F} \cdot \mathbf{T} ds = \int_{C} F(\mathbf{r(t)}) \cdot \mathbf{r'}(t) dt
$$
recall that 
$$
\mathbf{T} = \frac{\mathbf{r}'(t)}{\mathbf{|r(t)}|} 
$$
