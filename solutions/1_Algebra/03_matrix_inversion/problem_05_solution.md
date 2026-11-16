## Question

Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

## Solution

### 1. Invertibility Check

Compute $\det A$ by cofactor expansion along row 1:

$$
\det A = 1 \cdot
\begin{vmatrix}
1 & 1 \\
0 & 1 \\
\end{vmatrix}
- 1 \cdot
\begin{vmatrix}
0 & 1 \\
1 & 1 \\
\end{vmatrix}
+ 0 = 1(1 - 0) - 1(0 - 1) = 1 - (-1) = 2.
$$

Since $\det A = 2 \neq 0$, the inverse $A^{-1}$ exists.

### 2. Step-by-Step Gauss–Jordan Elimination

Set up the augmented matrix $[A \mid I]$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 & 0 & 1 & \mid & 0 & 0 & 1 \\
\end{pmatrix}.
$$

**Step 1:** Eliminate entry $(3,1)$ using $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & -1 & 1 & \mid & -1 & 0 & 1 \\
\end{pmatrix}.
$$

**Step 2:** Eliminate entry $(3,2)$ using $R_3 \leftarrow R_3 + R_2$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 2 & \mid & -1 & 1 & 1 \\
\end{pmatrix}.
$$

**Step 3:** Normalize row 3 using $R_3 \leftarrow \frac{1}{2} R_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}.
$$

**Step 4:** Eliminate entry $(2,3)$ using $R_2 \leftarrow R_2 - R_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}.
$$

**Step 5:** Eliminate entry $(1,2)$ using $R_1 \leftarrow R_1 - R_2$:

$$
\begin{pmatrix}
1 & 0 & 0 & \mid & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}.
$$

The left block is $I$, so the right block is $A^{-1}$:

$$
A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
= \frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$

### 3. Verification by Multiplication

Compute $A A^{-1}$:

$$
A A^{-1} =
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
\cdot \frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$

Evaluating row-by-column:

- Row 1:
  - $(1)(1) + (1)(1) + (0)(-1) = 2$
  - $(1)(-1) + (1)(1) + (0)(1) = 0$
  - $(1)(1) + (1)(-1) + (0)(1) = 0$
- Row 2:
  - $(0)(1) + (1)(1) + (1)(-1) = 0$
  - $(0)(-1) + (1)(1) + (1)(1) = 2$
  - $(0)(1) + (1)(-1) + (1)(1) = 0$
- Row 3:
  - $(1)(1) + (0)(1) + (1)(-1) = 0$
  - $(1)(-1) + (0)(1) + (1)(1) = 0$
  - $(1)(1) + (0)(-1) + (1)(1) = 2$

Multiplying by the scalar $\frac{1}{2}$:

$$
A A^{-1} = \frac{1}{2}
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
= I.
$$

The result is confirmed.
