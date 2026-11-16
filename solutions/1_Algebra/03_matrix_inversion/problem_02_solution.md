## Question

Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

## Solution

### 1. Invertibility Condition and Determinant

For a general $2\times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is:

$$
\det A = ad - bc.
$$

For the given matrix $A$:

$$
\det A = (3)(4) - (2)(5) = 12 - 10 = 2.
$$

Since $\det A = 2 \neq 0$, the matrix $A$ is invertible.

### 2. Application of the $2\times 2$ Inverse Formula

The explicit formula for the inverse of a $2\times 2$ matrix is:

$$
A^{-1} = \frac{1}{\det A}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}.
$$

Substituting $a = 3$, $b = 2$, $c = 5$, $d = 4$, and $\det A = 2$:

$$
A^{-1} = \frac{1}{2}
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}
= \begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}.
$$

### 3. Verification by Multiplication

Compute the product $A A^{-1}$:

$$
A A^{-1} =
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}.
$$

Evaluating each entry:

- Entry $(1,1)$: $3(2) + 2\left(-\frac{5}{2}\right) = 6 - 5 = 1$
- Entry $(1,2)$: $3(-1) + 2\left(\frac{3}{2}\right) = -3 + 3 = 0$
- Entry $(2,1)$: $5(2) + 4\left(-\frac{5}{2}\right) = 10 - 10 = 0$
- Entry $(2,2)$: $5(-1) + 4\left(\frac{3}{2}\right) = -5 + 6 = 1$

Therefore:

$$
A A^{-1} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$

The result is confirmed.
