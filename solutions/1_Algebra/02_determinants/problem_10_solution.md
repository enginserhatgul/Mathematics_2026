## Question

Without carrying out a full determinant calculation, explain why

$\det \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix} = 0.$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

## Solution

### 1. Identification of Linear Dependence Between the Rows

Let the row vectors of the matrix $A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix}$ be denoted by $R_1, R_2, R_3$:

$R_1 = (1, 2, 3),\qquad R_2 = (2, 4, 6),\qquad R_3 = (0, 1, 5).$

Comparing the entries of the first and second rows:

$R_2 = (2, 4, 6) = 2 \cdot (1, 2, 3) = 2 R_1.$

Row 2 is an exact scalar multiple of row 1. We can express this dependence as a non-trivial linear combination equaling the zero vector:

$2 R_1 - 1 R_2 + 0 R_3 = (0, 0, 0).$

Because non-zero coefficients ($c_1 = 2, c_2 = -1, c_3 = 0$) exist such that $c_1 R_1 + c_2 R_2 + c_3 R_3 = 0$, the set of row vectors $\{R_1, R_2, R_3\}$ is **linearly dependent**.

### 2. Explanation of Why Linear Dependence Forces $\det A = 0$

By the multilinearity and alternating properties of the determinant:

1. If one row of a matrix is a scalar multiple of another row ($R_i = c R_j$), applying the elementary row operation $R_i \leftarrow R_i - c R_j$ does not change the determinant:
   $\det A = \begin{vmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{vmatrix} = \begin{vmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{vmatrix}.$
2. The second row now consists entirely of zeros. Expanding along this zero row:
   $\det A = 0 \cdot C_{21} + 0 \cdot C_{22} + 0 \cdot C_{23} = 0.$

Thus, whenever two rows are linearly dependent, the determinant is identically zero without requiring any extensive algebraic expansion.

### 3. Connection with Non-Invertibility of the Matrix

A square matrix $A \in \mathbb{R}^{n\times n}$ is invertible if and only if any of the equivalent conditions of the **Invertible Matrix Theorem** hold:

1. $\det A \neq 0$.
2. The rows (and columns) of $A$ are linearly independent.
3. The rank of $A$ is full ($\mathrm{rank}(A) = n$).
4. The null space of $A$ contains only the zero vector ($\ker(A) = \{0\}$).
5. The linear mapping $x \mapsto Ax$ is bijective (one-to-one and onto).

In our matrix:

- Since row 2 is redundant ($R_2 = 2R_1$), the row space $\mathrm{row}(A) = \mathrm{span}\{R_1, R_2, R_3\} = \mathrm{span}\{R_1, R_3\}$ has dimension at most $2$.
- The rank of $A$ satisfies $\mathrm{rank}(A) \le 2 < 3$.
- By the Rank-Nullity Theorem, $\dim(\ker A) = 3 - \mathrm{rank}(A) \ge 1$, which means there exist non-zero vectors $x \neq 0$ such that $Ax = 0$.
- Geometrically, matrix $A$ collapses 3-dimensional space into at most a 2-dimensional plane, compressing 3D volume down to zero ($\det A = 0$).

Because multiple inputs map to the same output (loss of injectivity), it is impossible to uniquely reconstruct the input vector from the output vector. Therefore, matrix $A$ **cannot possess a two-sided inverse** and is singular.

### 4. Application to Parameter Problems: Finding Singular Configurations

This principle is the cornerstone of spectral analysis: solving $\det(M - \lambda I) = 0$ identifies precisely the parameter values $\lambda$ for which the shifted matrix $M - \lambda I$ develops linearly dependent rows and loses invertibility.
