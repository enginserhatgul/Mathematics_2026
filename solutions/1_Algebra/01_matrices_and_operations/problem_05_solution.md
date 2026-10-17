## Question

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## Solution

### 1. Direct Computation of $Ax$

Matrix $A$ has size $2\times 2$ and vector $x$ has size $2\times 1$. The product $Ax$ is a $2\times 1$ vector.

Using the row-by-column dot product definition:

$$
\begin{aligned}
Ax &=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2(4) + (-1)(2) \\
1(4) + 3(2) \\
\end{pmatrix} \\
&= \begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix} \\
&= \begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
\end{aligned}
$$

### 2. Linear Combination of Columns

Denote the two columns of matrix $A$ by $a_1$ and $a_2$:

$$
a_1=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\qquad a_2=
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}.
$$

The coordinates of vector $x$ are $x_1=4$ and $x_2=2$.

Forming the linear combination of the columns with scalar weights $x_1$ and $x_2$:

$$
\begin{aligned}
x_1 a_1 + x_2 a_2 &= 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix} + 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
4\cdot 2 \\
4\cdot 1 \\
\end{pmatrix} +
\begin{pmatrix}
2\cdot(-1) \\
2\cdot 3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
8 \\
4 \\
\end{pmatrix} +
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix} \\
&= \begin{pmatrix}
8 + (-2) \\
4 + 6 \\
\end{pmatrix} \\
&= \begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
\end{aligned}
$$

### 3. Comparison and Explanation

Both perspectives yield the identical result:

$$
Ax=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

This equality illustrates the fundamental column view of matrix-vector multiplication:

$$
A x=
\begin{pmatrix}
a_1 & a_2 & \dots & a_n \\
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n \\
\end{pmatrix}
= \sum_{j=1}^n x_j a_j.
$$

In oral defense, this concept is central to linear algebra: the vector $Ax$ always lies in the column space (span of the columns) of matrix $A$. The vector $x$ specifies the coordinates of the output vector with respect to the generating column vectors.