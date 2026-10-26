# Solutions: Determinants — Exercises 1–10

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

The formula for a 2×2 determinant is $\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$.

**First matrix:**

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}
= (3)(4) - (-2)(5) = 12 + 10 = 22.
$$

**Second matrix:**

$$
\det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}
= (1)(14) - (7)(2) = 14 - 14 = 0.
$$

**Invertibility:** A square matrix is invertible if and only if its determinant is non-zero.

- The first matrix has $\det = 22 \neq 0$, so it **is invertible**.
- The second matrix has $\det = 0$, so it **is not invertible**.

For the second matrix, notice that row 2 is exactly twice row 1 (since $2 \cdot (1,7) = (2,14)$), making the rows linearly dependent. A matrix with linearly dependent rows cannot be invertible.

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

compute $\det A$ using Sarrus' rule, then perform one simple check using a property of the determinant.

### Solution

**Sarrus' rule** for a 3×3 matrix $A = (a_{ij})$ is:

$$
\det A = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32}
- a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}.
$$

Identifying entries: $a_{11}=1$, $a_{12}=2$, $a_{13}=-1$, $a_{21}=0$, $a_{22}=3$, $a_{23}=4$, $a_{31}=2$, $a_{32}=1$, $a_{33}=5$.

**Positive diagonals:**

$$
\begin{aligned}
&a_{11}a_{22}a_{33} = (1)(3)(5) = 15, \\
&a_{12}a_{23}a_{31} = (2)(4)(2) = 16, \\
&a_{13}a_{21}a_{32} = (-1)(0)(1) = 0.
\end{aligned}
$$

**Negative diagonals:**

$$
\begin{aligned}
&a_{13}a_{22}a_{31} = (-1)(3)(2) = -6, \\
&a_{11}a_{23}a_{32} = (1)(4)(1) = 4, \\
&a_{12}a_{21}a_{33} = (2)(0)(5) = 0.
\end{aligned}
$$

Assembling:

$$
\det A = (15 + 16 + 0) - (-6 + 4 + 0) = 31 - (-2) = 31 + 2 = 33.
$$

**Check via cofactor expansion along row 1:**

$$
\det A = 1 \cdot \det\begin{pmatrix} 3 & 4 \\ 1 & 5 \end{pmatrix}
- 2 \cdot \det\begin{pmatrix} 0 & 4 \\ 2 & 5 \end{pmatrix}
+ (-1) \cdot \det\begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix}.
$$

Computing the 2×2 minors:

$$
\begin{aligned}
&\det\begin{pmatrix} 3 & 4 \\ 1 & 5 \end{pmatrix} = 15 - 4 = 11, \\
&\det\begin{pmatrix} 0 & 4 \\ 2 & 5 \end{pmatrix} = 0 - 8 = -8, \\
&\det\begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix} = 0 - 6 = -6.
\end{aligned}
$$

Therefore:

$$
\det A = 1(11) - 2(-8) + (-1)(-6) = 11 + 16 + 6 = 33. \checkmark
$$

Both methods confirm $\det A = 33$.

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

compute $\det A$. Form matrix $B$ by swapping rows 1 and 2 of $A$, predict $\det B$ using a determinant property, then verify by direct calculation.

### Solution

**Computing $\det A$ via Sarrus' rule:**

Entries: $a_{11}=1$, $a_{12}=2$, $a_{13}=0$, $a_{21}=0$, $a_{22}=3$, $a_{23}=1$, $a_{31}=2$, $a_{32}=1$, $a_{33}=1$.

Positive diagonals:

$$
\begin{aligned}
&(1)(3)(1) = 3, \\
&(2)(1)(2) = 4, \\
&(0)(0)(1) = 0.
\end{aligned}
$$

Negative diagonals:

$$
\begin{aligned}
&(0)(3)(2) = 0, \\
&(1)(1)(1) = 1, \\
&(2)(0)(1) = 0.
\end{aligned}
$$

$$
\det A = (3 + 4 + 0) - (0 + 1 + 0) = 7 - 1 = 6.
$$

**Prediction for $\det B$:** The determinant property states that swapping any two rows reverses the sign of the determinant. Therefore:

$$
\det B = -\det A = -6.
$$

**Verification:** Swapping rows 1 and 2 of $A$ gives

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}.
$$

Applying Sarrus' rule to $B$ with entries $b_{11}=0$, $b_{12}=3$, $b_{13}=1$, $b_{21}=1$, $b_{22}=2$, $b_{23}=0$, $b_{31}=2$, $b_{32}=1$, $b_{33}=1$:

Positive diagonals:

$$
\begin{aligned}
&(0)(2)(1) = 0, \\
&(3)(0)(2) = 0, \\
&(1)(1)(1) = 1.
\end{aligned}
$$

Negative diagonals:

$$
\begin{aligned}
&(1)(2)(2) = 4, \\
&(0)(1)(1) = 0, \\
&(3)(1)(1) = 3.
\end{aligned}
$$

$$
\det B = (0 + 0 + 1) - (4 + 0 + 3) = 1 - 7 = -6. \checkmark
$$

The prediction is confirmed: $\det B = -6 = -\det A$.

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

**Rule:** The determinant of any upper or lower triangular matrix (and in particular any diagonal matrix) equals the product of its diagonal entries.

For this upper triangular matrix the diagonal entries are $2$, $-3$, and $7$, so:

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}
= 2 \cdot (-3) \cdot 7 = -42.
$$

**Why off-diagonal terms vanish:** Apply cofactor expansion along the first column. The only non-zero entry in column 1 below the diagonal is $a_{11} = 2$ (both $a_{21}$ and $a_{31}$ are zero). This reduces the problem to a 2×2 upper triangular minor:

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}
= 2 \cdot \det\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}
= 2 \cdot \bigl((-3)(7) - (5)(0)\bigr)
= 2 \cdot (-21)
= -42.
$$

For the 2×2 minor, again only the diagonal term survives: $(-3)(7) = -21$. In general, for an $n \times n$ triangular matrix each cofactor expansion along the first column eliminates all off-diagonal entries, leaving only the product of the diagonal.

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

find $\det A$ by simplifying the matrix with row operations, indicating at each step how the determinant changes.

### Solution

**Key rule:** Adding a multiple of one row to another row does **not** change the determinant.

**Step 1:** $R_2 \leftarrow R_2 - 2R_1$ (determinant unchanged):

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

**Step 2:** $R_3 \leftarrow R_3 + R_1$ (determinant unchanged):

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

**Step 3:** $R_3 \leftarrow R_3 + 2R_2$ (determinant unchanged):

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}
$$

The result is upper triangular. Since no row swaps or row scalings were performed, $\det A$ equals the product of the diagonal entries:

$$
\det A = (1)(-3)(-7) = 21.
$$

**Verification via cofactor expansion along column 1 of the original matrix:**

$$
\det A = 1 \cdot \det\begin{pmatrix} 1 & 0 \\ 4 & 2 \end{pmatrix}
- 2 \cdot \det\begin{pmatrix} 2 & 3 \\ 4 & 2 \end{pmatrix}
+ (-1) \cdot \det\begin{pmatrix} 2 & 3 \\ 1 & 0 \end{pmatrix}.
$$

$$
\begin{aligned}
&\det\begin{pmatrix} 1 & 0 \\ 4 & 2 \end{pmatrix} = 2 - 0 = 2, \\
&\det\begin{pmatrix} 2 & 3 \\ 4 & 2 \end{pmatrix} = 4 - 12 = -8, \\
&\det\begin{pmatrix} 2 & 3 \\ 1 & 0 \end{pmatrix} = 0 - 3 = -3.
\end{aligned}
$$

$$
\det A = 1(2) - 2(-8) + (-1)(-3) = 2 + 16 + 3 = 21. \checkmark
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

find all values of $t$ for which the matrix is not invertible. Explain how the answer relates to the determinant being zero.

### Solution

Compute the determinant:

$$
\det A(t) = t \cdot t - 1 \cdot 2 = t^2 - 2.
$$

A matrix is not invertible if and only if its determinant equals zero. Setting $\det A(t) = 0$:

$$
t^2 - 2 = 0 \implies t^2 = 2 \implies t = \sqrt{2} \quad \mathrm{or} \quad t = -\sqrt{2}.
$$

**Conclusion:** $A(t)$ is not invertible exactly when $t = \sqrt{2}$ or $t = -\sqrt{2}$.

**Explanation:** When $t = \sqrt{2}$, the matrix becomes

$$
A(\sqrt{2})=
\begin{pmatrix}
\sqrt{2} & 1 \\
2 & \sqrt{2} \\
\end{pmatrix}.
$$

Row 2 equals $\sqrt{2}$ times row 1 (since $\sqrt{2} \cdot (\sqrt{2}, 1) = (2, \sqrt{2})$), so the rows are linearly dependent and the matrix is singular. The same reasoning applies for $t = -\sqrt{2}$. For all other values of $t$, the determinant is non-zero and the matrix is invertible.

---

## Exercise 7. Using Properties Instead of Recomputing

### Question

Suppose that for a $3\times3$ matrix $A$, $\det A = -4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

### Solution

**Property 1 — Scalar multiple:** If $A$ is $n\times n$, then $\det(cA) = c^n \det A$.

$$
\det(2A) = 2^3 \det A = 8 \cdot (-4) = -32.
$$

**Property 2 — Transpose:** $\det(A^T) = \det A$ for any square matrix.

$$
\det(A^T) = \det A = -4.
$$

**Property 3 — Multiplicative property:** $\det(AB) = \det A \cdot \det B$.

$$
\det(A^2) = \det(A \cdot A) = \det A \cdot \det A = (-4)(-4) = 16.
$$

**Property 4 — Negation is a scalar multiple with $c = -1$, $n = 3$:**

$$
\det(-A) = (-1)^3 \det A = -1 \cdot (-4) = 4.
$$

**Summary:**

| Expression | Value |
|------------|-------|
| $\det(2A)$ | $-32$ |
| $\det(A^T)$ | $-4$ |
| $\det(A^2)$ | $16$ |
| $\det(-A)$ | $4$ |

---

## Exercise 8. Determinant of a Product

### Question

Let $A$ and $B$ be square matrices with $\det A = 3$ and $\det B = -5$. Compute $\det(AB)$, $\det(BA)$, and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though generally $AB \neq BA$.

### Solution

**$\det(AB)$:** By the multiplicative property $\det(AB) = \det A \cdot \det B$:

$$
\det(AB) = 3 \cdot (-5) = -15.
$$

**$\det(BA)$:** Applying the same property:

$$
\det(BA) = \det B \cdot \det A = (-5) \cdot 3 = -15.
$$

**Why $\det(AB) = \det(BA)$:** Real numbers are commutative under multiplication, so $\det A \cdot \det B = \det B \cdot \det A$ regardless of whether $AB = BA$ as matrices. The determinant of a product depends only on the individual determinants, not on the order of the factors.

**$\det(A^{-1}B)$:** Since $\det A = 3 \neq 0$, the matrix $A$ is invertible and $A^{-1}$ exists. Using $\det(A^{-1}) = \frac{1}{\det A}$:

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

Place $u$ and $v$ as columns of a matrix and compute the determinant:

$$
\det
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}
= (3)(4) - (1)(1) = 12 - 1 = 11.
$$

The **area** of the parallelogram spanned by $u$ and $v$ is the absolute value of this determinant:

$$
\mathrm{Area} = |11| = 11.
$$

**Reversing the order** — place $v$ first, then $u$:

$$
\det
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}
= (1)(1) - (3)(4) = 1 - 12 = -11.
$$

Swapping the two column vectors is equivalent to swapping the two columns of the matrix, which reverses the sign of the determinant. Therefore $\det = -11$.

However, the **area does not change**: $|-11| = 11$, the same as before.

**Geometric meaning:** The sign of the determinant encodes **orientation**. The pair $(u, v)$ forms a counterclockwise basis (positive orientation), while the pair $(v, u)$ forms a clockwise basis (negative orientation). The area — a non-negative geometric quantity — is always the absolute value and is independent of the ordering.

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
\end{pmatrix}
= 0.
$$

Identify a specific dependence between the rows and connect it with non-invertibility of the matrix.

### Solution

**Observation:** Row 2 of the matrix is exactly $2$ times row 1:

$$
R_2 = (2, 4, 6) = 2 \cdot (1, 2, 3) = 2 \cdot R_1.
$$

**Why this forces $\det = 0$:** A fundamental property of determinants states that if two rows of a matrix are linearly dependent (in particular, if one row is a scalar multiple of another), then the determinant is zero. Formally, applying the row operation $R_2 \leftarrow R_2 - 2R_1$ (which does not change the determinant) yields:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}.
$$

The second row is now the zero row. Expanding along this row gives zero immediately, so $\det = 0$.

**Connection with non-invertibility:** A square matrix is invertible if and only if its rows (equivalently its columns) are linearly independent. Here rows 1 and 2 are linearly dependent ($R_2 = 2R_1$), so the three rows do not span $\mathbb{R}^3$. The matrix has rank at most 2, its row space is at most two-dimensional, and it therefore has no inverse. The determinant being zero is both the algebraic expression and the detection criterion for this non-invertibility.
