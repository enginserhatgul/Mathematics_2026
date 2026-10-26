## Question

Compute

$\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix},\qquad \det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}.$

Which matrix is invertible? Justify your answer.

## Solution

### 1. Definition and Formula for a 2×2 Determinant

For any $2\times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is defined by the formula:

$\det M = \begin{vmatrix} a & b \\ c & d \end{vmatrix} = ad - bc.$

This scalar value represents the signed area scaling factor of the linear mapping defined by the matrix.

### 2. Computation of the First Determinant

For the matrix $A = \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$, the coefficients are $a = 3$, $b = -2$, $c = 5$, and $d = 4$:

$\det A = \begin{vmatrix} 3 & -2 \\ 5 & 4 \end{vmatrix} = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22.$

### 3. Computation of the Second Determinant

For the matrix $B = \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$, the coefficients are $a = 1$, $b = 7$, $c = 2$, and $d = 14$:

$\det B = \begin{vmatrix} 1 & 7 \\ 2 & 14 \end{vmatrix} = (1)(14) - (7)(2) = 14 - 14 = 0.$

### 4. Determination of Invertibility

A square matrix is invertible (non-singular) if and only if its determinant is non-zero ($\det M \neq 0$). When the determinant is non-zero, the matrix transformation is bijective and an inverse matrix $M^{-1}$ exists.

- **Matrix $A$:** Since $\det A = 22 \neq 0$, the matrix $\begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$ **is invertible**.
  Its inverse can be directly constructed using the formula $A^{-1} = \frac{1}{\det A}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix} = \frac{1}{22}\begin{pmatrix} 4 & 2 \\ -5 & 3 \end{pmatrix}$.

- **Matrix $B$:** Since $\det B = 0$, the matrix $\begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$ **is not invertible** (it is singular).

### 5. Mathematical Explanation of Linear Dependence

The vanishing determinant of matrix $B$ occurs because its rows (and columns) are linearly dependent. Specifically:

$R_2 = (2, 14) = 2 \cdot (1, 7) = 2 R_1.$

Because row 2 is an exact scalar multiple of row 1, the row vectors span only a 1-dimensional subspace (a line) in $\mathbb{R}^2$ rather than the full 2-dimensional plane. Consequently, the linear transformation collapses 2-dimensional areas to zero, making it impossible to invert.
