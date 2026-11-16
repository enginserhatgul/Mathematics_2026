## Question

Consider the system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Solution

### 1. Augmented Matrix Setup and Elimination

Set up the augmented matrix for the unknowns $(x_1, x_2, x_3)$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
1 & 0 & -1 & \mid & 2 \\
\end{pmatrix}.
$$

**Step 1:** Eliminate entry $(3,1)$ using $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & -1 & -1 & \mid & 2 - 10 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & -1 & -1 & \mid & -8 \\
\end{pmatrix}.
$$

**Step 2:** Eliminate entry $(3,2)$ using $R_3 \leftarrow R_3 + R_2$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

The third row reduces completely to $0 = 0$.

### 2. Solving the System

The row echelon form shows $2$ pivots and $1$ free variable ($x_3$):

From row 2:

$$
x_2 + x_3 = 8 \implies x_2 = 8 - x_3.
$$

From row 1:

$$
x_1 + x_2 = 10 \implies x_1 = 10 - x_2 = 10 - (8 - x_3) = 2 + x_3.
$$

Setting $x_3 = t$ ($t \in \mathbb{R}$):

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix}
= \begin{pmatrix} 2 + t \\ 8 - t \\ t \end{pmatrix}
= \begin{pmatrix} 2 \\ 8 \\ 0 \end{pmatrix}
+ t
\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

The system has **infinitely many solutions**.

### 3. Redundancy of Equations

Not all three equations are independently necessary. The third equation is completely redundant and follows directly from the first two.

**Calculation Showing Dependence:**
Subtract the second equation from the first equation:

$$
(x_1 + x_2) - (x_2 + x_3) = 10 - 8.
$$

Simplifying the left-hand side:

$$
x_1 - x_3 = 2.
$$

This is precisely the third equation. Since Equation 3 is a linear combination of Equations 1 and 2 ($E_3 = E_1 - E_2$), dropping the third equation leaves the solution set unchanged.
