## Question

The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

## Solution

### 1. Finding $S^{-1}$

Compute $\det S$:

$$
\det S = (2)\left(\frac{1}{2}\right) - (0)(0) = 1 \neq 0.
$$

Since $S$ is a diagonal matrix, its inverse is obtained by taking the reciprocals of its diagonal entries:

$$
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}.
$$

### 2. Geometric Interpretation

- The matrix $S$ scales vectors in $\mathbb{R}^2$ by stretching the horizontal coordinate $x$ by a factor of $2$, while compressing the vertical coordinate $y$ by a factor of $\frac{1}{2}$.
- The inverse matrix $S^{-1}$ performs the opposite operations: it compresses the horizontal coordinate $x$ by a factor of $\frac{1}{2}$, and stretches the vertical coordinate $y$ by a factor of $2$.

Because $(2)(\frac{1}{2}) = 1$ and $(\frac{1}{2})(2) = 1$, applying $S$ and then $S^{-1}$ restores the plane to its original geometry.

### 3. Verification on a Specific Vector

Choose the vector $v = \begin{pmatrix} 4 \\ 6 \end{pmatrix}$.

Apply transformation $S$:

$$
Sv =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
\begin{pmatrix}
4 \\
6 \\
\end{pmatrix}
= \begin{pmatrix}
2(4) \\
\frac{1}{2}(6) \\
\end{pmatrix}
= \begin{pmatrix}
8 \\
3 \\
\end{pmatrix}.
$$

Apply the inverse transformation $S^{-1}$:

$$
S^{-1}(Sv) =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
8 \\
3 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2}(8) \\
2(3) \\
\end{pmatrix}
= \begin{pmatrix}
4 \\
6 \\
\end{pmatrix}
= v.
$$

The vector is restored to its original value.
