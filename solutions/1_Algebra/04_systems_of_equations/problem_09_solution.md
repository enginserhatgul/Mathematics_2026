## Question

Find numbers $x,y$ satisfying

$$
x+y=10,\qquad 2x+5y=32.
$$

Solve the system and explain geometrically why the solution is unique.

## Solution

### 1. Solving the System

The system of equations is:

$$
\begin{cases}
x + y = 10, \\
2x + 5y = 32.
\end{cases}
$$

Set up the augmented matrix:

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
2 & 5 & \mid & 32 \\
\end{pmatrix}.
$$

Apply the elimination step $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
2 - 2(1) & 5 - 2(1) & \mid & 32 - 2(10) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 1 & \mid & 10 \\
0 & 3 & \mid & 12 \\
\end{pmatrix}.
$$

From row 2:

$$
3y = 12 \implies y = 4.
$$

Substitute $y = 4$ into row 1:

$$
x + 4 = 10 \implies x = 6.
$$

The solution is:

$$
(x, y) = (6, 4).
$$

### 2. Geometric Explanation of Uniqueness

Each linear equation represents a straight line in the 2-dimensional plane $\mathbb{R}^2$:

- Line $L_1$: $x + y = 10 \implies y = -x + 10$.
  - Slope: $m_1 = -1$.
  - Normal vector: $n_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$.

- Line $L_2$: $2x + 5y = 32 \implies y = -\frac{2}{5}x + \frac{32}{5}$.
  - Slope: $m_2 = -\frac{2}{5}$.
  - Normal vector: $n_2 = \begin{pmatrix} 2 \\ 5 \end{pmatrix}$.

**Why the Solution is Unique:**
1. The two lines have different slopes ($m_1 = -1 \neq -\frac{2}{5} = m_2$).
2. Equivalently, their normal vectors are linearly independent, as verified by the determinant of the coefficient matrix:

$$
\det A =
\begin{vmatrix}
1 & 1 \\
2 & 5 \\
\end{vmatrix}
= (1)(5) - (1)(2) = 5 - 2 = 3 \neq 0.
$$

In Euclidean geometry, two lines in a plane that are not parallel must intersect at **exactly one unique point**. The intersection point is $(6, 4)$, which is the only point in the plane that lies on both lines simultaneously.
