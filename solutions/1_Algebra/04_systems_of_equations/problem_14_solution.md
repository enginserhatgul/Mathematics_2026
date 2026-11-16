## Question

Compare the systems

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
$$

and

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

## Solution

### 1. Analysis of System A

$$
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3.
\end{cases}
$$

From the third equation:

$$
3x = 3 \implies x = 1.
$$

Substitute $x = 1$ into the first equation:

$$
1 + y = 2 \implies y = 1.
$$

Now test candidate solution $(x, y) = (1, 1)$ in the second equation:

$$
2(1) - (1) = 2 - 1 = 1.
$$

The second equation is satisfied ($1 = 1$).
Therefore, System A is **consistent** and has **exactly one solution**:

$$
(x, y) = (1, 1).
$$

### 2. Analysis of System B

$$
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3.1.
\end{cases}
$$

From the third equation:

$$
3x = 3.1 \implies x = \frac{3.1}{3} = \frac{31}{30}.
$$

Substitute $x = \frac{31}{30}$ into the first equation:

$$
y = 2 - x = 2 - \frac{31}{30} = \frac{60 - 31}{30} = \frac{29}{30}.
$$

Now test candidate values in the second equation:

$$
2x - y = 2\left(\frac{31}{30}\right) - \frac{29}{30} = \frac{62 - 29}{30} = \frac{33}{30} = 1.1.
$$

However, the second equation demands that $2x - y = 1$. Since $1.1 \neq 1$, we reach a contradiction ($1.1 = 1$).
Therefore, System B is **inconsistent** and has **no solution**.

### 3. Geometric and Algebraic Explanation

Both systems are **overdetermined**: they contain $3$ equations for only $2$ unknowns.
In the Cartesian plane $\mathbb{R}^2$, each equation represents a straight line.

- In System A, the first two lines intersect at $(1, 1)$. The third line ($x = 1$) happens to pass precisely through that same intersection point. All three lines are **concurrent** at the single point $(1, 1)$.
- In System B, changing the right-hand side from $3$ to $3.1$ shifts the vertical line from $x = 1$ to $x = 1.0333$. The three lines no longer share a common intersection point; instead, they intersect pairwise to form a small triangle.

Because an overdetermined system requires all lines to meet at a single point, consistency holds only when the right-hand side vector lies in the column space of the coefficient matrix. A tiny perturbation of $0.1$ pushes the vector outside that subspace, transforming a consistent system into an inconsistent one.
