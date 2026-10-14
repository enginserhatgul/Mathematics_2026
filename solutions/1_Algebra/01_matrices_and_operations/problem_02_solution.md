## Question

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

## Solution

Both matrices $A$ and $B$ have size $2\times 2$, so their entries can be paired position by position.

### 1. Matrix Addition $A+B$

Add corresponding entries:

$$
A+B=
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5 \\
\end{pmatrix}
= \begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}.
$$

### 2. Matrix Subtraction $A-B$

Subtract corresponding entries:

$$
A-B=
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5 \\
\end{pmatrix}
= \begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}.
$$

### 3. Linear Combination $3A-2B$

Multiply $A$ by scalar $3$ and $B$ by scalar $2$:

$$
3A=
\begin{pmatrix}
3\cdot 1 & 3\cdot 2 \\
3\cdot(-1) & 3\cdot 3 \\
\end{pmatrix}
= \begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix},
$$

$$
2B=
\begin{pmatrix}
2\cdot 4 & 2\cdot(-2) \\
2\cdot 0 & 2\cdot 5 \\
\end{pmatrix}
= \begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}.
$$

Now subtract $2B$ from $3A$:

$$
3A-2B=
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10 \\
\end{pmatrix}
= \begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$

### 4. Verification

We check the addition result by reversing the operation:

$$
(A+B)-B=
\begin{pmatrix}
5-4 & 0-(-2) \\
-1-0 & 8-5 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix} = A.
$$

Similarly, for the linear combination:

$$
(3A-2B)+2B=
\begin{pmatrix}
-5+8 & 10+(-4) \\
-3+0 & -1+10 \\
\end{pmatrix}
= \begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix} = 3A.
$$

### 5. Why Sizes Must Agree

Matrix addition is defined componentwise by the formula:

$$
(A+B)_{ij}=a_{ij}+b_{ij}.
$$

This operation requires a bijective correspondence between the entry positions $(i,j)$ of matrix $A$ and matrix $B$. If two matrices differ in their row count or column count, there exist entries in one matrix with no corresponding counterpart in the other, making entrywise addition undefined.

