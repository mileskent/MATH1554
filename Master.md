[Barone Website](https://sbarone7.math.gatech.edu/ma1554s24.html)
[Master Website](https://gatech.instructure.com/courses/114544)

course id: *barone36886*

# Systems of Linear Equations
https://sbarone7.math.gatech.edu/Chapters_1_and_2.pdf
## Linear Equation
$a_1x_1 + a_2x_2 + ... + a_n x_n = b$
a's are **coefficients**, x's are **variables**, n is the **dimension** (number of variables)
e.g. $2x_1 + 4x_2 = 4$ has two dimensions

## Row Reduction
#### Row Operations
1. Replacement/Addition
2. Interchange
3. Scaling
Row operations can be used to solve systems of linear equations

![[augmented-matrix.png]]
A system of equations written as an **augmented matrix**

**Row operation** example (these are augmented)
$$
\begin{bmatrix}
1 & -2 & 1 & 0 \\
0 & 2 & -8 & 8 \\
5 & 0 & -5 & 0
\end{bmatrix}
\begin{bmatrix}
1 & -2 & 1 & 0 \\
0 & 2 & -8 & 8 \\
0 & -10 & 10 & 10
\end{bmatrix}
\begin{bmatrix}
1 & -2 & 1 & 0 \\
0 & 2 & -8 & 8 \\
0 & -10 & 10 & 10
\end{bmatrix}
\begin{bmatrix}
1 & -2 & 1 & 0 \\
0 & 2 & -8 & 8 \\
0 & 0 & 30 & -30
\end{bmatrix}
$$$$\begin{bmatrix}
1 & -2 & 1 & 0 \\
0 & 1 & -4 & 4 \\
0 & 0 & 1 & -1
\end{bmatrix}
\begin{bmatrix}
1 & -2 & 1 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & -1
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 0 & 1 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & -1
\end{bmatrix}$$

A linear system is considered ***consistent*** if it has $>=1$ solution(s)
If two matrices are ***row equivalent*** they have the same solution set, meaning that one can be transformed into the other

# Row Reduction and Echelon Forms
A rectangular matrix is in **echelon form** if 
1. If there are any, all zero rows are at the bottom
2. The first non-zero entry (leading entry) of a row is to the right of any leading entries in the row above it
3. All elements below a leading entry are zero
![[Pasted image 20240821095448.png]]
For **reduced row echelon form**
4. All leading entries, if any, are equal to 1.
5. Leading entries are the only nonzero entry in their respective column.

**Pivot position** in a matrix A is a location in A that corresponds to a leading 1 in the REF of A
**Pivot column** is the column of the pivot

**Free variables** are the variables of the non-pivot columns
Any choice of the free variables leads to a solution of the system
![[Pasted image 20240821100548.png]]

### Theorem
> A linear system is *consistent* if and only if (exactly when) the last
> column of the augmented matrix does not have a pivot. This is
> the same as saying that the RREF of the augmented matrix does
> not have a row of the form $[0\ 0\ 0\ 0\ ...\ |\ 1]$ 
> 
> Moreover, if a linear system is consistent, then it has
> 1. a unique solution if and only if there are no free variables.
> 2. infinitely many solutions that are parameterized by free variables

# Vector Equations
...