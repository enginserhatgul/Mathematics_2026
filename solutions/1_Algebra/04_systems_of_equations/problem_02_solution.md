## Question

Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

## Solution

### 1. Augmented Matrix Setup

Write the system as an augmented matrix $[A \mid b]$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
2 & -1 & 1 & \mid & 3 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}.
$$

### 2. Forward Elimination

**Step 1:** Eliminate entry $(2,1)$ using $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}.
$$

**Step 2:** Eliminate entry $(3,1)$ using $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
0 & 1 & -2 & \mid & -4 \\
\end{pmatrix}.
$$

**Step 3:** Swap $R_2 \leftrightarrow R_3$ to obtain a pivot of $1$ in row 2:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & -3 & -1 & \mid & -9 \\
\end{pmatrix}.
$$

**Step 4:** Eliminate entry $(3,2)$ using $R_3 \leftarrow R_3 + 3R_2$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & 0 & -7 & \mid & -21 \\
\end{pmatrix}.
$$

The system is now in upper triangular (row echelon) form.

### 3. Back-Substitution

From row 3:

$$
-7z = -21 \implies z = 3.
$$

From row 2:

$$
y - 2z = -4 \implies y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2.
$$

From row 1:

$$
x + y + z = 6 \implies x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1.
$$

The unique solution is:

$$
(x, y, z) = (1, 2, 3).
$$

### 4. Verification in All Three Equations

1. First equation: $1 + 2 + 3 = 6$ (holds).
2. Second equation: $2(1) - 2 + 3 = 2 - 2 + 3 = 3$ (holds).
3. Third equation: $1 + 2(2) - 3 = 1 + 4 - 3 = 2$ (holds).

All equations are satisfied simultaneously, confirming the solution.
