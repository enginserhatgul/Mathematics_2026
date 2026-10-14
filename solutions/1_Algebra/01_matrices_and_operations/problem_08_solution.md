## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

We start with the initial matrix:

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

### 1. First Row Operation: $R_2\leftarrow R_2-2R_1$

Compute the new second row:

$$
R_2 - 2R_1 =
\begin{pmatrix}
2 - 2(1) & 4 - 2(2) & 1 - 2(-1) \\
\end{pmatrix}
= \begin{pmatrix}
0 & 0 & 3 \\
\end{pmatrix}.
$$

The resulting matrix is:

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

Reversing operation: $R_2\leftarrow R_2+2R_1$.

### 2. Second Row Operation: $R_3\leftarrow R_3+R_1$

Apply this operation to $A_1$, updating the third row:

$$
R_3 + R_1 =
\begin{pmatrix}
-1 + 1 & 1 + 2 & 3 + (-1) \\
\end{pmatrix}
= \begin{pmatrix}
0 & 3 & 2 \\
\end{pmatrix}.
$$

The resulting matrix is:

$$
A_2=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}.
$$

Reversing operation: $R_3\leftarrow R_3-R_1$.

### 3. Third Row Operation: Interchange $R_2$ and $R_3$

Swap the second and third rows of $A_2$:

The resulting matrix in upper-triangular echelon form is:

$$
A_3=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}.
$$

Reversing operation: Interchange $R_2$ and $R_3$ (an interchange operation is its own inverse).

### 4. Summary of Reversing Operations

To restore the original matrix $A$ from the final matrix $A_3$, apply the inverse operations in reverse order:

1. Interchange $R_2$ and $R_3$ (returns $A_2$).
2. $R_3\leftarrow R_3-R_1$ (returns $A_1$).
3. $R_2\leftarrow R_2+2R_1$ (returns $A$).

### 5. Mathematical Explanation

Elementary row operations represent invertible linear transformations of the row vectors. In matrix algebra, each row operation is equivalent to multiplying the matrix from the left by an elementary matrix $E$:

$$
A_3 = E_3 E_2 E_1 A.
$$

Since every elementary matrix is invertible:

$$
A = E_1^{-1} E_2^{-1} E_3^{-1} A_3.
$$

Because elementary row operations are invertible, they preserve the row space and guarantee that the solution set of any corresponding linear system of equations remains unchanged.
