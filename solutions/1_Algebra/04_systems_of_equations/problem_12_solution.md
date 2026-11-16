## Question

Solve

$$
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

## Solution

### 1. Augmented Matrix and Elimination

A system with all right-hand sides equal to zero is called a **homogeneous linear system**. Set up the augmented matrix:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
2 & 4 & -2 & \mid & 0 \\
1 & -1 & 2 & \mid & 0 \\
\end{pmatrix}.
$$

**Step 1:** $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
1 & -1 & 2 & \mid & 0 \\
\end{pmatrix}.
$$

Row 2 is entirely zero (the second equation was an exact duplicate multiple of the first).

**Step 2:** $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
\end{pmatrix}.
$$

**Step 3:** Swap $R_2 \leftrightarrow R_3$:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

**Step 4:** Scale $R_2 \leftarrow -\frac{1}{3} R_2$:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 1 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

### 2. Parametric Solution

From row 2:

$$
y - z = 0 \implies y = z.
$$

From row 1:

$$
x + 2y - z = 0 \implies x + 2(z) - z = 0 \implies x + z = 0 \implies x = -z.
$$

Here $z$ is the free variable. Assigning parameter $z = t$ ($t \in \mathbb{R}$):

$$
\begin{cases}
x = -t, \\
y = t, \\
z = t,
\end{cases}
\qquad t \in \mathbb{R}.
$$

In vector form:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
= t
\begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

The solution set consists of **infinitely many solutions** representing the 1-dimensional line through the origin spanned by $(-1, 1, 1)^T$.

### 3. Why $(0, 0, 0)$ Always Satisfies a Homogeneous System

In any homogeneous system of equations:

$$
a_{i1} x_1 + a_{i2} x_2 + \dots + a_{in} x_n = 0,
$$

substituting $x_1 = 0, x_2 = 0, \dots, x_n = 0$ yields:

$$
a_{i1}(0) + a_{i2}(0) + \dots + a_{in}(0) = 0 + 0 + \dots + 0 = 0,
$$

which is identically true for all equations regardless of the coefficients $a_{ij}$.
In matrix form:

$$
A \cdot \mathbf{0} = \mathbf{0}.
$$

Therefore, the zero vector $\mathbf{0} = (0, 0, 0)^T$ (the **trivial solution**) is always guaranteed to be a solution of every homogeneous linear system.
