## Question

For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Solution

Both matrices are square with size $2\times 2$, so both products $AB$ and $BA$ are well-defined and yield $2\times 2$ matrices.

### 1. Computation of $AB$

Multiply row by column:

$$
AB=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1\cdot 2 + 2\cdot 3 & 1\cdot 0 + 2\cdot 1 \\
0\cdot 2 + 1\cdot 3 & 0\cdot 0 + 1\cdot 1 \\
\end{pmatrix}
= \begin{pmatrix}
2+6 & 0+2 \\
0+3 & 0+1 \\
\end{pmatrix}.
$$

Thus,

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}.
$$

### 2. Computation of $BA$

Multiply row by column:

$$
BA=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
2\cdot 1 + 0\cdot 0 & 2\cdot 2 + 0\cdot 1 \\
3\cdot 1 + 1\cdot 0 & 3\cdot 2 + 1\cdot 1 \\
\end{pmatrix}
= \begin{pmatrix}
2+0 & 4+0 \\
3+0 & 6+1 \\
\end{pmatrix}.
$$

Thus,

$$
BA=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

### 3. Comparison

Comparing corresponding entries:

$$
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
\neq
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

Hence, $AB\neq BA$.

### 4. Meaning of Noncommutativity

A binary operation $*$ is commutative if $x * y = y * x$ for all elements. Real numbers satisfy commutativity under ordinary multiplication ($ab = ba$).

In contrast, matrix multiplication is in general noncommutative: even when both products are defined and have the identical size, $AB$ and $BA$ are usually distinct matrices.

Geometrically, a matrix represents a linear transformation. Matrix multiplication corresponds to function composition:

$$
(AB)x = A(Bx).
$$

Here, $AB$ means first applying transformation $B$ and then applying transformation $A$. Conversely, $BA$ means applying $A$ first, then $B$. Because the sequential order of applying geometric operations (such as shears, rotations, and scalings) generally alters the final position of points in the plane, function composition is not commutative, and neither is matrix multiplication.
