## Question

Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Solution

### 1. Augmented Matrix Setup

Write the system as an augmented matrix:

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
2 & 4 & \mid & 7 \\
\end{pmatrix}.
$$

### 2. Elimination Step

Apply the row operation $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
2 - 2(1) & 4 - 2(2) & \mid & 7 - 2(3) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 2 & \mid & 3 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}.
$$

### 3. Appearance of the Contradiction

The second row of the echelon matrix corresponds to the algebraic equation:

$$
0 \cdot x + 0 \cdot y = 1 \iff 0 = 1.
$$

Because $0 = 1$ is impossible for any choice of real numbers $x$ and $y$, the system has **no solution** (it is inconsistent).

### 4. Geometric and Algebraic Interpretation

- **Algebraic Interpretation:** Multiplying the first equation by $2$ gives $2x + 4y = 6$. The second equation demands that the identical linear combination $2x + 4y$ equals $7$. A single quantity cannot equal both $6$ and $7$ simultaneously.
- **Geometric Interpretation:** Each linear equation describes a line in the Cartesian plane $\mathbb{R}^2$:
  - $L_1: y = -\frac{1}{2}x + \frac{3}{2}$
  - $L_2: y = -\frac{1}{2}x + \frac{7}{4}$
  Both lines have the same slope $m = -\frac{1}{2}$ but different $y$-intercepts ($\frac{3}{2} \neq \frac{7}{4}$). They are distinct parallel lines that never intersect.
- **Rank Condition:** The coefficient matrix has $\mathrm{rank}(A) = 1$, whereas the augmented matrix has $\mathrm{rank}([A \mid b]) = 2$. By the Rouché–Capelli Theorem, because $\mathrm{rank}(A) < \mathrm{rank}([A \mid b])$, the system is inconsistent.
