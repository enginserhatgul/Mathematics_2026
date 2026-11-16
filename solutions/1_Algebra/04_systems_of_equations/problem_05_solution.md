## Question

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## Solution

### 1. Analyzing the Row Echelon Form

The given matrix is already in row echelon form:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

Let the variables be denoted by $x_1, x_2, x_3$.

- Total number of variables: $n = 3$.
- Number of non-zero rows (pivots): $r = 2$.
  - The pivot of row 1 is in column 1 (corresponding to $x_1$).
  - The pivot of row 2 is in column 2 (corresponding to $x_2$).
- The third row is $(0, 0, 0 \mid 0)$, which represents the consistent identity $0 = 0$.

### 2. Number of Free Variables

**Rule:** In any consistent linear system in row echelon form, the number of free variables equals the total number of unknowns minus the number of pivot columns (the rank):

$$
\mathrm{Number of free variables} = n - r = 3 - 2 = 1.
$$

Column 3 contains no pivot, so $x_3$ is the free variable. Because there is at least one free variable and no contradictory row $(0, 0, 0 \mid c)$ with $c \neq 0$, the system has **infinitely many solutions**.

### 3. Parametric Form of the Solution

Express the pivot variables in terms of the free variable $x_3$:

From row 2:

$$
x_2 + 2x_3 = 1 \implies x_2 = 1 - 2x_3.
$$

From row 1:

$$
x_1 + 2x_2 - x_3 = 3.
$$

Substitute $x_2 = 1 - 2x_3$:

$$
x_1 + 2(1 - 2x_3) - x_3 = 3 \implies x_1 + 2 - 4x_3 - x_3 = 3 \implies x_1 + 2 - 5x_3 = 3 \implies x_1 = 1 + 5x_3.
$$

Assigning the parameter $x_3 = t$ ($t \in \mathbb{R}$):

$$
\begin{cases}
x_1 = 1 + 5t, \\
x_2 = 1 - 2t, \\
x_3 = t,
\end{cases}
\qquad t \in \mathbb{R}.
$$

In vector form:

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix}
= \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}
+ t
\begin{pmatrix} 5 \\ -2 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$
