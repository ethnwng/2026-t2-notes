[[MATH317]]

*Conservative fields cont.*

a vector field $\mathbf{F}$ is *conservative* if there is a scalar function $f$ such that
$$
\nabla f = \mathbf{F}
$$
where $f$ is the *potential function* of $\mathbf{F}$ 

The test, let $\mathbf{F} = <P,Q>$ then
$$
f_{x} = P, \quad \text{and} \quad f_{y} =Q
$$
or
$$
P_{y} = f_{x,y} = f_{y,x} = Q_{x}
$$
in three dimensions
$$
P_{y} = Q_{x}, \quad P_{z} = R_{x}, \quad Q_{z} = R_{y}
$$
##### Curl

*defn* The curl of a vector field $\mathbf{F}=<P,Q,R>$ is 
$$
\text{curl }\mathbf{F} = < R_{y}-Q_{z}, P_{z} - R_{X}, Q_{x} - P_{y}>
$$
easy way to remember this is to take the cross product of $\mathbf{u} = \begin{bmatrix}\frac{ \partial  }{ \partial x } & \frac{ \partial  }{ \partial y }& \frac{ \partial  }{ \partial z }\end{bmatrix}$ with $\mathbf{F}$. 
$$
\text{curl } \mathbf{F} = \mathbf{u} \times \mathbf{F}
$$

##### Line Integrals
For a curve $C$ parameterized by some function $\mathbf{r}(t)$ with $f(x,y)$ being some continuous function, the "line integral" of $f$ over $C$ is
$$
\int_{C} fdS = \int_{a}^b f(x(t),y(t)) |r'(t)| dt
$$
- if $f=1$ then we just get the "length" of the line/curve

Interpretations:
- The integral is the area of some fence/curtain along $C$ which has height $f(x,y)$ 

some examples:
- $C$ is some wire with variable density $p(x,y)$, the mass of the wire is then given by
$$
m = \int_{C} p dS
$$
	the center of mass $(\bar{x},\bar{y})$ is given by 
	$$
\bar{x} = \frac{1}{m} \int_{C} x p ds, \quad \bar{y} =\frac{1}{m} \int_{C} y p dS
$$
