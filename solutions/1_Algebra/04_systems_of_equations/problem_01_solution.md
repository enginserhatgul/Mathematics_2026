## Question

Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7
\end{cases}
$$

in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Solution

### 1. Matrix Form $Ax = b$

The linear system can be expressed compactly in matrix-vector notation as:

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}.
$$

### 2. Identification of Components

- **Coefficient Matrix ($A$):** The $3\times 3$ matrix formed by collecting the coefficients of the variables $x, y, z$ in order:

$$
A =
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}.
$$

- **Vector of Unknowns ($x$):** The $3\times 1$ column vector of variables:

$$
x =
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}.
$$

- **Right-Hand Side Vector ($b$):** The $3\times 1$ column vector containing the constants from the right-hand side of each equation:

$$
b =
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}.
$$

- **Augmented Matrix ($[A \mid b]$):** Combining the coefficient matrix and the constant vector:

$$
[A \mid b] =
\begin{pmatrix}
2 & -1 & 1 & \mid & 4 \\
1 & 3 & -2 & \mid & 1 \\
3 & 1 & 1 & \mid & 7 \\
\end{pmatrix}.
$$

### 3. Row-to-Equation Correspondence

By the definition of matrix-vector multiplication, the $i$-th entry of the product $Ax$ is obtained by computing the dot product of the $i$-th row of $A$ with the vector of unknowns $x$:

- **Row 1:** $(2, -1, 1) \cdot (x, y, z)^T = 2x - y + z = 4$ (Equation 1).
- **Row 2:** $(1, 3, -2) \cdot (x, y, z)^T = x + 3y - 2z = 1$ (Equation 2).
- **Row 3:** $(3, 1, 1) \cdot (x, y, z)^T = 3x + y + z = 7$ (Equation 3).

Each row of the matrix $A$ encodes the linear weights of the variables for one specific equation, while the corresponding entry of $b$ specifies the target value.
