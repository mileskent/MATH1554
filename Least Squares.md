Given many data points, construct a matrix equation in the form of a linear equation (this matrix equation will be overdetermined).
$$\begin{bmatrix}
 &  \\
 &  \\
 &  \\
 &  \\
 &  \\
 & 
\end{bmatrix}\begin{bmatrix}
b \\
m
\end{bmatrix} = \begin{bmatrix}
y_0 \\
y_1 \\
y_2 \\
y_3 \\
y_4 \\
y_5
\end{bmatrix}$$

#q x vs xhat???
p sure x is in the original equation and xhat is only for the final solution?

Let A be a m x n matrix. A least squares solution to Ax = b is the solution $\hat{x}$ for which 
$$\forall \vec{x} \in \mathbb{R}^n \quad\quad ||\vec{b} - A\hat{x}|| \leq ||\vec{b} - A \vec{x}||$$
- minimize the difference b - Axhat
	- ||b - bhat|| is the minimal distance between the different solutions
- for any x in Rn, Ax in Col A, but no guaranttee b is in Col A
- want to find xhat st Axhat in col A is closest to b
Use principles from [[Best Approximation]]
![[Pasted image 20241030094647.png]]
b is closer to Axhat than to Ax for all other x in Col A
- If b in Col A, then xhat is...
- Seek $\hat{x}$ so that $A\hat{x}$ is as close to $\vec{b}$ as possible, i.e. $\hat{x}$ should solve Axhat = bhat
	- $\hat{b} = A\hat{x}= proj_{Col(A)} \vec{b}$


### Normal Equations
The least squares solutions to $A\vec{x} = \vec{b}$ corresponds to the solution to 
$$A^T A\vec{x} = A^T \vec{b}$$
- Turns the $A\vec{x} = \vec{b}$ equation from above and transforms it into a square matrix equation

### Derivation
##### Method A
b - bhat perp Col A \implies a_j dot (b - bhat) = 0 \implies a_j (b - Axhat) = 0 \implies a_j^T (b - Axhat) = 0, for all j \implies A^T (b - Axhat) = 0 \implies A^T A\vec{x} = A^T \vec{b}
##### Method B
![[Pasted image 20241030095559.png]]
$(Col A)^{\perp} - Null(A^T)$
- xhat is the least squares solution, is equiv to b - Axhat is orthogonal to Col A
- vector v is in Null(A^T) $\iff$ A^T v = 0
- A^T (b - Ahat) = 0
### Usage
- Use when non-square matrix
	- Over/Under determined
- Regression

### Theorem (Unique Solutions for Least Squares)
If A is m x n
- Ax = b has a unique least squares solution for each b in Rm
- Cols of A are linearly independent
- The matrix A^T A is invertible
If the above hold, the least square solution is
$$\hat{x} = (A^T A)^{-1} A^T \vec{b}$$
Note: $A^T A$ plays the role of the "length squared" of the matrix A

### Theorem (Least Squares and QR)
Let m x n matrix A have a QR decomposition. Then for each b in Rm, the equation Ax = b has the unique least squares solution
$$R\hat{x} = Q^T \vec{b}$$
$R$ is upper triangular, so the equation above is solved by reverting it back to the system of equations

## Examples
$$\displaylines{
A = \begin{bmatrix}
4 & 0 \\
 0&2  \\
1 & 1
\end{bmatrix}, \quad \vec{b} = \begin{bmatrix}
2 \\
0 \\
11
\end{bmatrix}\\
\\
A^T A = \begin{bmatrix}
17 & 1 \\
1 & 8
\end{bmatrix}\\
A^T \vec{b} = \begin{bmatrix}
19 \\
11
\end{bmatrix}\\
\text{Now setup the Normal Equations:}\\
A^T A \vec{x}= A^T \vec{b}\\

\begin{bmatrix}
17 & 1 \\
1 & 8
\end{bmatrix}\vec{x} = \begin{bmatrix}
19 \\
11
\end{bmatrix}\\

\vec{x} = \begin{bmatrix}
17 & 1 \\
1 & 8
\end{bmatrix}^{-1}
\begin{bmatrix}
19 \\
11
\end{bmatrix}\\

\hat{x} = 
\begin{bmatrix}
1 \\
2
\end{bmatrix}
}$$

See also: [[LeastSquaresHW6_5.pdf]]

