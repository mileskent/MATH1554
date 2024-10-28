Let $X$ be a set of vectors that form a basis for subspace $W$ of $\mathbb{R}^n$,
Let $V$ be a set of vectors that form an [[Orthogonal Basis]] for $W$
The Gram-Schmidt process defines how $V$ can be derived from $X$
It depends on [[Orthogonal Decomposition]]

If $X = \{\vec{x_1}, \cdots \vec{x_p}\}$, iteratively define vectors in $V = \{\vec{v_1}, \cdots, \vec{v}_p\}$
$\vec{v_1}=\vec{x_1}$
$\vec{v_2}=\vec{x_2} - proj_{\vec{v_1}}\vec{x_2}$
$\vec{v_3}=\vec{x_3} - proj_{\vec{v_1}}\vec{x_3} -  proj_{\vec{v_2}}\vec{x_3}$
$\cdots$
$\vec{v}_p = \vec{x_p} - proj_{\vec{v}_1} \vec{x_p} - \cdots - proj_{\vec{v}_1} \vec{x}_{p-1}$

![[Pasted image 20241028145639.png|500]]