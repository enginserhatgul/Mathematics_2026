## Question

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

## Solution

### 1. Invertibility Condition

Compute the determinant of $A(t)$:

$$
\det A(t) = (1)(1) - (t)(t) = 1 - t^2 = (1 - t)(1 + t).
$$

A matrix is invertible if and only if its determinant is non-zero:

$$
\det A(t) \neq 0 \iff 1 - t^2 \neq 0 \iff t^2 \neq 1 \iff t \neq 1 \quad \mathrm{and} \quad t \neq -1.
$$

Thus, $A(t)$ is invertible for all real numbers $t \in \mathbb{R} \setminus \{-1, 1\}$.

### 2. Formula for $A(t)^{-1}$

For $t \neq \pm 1$, use the $2\times 2$ matrix inverse formula:

$$
A(t)^{-1} = \frac{1}{\det A(t)}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
= \frac{1}{1 - t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}.
$$

### 3. Explanation of Excluded Values

At $t = 1$ and $t = -1$, the factor $\frac{1}{1 - t^2}$ involves division by zero, which is undefined.

- For $t = 1$:

$$
A(1) =
\begin{pmatrix}
1 & 1 \\
1 & 1 \\
\end{pmatrix}.
$$

Row 2 is identical to Row 1 ($R_2 = R_1$). The columns are also identical. The matrix has rank $1 < 2$, so it compresses the entire plane $\mathbb{R}^2$ onto the 1D line $y = x$.

- For $t = -1$:

$$
A(-1) =
\begin{pmatrix}
1 & -1 \\
-1 & 1 \\
\end{pmatrix}.
$$

Row 2 is the exact negative of Row 1 ($R_2 = -R_1$). Again, the matrix has rank $1 < 2$, compressing $\mathbb{R}^2$ onto the line $y = -x$.

In both cases, dimensional collapse causes loss of information (the mapping is not one-to-one), so no inverse mapping exists.
