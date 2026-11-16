## Question

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## Solution

### 1. Definition of the Inverse Matrix

An $n\times n$ matrix $B$ is the inverse of an $n\times n$ matrix $A$ (denoted $B = A^{-1}$) if and only if both products satisfy:

$$
AB = I \qquad \mathrm{and} \qquad BA = I,
$$

where $I$ is the identity matrix of the matching size ($2\times 2$ in this case).

### 2. Computation of $AB$

Multiply $A$ on the left and $B$ on the right:

$$
AB =
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

Evaluating row-by-column:

- Row 1, Column 1: $2(1) + 1(-1) = 2 - 1 = 1$
- Row 1, Column 2: $2(-1) + 1(2) = -2 + 2 = 0$
- Row 2, Column 1: $1(1) + 1(-1) = 1 - 1 = 0$
- Row 2, Column 2: $1(-1) + 1(2) = -1 + 2 = 1$

Therefore:

$$
AB =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$

### 3. Computation of $BA$

Multiply $B$ on the left and $A$ on the right:

$$
BA =
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}.
$$

Evaluating row-by-column:

- Row 1, Column 1: $1(2) + (-1)(1) = 2 - 1 = 1$
- Row 1, Column 2: $1(1) + (-1)(1) = 1 - 1 = 0$
- Row 2, Column 1: $-1(2) + 2(1) = -2 + 2 = 0$
- Row 2, Column 2: $-1(1) + 2(1) = -1 + 2 = 1$

Therefore:

$$
BA =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$

### 4. Conclusion

Since both $AB = I$ and $BA = I$ hold true, matrix $B$ satisfies the formal definition of the inverse matrix of $A$. Hence:

$$
B = A^{-1}.
$$
