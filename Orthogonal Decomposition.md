Orthogonal decomposition is the process where a vector is split into orthogonal components. 
I proceed to define the orthogonal decomposition for some vector $y$, where $y \in \mathbb{R}^n$, where $W$ is a subspace of $\mathbb{R}^n$, where $W^{\perp}$ is the [[Orthogonal Complement]] of $W$
$$y = (\hat{y} \in W) + (\vec{z} \in W^{\perp})$$
Every $y \in \mathbb{R}^n$ has a **unique** sum in the form, so long as $W$ is a subspace of $\mathbb{R}^n$

If $\vec{u_1}, \cdots, \vec{u_p}$ is an [[Orthogonal Basis]] for $W$, then
$$\displaylines{
\hat{y} =  proj_{\vec{u_1}}\vec{y} + \cdots + proj_{\vec{u_p}}\vec{y} = proj_{W} \vec{y{}}
}
$$
Geometrically, $\hat{y}$ is the orthogonal projection of $\vec{y}$ onto $W$, and $\vec{z}$ is a vector orthogonal to $\hat{y}$

![[Pasted image 20241028135920.png]]