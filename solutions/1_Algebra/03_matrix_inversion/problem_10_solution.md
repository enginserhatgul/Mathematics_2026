## Question

Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## Solution

### 1. Invertibility Criterion for Diagonal Matrices

The determinant of a diagonal matrix equals the product of its diagonal entries:

$$
\det D = (2)(-3)(5) = -30 \neq 0.
$$

$$
\det E = (2)(0)(5) = 0.
$$

- **Matrix $D$ is invertible** because all diagonal entries are non-zero ($\det D \neq 0$).
- **Matrix $E$ is not invertible** because it contains a zero on its main diagonal ($\det E = 0$). In fact, the entire second row and second column of $E$ are zero, so its rank is at most $2 < 3$.

### 2. Inverse of Matrix $D$

For any diagonal matrix with non-zero diagonal entries $d_1, d_2, \dots, d_n$, its inverse is simply the diagonal matrix with reciprocal entries $\frac{1}{d_1}, \frac{1}{d_2}, \dots, \frac{1}{d_n}$:

$$
D^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}.
$$

### 3. Verification by Multiplication

Compute $D D^{-1}$:

$$
D D^{-1} =
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}
= \begin{pmatrix}
2\left(\frac{1}{2}\right) & 0 & 0 \\
0 & (-3)\left(-\frac{1}{3}\right) & 0 \\
0 & 0 & 5\left(\frac{1}{5}\right) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
= I.
$$

The result is confirmed.
