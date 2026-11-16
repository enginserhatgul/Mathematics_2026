## Question

For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

## Solution

### 1. The Row Operation

Apply $R_2 \leftarrow R_2 - 2R_1$. This operation does not change the determinant:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t-6 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

### 2. Determinant from the New Structure

The first column now contains only one nonzero entry, so expand along it:

$$
\det A(t) = 1 \cdot
\det
\begin{pmatrix}
0 & t-6 \\
1 & 1 \\
\end{pmatrix}
= 0\cdot 1 - (t-6)\cdot 1 = 6 - t.
$$

Equivalently, swapping $R_2$ and $R_3$ gives an upper triangular matrix with diagonal $1, 1, t-6$ and changes the sign once, so $\det A(t) = -(t-6) = 6-t$.

### 3. Values of $t$ for Which the Matrix Is Not Invertible

A square matrix is not invertible exactly when its determinant is zero:

$$
6 - t = 0 \quad\Longleftrightarrow\quad t = 6.
$$

For every $t \neq 6$ the matrix is invertible.

### 4. What Happens to the Rows for $t = 6$

For $t = 6$ the second row of the original matrix is

$$
R_2 = (2, 4, 6) = 2\cdot(1, 2, 3) = 2R_1.
$$

The rows are linearly dependent: $R_2 - 2R_1 = (0,0,0)$. After the operation, one row is entirely zero, so the rank is less than $3$ and the matrix cannot be invertible.

### 5. Check by Direct Expansion

Expanding along the first row of $A(t)$:

$$
\det A(t) = 1(4\cdot 1 - t\cdot 1) - 2(2\cdot 1 - t\cdot 0) + 3(2\cdot 1 - 4\cdot 0) = 4 - t - 4 + 6 = 6 - t.
$$

The result agrees.
