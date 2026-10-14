## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

## Solution

Matrix $A$ has size $2\times 3$ and matrix $B$ has size $3\times 2$.

### 1. Transpose Matrices $A^T$ and $B^T$

The transpose of an $m\times n$ matrix is an $n\times m$ matrix formed by writing row $i$ as column $i$:

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix},\qquad B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}.
$$

### 2. Computation of $AB$

Since $A$ is $2\times 3$ and $B$ is $3\times 2$, the product $AB$ has size $2\times 2$:

$$
AB=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}.
$$

Compute each entry:

- Entry $(1,1)$: $1(1) + 2(2) + 3(-1) = 1 + 4 - 3 = 2$,
- Entry $(1,2)$: $1(0) + 2(1) + 3(3) = 0 + 2 + 9 = 11$,
- Entry $(2,1)$: $4(1) + 5(2) + 6(-1) = 4 + 10 - 6 = 8$,
- Entry $(2,2)$: $4(0) + 5(1) + 6(3) = 0 + 5 + 18 = 23$.

Thus,

$$
AB=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}.
$$

### 3. Computation of $(AB)^T$

Transposing $AB$ swaps its off-diagonal entries:

$$
(AB)^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

### 4. Computation of $B^T A^T$

Here $B^T$ has size $2\times 3$ and $A^T$ has size $3\times 2$, so their product is $2\times 2$:

$$
B^T A^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}.
$$

Compute each entry:

- Entry $(1,1)$: $1(1) + 2(2) + (-1)(3) = 1 + 4 - 3 = 2$,
- Entry $(1,2)$: $1(4) + 2(5) + (-1)(6) = 4 + 10 - 6 = 8$,
- Entry $(2,1)$: $0(1) + 1(2) + 3(3) = 0 + 2 + 9 = 11$,
- Entry $(2,2)$: $0(4) + 1(5) + 3(6) = 0 + 5 + 18 = 23$.

Thus,

$$
B^T A^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

### 5. Verification of the Transpose Product Identity

Comparing the two matrices:

$$
(AB)^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
= B^T A^T.
$$

The identity holds.

### 6. Order Reversal of Factors

The entry in row $i$, column $j$ of the product $AB$ is the dot product of row $i$ of $A$ and column $j$ of $B$:

$$
(AB)_{ij} = \sum_k a_{ik} b_{kj}.
$$

In the transposed matrix $(AB)^T$, this scalar is placed at position $(j, i)$.

In the product $B^T A^T$, the entry at $(j, i)$ is computed by taking the dot product of row $j$ of $B^T$ and column $i$ of $A^T$. Since row $j$ of $B^T$ is column $j$ of $B$, and column $i$ of $A^T$ is row $i$ of $A$:

$$
(B^T A^T)_{ji} = \sum_k (B^T)_{jk} (A^T)_{ki} = \sum_k b_{kj} a_{ik} = \sum_k a_{ik} b_{kj} = (AB)_{ij}.
$$

Furthermore, reversing the order is required for dimension compatibility: $A^T$ ($3\times 2$) multiplied by $B^T$ ($2\times 3$) would give a $3\times 3$ matrix, whereas $(AB)^T$ is $2\times 2$.
