## Question

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## Solution

### 1. Invertibility Check

Compute $\det A$:

$$
\det A = (1)(5) - (2)(3) = 5 - 6 = -1 \neq 0.
$$

Since $\det A \neq 0$, the inverse $A^{-1}$ exists.

### 2. Step-by-Step Gauss–Jordan Elimination

Set up the augmented matrix $[A \mid I]$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}.
$$

**Step 1:** Eliminate entry $(2,1)$ using $R_2 \leftarrow R_2 - 3R_1$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 - 3(1) & 5 - 3(2) & \mid & 0 - 3(1) & 1 - 3(0) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}.
$$

**Step 2:** Normalize the pivot in row 2 using $R_2 \leftarrow -R_2$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}.
$$

**Step 3:** Eliminate entry $(1,2)$ using $R_1 \leftarrow R_1 - 2R_2$:

$$
\begin{pmatrix}
1 - 2(0) & 2 - 2(1) & \mid & 1 - 2(3) & 0 - 2(-1) \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}.
$$

The left block is now the identity matrix $I$. Therefore, the right block is $A^{-1}$:

$$
A^{-1} =
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

### 3. Why Obtaining $I$ on the Left Gives $A^{-1}$ on the Right

Each elementary row operation corresponds to multiplying the matrix from the left by an elementary matrix $E_k$. Suppose a sequence of row operations $E_1, E_2, \dots, E_k$ reduces $A$ to the identity matrix:

$$
(E_k \cdots E_2 E_1) A = I.
$$

By definition of the inverse matrix, this product of elementary matrices is precisely $A^{-1}$:

$$
E_k \cdots E_2 E_1 = A^{-1}.
$$

Because the identical row operations are performed on the right block $I$:

$$
(E_k \cdots E_2 E_1) I = A^{-1} I = A^{-1}.
$$

Thus, the transformed right block is guaranteed to be $A^{-1}$.

### 4. Verification

$$
A A^{-1} =
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
= \begin{pmatrix}
1(-5) + 2(3) & 1(2) + 2(-1) \\
3(-5) + 5(3) & 3(2) + 5(-1) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$
