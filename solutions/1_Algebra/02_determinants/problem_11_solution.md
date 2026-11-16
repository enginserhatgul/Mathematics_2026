## Question

Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## Solution

### 1. Strategy

The first column is $(1,1,1)^T$, so the entry $1$ in the position $(1,1)$ can be used as a pivot to clear the two entries below it. The operation $R_i \leftarrow R_i - cR_j$ (with $i \neq j$) **does not change the determinant**, so both eliminations are safe.

### 2. Creating Zeros Below the Pivot

Apply $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
$$

Both operations add a multiple of another row to a row, hence the determinant is unchanged.

### 3. Completing the Triangular Form

Apply $R_3 \leftarrow R_3 - 2R_2$:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

This operation again does not change the determinant. The matrix is upper triangular, so its determinant is the product of the diagonal entries:

$$
\det = 1 \cdot 1 \cdot 1 = 1.
$$

### 4. Check by Direct Expansion

Expanding along the first row:

$$
\begin{aligned}
\det &= 1(3\cdot 6 - 4\cdot 4) - 2(1\cdot 6 - 4\cdot 1) + 3(1\cdot 4 - 3\cdot 1) \\
     &= 1\cdot 2 - 2\cdot 2 + 3\cdot 1 \\
     &= 1.
\end{aligned}
$$

### 5. Conclusion

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
= 1.
$$

Operations of the form $R_i \leftarrow R_i + cR_j$ do not change the determinant. By contrast, swapping two rows changes its sign, and multiplying a row by $c$ multiplies the determinant by $c$; neither was needed here.
