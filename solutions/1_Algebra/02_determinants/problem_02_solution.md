## Question

For

$A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## Solution

### 1. Statement of Sarrus' Rule

For any $3\times 3$ matrix, Sarrus' rule provides a direct computational scheme by adding the products of the three main diagonals and subtracting the products of the three anti-diagonals:

$\det A = \begin{vmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{vmatrix} = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}.$

Here the matrix is:

$A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}.$

### 2. Computation of the Diagonal Products

**Three downward (positive) products:**

1. Main diagonal: $(1) \cdot (3) \cdot (5) = 15$
2. Second diagonal: $(2) \cdot (4) \cdot (2) = 16$
3. Third diagonal: $(-1) \cdot (0) \cdot (1) = 0$

Sum of positive terms:

$P = 15 + 16 + 0 = 31.$

**Three upward (negative) products:**

1. First anti-diagonal: $(-1) \cdot (3) \cdot (2) = -6$
2. Second anti-diagonal: $(1) \cdot (4) \cdot (1) = 4$
3. Third anti-diagonal: $(2) \cdot (0) \cdot (5) = 0$

Sum of negative terms:

$N = -6 + 4 + 0 = -2.$

### 3. Final Determinant Value

Subtracting the anti-diagonal sum from the main diagonal sum:

$\det A = P - N = 31 - (-2) = 31 + 2 = 33.$

### 4. Verification via Laplace Expansion along the First Row

We verify this result using cofactor expansion along the first row ($i = 1$). The signs follow the alternating pattern $(-1)^{1+j}$:

$\det A = a_{11} \begin{vmatrix} 3 & 4 \\ 1 & 5 \end{vmatrix} - a_{12} \begin{vmatrix} 0 & 4 \\ 2 & 5 \end{vmatrix} + a_{13} \begin{vmatrix} 0 & 3 \\ 2 & 1 \end{vmatrix}.$

Evaluating each $2\times 2$ minor determinant:

- First minor: $\begin{vmatrix} 3 & 4 \\ 1 & 5 \end{vmatrix} = (3)(5) - (4)(1) = 15 - 4 = 11$
- Second minor: $\begin{vmatrix} 0 & 4 \\ 2 & 5 \end{vmatrix} = (0)(5) - (4)(2) = 0 - 8 = -8$
- Third minor: $\begin{vmatrix} 0 & 3 \\ 2 & 1 \end{vmatrix} = (0)(1) - (3)(2) = 0 - 6 = -6$

Substituting these minors back into the expansion:

$\det A = 1(11) - 2(-8) + (-1)(-6) = 11 + 16 + 6 = 33.$

Both independent methods confirm that $\det A = 33$.
