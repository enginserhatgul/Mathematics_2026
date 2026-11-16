## Question

It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

## Solution

### 1. Computation of $(3A)^{-1}$

**Property:** For any non-zero scalar $c$ and invertible matrix $A$, scaling the matrix scales its inverse by the reciprocal:

$$
(cA)^{-1} = \frac{1}{c} A^{-1}.
$$

Here $c = 3$:

$$
(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3} \\
\end{pmatrix}.
$$

### 2. Computation of $(A^T)^{-1}$

**Property:** Inversion and transposition commute with each other:

$$
(A^T)^{-1} = (A^{-1})^T.
$$

Transposing the given $A^{-1}$:

$$
(A^T)^{-1} =
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}^T
= \begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}.
$$

### 3. Computation of $(A^2)^{-1}$

**Property:** The inverse of a matrix power is the power of the inverse matrix:

$$
(A^k)^{-1} = (A^{-1})^k.
$$

For $k = 2$:

$$
(A^2)^{-1} = (A^{-1})^2 = A^{-1} A^{-1} =
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Evaluating row-by-column:

- Entry $(1,1)$: $2(2) + (-1)(-3) = 4 + 3 = 7$
- Entry $(1,2)$: $2(-1) + (-1)(2) = -2 - 2 = -4$
- Entry $(2,1)$: $-3(2) + 2(-3) = -6 - 6 = -12$
- Entry $(2,2)$: $-3(-1) + 2(2) = 3 + 4 = 7$

Therefore:

$$
(A^2)^{-1} =
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}.
$$
