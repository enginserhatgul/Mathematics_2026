# Solutions: Determinants

This document contains step-by-step solutions for all exercises in `02_determinants_en.md`.

---

## Exercise 1. Determinant of a 2×2 Matrix

### Question

Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

### Solution

For any $2\times 2$ matrix

$$
M=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix},
$$

the determinant is defined by the formula:

$$
\det M = ad - bc.
$$

#### 1. Computation of the First Determinant

For the first matrix, identify $a = 3$, $b = -2$, $c = 5$, and $d = 4$:

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}
= (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22.
$$

#### 2. Computation of the Second Determinant

For the second matrix, identify $a = 1$, $b = 7$, $c = 2$, and $d = 14$:

$$
\det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}
= (1)(14) - (7)(2) = 14 - 14 = 0.
$$

#### 3. Invertibility Analysis

A square matrix is invertible if and only if its determinant is non-zero ($\det M \neq 0$).

- For the first matrix, $\det = 22 \neq 0$, so the matrix $\begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$ **is invertible**.
- For the second matrix, $\det = 0$, so the matrix $\begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$ **is not invertible** (singular).

In the second matrix, the second row is an exact scalar multiple of the first row ($R_2 = 2R_1$):

$$
(2, 14) = 2 \cdot (1, 7).
$$

Because the rows are linearly dependent, the matrix collapses 2-dimensional area to zero, meaning no inverse transformation exists.

---

## Exercise 2. Determinant of a 3×3 Matrix

### Question

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

### Solution

#### 1. Computation via Sarrus' Rule

Sarrus' rule states that for a $3\times 3$ matrix, the determinant is the sum of the three downward diagonal products minus the sum of the three upward anti-diagonal products:

$$
\det A = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}.
$$

Evaluating the positive diagonal products:

$$
\begin{aligned}
(1)(3)(5) &= 15, \\
(2)(4)(2) &= 16, \\
(-1)(0)(1) &= 0.
\end{aligned}
$$

Sum of positive products:

$$
15 + 16 + 0 = 31.
$$

Evaluating the negative anti-diagonal products:

$$
\begin{aligned}
(-1)(3)(2) &= -6, \\
(1)(4)(1) &= 4, \\
(2)(0)(5) &= 0.
\end{aligned}
$$

Sum of negative products:

$$
-6 + 4 + 0 = -2.
$$

Combining both parts:

$$
\det A = 31 - (-2) = 31 + 2 = 33.
$$

#### 2. Verification via Laplace Expansion along Row 1

Expanding along the first row:

$$
\det A = 1 \cdot
\begin{vmatrix}
3 & 4 \\
1 & 5 \\
\end{vmatrix}
- 2 \cdot
\begin{vmatrix}
0 & 4 \\
2 & 5 \\
\end{vmatrix}
+ (-1) \cdot
\begin{vmatrix}
0 & 3 \\
2 & 1 \\
\end{vmatrix}.
$$

Computing the $2\times 2$ minors:

$$
\begin{aligned}
\begin{vmatrix} 3 & 4 \\ 1 & 5 \end{vmatrix} &= (3)(5) - (4)(1) = 15 - 4 = 11, \\
\begin{vmatrix} 0 & 4 \\ 2 & 5 \end{vmatrix} &= (0)(5) - (4)(2) = 0 - 8 = -8, \\
\begin{vmatrix} 0 & 3 \\ 2 & 1 \end{vmatrix} &= (0)(1) - (3)(2) = 0 - 6 = -6.
\end{aligned}
$$

Substituting back:

$$
\det A = 1(11) - 2(-8) + (-1)(-6) = 11 + 16 + 6 = 33.
$$

Both methods yield $\det A = 33$, confirming the result.

---

## Exercise 3. Swapping Two Rows

### Question

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

### Solution

#### 1. Computation of $\det A$

Expanding along the first row:

$$
\det A = 1 \cdot
\begin{vmatrix}
3 & 1 \\
1 & 1 \\
\end{vmatrix}
- 2 \cdot
\begin{vmatrix}
0 & 1 \\
2 & 1 \\
\end{vmatrix}
+ 0 \cdot
\begin{vmatrix}
0 & 3 \\
2 & 1 \\
\end{vmatrix}.
$$

Evaluating the minors:

$$
\begin{aligned}
\begin{vmatrix} 3 & 1 \\ 1 & 1 \end{vmatrix} &= 3(1) - 1(1) = 2, \\
\begin{vmatrix} 0 & 1 \\ 2 & 1 \end{vmatrix} &= 0(1) - 1(2) = -2.
\end{aligned}
$$

Therefore:

$$
\det A = 1(2) - 2(-2) = 2 + 4 = 6.
$$

#### 2. Theoretical Prediction for $\det B$

Matrix $B$ is obtained from $A$ by swapping row 1 and row 2 ($R_1 \leftrightarrow R_2$):

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}.
$$

**Property:** Swapping two rows of a square matrix negates its determinant. Therefore:

$$
\det B = -\det A = -6.
$$

#### 3. Verification by Direct Calculation

Expanding $\det B$ along row 1:

$$
\det B = 0 \cdot
\begin{vmatrix}
2 & 0 \\
1 & 1 \\
\end{vmatrix}
- 3 \cdot
\begin{vmatrix}
1 & 0 \\
2 & 1 \\
\end{vmatrix}
+ 1 \cdot
\begin{vmatrix}
1 & 2 \\
2 & 1 \\
\end{vmatrix}.
$$

Evaluating the minors:

$$
\begin{aligned}
\begin{vmatrix} 1 & 0 \\ 2 & 1 \end{vmatrix} &= 1(1) - 0(2) = 1, \\
\begin{vmatrix} 1 & 2 \\ 2 & 1 \end{vmatrix} &= 1(1) - 2(2) = 1 - 4 = -3.
\end{aligned}
$$

Therefore:

$$
\det B = 0 - 3(1) + 1(-3) = -3 - 3 = -6.
$$

The direct calculation verifies that $\det B = -6 = -\det A$.

---

## Exercise 4. Triangular Matrix

### Question

Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

### Solution

#### 1. Rule for Triangular Matrices

The determinant of an upper triangular, lower triangular, or diagonal matrix equals the product of its main diagonal entries:

$$
\det T = \prod_{i=1}^n t_{ii} = t_{11} t_{22} \cdots t_{nn}.
$$

#### 2. Computation

The given matrix is upper triangular because all entries below the main diagonal are zero. Applying the rule:

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}
= (2)(-3)(7) = -42.
$$

#### 3. Explanation

Applying Laplace expansion along the first column, which has only one non-zero entry ($t_{11} = 2$):

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}
= 2 \cdot
\begin{vmatrix}
-3 & 5 \\
0 & 7 \\
\end{vmatrix}.
$$

Expanding the resulting $2\times 2$ minor along its first column:

$$
\begin{vmatrix}
-3 & 5 \\
0 & 7 \\
\end{vmatrix}
= (-3)(7) - (5)(0) = (-3)(7) = -21.
$$

Hence:

$$
\det = 2 \cdot (-3) \cdot 7 = -42.
$$

All off-diagonal terms vanish because every non-diagonal product in the determinant expansion contains at least one entry from below the main diagonal, which is zero.

---

## Exercise 5. Row Operations

### Question

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

### Solution

Row operations of the type $R_i \leftarrow R_i + c R_j$ ($i \neq j$) preserve the determinant: $\det(A_{\mathrm{new}}) = \det(A)$.

Starting with:

$$
\det A =
\begin{vmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{vmatrix}.
$$

**Step 1:** $R_2 \leftarrow R_2 - 2R_1$ (determinant unchanged):

$$
\begin{vmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{vmatrix}.
$$

**Step 2:** $R_3 \leftarrow R_3 + R_1$ (determinant unchanged):

$$
\begin{vmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{vmatrix}.
$$

**Step 3:** $R_3 \leftarrow R_3 + 2R_2$ (determinant unchanged):

$$
\begin{vmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{vmatrix}.
$$

The matrix is now upper triangular. The determinant is the product of the diagonal entries:

$$
\det A = (1)(-3)(-7) = 21.
$$

#### Verification via Expansion along Column 1

$$
\det A = 1 \cdot
\begin{vmatrix}
1 & 0 \\
4 & 2 \\
\end{vmatrix}
- 2 \cdot
\begin{vmatrix}
2 & 3 \\
4 & 2 \\
\end{vmatrix}
+ (-1) \cdot
\begin{vmatrix}
2 & 3 \\
1 & 0 \\
\end{vmatrix}.
$$

Evaluating minors:

$$
\begin{aligned}
\begin{vmatrix} 1 & 0 \\ 4 & 2 \end{vmatrix} &= 1(2) - 0(4) = 2, \\
\begin{vmatrix} 2 & 3 \\ 4 & 2 \end{vmatrix} &= 2(2) - 3(4) = 4 - 12 = -8, \\
\begin{vmatrix} 2 & 3 \\ 1 & 0 \end{vmatrix} &= 2(0) - 3(1) = -3.
\end{aligned}
$$

Combining:

$$
\det A = 1(2) - 2(-8) - 1(-3) = 2 + 16 + 3 = 21.
$$

---

## Exercise 6. Parameter and Invertibility

### Question

For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

### Solution

#### 1. Determinant Calculation

$$
\det A(t) = (t)(t) - (1)(2) = t^2 - 2.
$$

#### 2. Determining Non-Invertible Values

A matrix is not invertible if and only if its determinant is zero:

$$
\det A(t) = 0 \iff t^2 - 2 = 0 \iff t^2 = 2 \iff t = \sqrt{2} \quad \mathrm{or} \quad t = -\sqrt{2}.
$$

Thus, $A(t)$ is not invertible precisely when $t \in \{-\sqrt{2}, \sqrt{2}\}$.

#### 3. Geometric and Algebraic Meaning

When $t = \sqrt{2}$:

$$
A(\sqrt{2})=
\begin{pmatrix}
\sqrt{2} & 1 \\
2 & \sqrt{2} \\
\end{pmatrix}.
$$

The second row is a scalar multiple of the first: $R_2 = \sqrt{2} R_1$. The rows are linearly dependent, so the column vectors lie along a single line in $\mathbb{R}^2$. The linear map squashes $\mathbb{R}^2$ into a 1-dimensional line, so information is lost and the transformation cannot be inverted. The same holds for $t = -\sqrt{2}$ with $R_2 = -\sqrt{2} R_1$.

---

## Exercise 7. Using Properties Instead of Recomputing

### Question

Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

### Solution

#### 1. $\det(2A)$

**Property:** For an $n\times n$ matrix $M$ and scalar $c$, $\det(cM) = c^n \det M$.
Here $n = 3$ and $c = 2$:

$$
\det(2A) = 2^3 \det A = 8(-4) = -32.
$$

#### 2. $\det(A^T)$

**Property:** Transposition preserves the determinant: $\det(M^T) = \det M$.

$$
\det(A^T) = \det A = -4.
$$

#### 3. $\det(A^2)$

**Property:** Multiplicativity of the determinant: $\det(MN) = \det M \cdot \det N$.
For powers, $\det(M^k) = (\det M)^k$:

$$
\det(A^2) = (\det A)^2 = (-4)^2 = 16.
$$

#### 4. $\det(-A)$

**Property:** Negation is scalar multiplication by $c = -1$:

$$
\det(-A) = (-1)^3 \det A = -1(-4) = 4.
$$

---

## Exercise 8. Determinant of a Product

### Question

Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

### Solution

#### 1. $\det(AB)$ and $\det(BA)$

By the multiplicative property of determinants:

$$
\det(AB) = \det A \cdot \det B = (3)(-5) = -15.
$$

$$
\det(BA) = \det B \cdot \det A = (-5)(3) = -15.
$$

#### 2. Why $\det(AB) = \det(BA)$

Matrix multiplication is generally non-commutative ($AB \neq BA$). However, the determinant is a scalar in $\mathbb{R}$. Because multiplication of real numbers is commutative:

$$
\det A \cdot \det B = \det B \cdot \det A.
$$

Thus, $\det(AB) = \det(BA)$ always holds for square matrices of the same size.

#### 3. $\det(A^{-1}B)$

Since $\det A = 3 \neq 0$, $A$ is invertible and:

$$
\det(A^{-1}) = \frac{1}{\det A} = \frac{1}{3}.
$$

Applying the multiplicative property:

$$
\det(A^{-1}B) = \det(A^{-1}) \cdot \det B = \frac{1}{3} \cdot (-5) = -\frac{5}{3}.
$$

---

## Exercise 9. Area and the Determinant

### Question

The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

### Solution

#### 1. Area with Order $(u, v)$

Construct the matrix with columns $u$ and $v$:

$$
M = (u \mid v) =
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}.
$$

Compute the determinant:

$$
\det M = (3)(4) - (1)(1) = 12 - 1 = 11.
$$

The area of the parallelogram is the absolute value of the determinant:

$$
\mathrm{Area} = |11| = 11.
$$

#### 2. Reversed Order $(v, u)$

Construct the matrix with columns $v$ and $u$:

$$
N = (v \mid u) =
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

Compute the determinant:

$$
\det N = (1)(1) - (3)(4) = 1 - 12 = -11.
$$

#### 3. Comparison

- **What changes:** The sign of the determinant changes from $+11$ to $-11$. Swapping two columns negates the determinant, reflecting a reversal in orientation (from counterclockwise to clockwise).
- **What does not change:** The geometric area remains invariant: $\mathrm{Area} = |-11| = 11$.

---

## Exercise 10. Detecting Dependence

### Question

Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

### Solution

#### 1. Linear Dependence Between Rows

Let $R_1 = (1, 2, 3)$, $R_2 = (2, 4, 6)$, and $R_3 = (0, 1, 5)$. Comparing row 1 and row 2:

$$
R_2 = (2, 4, 6) = 2 \cdot (1, 2, 3) = 2 R_1.
$$

Row 2 is an exact scalar multiple of row 1, meaning the rows are linearly dependent:

$$
2 R_1 - R_2 + 0 R_3 = (0, 0, 0).
$$

#### 2. Effect on the Determinant

Applying the row operation $R_2 \leftarrow R_2 - 2R_1$, which preserves the determinant:

$$
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}.
$$

Because row 2 is entirely zero, Laplace expansion along row 2 gives $\det = 0$.

#### 3. Connection to Non-Invertibility

A matrix is invertible if and only if its rows form a linearly independent set (spanning $\mathbb{R}^3$). Because $R_2 = 2R_1$, the row space has dimension at most 2 ($\mathrm{rank} \le 2 < 3$). The linear map compresses 3D volume to zero, so it is not bijective and cannot have an inverse.

---

## Exercise 11. Shortening the Calculation with Row Operations

### Question

Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

### Solution

Row additions of the form $R_i \leftarrow R_i + c R_j$ ($i \neq j$) do not change the value of the determinant.

Starting with:

$$
D =
\begin{vmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{vmatrix}.
$$

**Step 1:** $R_2 \leftarrow R_2 - R_1$ (determinant unchanged):

$$
D =
\begin{vmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
1 & 4 & 6 \\
\end{vmatrix}.
$$

**Step 2:** $R_3 \leftarrow R_3 - R_1$ (determinant unchanged):

$$
D =
\begin{vmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{vmatrix}.
$$

**Step 3:** $R_3 \leftarrow R_3 - 2R_2$ (determinant unchanged):

$$
D =
\begin{vmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{vmatrix}.
$$

The matrix is now upper triangular. Its determinant is the product of its diagonal entries:

$$
D = (1)(1)(1) = 1.
$$

---

## Exercise 12. A Parameter Revealed by a Row Operation

### Question

For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

### Solution

#### 1. Perform the Row Operation

Applying $R_2 \leftarrow R_2 - 2R_1$, which preserves the determinant:

$$
\begin{aligned}
\det A(t) &=
\begin{vmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{vmatrix} \\
&=
\begin{vmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1 \\
\end{vmatrix}.
\end{aligned}
$$

#### 2. Compute the Determinant

Expanding along the first column:

$$
\det A(t) = 1 \cdot
\begin{vmatrix}
0 & t - 6 \\
1 & 1 \\
\end{vmatrix}
= 1 \cdot \bigl(0(1) - (t - 6)(1)\bigr) = -(t - 6) = 6 - t.
$$

#### 3. Invertibility Condition

The matrix is not invertible if and only if $\det A(t) = 0$:

$$
6 - t = 0 \iff t = 6.
$$

#### 4. Row Behavior at $t = 6$

When $t = 6$, row 2 of the original matrix becomes:

$$
R_2 = (2, 4, 6) = 2 \cdot (1, 2, 3) = 2 R_1.
$$

Row 2 is an exact scalar multiple of row 1. This linear dependence makes the rows linearly dependent and the matrix singular.

---

## Exercise 13. Determinant by Elimination

### Question

Compute the determinant

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

### Solution

Starting with:

$$
\det A =
\begin{vmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{vmatrix}.
$$

**Step 1:** $R_2 \leftarrow R_2 - 2R_1$.
- Effect: Determinant is unchanged.

$$
\det A =
\begin{vmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
1 & 0 & 2 \\
\end{vmatrix}.
$$

**Step 2:** $R_3 \leftarrow R_3 - R_1$.
- Effect: Determinant is unchanged.

$$
\det A =
\begin{vmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{vmatrix}.
$$

**Step 3:** $R_3 \leftarrow R_3 + 2R_2$.
- Effect: Determinant is unchanged.

$$
\det A =
\begin{vmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{vmatrix}.
$$

The matrix is now upper triangular. The determinant is the product of the diagonal entries:

$$
\det A = (1)(1)(1) = 1.
$$

#### Verification via Laplace Expansion along Row 3

$$
\det A = 1 \cdot
\begin{vmatrix}
2 & 3 \\
5 & 7 \\
\end{vmatrix}
- 0 + 2 \cdot
\begin{vmatrix}
1 & 2 \\
2 & 5 \\
\end{vmatrix}
= 1(14 - 15) + 2(5 - 4) = -1 + 2(1) = 1.
$$

---

## Exercise 14. A System of Equations and the Determinant

### Question

Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

### Solution

#### 1. Unique Solution Condition

A linear system $Ax = b$ with a square matrix $A$ has a unique solution for every right-hand side $b$ if and only if $\det A \neq 0$:

$$
\det A = (1)(4) - (2)(k) = 4 - 2k.
$$

Setting $\det A \neq 0$:

$$
4 - 2k \neq 0 \iff 2k \neq 4 \iff k \neq 2.
$$

Thus, the system has exactly one solution for every $b$ if and only if $k \neq 2$.

#### 2. The Case $k = 2$

When $k = 2$, the matrix is:

$$
A =
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}.
$$

The system $Ax = b$ corresponds to the equations:

$$
\begin{aligned}
x_1 + 2x_2 &= b_1, \\
2x_1 + 4x_2 &= b_2.
\end{aligned}
$$

Notice that the left-hand side of the second equation is twice the left-hand side of the first: $2(x_1 + 2x_2) = 2b_1$.

- **Infinitely many solutions:** Choose $b$ such that $b_2 = 2b_1$, for example $b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$.
  Then the second equation $2x_1 + 4x_2 = 2$ is equivalent to the first equation $x_1 + 2x_2 = 1$. The solutions form a 1-parameter family:
  $x_1 = 1 - 2s$, $x_2 = s$ for any $s \in \mathbb{R}$.

- **No solution:** Choose $b$ such that $b_2 \neq 2b_1$, for example $b = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$.
  Then $2(x_1 + 2x_2) = 2(1) = 2 \neq 1$, which is a contradiction ($2 = 1$). The system is inconsistent.

---

## Exercise 15. Combining Determinant Properties

### Question

Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

### Solution

#### 1. Step-by-Step Computation

Using the properties of determinants:

**Step 1: Multiplicative Property of Determinants**
The determinant of a product of square matrices equals the product of their individual determinants:

$$
\det(B^{-1} A^T B) = \det(B^{-1}) \cdot \det(A^T) \cdot \det(B).
$$

**Step 2: Determinant of an Inverse Matrix**
For any invertible matrix $B$:

$$
\det(B^{-1}) = \frac{1}{\det B}.
$$

**Step 3: Determinant of a Transpose**
Transposition preserves the determinant:

$$
\det(A^T) = \det A.
$$

**Step 4: Substitution and Evaluation**
Substituting these identities into the expression:

$$
\det(B^{-1} A^T B) = \frac{1}{\det B} \cdot \det A \cdot \det B.
$$

Using the commutativity of scalar multiplication in $\mathbb{R}$:

$$
\det(B^{-1} A^T B) = \left(\frac{1}{\det B} \cdot \det B\right) \cdot \det A = 1 \cdot \det A = \det A.
$$

Substituting the given value $\det A = -2$:

$$
\det(B^{-1} A^T B) = -2.
$$

#### 2. Why Factors Involving $B$ Cancel

The transformation $M \mapsto B^{-1} M B$ is a similarity transformation (conjugation). Determinants are similarity invariants: geometrically, $B$ changes the coordinate basis, scales volume by $\det B$, and then $B^{-1}$ scales volume by $\frac{1}{\det B}$, perfectly neutralizing the effect of $B$. Therefore, conjugation by any invertible matrix $B$ leaves the determinant unchanged.
