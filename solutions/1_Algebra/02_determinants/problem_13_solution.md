## Question

Compute the determinant

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

## Solution

### 1. Clearing the First Column

Use the pivot $a_{11} = 1$.

Step 1: $R_2 \leftarrow R_2 - 2R_1$. The determinant is **unchanged**.

Step 2: $R_3 \leftarrow R_3 - R_1$. The determinant is **unchanged**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}
$$

### 2. Clearing the Second Column

Step 3: $R_3 \leftarrow R_3 + 2R_2$. The determinant is **unchanged**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

### 3. Reading Off the Determinant

All three operations are of the type $R_i \leftarrow R_i + cR_j$, so the determinant of the original matrix equals the determinant of the triangular matrix:

$$
\det A = 1 \cdot 1 \cdot 1 = 1.
$$

No row swaps or row scalings were used, so no correcting factor is needed.

### 4. Check by Direct Expansion

$$
\begin{aligned}
\det A &= 1(5\cdot 2 - 7\cdot 0) - 2(2\cdot 2 - 7\cdot 1) + 3(2\cdot 0 - 5\cdot 1) \\
       &= 10 - 2(-3) + 3(-5) \\
       &= 10 + 6 - 15 \\
       &= 1.
\end{aligned}
$$

### 5. Conclusion

$$
\det A = 1,
$$

so $A$ is invertible.
