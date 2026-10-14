## Question

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## Solution

### 1. Matrix Sizes

The size of a matrix is given as $m\times n$, where $m$ is the number of rows and $n$ is the number of columns:

- Matrix $A$ has $2$ rows and $3$ columns, so its size is $2\times 3$.
- Matrix $B$ has $3$ rows and $2$ columns, so its size is $3\times 2$.

### 2. Matrix Entries

The notation $m_{ij}$ denotes the entry located in row $i$ and column $j$:

- $a_{12}$ is the entry in row $1$, column $2$ of $A$: $a_{12} = -1$.
- $a_{23}$ is the entry in row $2$, column $3$ of $A$: $a_{23} = 5$.
- $b_{21}$ is the entry in row $2$, column $1$ of $B$: $b_{21} = -2$.
- $b_{32}$ is the entry in row $3$, column $2$ of $B$: $b_{32} = 1$.

### 3. Row and Column Vectors

The second row of matrix $A$ forms the $1\times 3$ row vector:

$$
r_2(A)=
\begin{pmatrix}
0 & 4 & 5 \\
\end{pmatrix}.
$$

The first column of matrix $B$ forms the $3\times 1$ column vector:

$$
c_1(B)=
\begin{pmatrix}
1 \\
-2 \\
4 \\
\end{pmatrix}.
$$

### 4. Mathematical Explanation

Matrix dimensions define the shape of linear mappings between finite-dimensional vector spaces: an $m\times n$ matrix represents a linear transformation from $\mathbb R^n$ to $\mathbb R^m$. Each row vector contains $n$ entries (belonging to $\mathbb R^n$), while each column vector contains $m$ entries (belonging to $\mathbb R^m$). Specifically, the row vector $r_2(A)$ has $3$ components in $\mathbb R^3$, while the column vector $c_1(B)$ has $3$ components in $\mathbb R^3$.
