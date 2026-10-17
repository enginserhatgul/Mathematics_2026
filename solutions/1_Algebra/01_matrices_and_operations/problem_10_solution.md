## Question

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Solution

We denote the column vectors of matrix $B$ by $b_1$ and $b_2$:

$$
b_1=
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},\qquad b_2=
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}.
$$

### 1. Computation of $Ab_1$ and $Ab_2$

Multiply matrix $A$ (size $2\times 3$) by column vector $b_1$ (size $3\times 1$):

$$
Ab_1=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}
= \begin{pmatrix}
1(1) + 2(-1) + 0(3) \\
0(1) + 1(-1) + 1(3) \\
\end{pmatrix}
= \begin{pmatrix}
1 - 2 + 0 \\
0 - 1 + 3 \\
\end{pmatrix}
= \begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}.
$$

Multiply matrix $A$ (size $2\times 3$) by column vector $b_2$ (size $3\times 1$):

$$
Ab_2=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
= \begin{pmatrix}
1(2) + 2(0) + 0(1) \\
0(2) + 1(0) + 1(1) \\
\end{pmatrix}
= \begin{pmatrix}
2 + 0 + 0 \\
0 + 0 + 1 \\
\end{pmatrix}
= \begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

### 2. Computation of Matrix Product $AB$

Matrix $A$ has size $2\times 3$ and matrix $B$ has size $3\times 2$, producing a $2\times 2$ matrix:

$$
AB=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Compute the entries row by column:

- Entry $(1,1)$: $1(1) + 2(-1) + 0(3) = 1 - 2 + 0 = -1$,
- Entry $(1,2)$: $1(2) + 2(0) + 0(1) = 2 + 0 + 0 = 2$,
- Entry $(2,1)$: $0(1) + 1(-1) + 1(3) = 0 - 1 + 3 = 2$,
- Entry $(2,2)$: $0(2) + 1(0) + 1(1) = 0 + 0 + 1 = 1$.

Thus,

$$
AB=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

### 3. Comparison of the Results

We compare the matrix product $AB$ with the column vectors $Ab_1$ and $Ab_2$:

The first column of $AB$ is:

$$
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix} = Ab_1.
$$

The second column of $AB$ is:

$$
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix} = Ab_2.
$$

Combining these columns confirms that the columns of $AB$ are precisely $Ab_1$ and $Ab_2$:

$$
AB=
\begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix}
= \begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

### 4. Mathematical Explanation

By definition of matrix multiplication, entry $(i,j)$ of the product $AB$ is computed by taking the dot product of row $i$ of matrix $A$ and column $j$ of matrix $B$:

$$
(AB)_{ij} = \sum_{k=1}^3 a_{ik} b_{kj}.
$$

For a fixed column index $j$, the entries $b_{1j}, b_{2j}, b_{3j}$ are exactly the components of the column vector $b_j$ of matrix $B$. Stacking the entries across all rows $i=1, 2$ forms the $j$-th column of $AB$:

$$
\begin{pmatrix}
(AB)_{1j} \\
(AB)_{2j} \\
\end{pmatrix}
= \begin{pmatrix}
\sum_{k=1}^3 a_{1k} b_{kj} \\
\sum_{k=1}^3 a_{2k} b_{kj} \\
\end{pmatrix}.
$$

By definition of matrix-vector multiplication, this resulting column vector is precisely the product $A b_j$:

$$
A b_j =
\begin{pmatrix}
a_{11} b_{1j} + a_{12} b_{2j} + a_{13} b_{3j} \\
a_{21} b_{1j} + a_{22} b_{2j} + a_{23} b_{3j} \\
\end{pmatrix}.
$$

Therefore, the columns of the matrix product $AB$ are exactly the transformed column vectors $Ab_1$ and $Ab_2$:

$$
AB =
\begin{pmatrix}
A b_1 & A b_2 \\
\end{pmatrix}.
$$

This explains why matrix multiplication can be carried out and understood column by column: the $j$-th column of $AB$ is the image of the $j$-th column of $B$ under the linear transformation represented by $A$.
