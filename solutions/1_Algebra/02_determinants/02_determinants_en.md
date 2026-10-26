# Solutions: Determinants — Exercises 1–10

---

## Exercise 1. Determinant of a 2×2 Matrix

### Question

Compute

$\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix},\qquad \det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}.$

Which matrix is invertible? Justify your answer.

### Solution

The general formula for the determinant of a $2\times 2$ matrix is:

$\det \begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc.$

#### 1. First Matrix Calculation

For the matrix $\begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$, we identify $a = 3$, $b = -2$, $c = 5$, and $d = 4$:

$\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix} = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22.$

#### 2. Second Matrix Calculation

For the matrix $\begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$, we identify $a = 1$, $b = 7$, $c = 2$, and $d = 14$:

$\det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix} = (1)(14) - (7)(2) = 14 - 14 = 0.$

#### 3. Invertibility Analysis

A square matrix is invertible if and only if its determinant is non-zero ($\det M \neq 0$).

- For the first matrix, $\det = 22 \neq 0$, therefore the matrix $\begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$ **is invertible**.
- For the second matrix, $\det = 0$, therefore the matrix $\begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$ **is not invertible** (singular).

Notice that in the second matrix, the second row is an exact scalar multiple of the first row: $R_2 = 2 R_1$, since $2 \cdot (1, 7) = (2, 14)$. Hence, the rows are linearly dependent, which directly corresponds to a zero determinant and non-invertibility.

---

## Exercise 2. Determinant of a 3×3 Matrix

### Question

For

$A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

### Solution

#### 1. Sarrus' Rule (Diagonal Expansion)

For an arbitrary $3\times 3$ matrix $A = (a_{ij})$, Sarrus' rule computes the determinant by summing the products along the three main downward diagonals and subtracting the products along the three upward anti-diagonals:

$\det A = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}.$

Identifying the entries of $A$:
$a_{11} = 1,\ a_{12} = 2,\ a_{13} = -1$
$a_{21} = 0,\ a_{22} = 3,\ a_{23} = 4$
$a_{31} = 2,\ a_{32} = 1,\ a_{33} = 5$

**Three positive diagonal products:**

- First diagonal: $a_{11}a_{22}a_{33} = (1)(3)(5) = 15$
- Second diagonal: $a_{12}a_{23}a_{31} = (2)(4)(2) = 16$
- Third diagonal: $a_{13}a_{21}a_{32} = (-1)(0)(1) = 0$

Sum of positive terms: $15 + 16 + 0 = 31$.

**Three negative diagonal products:**

- First anti-diagonal: $a_{13}a_{22}a_{31} = (-1)(3)(2) = -6$
- Second anti-diagonal: $a_{11}a_{23}a_{32} = (1)(4)(1) = 4$
- Third anti-diagonal: $a_{12}a_{21}a_{33} = (2)(0)(5) = 0$

Sum of negative terms: $-6 + 4 + 0 = -2$.

Combining these according to Sarrus' rule:

$\det A = 31 - (-2) = 31 + 2 = 33.$

#### 2. Verification via Laplace Expansion along the First Row

We verify this calculation by expanding along the first row:

$\det A = a_{11} C_{11} + a_{12} C_{12} + a_{13} C_{13},$

where the cofactors are $C_{ij} = (-1)^{i+j} M_{ij}$:

- For $a_{11} = 1$: $C_{11} = +1 \cdot \det \begin{pmatrix} 3 & 4 \\ 1 & 5 \end{pmatrix} = (3)(5) - (4)(1) = 15 - 4 = 11$.
- For $a_{12} = 2$: $C_{12} = -1 \cdot \det \begin{pmatrix} 0 & 4 \\ 2 & 5 \end{pmatrix} = -1 \cdot \bigl((0)(5) - (4)(2)\bigr) = -1 \cdot (-8) = 8$.
- For $a_{13} = -1$: $C_{13} = +1 \cdot \det \begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix} = (0)(1) - (3)(2) = -6$.

Summing the terms:

$\det A = 1(11) + 2(-8 \cdot (-1)) + (-1)(-6) = 11 + 16 + 6 = 33.$

Both methods yield exactly $\det A = 33$, verifying the calculation.

---

## Exercise 3. Swapping Two Rows

### Question

For

$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$. First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

### Solution

#### 1. Computation of $\det A$

Using Sarrus' rule for $A$:

- Downward diagonals:
  - $(1)(3)(1) = 3$
  - $(2)(1)(2) = 4$
  - $(0)(0)(1) = 0$
  - Sum $= 3 + 4 + 0 = 7$.

- Upward diagonals:
  - $(0)(3)(2) = 0$
  - $(1)(1)(1) = 1$
  - $(2)(0)(1) = 0$
  - Sum $= 0 + 1 + 0 = 1$.

Subtracting the anti-diagonals:

$\det A = 7 - 1 = 6.$

#### 2. Prediction for $\det B$

Matrix $B$ is obtained from $A$ by swapping row 1 and row 2 ($R_1 \leftrightarrow R_2$):

$B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}.$

**Theoretical Property:** Interchanging any two rows (or two columns) of a matrix negates the determinant:

$\det B = -\det A = -6.$

#### 3. Verification of $\det B$ by Direct Calculation

Applying Sarrus' rule directly to matrix $B$:

- Downward diagonals:
  - $(0)(2)(1) = 0$
  - $(3)(0)(2) = 0$
  - $(1)(1)(1) = 1$
  - Sum $= 0 + 0 + 1 = 1$.

- Upward diagonals:
  - $(1)(2)(2) = 4$
  - $(0)(1)(1) = 0$
  - $(3)(1)(1) = 3$
  - Sum $= 4 + 0 + 3 = 7$.

Subtracting the anti-diagonals:

$\det B = 1 - 7 = -6.$

The direct computation confirms the theoretical prediction: $\det B = -6 = -\det A$.

---

## Exercise 4. Triangular Matrix

### Question

Without expanding the determinant, compute

$\det \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}.$

State the rule for an arbitrary triangular matrix and explain it using this example.

### Solution

#### 1. Direct Computation Using the Diagonal Rule

The given matrix is upper triangular because all entries strictly below the main diagonal are zero ($a_{21} = 0$, $a_{31} = 0$, $a_{32} = 0$).

**Rule:** The determinant of any triangular matrix (upper triangular, lower triangular, or diagonal) is simply the product of all entries on its main diagonal:

$\det T = \prod_{i=1}^n t_{ii} = t_{11} t_{22} \cdots t_{nn}.$

Applying this rule directly:

$\det \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix} = (2) \cdot (-3) \cdot (7) = -42.$

#### 2. Theoretical Explanation: Why Off-Diagonal Terms Vanish

To see why the off-diagonal entries vanish, consider Laplace expansion along the first column:

The first column contains only one non-zero entry, which is the pivot $a_{11} = 2$, while $a_{21} = 0$ and $a_{31} = 0$:

$\det \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix} = 2 \cdot \det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} - 0 \cdot \det \begin{pmatrix} 4 & 1 \\ 0 & 7 \end{pmatrix} + 0 \cdot \det \begin{pmatrix} 4 & 1 \\ -3 & 5 \end{pmatrix}.$

The remaining $2\times 2$ minor is itself an upper triangular matrix:

$\det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} = (-3)(7) - (5)(0) = -21.$

Multiplying by the leading element:

$\det = 2 \cdot (-21) = -42.$

In any general upper triangular matrix, every product in Sarrus' rule or the permutation expansion that contains an entry from above the diagonal must also select at least one entry from below the diagonal (which is zero). Consequently, every term in the expansion vanishes except the single term consisting of the main diagonal product $a_{11} a_{22} \cdots a_{nn}$.

---

## Exercise 5. Row Operations

### Question

For

$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

### Solution

#### 1. Key Rules Governing Row Operations on Determinants

- **Row Addition ($R_i \leftarrow R_i + c R_j$, $i \neq j$):** The determinant remains completely unchanged.
- **Row Swap ($R_i \leftrightarrow R_j$):** The determinant changes sign ($\det \to -\det$).
- **Row Scaling ($R_i \leftarrow c R_i$):** The determinant is scaled by $c$ ($\det \to c \det$).

#### 2. Systematic Reduction to Upper Triangular Form

We start with:

$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}.$

**Step 1: Eliminate $a_{21}$ using $R_2 \leftarrow R_2 - 2 R_1$.**
Adding a multiple of one row to another does not change the determinant:
New row 2: $(2 - 2(1),\ 1 - 2(2),\ 0 - 2(3)) = (0, -3, -6)$.

$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{pmatrix}.$

**Step 2: Eliminate $a_{31}$ using $R_3 \leftarrow R_3 + R_1$.**
This row addition also leaves the determinant unchanged:
New row 3: $(-1 + 1,\ 4 + 2,\ 2 + 3) = (0, 6, 5)$.

$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}.$

**Step 3: Eliminate $a_{32}$ using $R_3 \leftarrow R_3 + 2 R_2$.**
Notice that adding $2 \cdot (-3) = -6$ to $6$ produces $0$. This row addition preserves the determinant:
New row 3: $(0 + 2(0),\ 6 + 2(-3),\ 5 + 2(-6)) = (0, 0, -7)$.

$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}.$

#### 3. Evaluation of the Resulting Triangular Matrix

The matrix is now in upper triangular form. Since every operation performed was a row addition of the form $R_i \leftarrow R_i + c R_j$, the determinant never changed:

$\det A = (1) \cdot (-3) \cdot (-7) = 21.$

#### 4. Verification via Laplace Expansion along Column 1

Expanding along the first column of the original matrix $A$:

$\det A = 1 \cdot \det \begin{pmatrix} 1 & 0 \\ 4 & 2 \end{pmatrix} - 2 \cdot \det \begin{pmatrix} 2 & 3 \\ 4 & 2 \end{pmatrix} + (-1) \cdot \det \begin{pmatrix} 2 & 3 \\ 1 & 0 \end{pmatrix}.$

Evaluating the $2\times 2$ determinants:

- $\det \begin{pmatrix} 1 & 0 \\ 4 & 2 \end{pmatrix} = (1)(2) - (0)(4) = 2$
- $\det \begin{pmatrix} 2 & 3 \\ 4 & 2 \end{pmatrix} = (2)(2) - (3)(4) = 4 - 12 = -8$
- $\det \begin{pmatrix} 2 & 3 \\ 1 & 0 \end{pmatrix} = (2)(0) - (3)(1) = -3$

Combining:

$\det A = 1(2) - 2(-8) - 1(-3) = 2 + 16 + 3 = 21.$

Both methods yield $\det A = 21$.

---

## Exercise 6. Parameter and Invertibility

### Question

For

$A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

### Solution

#### 1. Characteristic Determinant Expression

Compute the determinant of $A(t)$ as a function of the real parameter $t$:

$\det A(t) = (t)(t) - (1)(2) = t^2 - 2.$

#### 2. Finding Non-Invertible Parameter Values

A square matrix is not invertible (singular) if and only if its determinant is zero:

$\det A(t) = 0 \iff t^2 - 2 = 0 \iff t^2 = 2 \iff t = \sqrt{2} \quad \mathrm{or} \quad t = -\sqrt{2}.$

#### 3. Geometric and Algebraic Meaning of the Singular Cases

- **Case $t = \sqrt{2}$:**
  The matrix becomes:
  $A(\sqrt{2}) = \begin{pmatrix} \sqrt{2} & 1 \\ 2 & \sqrt{2} \end{pmatrix}.$
  Comparing the rows, row 2 is a multiple of row 1:
  $R_2 = (2, \sqrt{2}) = \sqrt{2} \cdot (\sqrt{2}, 1) = \sqrt{2} R_1.$
  Since the rows are collinear, the rows and columns span only a 1-dimensional line instead of the entire plane $\mathbb{R}^2$. The linear map collapses area to zero, meaning no inverse map exists.

- **Case $t = -\sqrt{2}$:**
  The matrix becomes:
  $A(-\sqrt{2}) = \begin{pmatrix} -\sqrt{2} & 1 \\ 2 & -\sqrt{2} \end{pmatrix}.$
  Here $R_2 = (2, -\sqrt{2}) = -\sqrt{2} \cdot (-\sqrt{2}, 1) = -\sqrt{2} R_1.$
  The rows are again linearly dependent, producing $\det = 0$.

**Conclusion:** The matrix $A(t)$ is not invertible precisely for $t \in \{-\sqrt{2}, \sqrt{2}\}$. For all other real values $t \notin \{-\sqrt{2}, \sqrt{2}\}$, $\det A(t) \neq 0$ and $A(t)$ is invertible.

---

## Exercise 7. Using Properties Instead of Recomputing

### Question

Suppose that for a $3\times3$ matrix $A$, $\det A = -4$. Compute

$\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).$

Justify each answer using the appropriate property.

### Solution

#### 1. Computation of $\det(2A)$

**Property:** For an $n\times n$ matrix $M$ and scalar $c$, scaling the matrix scales each of its $n$ rows by $c$. Therefore:

$\det(cM) = c^n \det M.$

Here $A$ is of size $n = 3$ and $c = 2$:

$\det(2A) = 2^3 \det A = 8 \cdot (-4) = -32.$

#### 2. Computation of $\det(A^T)$

**Property:** Transposition swaps rows with columns, leaving all term products and permutation signs in the determinant definition unchanged:

$\det(M^T) = \det M.$

Applying this directly:

$\det(A^T) = \det A = -4.$

#### 3. Computation of $\det(A^2)$

**Property (Multiplicativity):** The determinant of a product of square matrices equals the product of their individual determinants:

$\det(MN) = \det M \cdot \det N.$

For powers of a matrix: $\det(M^k) = (\det M)^k$. Here $k = 2$:

$\det(A^2) = \det(A \cdot A) = (\det A)^2 = (-4)^2 = 16.$

#### 4. Computation of $\det(-A)$

**Property:** The negation $-A$ is equivalent to scalar multiplication by $c = -1$. For an $n = 3$ matrix:

$\det(-A) = (-1)^3 \det A = -1 \cdot \det A = -1 \cdot (-4) = 4.$

#### Summary Table

| Expression | Applicable Theoretical Property | Value |
|---|---|---|
| $\det(2A)$ | $\det(cA) = c^n \det A$ with $n=3, c=2$ | $-32$ |
| $\det(A^T)$ | $\det(A^T) = \det A$ | $-4$ |
| $\det(A^2)$ | $\det(A^2) = (\det A)^2$ | $16$ |
| $\det(-A)$ | $\det(-A) = (-1)^n \det A$ with $n=3$ | $4$ |

---

## Exercise 8. Determinant of a Matrix Product

### Question

Let $A, B$ be square matrices such that $\det A = 3$ and $\det B = -5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB \neq BA$.

### Solution

#### 1. Computation of $\det(AB)$ and $\det(BA)$

By the multiplicative property of determinants:

$\det(AB) = \det A \cdot \det B = (3) \cdot (-5) = -15.$

Similarly, for the reverse product:

$\det(BA) = \det B \cdot \det A = (-5) \cdot (3) = -15.$

#### 2. Why $\det(AB) = \det(BA)$ While $AB \neq BA$

While matrix multiplication is generally **non-commutative** ($AB \neq BA$), the determinant maps each matrix to a scalar in the underlying field $\mathbb{R}$. Scalar multiplication in $\mathbb{R}$ is strictly commutative:

$\det(AB) = \det A \cdot \det B = \det B \cdot \det A = \det(BA).$

Thus, even though the matrix transformations $AB$ and $BA$ represent different geometric mappings applied in opposite orders, the total volume scaling factor of both composite transformations is identical.

#### 3. Computation of $\det(A^{-1}B)$

First, we verify whether $A^{-1}$ exists. Since $\det A = 3 \neq 0$, matrix $A$ is non-singular and its inverse $A^{-1}$ is guaranteed to exist.

Using the property of the determinant of an inverse matrix:

$\det(A \cdot A^{-1}) = \det(I) = 1 \implies \det(A^{-1}) = \frac{1}{\det A} = \frac{1}{3}.$

Now applying the multiplicative property to $A^{-1}B$:

$\det(A^{-1}B) = \det(A^{-1}) \cdot \det B = \left(\frac{1}{3}\right) \cdot (-5) = -\frac{5}{3}.$

---

## Exercise 9. Geometric Interpretation of the 2×2 Determinant (Area)

### Question

The vectors

$u = \begin{pmatrix} 3 \\ 1 \end{pmatrix},\qquad v = \begin{pmatrix} 1 \\ 4 \end{pmatrix}$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

### Solution

#### 1. Area Computation via Matrix Determinant

Let matrix $M = (u \mid v)$ have the vectors $u$ and $v$ as its columns:

$M = \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix}.$

Compute the determinant:

$\det M = \det \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix} = (3)(4) - (1)(1) = 12 - 1 = 11.$

The geometric area of the parallelogram spanned by $u$ and $v$ in $\mathbb{R}^2$ equals the absolute value of the determinant:

$\mathrm{Area}(P) = |\det(u \mid v)| = |11| = 11.$

#### 2. Reversing the Order of Vectors

Construct the matrix with the vectors in reversed order, $N = (v \mid u)$:

$N = \begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix}.$

Compute its determinant:

$\det N = \det \begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix} = (1)(1) - (3)(4) = 1 - 12 = -11.$

#### 3. What Changes vs. What Does Not Change

- **What changes:** The **sign of the determinant** changes from $+11$ to $-11$. This sign change directly reflects the change in **orientation**:
  - The ordered pair $(u, v)$ forms a positively oriented (counterclockwise) system: rotating vector $u$ towards vector $v$ passes through the shortest angle in the counterclockwise direction.
  - The ordered pair $(v, u)$ forms a negatively oriented (clockwise) system.
- **What does not change:** The **geometric area** of the parallelogram remains invariant:
  $\mathrm{Area} = |-11| = 11.$
  Area is an unsigned geometric measure of surface, whereas the determinant is an **oriented area**.

---

## Exercise 10. Singular Matrices, Linear Dependence, and Characteristic Parameter

### Question

Without carrying out a full determinant calculation, explain why

$\det \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix} = 0.$

Identify a specific dependence between the rows and connect it with non-invertibility of the matrix. Furthermore, demonstrate how a determinant with an unknown parameter $\lambda$ determines non-invertibility by solving $\det(A - \lambda I) = 0$ for $A = \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}$.

### Solution

#### 1. Detecting Linear Dependence in the Given 3×3 Matrix

Let the rows of the matrix be denoted by $R_1, R_2, R_3$:

$R_1 = (1, 2, 3),\qquad R_2 = (2, 4, 6),\qquad R_3 = (0, 1, 5).$

Inspecting the entries of $R_1$ and $R_2$:

$R_2 = (2, 4, 6) = 2 \cdot (1, 2, 3) = 2 R_1.$

Row 2 is an exact scalar multiple of row 1. Thus, the linear combination:

$2 R_1 - R_2 + 0 R_3 = (0, 0, 0)$

proves that the set of row vectors $\{R_1, R_2, R_3\}$ is linearly dependent.

#### 2. Theoretical Consequence on the Determinant

Performing the elementary row operation $R_2 \leftarrow R_2 - 2 R_1$ does not alter the determinant:

$\det \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix} = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{pmatrix}.$

Expanding along the second row (which consists entirely of zeros):

$\det = 0 \cdot C_{21} + 0 \cdot C_{22} + 0 \cdot C_{23} = 0.$

Hence, the determinant is identically zero without requiring any lengthy computation.

#### 3. Connection with Non-Invertibility

A square matrix represents a bijective linear operator if and only if its rows form a basis of $\mathbb{R}^n$. Because $R_2 = 2 R_1$, the subspace spanned by the three rows has dimension at most $2$ ($\mathrm{rank} \le 2$). The matrix maps $\mathbb{R}^3$ into a flattened 2-dimensional plane, collapsing 3-dimensional volume to zero. Because information along the collapsed direction is lost, no inverse mapping exists. Therefore, $\det M = 0$ is the definitive algebraic test for non-invertibility.

#### 4. Characteristic Parameter Problem: $\det(A - \lambda I) = 0$

To illustrate how setting a parameter-dependent determinant to zero finds singular configurations (eigenvalues), consider the $2\times 2$ matrix formed by the first two rows and columns:

$A = \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}.$

Form the matrix $A - \lambda I$:

$A - \lambda I = \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix} - \begin{pmatrix} \lambda & 0 \\ 0 & \lambda \end{pmatrix} = \begin{pmatrix} 1 - \lambda & 2 \\ 2 & 4 - \lambda \end{pmatrix}.$

Compute its determinant:

$\det(A - \lambda I) = (1 - \lambda)(4 - \lambda) - (2)(2) = (4 - 5\lambda + \lambda^2) - 4 = \lambda^2 - 5\lambda = \lambda(\lambda - 5).$

Setting the determinant to zero to find the parameter values where $A - \lambda I$ is non-invertible:

$\lambda(\lambda - 5) = 0 \implies \lambda = 0 \quad \mathrm{or} \quad \lambda = 5.$

- For $\lambda = 0$, $A - 0I = A = \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}$, which has $\det = 1(4) - 2(2) = 0$, confirming that $A$ itself is singular.
- For $\lambda = 5$, $A - 5I = \begin{pmatrix} -4 & 2 \\ 2 & -1 \end{pmatrix}$, which has $\det = (-4)(-1) - (2)(2) = 4 - 4 = 0$, also making $A - 5I$ singular.
