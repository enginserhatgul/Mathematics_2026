## Question

Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## Solution

### 1. Simultaneous Augmented Matrix Formulation

Both systems share the identical coefficient matrix:

$$
A =
\begin{pmatrix}
2 & 1 \\
1 & -1 \\
\end{pmatrix}.
$$

They differ only in their right-hand side vectors: $b_1 = \begin{pmatrix} 5 \\ 1 \end{pmatrix}$ and $b_2 = \begin{pmatrix} 1 \\ 4 \end{pmatrix}$.
We can combine both right-hand sides into a single augmented matrix $[A \mid b_1 \mid b_2]$:

$$
\begin{pmatrix}
2 & 1 & \mid & 5 & 1 \\
1 & -1 & \mid & 1 & 4 \\
\end{pmatrix}.
$$

### 2. Elimination Steps

**Step 1:** Swap $R_1 \leftrightarrow R_2$ to place a pivot of $1$ in the first position:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 & 4 \\
2 & 1 & \mid & 5 & 1 \\
\end{pmatrix}.
$$

**Step 2:** Eliminate entry $(2,1)$ using $R_2 \leftarrow R_2 - 2R_1$:

- Row 2 on $A$: $(2 - 2(1), 1 - 2(-1)) = (0, 3)$.
- Row 2 on $b_1$: $5 - 2(1) = 3$.
- Row 2 on $b_2$: $1 - 2(4) = -7$.

The echelon form is:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 & 4 \\
0 & 3 & \mid & 3 & -7 \\
\end{pmatrix}.
$$

### 3. Solving the Individual Systems

- **For System 1 (using column $b_1$):**
  From row 2: $3y = 3 \implies y = 1$.
  From row 1: $x - y = 1 \implies x - 1 = 1 \implies x = 2$.
  Unique solution: $(x, y) = (2, 1)$.

- **For System 2 (using column $b_2$):**
  From row 2: $3y = -7 \implies y = -\frac{7}{3}$.
  From row 1: $x - y = 4 \implies x - \left(-\frac{7}{3}\right) = 4 \implies x = 4 - \frac{7}{3} = \frac{5}{3}$.
  Unique solution: $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$.

### 4. Comparison and Explanation

- **What is the same:** The row operations chosen ($R_1 \leftrightarrow R_2$, then $R_2 \leftarrow R_2 - 2R_1$) and all calculations performed on the left-hand side of the augmented matrix are 100% identical in both cases. The resulting coefficient matrix $\begin{pmatrix} 1 & -1 \\ 0 & 3 \end{pmatrix}$ is the same.
- **Why:** The sequence of row operations in Gaussian elimination is determined strictly by the entries of the coefficient matrix $A$, which defines the linear relationships between the unknowns. The right-hand sides merely undergo the arithmetic specified by those operations, but never influence the choice of operations.
