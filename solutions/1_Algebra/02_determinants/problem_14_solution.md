## Question

Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

## Solution

### 1. The Determinant

$$
\det A = 1\cdot 4 - 2\cdot k = 4 - 2k.
$$

### 2. Unique Solution for Every $b$

The system $Ax=b$ has exactly one solution for every $b$ if and only if $A$ is invertible, that is, if and only if $\det A \neq 0$:

$$
4 - 2k \neq 0 \quad\Longleftrightarrow\quad k \neq 2.
$$

In that case $x = A^{-1}b$ is the unique solution.

### 3. The Exceptional Value $k = 2$

For $k = 2$ the matrix is

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix},
$$

and the second row is twice the first. Writing $b = (b_1, b_2)^T$, the operation $R_2 \leftarrow R_2 - 2R_1$ gives the augmented matrix

$$
\begin{pmatrix}
1 & 2 & \mid & b_1 \\
0 & 0 & \mid & b_2 - 2b_1 \\
\end{pmatrix}.
$$

- If $b_2 = 2b_1$, the second row is $0 = 0$ and the system has infinitely many solutions.
- If $b_2 \neq 2b_1$, the second row is a contradiction and the system has no solution.

### 4. Example with Infinitely Many Solutions

Take $b = (1, 2)^T$. Then $b_2 = 2b_1$ and both equations reduce to $x + 2y = 1$. Choosing $y = s$ as a free parameter:

$$
x = 1 - 2s, \qquad y = s, \qquad s \in \mathbb{R}.
$$

### 5. Example with No Solution

Take $b = (1, 3)^T$. The equations are

$$
\begin{cases}
x + 2y = 1, \\
2x + 4y = 3.
\end{cases}
$$

Doubling the first equation gives $2x + 4y = 2$, which contradicts $2x + 4y = 3$. Hence there is no solution.

### 6. Conclusion

The system has exactly one solution for every $b$ if and only if $k \neq 2$. For $k = 2$ the outcome depends on $b$: infinitely many solutions when $b_2 = 2b_1$ and none otherwise.
