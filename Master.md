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
![[Pasted image 20240821095448.png|450]] 
For **reduced row echelon form**
4. All leading entries, if any, are equal to 1.
5. Leading entries are the only nonzero entry in their respective column.

## Pivots and Free Variables
**Pivot position** in a matrix A is a location in A that corresponds to a leading 1 in the REF of A
**Pivot column** is the column of the pivot

**Free variables** are the variables of the non-pivot columns
Any choice of the free variables leads to a solution of the system
^[If you have any free variables you do not have a unique solution]
![[Pasted image 20240821100548.png]]

## Theorem for Consistency
> A linear system is *consistent* iff the last
> column of the augmented matrix does not have a pivot. This is
> the same as saying that the RREF of the augmented matrix does
> not have a row of the form $[0\ 0\ 0\ 0\ ...\ |\ 1]$ 
> 
> Moreover, if a linear system is consistent, then it has
> **1. a unique solution iff there are no free variables.**
> **2. infinitely many solutions that are parameterized by free variables**

# Vector Equations
$\mathbb{R}$ is all real numbers
$\mathbb{R}^n$ is $n$ dimensions of $\mathbb{R}$
$\mathbb{R}^{n \times m}$ is $n$ rows and $m$ columns

## Linear Combination
Let $c_i \in \mathbb{R} \land \vec{v}_i \in \mathbb{R}^{>=1}$
$c_1 \vec{v}_1 + ... c_n \vec{v}_n = \vec{B}$
is a **linear combination** of the $v$ vectors, with weights of the $c$'s

## Span
* The set of all linear combinations of the $v$'s in called the **span** of the $v$'s
* e.g. $$SPAN(\begin{bmatrix}
1 \\
0
\end{bmatrix}, \begin{bmatrix}
0 \\
1
\end{bmatrix}) = \mathbb{R}^2$$
* any 2 vectors in $\mathbb{R}^2$ that are not scalar multiplies of each other span $\mathbb{R}^2$
Q: Is $\vec{b} \in SPAN(\vec{a}_1, \vec{a}_2)$
$$\vec{b} = \begin{bmatrix}
7 \\
4 \\
3
\end{bmatrix}, \vec{a}_1 = \begin{bmatrix}
1 \\
-2 \\
-5
\end{bmatrix}, \vec{a}_2 = \begin{bmatrix}
2 \\
5 \\
6
\end{bmatrix}$$
Matrix below in form of system of equations where X and Y scale columns 0 and 1, and column 2 are coefficients on the right hand side of the equation. By reducing this matrix to RREF, we can systematically reveal the values of X and Y

$$\begin{bmatrix}
1 &  2&  7\\
-2 & 5&  4\\
-5 &  6&  3
\end{bmatrix}

\begin{bmatrix}
1 &  2&  7\\
0 & 9&  18\\
-5 &  6&  3
\end{bmatrix}

\begin{bmatrix}
1 &  2&  7\\
0 & 1&  2\\
-5 &  6&  3
\end{bmatrix}

\begin{bmatrix}
1 &  2&  7\\
0 & 1&  2\\
0 &  16&  38
\end{bmatrix}

\begin{bmatrix}
1 &  2&  7\\
0 & 1&  2\\
0 &  0&  0
\end{bmatrix}

\begin{bmatrix}
1 &  0&  3\\
0 & 1&  2\\
0 &  0&  0
\end{bmatrix}
$$
Yes.

$\vec{A} \vec{x} = \vec{b}$ exists



![[Pasted image 20240826095038.png]]
$$\begin{bmatrix}
2 & 3 & 7 \\
1 & -1 & 5
\end{bmatrix}

\begin{bmatrix}
5 & 0 & 22 \\
1 & -1 & 5
\end{bmatrix}

\begin{bmatrix}
1 & 0 & 22/5 \\
0 & 1 & 22/5-5
\end{bmatrix}
$$
## Homogeneous vs Inhomogeneous
Homogeneous:
$\vec{A} \vec{x} = \vec{0}$
Homogeneous systems always have a trivial $\vec{0}$ solution, so naturally we would like to know if there are nontrivial, perhaps infinite solutions, namely if there is a free variable and a column with no pivots

## Parametric vector forms of solutions to linear systems
You can parameterize the free variables and then write the solution as a vector sum.

The solution is $\vec{x}$ which is
$x_1 = 2x_3, x_2 = -x_3, x_3=x_3$
Let $x_3 = t$
$$\vec{x} = \begin{bmatrix}
2 \\
-1 \\
1
\end{bmatrix} t$$

## Nonhomogenous System
Because right side of augmented is nonzero
$$\begin{bmatrix}
1 & 3 & 1 & 9 \\
2 & -1 & -5 & 11 \\
0 & 1 & -2 & 6
\end{bmatrix} \rightarrow^{RREF} \begin{bmatrix}
1 & 0 & -2 & 6 \\
0 & 1 & 1 & 1 \\
0 & 0 & 0 & 0
\end{bmatrix}$$
Let $x_3 = t$
$$\vec{x} = \begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix}
=
\begin{bmatrix}
2 \\
-1 \\
1
\end{bmatrix} t
+ \begin{bmatrix}
6 \\
1 \\
0
\end{bmatrix}
$$

## Linear Independence
Given $\vec{A} \vec{x} = \vec{0}$, if the only solution $\vec{x}$ is $\vec{0}$ $\implies$ Linearly Independent

Note: (This might just be wrong)
$\vec{A} = [\vec{a_0}\ ... \vec{a_n}]\ \big{|}\ \vec{a_i} \in \mathbb{R}^n$
$\land$
$span([\vec{a_0}\ ... \vec{a_n}]) = \mathbb{R}^n \quad \quad$ ^[Same as having n rows of pivots]
$\iff$ Linearly Independent
## Dependence
* Any of the vectors in the set are a linear combination of the others
* If there is a free variable, so there are infinite solutions to the homogenous equation
* If the columns of A are in $\mathbb{R}^n$, and there are $n$ basis vectors in $\mathbb{R}^n$ (which is always true), then if the amount of columns in A exceeds the amount of basis vectors that exist in that dimension, it means that there are free variables, which indicates linear dependence
* If one or more of the columns of A is $\vec{0}$
## Geometric interpretation of linearly independent vectors
If two vectors are linearly independent, the are not colinear
If 3, then not coplanal
If 4, not cospacial

# Intro to Linear Transformations
## Linear Transformation
$A \in R^{m \times n}$
Linear transformation $T: \mathbb{R}^n \rightarrow \mathbb{R}^m, T(\vec{v}) = A \vec{v}$
* **Domain** of T is $\mathbb{R}^n$ (where we start)
* **Codomain** or **target** of T is $\mathbb{R}^m$
* The vector $T(\vec{x})$ is the **image** of $\vec{x}$ under T
* The set of all possible images is called the **range**
* image $\in$ range $\in$ codomain
* When the domain and codomain are both $\mathbb{R}$, you can represent them as a Cartesian Graph in $\mathbb{R}^2$, as in *a mapping of* $\mathbb{R} \rightarrow \mathbb{R}$
	* If y is the codomain and x is the domain, the range is the range, the domain is all the images of f(x)
## The interpretation of matrix multiplication as a linear transformation
$$A = \begin{bmatrix}
1 & 1 \\
0 & 1 \\
1 & 1
\end{bmatrix}, \vec{u} = \begin{bmatrix}
3 \\
4
\end{bmatrix}, \vec{b} = \begin{bmatrix}
7 \\
5 \\
7
\end{bmatrix}$$
$$T: \mathbb{R}^2 \rightarrow \mathbb{R}^3$$
Compute $T(\vec{u})$
$$A \vec{u} = \begin{bmatrix}
1 & 1 \\
0 & 1 \\
1 & 1
\end{bmatrix}\begin{bmatrix}
3 \\
4
\end{bmatrix} = \begin{bmatrix}
7 \\
4 \\
7
\end{bmatrix}$$
Calculate $\vec{v} \in \mathbb{R}^2$ so that $T(\vec{v}) = \vec{b}$
$$A\vec{v} = \vec{b}$$
$$\begin{bmatrix}
1 & 1 & 7\\
0 & 1 & 5\\
1 & 1 & 7
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 2\\
0 & 1 & 5\\
1 & 1 & 7
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 2\\
0 & 1 & 5\\
0 & 1 & 5
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 2\\
0 & 1 & 5\\
0 & 0 & 0
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 2\\
0 & 1 & 5\\
\end{bmatrix}
$$
$$\vec{v} = \begin{bmatrix}
2 \\
5
\end{bmatrix}
$$
#star
Give a 
$\vec{c} \in \mathbb{R}^3 | \neg \exists \vec{v} | T(\vec{v}) = \vec{c}$
$\lor$
Give a $\vec{c}$ that is not in the range of $T$
$\lor$
Give a $\vec{c}$ that is not in the span of the columns of $A$
(Same question for all)

Range of $T$ is a bunch of images of the following form:
$$A \vec{v} = \begin{bmatrix}
v_1 + v_2 \\
v_2 \\
v_1 + v_2
\end{bmatrix}$$
For $\vec{c}$ to not be in the range of $T$, it cannot be in the above form, e.g. it can be
$$\begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix}$$

## Linear
A function $T: \mathbb{R}^n \rightarrow m$ is linear if 
* T(u + v) = T(u) + T(v)
* T(c$\vec{v}$) = cT(v)
* "Principle of Superposition"
	* If we know $T(e_1)$, ...,  $T(e_n)$ then we know every T(v)
* Prove it is linear by proving the addition and multiplication rules

# Matrix of Linear Transformations
## The standard (basis) vectors
Standard vectors in $\mathbb{R}^n$ have a one entry for each dimension, and zeros for the rest, 
e.g. for $\mathbb{R}^3$:  $\vec{e_1}, \vec{e_2}, \vec{e_3} = \hat{i}, \hat{j}, \hat{k}$
## Standard matrix
Theorem
> Let $T: \mathbb{R}^n \rightarrow \mathbb{R}^m$ be a linear transformation. Then there is a unique matrix $A$ such that
> $T(\vec{x}) = A\vec{x}, \vec{x} \in \mathbb{R}^n$
> In fact, $A$ is a $m \times n$ and its $j^{th}$ column is a vector $T(\vec{e_j})$
> $A = [T(\vec{e_1}), T(\vec{e_2}), ... T(\vec{e_n})]$

## Two and three dimensional transformations in more detail.
$$T(\vec{e_1}) = \begin{bmatrix}
5 \\
 -7\\
2
\end{bmatrix}, T(\vec{e_2})=\begin{bmatrix}
-3 \\
 -8\\
0
\end{bmatrix}$$
$$A = \begin{bmatrix}
T(\vec{e_1}) & T(\vec{e_2}) 
\end{bmatrix} = \begin{bmatrix}
5 & -3 \\
-7 &  -8\\
2 & 0
\end{bmatrix}$$

Find standard matrix A for T(x) = 3$\vec{x}$ for x in $\mathbb{R}^2$
$A \in \mathbb{R}^2$

$$A = \begin{bmatrix}
T(\vec{e_1}) & T(\vec{e_2}) 
\end{bmatrix} = \begin{bmatrix}
\begin{bmatrix}
3 \\
0
\end{bmatrix} & \begin{bmatrix}
0 \\
3
\end{bmatrix}
\end{bmatrix} = \begin{bmatrix}
3 & 0 \\
0 & 3
\end{bmatrix}$$

## Onto and one-to-one transformations
## Onto
A linear transformation $T: \mathbb{R}^n \rightarrow \mathbb{R}^m$ is onto if there exists a location in the codomain for every location in the domain
onto iff the standard matrix has a pivot in every row


The matrix A has columns which span $\mathbb{R}^m$.
The matrix A has m pivotal columns.

## 1-1
* If there is at most one location in the codomain for every location in the domain
* 1-1 iff standard matrix has pivot in every column

### Example(s)
* e.g. $F(x) = x^2$ is not 1-1, because multiple x values for a single y value


The unique solution to $T (\vec{x}) = \vec{0}$ is the trivial one.
The matrix A ***linearly independent*** columns.
Each column of A is pivotal.

## 1-1 and Onto
need square matrix
if 1-1 then onto
if Onto then 1-1

# Identity and zero matrices
0 Matrix is matrix full of zeroes
Identity matrix is a square matrix full of zeroes except for the diagonal, which is all ones. Multiplying with identity matrix always yields the same matrix.
# Matrix algebra (sums and products, scalar multiplies, matrix powers)
Sums: same dimensions
Matrix multiplication: $r_1 * (c_1 \times r_2) * c_2 \rightarrow r_1 \times c_2$, $AB \neq BA$, $AB = AC \not \implies B = C$, $AB = 0 \not \implies A = 0 \lor B = 0$, $AB = [Ab_1\ Ab_2]$
# Transpose of a matrix
$$ A=\begin{bmatrix}
a & b \\
c & d \\
e & f
\end{bmatrix}, A^T = \begin{bmatrix}
a & b & c \\
d & e & f
\end{bmatrix}$$
$(A^T)^T = A$
$(A + B)^T + A^T + B^T$
$(sA)^T = s(A^T)$
$(AB)^T = B^T A^T$

## Invertibility
A property of only square matrices, because Matrix A is invertible if and only if it is row equivalent to the identity.
$A \in \mathbb{R}^{n \times n}$ is invertible if $\exists C \in \mathbb{R}^{n \times n} s.t. AC = CA = I_n$

$A \in \mathbb{R}^{n \times n}$ is invertible $\iff \forall \vec{b} \in \mathbb{R}^n\ \exists !\ \vec{x}\ s.t.\ A \vec{x} = \vec{b}$

## $2 \times 2$ Inverse Shortcut
$$A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$
$$\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}^{-1} = \frac{1}{det(A)}
\begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}
$$
## Inverse Properties
$(A^{-1})^{-1} = A$
$(AB)^{-1} = B^{-1} A^{-1}$
$(A^T)^{-1} = (A^{-1})^T$

## Elementary Matrix
An elementary matrix, E, is one that differs by $I_n$ by one row operation.
## General way to compute inverse
Row reduce $(A | I_n)$ until you get $I_n$ for A

Therefore, if
$(E^n E^{n-1} ... E_1) A = I_n$
then
$(E^n E^{n-1} ... E_1) = A^{-1}$


## Invertible Matrix Properties
Let A be an n x n matrix. These statements are all equivalent
> a) A is invertible.
> b) A is row equivalent to I^n.
> c) A has n pivotal columns. (All columns are pivotal.)
> d) Ax = 0 has only the trivial solution.
> e) The columns of A are linearly independent.
> f) The linear transformation x -> Ax is one-to-one.
> g) The equation Ax = b has a solution for all b in R^n.
> h) The columns of A span R^n.
> i) The linear transformation x -> Ax is onto.
> j) There is a n x n matrix C so that CA = I_n. (A has a left inverse.)
> k) There is a n x n matrix D so that AD = I_n. (A has a right inverse.)
> l) A^T is invertible.

## Abbreviated, invertible matrix theorem (IMT)
$AB = I \implies A = B^{-1}, B = A^{-1},$ B is invertible, A is invertible

## Singular
Noninvertible

## Partitioned/Block Matrix
A partitioned matrix is a matrix that you write as a matrix of matrices
When doing multiplication with a block matrix, make sure the "receiving" matrix's entries go first, to respect the lack of commutativity in matrix multiplication. See HW 2.4 if this doesn't make sense.

## Row Column Method
Let A be m x n and B be n x p matrix. Then, the (i, j) entry of AB is 
row_i A · col_j B.
This is the Row Column Method for matrix multiplication

![[Pasted image 20240917100516.png]]

# LU Factorization
## Triangular Matrices
Upper Triangular: Nonzero along and above
Lower Triangular: Nonzero along and below 

If A is an m x n matrix that can be row reduced to echelon form
without row exchanges, then A = LU . L is a lower triangular m x m
matrix with 1’s on the diagonal, U is an echelon form of A.

Suppose A can be row reduced to echelon form U without interchanging
rows. Then,
$E_p ... E_0 A = U$
$A = LU = (E_p ... E_0)^{-1}$
To compute the LU decomposition:
1. Reduce A to an echelon form U by a sequence of row replacement
operations, if possible.
2. Place entries in L such that the same sequence of row operations
reduces L to I.

## Subspaces of $\mathbb{R}^n$
Subset
A subset of $\mathbb{R}^n$, for example, is any collection of vectors that are in $\mathbb{R}^n$

Subspace
A subset H of $\mathbb{R}^n$ is a subspace if it is closed within scalar multiplication and vector addition, i.e. 
$c \in \mathbb{R}; \vec{u}, \vec{v} \in H$
$c \vec{u} \in H$, $\vec{u} + \vec{v} \in H$

when c = 0 then $\vec{0} \in H$

Columnspace
span of columns of A
same as range of A

Nullspace
span of set of $\vec{x}$ that satisfy $A\vec{x} = \vec{0}$
Null $A = \{\vec{x} | A\vec{x} = \vec{0}\}$

Basis
Linearly independent vectors that span a subspace

# Coordinates, relative to a basis
There are many different possible choice of basis for a subspace. Our choice can give us dramatically different properties.

Standard basis are i, j, k, but you can use other vectors to span the same amount of space if you want.

Qs: 
1. What is a determinant? Given a linear transformation T, let us focus on the magnitude of the cross product of the basis vectors. The determinant would be the scalar factor between the original and transformed areas?
2. If you are calculating some integral over a transformed space, is the jacobian just the determinant of the transformation, or is it related---possibly scaling the result to make sense given standard basis vectors?

## Dimension
Dimension/Cardinality of a non-zero subspace H, dim H, is the number of vectors in the basis of H. We define dim{0} = 0.

Theorem
*Any two choices of $\mathcal{B}_1$, $\mathcal{B}_2$ of a non-zero subspace H have the same dimension*
1. dim $\mathbb{R}^n$
	1. n
2. H = $\{(x_1 ...., x_n) : x_1 + ... + x_n = 0\}$ has dimension
	1. n - 1
	2. use the idea of # 3
	3. n variables, solve for $x_1$ ito everything else. -> one pivot everything else free vars. Therefore n - 1 free vars
3. dim(Null A) is the number of 
	1. # of free vars
4. dim(Col A) is the number of 
	1. # of pivots

## Rank
the rank of a matrix A is the dimension of its column space

![[Pasted image 20240923104520.png|400]]
## Nullity
dim(Null A) = Nullity

## Rank Theorem $\star$
If a mtrix A has n columns, then Rank A + dim Nul A = n

## Basis Theorem
Any two bases for a subspace have the same dimension

## Invertibility Theorem
Let A be a n x n matrix. These conditions are equivalent.
1. A is invertible
2. The columns of A are a basis for $\mathbb{R}^n$
3. Col A = $\mathbb{R}^n$
4. rank A = dim Col A = n
5. Null A = {0}


