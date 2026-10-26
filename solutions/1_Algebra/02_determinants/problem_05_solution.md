## Question

For

$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Solution

### 1. Behavior of the Determinant Under Elementary Row Operations

When using Gaussian elimination to compute determinants, the effect of each type of elementary row operation is as follows:

1. **Row Addition ($R_i \leftarrow R_i + c R_j$ with $i \neq j$):** The determinant remains **unchanged** ($\det \to \det$).
2. **Row Swap ($R_i \leftrightarrow R_j$):** The determinant **changes sign** ($\det \to -\det$).
3. **Row Scaling ($R_i \leftarrow c R_i$ with $c \neq 0$):** The determinant is **multiplied by $c$** ($\det \to c \det$).

Our goal is to systematically transform matrix $A$ into an upper triangular matrix using row addition operations so that the determinant value is preserved at every stage.

### 2. Step-by-Step Row Reduction

We start with:

$\det A = \begin{vmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{vmatrix}.$

#### Step 1: Eliminate the entry in position $(2,1)$

Apply the operation $R_2 \leftarrow R_2 - 2R_1$.

- New row 2 entries:
  - $2 - 2(1) = 0$
  - $1 - 2(2) = 1 - 4 = -3$
  - $0 - 2(3) = 0 - 6 = -6$
- **Determinant effect:** Unchanged (operation of type $R_i + c R_j$).

$\det A = \begin{vmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{vmatrix}.$

#### Step 2: Eliminate the entry in position $(3,1)$

Apply the operation $R_3 \leftarrow R_3 + R_1$.

- New row 3 entries:
  - $-1 + 1 = 0$
  - $4 + 2 = 6$
  - $2 + 3 = 5$
- **Determinant effect:** Unchanged (operation of type $R_i + c R_j$).

$\det A = \begin{vmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{vmatrix}.$

#### Step 3: Eliminate the entry in position $(3,2)$

Apply the operation $R_3 \leftarrow R_3 + 2R_2$.

- New row 3 entries:
  - $0 + 2(0) = 0$
  - $6 + 2(-3) = 6 - 6 = 0$
  - $5 + 2(-6) = 5 - 12 = -7$
- **Determinant effect:** Unchanged (operation of type $R_i + c R_j$).

$\det A = \begin{vmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{vmatrix}.$

### 3. Computation of the Determinant

The matrix is now in upper triangular form. Because each step involved only row addition operations, the determinant of the original matrix is equal to the product of the main diagonal entries of this triangular matrix:

$\det A = (1) \cdot (-3) \cdot (-7) = 21.$

### 4. Verification via Laplace Expansion along Column 1

We verify this result by expanding along the first column of the original matrix $A$:

$\det A = 1 \cdot \begin{vmatrix} 1 & 0 \\ 4 & 2 \end{vmatrix} - 2 \cdot \begin{vmatrix} 2 & 3 \\ 4 & 2 \end{vmatrix} + (-1) \cdot \begin{vmatrix} 2 & 3 \\ 1 & 0 \end{vmatrix}.$

Evaluating each $2\times 2$ minor:

- $\begin{vmatrix} 1 & 0 \\ 4 & 2 \end{vmatrix} = (1)(2) - (0)(4) = 2$
- $\begin{vmatrix} 2 & 3 \\ 4 & 2 \end{vmatrix} = (2)(2) - (3)(4) = 4 - 12 = -8$
- $\begin{vmatrix} 2 & 3 \\ 1 & 0 \end{vmatrix} = (2)(0) - (3)(1) = 0 - 3 = -3$

Combining the terms:

$\det A = 1(2) - 2(-8) - 1(-3) = 2 + 16 + 3 = 21.$

Both methods yield $\det A = 21$, confirming that the row operations preserved the determinant.
