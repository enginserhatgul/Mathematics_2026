## Question

Suppose that for a $3\times 3$ matrix $A$, $\det A = -4$. Compute

$\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).$

Justify each answer using the appropriate property.

## Solution

### 1. Computation of $\det(2A)$

**Property (Scalar Multiplication):** For any $n\times n$ matrix $M$ and scalar $c \in \mathbb{R}$, multiplying the matrix by $c$ scales each of its $n$ rows by $c$. By multilinearity of the determinant with respect to rows:

$\det(cM) = c^n \det M.$

Here, $A$ is a $3\times 3$ matrix ($n = 3$) and the scalar factor is $c = 2$:

$\det(2A) = 2^3 \det A = 8 \cdot (-4) = -32.$

### 2. Computation of $\det(A^T)$

**Property (Transposition):** The determinant of the transpose of any square matrix is identical to the determinant of the original matrix:

$\det(M^T) = \det M.$

This property holds because transposing a matrix interchanges its rows and columns, leaving the set of all diagonal products and their permutation signs in the Leibniz expansion completely unchanged.

Applying this property directly:

$\det(A^T) = \det A = -4.$

### 3. Computation of $\det(A^2)$

**Property (Multiplicativity of Determinants):** For any two square matrices $M$ and $N$ of the same size, the determinant of their product is the product of their determinants:

$\det(MN) = \det M \cdot \det N.$

Consequently, for any positive integer power $k$:

$\det(M^k) = (\det M)^k.$

For $k = 2$:

$\det(A^2) = \det(A \cdot A) = (\det A)^2 = (-4)^2 = 16.$

### 4. Computation of $\det(-A)$

**Property (Matrix Negation):** The matrix negation $-A$ is equivalent to scalar multiplication by $c = -1$:

$-A = (-1) A.$

Using the scalar multiplication property with $n = 3$ and $c = -1$:

$\det(-A) = (-1)^3 \det A = (-1) \cdot (-4) = 4.$

### 5. Summary Table

| Expression | Applicable Theoretical Property | Intermediate Step | Final Value |
|---|---|---|---|
| $\det(2A)$ | $\det(cA) = c^n \det A$ with $n=3, c=2$ | $2^3 \cdot (-4) = 8 \cdot (-4)$ | $-32$ |
| $\det(A^T)$ | $\det(A^T) = \det A$ | $\det A = -4$ | $-4$ |
| $\det(A^2)$ | $\det(A^k) = (\det A)^k$ with $k=2$ | $(-4)^2$ | $16$ |
| $\det(-A)$ | $\det(-A) = (-1)^n \det A$ with $n=3$ | $(-1)^3 \cdot (-4) = -1 \cdot (-4)$ | $4$ |
