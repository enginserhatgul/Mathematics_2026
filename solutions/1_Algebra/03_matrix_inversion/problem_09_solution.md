## Question

Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

## Solution

### 1. Algebraic Analysis: Which Side to Multiply

In the matrix equation $AX = B$, the coefficient matrix $A$ multiplies the unknown matrix $X$ from the left. Because matrix multiplication is non-commutative in general ($M_1 M_2 \neq M_2 M_1$), we must multiply both sides on the **left** by $A^{-1}$:

$$
A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B.
$$

Multiplying on the right would give $AXA^{-1} = BA^{-1}$, which does not simplify the left-hand side to $X$.

### 2. Computation of $A^{-1}$

Compute $\det A$:

$$
\det A = (1)(1) - (2)(0) = 1.
$$

Since $\det A = 1 \neq 0$, $A$ is invertible:

$$
A^{-1} = \frac{1}{1}
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}.
$$

### 3. Computation of $X = A^{-1}B$

$$
X =
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Evaluating row-by-column:

- Entry $(1,1)$: $1(3) + (-2)(2) = 3 - 4 = -1$
- Entry $(1,2)$: $1(1) + (-2)(4) = 1 - 8 = -7$
- Entry $(2,1)$: $0(3) + 1(2) = 2$
- Entry $(2,2)$: $0(1) + 1(4) = 4$

Therefore:

$$
X =
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
$$

### 4. Verification by Computing $AX$

$$
AX =
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
= \begin{pmatrix}
1(-1) + 2(2) & 1(-7) + 2(4) \\
0(-1) + 1(2) & 0(-7) + 1(4) \\
\end{pmatrix}
= \begin{pmatrix}
-1 + 4 & -7 + 8 \\
2 & 4 \\
\end{pmatrix}
= \begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}
= B.
$$

The solution is confirmed.
