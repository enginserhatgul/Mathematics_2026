## Question

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

## Solution

### 1. Augmented Matrix and Elimination

Set up the augmented matrix:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}.
$$

Apply the row operation $R_2 \leftarrow R_2 - a R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a - a(1) & a - a(1) & \mid & 4 - 2a \\
\end{pmatrix}
= \begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 4 - 2a \\
\end{pmatrix}.
$$

### 2. Case Analysis Depending on $a$

The second row corresponds to the equation:

$$
0 \cdot x + 0 \cdot y = 4 - 2a \iff 0 = 4 - 2a.
$$

- **Case 1: $4 - 2a = 0 \iff a = 2$**
  The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

  The second row is $0 = 0$, which is always true. The system reduces to the single equation $x + y = 2$.
  With $y = t$ ($t \in \mathbb{R}$) as the free parameter:

$$
\begin{pmatrix} x \\ y \end{pmatrix}
= \begin{pmatrix} 2 - t \\ t \end{pmatrix}
= \begin{pmatrix} 2 \\ 0 \end{pmatrix}
+ t
\begin{pmatrix} -1 \\ 1 \end{pmatrix},
\qquad t \in \mathbb{R}.
$$

  Therefore, for $a = 2$, the system has **infinitely many solutions**.

- **Case 2: $4 - 2a \neq 0 \iff a \neq 2$**
  The second row reads $0 = 4 - 2a$, where $4 - 2a \neq 0$. This is a mathematical contradiction ($0 = \mathrm{non-zero}$).
  Therefore, for all $a \neq 2$, the system has **no solution** (it is inconsistent).

### 3. Which Case Cannot Occur and Why

The possibility of **exactly one solution** cannot occur for any real value of $a$.

**Mathematical Reason:**
The coefficient matrix is:

$$
A =
\begin{pmatrix}
1 & 1 \\
a & a \\
\end{pmatrix}.
$$

Its determinant is:

$$
\det A = (1)(a) - (1)(a) = a - a = 0
$$

for every value of $a \in \mathbb{R}$.

A square system $Ax = b$ possesses a unique solution if and only if $\det A \neq 0$ (or equivalently $\mathrm{rank}(A) = 2$). Since $\det A = 0$ identically, $\mathrm{rank}(A) = 1 < 2$ for all $a$. The two lines represented by the equations always have identical slopes ($m = -1$) and are therefore always parallel. They can either be coincident ($a = 2$) or strictly parallel ($a \neq 2$), but can never intersect at a single unique point.
