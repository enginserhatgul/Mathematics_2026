## Question

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

## Solution

### 1. System 1

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
1 & -1 & \mid & 0 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - R_1}
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -2 & \mid & -2 \\
\end{pmatrix}.
$$

- **Classification:** **Exactly one solution (unique solution)**.
- **Justification:** Both columns have pivots (pivot in row 1 column 1, pivot in row 2 column 2). The rank of the coefficient matrix is $r = 2$, which equals the number of variables $n = 2$. There are no contradictory rows. Solving yields $y = 1, x = 1$, corresponding to two lines that intersect at the single point $(1, 1)$.

### 2. System 2

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 4 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

- **Classification:** **Infinitely many solutions**.
- **Justification:** The second row reduces entirely to $0 = 0$. The rank of the matrix is $r = 1$, which is less than the number of variables $n = 2$. This gives $n - r = 2 - 1 = 1$ free variable. The two equations describe the identical line ($x + y = 2$). With $y = t$ as parameter, the solutions are $(x, y) = (2 - t, t)$ for all $t \in \mathbb{R}$.

### 3. System 3

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 5 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}.
$$

- **Classification:** **No solution (inconsistent system)**.
- **Justification:** The second row yields $0 \cdot x + 0 \cdot y = 1 \iff 0 = 1$, which is an explicit contradiction. Here $\mathrm{rank}(A) = 1$ while $\mathrm{rank}([A \mid b]) = 2$. Geometrically, the two equations describe distinct parallel lines with equal slope ($m = -1$) and different intercepts, which never meet.
