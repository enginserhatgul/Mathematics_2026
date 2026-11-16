## Question

Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## Solution

### 1. Augmented Matrix and Elimination

Set up the augmented matrix:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
2 & 2 & 2 & \mid & 4 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}.
$$

**Step 1:** $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}.
$$

Row 2 is entirely zero, showing that the second equation is a redundant multiple of the first ($E_2 = 2E_1$).

**Step 2:** $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
0 & -2 & 0 & \mid & -2 \\
\end{pmatrix}.
$$

**Step 3:** Swap $R_2 \leftrightarrow R_3$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & -2 & 0 & \mid & -2 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

**Step 4:** Scale $R_2 \leftarrow -\frac{1}{2} R_2$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 1 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

### 2. Identifying Pivot and Free Variables

- Pivot variables: $x$ (column 1) and $y$ (column 2).
- Free variable: $z$ (column 3 has no pivot).

From row 2:

$$
y = 1.
$$

From row 1:

$$
x + y + z = 2 \implies x + 1 + z = 2 \implies x = 1 - z.
$$

### 3. Parametric Solution

Setting the free variable $z = t$ ($t \in \mathbb{R}$):

$$
\begin{cases}
x = 1 - t, \\
y = 1, \\
z = t,
\end{cases}
\qquad t \in \mathbb{R}.
$$

In vector form:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
= \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}
+ t
\begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

The system has **infinitely many solutions**, geometrically forming a line in $\mathbb{R}^3$.

### 4. Verification for a Chosen Parameter Value

Choose parameter $t = 2$. The corresponding solution point is:

$$
x = 1 - 2 = -1, \qquad y = 1, \qquad z = 2.
$$

Substitute $(-1, 1, 2)$ into all three original equations:
1. $x + y + z = -1 + 1 + 2 = 2$ (satisfied).
2. $2x + 2y + 2z = 2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4$ (satisfied).
3. $x - y + z = -1 - 1 + 2 = 0$ (satisfied).

The chosen point satisfies all three equations.
