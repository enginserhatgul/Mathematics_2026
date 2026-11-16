## Question

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## Solution

### 1. Explanation via the Determinant

Compute the determinant of matrix $A$:

$$
\det A = (2)(2) - (4)(1) = 4 - 4 = 0.
$$

By the Invertible Matrix Theorem, a square matrix $A$ possesses an inverse if and only if $\det A \neq 0$. If an inverse $A^{-1}$ existed, then by multiplicativity of the determinant:

$$
\det(A A^{-1}) = \det(I) \implies \det(A) \cdot \det(A^{-1}) = 1.
$$

Substituting $\det A = 0$ gives $0 \cdot \det(A^{-1}) = 1$, which is impossible ($0 \neq 1$). Therefore, $A$ cannot be invertible.

### 2. Explanation via Row Dependence

Let the rows of $A$ be denoted by $R_1 = (2, 4)$ and $R_2 = (1, 2)$.

Notice that:

$$
R_1 = (2, 4) = 2 \cdot (1, 2) = 2 R_2.
$$

Row 1 is an exact scalar multiple of Row 2. This means the row vectors are linearly dependent:

$$
R_1 - 2 R_2 = (0, 0).
$$

**Consequence for Invertibility:**
Because the rows are linearly dependent, the row space has dimension $1$ (rank $= 1 < 2$). As a linear mapping from $\mathbb{R}^2$ to $\mathbb{R}^2$, matrix $A$ maps every vector $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ to:

$$
Ax =
\begin{pmatrix}
2x_1 + 4x_2 \\
x_1 + 2x_2 \\
\end{pmatrix}
= (x_1 + 2x_2)
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

The image of $\mathbb{R}^2$ under $A$ is compressed onto a 1-dimensional line. Infinitely many distinct vectors (such as all vectors satisfying $x_1 + 2x_2 = 0$) map to the zero vector. Because the mapping is not injective (information is collapsed), it cannot be reversed. Hence, no inverse transformation $A^{-1}$ exists.
