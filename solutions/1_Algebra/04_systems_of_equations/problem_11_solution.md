## Question

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Solution

### 1. Augmented Matrix Setup

Write the system as an augmented matrix $[A(t) \mid b]$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
1 & t & 1 & \mid & 2 \\
1 & 1 & t & \mid & 3 \\
\end{pmatrix}.
$$

### 2. Elimination Steps

**Step 1:** Eliminate entry $(2,1)$ using $R_2 \leftarrow R_2 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & t - 1 & 0 & \mid & 1 \\
1 & 1 & t & \mid & 3 \\
\end{pmatrix}.
$$

**Step 2:** Eliminate entry $(3,1)$ using $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & t - 1 & 0 & \mid & 1 \\
0 & 0 & t - 1 & \mid & 2 \\
\end{pmatrix}.
$$

The augmented matrix is now in upper triangular form. The critical parameter value where division by the pivot ceases to be valid is $t = 1$.

### 3. Case Analysis Depending on $t$

#### Case 1: $t = 1$

Substitute $t = 1$ into the reduced matrix:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & 0 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 2 \\
\end{pmatrix}.
$$

- Row 2 represents $0 \cdot x + 0 \cdot y + 0 \cdot z = 1 \iff 0 = 1$ (contradiction).
- Row 3 represents $0 \cdot x + 0 \cdot y + 0 \cdot z = 2 \iff 0 = 2$ (contradiction).

Therefore, for $t = 1$, the system is inconsistent and has **no solution**.

#### Case 2: $t \neq 1$

When $t \neq 1$, $t - 1 \neq 0$, so we can safely divide rows 2 and 3 by $t - 1$:

From row 3:

$$
(t - 1)z = 2 \implies z = \frac{2}{t - 1}.
$$

From row 2:

$$
(t - 1)y = 1 \implies y = \frac{1}{t - 1}.
$$

From row 1:

$$
x + y + z = 1 \implies x = 1 - y - z = 1 - \frac{1}{t - 1} - \frac{2}{t - 1} = 1 - \frac{3}{t - 1} = \frac{t - 1 - 3}{t - 1} = \frac{t - 4}{t - 1}.
$$

Therefore, for every $t \neq 1$, there is **exactly one unique solution**:

$$
(x, y, z) = \left(\frac{t - 4}{t - 1}, \, \frac{1}{t - 1}, \, \frac{2}{t - 1}\right).
$$

### 4. Summary of Cases

- For $t = 1$: **no solution**.
- For all $t \neq 1$: **exactly one solution**.
- The case of infinitely many solutions **never occurs** for any value of $t$.
