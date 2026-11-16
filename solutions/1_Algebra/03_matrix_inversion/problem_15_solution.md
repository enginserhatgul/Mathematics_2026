## Question

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Solution

### 1. Method 1: Using $x = A^{-1}b$

**Step 1: Check invertibility and find $\det A$**

$$
\det A = (2)(3) - (1)(1) = 6 - 1 = 5 \neq 0.
$$

**Step 2: Form the inverse matrix $A^{-1}$**

$$
A^{-1} = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

**Step 3: Multiply by vector $b$**

$$
x = A^{-1} b = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
3(7) + (-1)(8) \\
-1(7) + 2(8) \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
21 - 8 \\
-7 + 16 \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
13 \\
9 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}.
$$

### 2. Method 2: Using Gaussian Elimination

Set up the augmented matrix $[A \mid b]$:

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
1 & 3 & \mid & 8 \\
\end{pmatrix}.
$$

**Step 1: Swap rows to obtain a convenient pivot ($R_1 \leftrightarrow R_2$):**

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 & 1 & \mid & 7 \\
\end{pmatrix}.
$$

**Step 2: Eliminate entry $(2,1)$ using $R_2 \leftarrow R_2 - 2R_1$:**

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & 1 - 2(3) & \mid & 7 - 2(8) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & -5 & \mid & -9 \\
\end{pmatrix}.
$$

**Step 3: Back substitution**
From the second row:

$$
-5 x_2 = -9 \implies x_2 = \frac{9}{5}.
$$

From the first row:

$$
x_1 + 3 x_2 = 8 \implies x_1 = 8 - 3\left(\frac{9}{5}\right) = \frac{40 - 27}{5} = \frac{13}{5}.
$$

Thus:

$$
x =
\begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}.
$$

### 3. Comparison of the Two Methods

- **Consistency:** Both methods produce the identical unique solution:
  $x_1 = \frac{13}{5}$, $x_2 = \frac{9}{5}$.
- **Simplicity in this Example:**
  Gaussian elimination was simpler and more direct. It required only one row elimination and simple back-substitution, avoiding the calculation of the determinant and the four entries of the inverse matrix.
- **General Takeaway:**
  Gaussian elimination is computationally faster for solving a single system with a specific right-hand side $b$. However, if one needs to solve $Ax = b$ for many different vectors $b$, finding $A^{-1}$ once allows computing each subsequent solution with a single matrix-vector multiplication.
