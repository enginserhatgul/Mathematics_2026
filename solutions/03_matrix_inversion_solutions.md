# Solutions: Inverse Matrix

This document contains step-by-step solutions for all exercises in `03_matrix_inversion_en.md`.

---

## Exercise 1. Definition of the Inverse

### Question

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

### Solution

#### 1. Definition of the Inverse Matrix

An $n\times n$ matrix $B$ is the inverse of an $n\times n$ matrix $A$ (written $B = A^{-1}$) if and only if:

$$
AB = I_n \quad \mathrm{and} \quad BA = I_n,
$$

where $I_n$ is the $n\times n$ identity matrix.

#### 2. Computation of $AB$

Multiply $A$ on the left and $B$ on the right:

$$
AB =
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

Evaluating entry by entry:

$$
\begin{aligned}
(AB)_{11} &= 2(1) + 1(-1) = 2 - 1 = 1, \\
(AB)_{12} &= 2(-1) + 1(2) = -2 + 2 = 0, \\
(AB)_{21} &= 1(1) + 1(-1) = 1 - 1 = 0, \\
(AB)_{22} &= 1(-1) + 1(2) = -1 + 2 = 1.
\end{aligned}
$$

Therefore:

$$
AB =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$

#### 3. Computation of $BA$

Multiply $B$ on the left and $A$ on the right:

$$
BA =
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}.
$$

Evaluating entry by entry:

$$
\begin{aligned}
(BA)_{11} &= 1(2) + (-1)(1) = 2 - 1 = 1, \\
(BA)_{12} &= 1(1) + (-1)(1) = 1 - 1 = 0, \\
(BA)_{21} &= -1(2) + 2(1) = -2 + 2 = 0, \\
(BA)_{22} &= -1(1) + 2(1) = -1 + 2 = 1.
\end{aligned}
$$

Therefore:

$$
BA =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$

#### 4. Conclusion

Since both products satisfy $AB = I$ and $BA = I$, matrix $B$ satisfies the formal definition of the inverse. Thus, $B = A^{-1}$.

---

## Exercise 2. Formula for a 2×2 Matrix

### Question

Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

### Solution

#### 1. Invertibility Check

For a $2\times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is:

$$
\det A = ad - bc.
$$

For the given matrix $A$:

$$
\det A = (3)(4) - (2)(5) = 12 - 10 = 2.
$$

Since $\det A = 2 \neq 0$, the matrix $A$ is invertible.

#### 2. Application of the 2×2 Inverse Formula

The explicit formula for the inverse of a $2\times 2$ matrix is:

$$
A^{-1} = \frac{1}{\det A}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}.
$$

Substituting $a = 3$, $b = 2$, $c = 5$, $d = 4$, and $\det A = 2$:

$$
A^{-1} = \frac{1}{2}
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}
= \begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}.
$$

#### 3. Verification by Multiplication

Compute the product $A A^{-1}$:

$$
A A^{-1} =
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}.
$$

Evaluating entry by entry:

$$
\begin{aligned}
(A A^{-1})_{11} &= 3(2) + 2\left(-\frac{5}{2}\right) = 6 - 5 = 1, \\
(A A^{-1})_{12} &= 3(-1) + 2\left(\frac{3}{2}\right) = -3 + 3 = 0, \\
(A A^{-1})_{21} &= 5(2) + 4\left(-\frac{5}{2}\right) = 10 - 10 = 0, \\
(A A^{-1})_{22} &= 5(-1) + 4\left(\frac{3}{2}\right) = -5 + 6 = 1.
\end{aligned}
$$

Therefore:

$$
A A^{-1} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$

The result is verified.

---

## Exercise 3. When Does the Inverse Not Exist?

### Question

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

### Solution

#### 1. Method 1: Using the Determinant

Compute the determinant of $A$:

$$
\det A = (2)(2) - (4)(1) = 4 - 4 = 0.
$$

By the Invertible Matrix Theorem, a square matrix $A$ is invertible if and only if $\det A \neq 0$. If an inverse $A^{-1}$ existed, then by the multiplicative property of determinants:

$$
\det(A \cdot A^{-1}) = \det(I) \implies \det(A) \cdot \det(A^{-1}) = 1.
$$

Substituting $\det A = 0$ gives $0 \cdot \det(A^{-1}) = 1$, which is impossible ($0 \neq 1$). Therefore, $A^{-1}$ cannot exist.

#### 2. Method 2: Using Dependence Between the Rows

Let $R_1 = (2, 4)$ and $R_2 = (1, 2)$ be the rows of $A$. Comparing them:

$$
R_1 = (2, 4) = 2 \cdot (1, 2) = 2 R_2.
$$

The first row is an exact scalar multiple of the second row, meaning the set $\{R_1, R_2\}$ is linearly dependent.

**Consequence for Invertibility:**
The row space of $A$ has dimension $1$ ($\mathrm{rank}(A) = 1 < 2$). As a linear mapping from $\mathbb{R}^2$ to $\mathbb{R}^2$, matrix $A$ maps every vector $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ into a scalar multiple of $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$:

$$
Ax =
\begin{pmatrix}
2x_1 + 4x_2 \\
x_1 + 2x_2 \\
\end{pmatrix}
= (x_1 + 2x_2)
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

The range of $A$ is a 1-dimensional line in $\mathbb{R}^2$. Entire lines of vectors (such as all vectors satisfying $x_1 + 2x_2 = 0$) are mapped to the zero vector. Because distinct input vectors produce the identical output vector, the mapping is not injective (one-to-one). Hence, it is impossible to uniquely reconstruct input vectors from output vectors, and no inverse mapping can exist.

---

## Exercise 4. Gauss–Jordan

### Question

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

### Solution

#### 1. Invertibility Check

$$
\det A = (1)(5) - (2)(3) = 5 - 6 = -1 \neq 0.
$$

Since $\det A \neq 0$, the inverse exists.

#### 2. Step-by-Step Gauss–Jordan Elimination

Set up the augmented matrix $[A \mid I]$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}.
$$

**Step 1:** Eliminate the entry below the pivot in column 1 using $R_2 \leftarrow R_2 - 3R_1$:

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

**Step 3:** Eliminate the entry above the pivot in column 2 using $R_1 \leftarrow R_1 - 2R_2$:

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

#### 3. Why Obtaining $I$ on the Left Yields $A^{-1}$ on the Right

Each elementary row operation corresponds to multiplying the augmented matrix from the left by an elementary matrix $E_k$. Suppose a sequence of row operations $E_1, E_2, \dots, E_k$ transforms $A$ into $I$:

$$
(E_k \cdots E_2 E_1) A = I.
$$

By definition of the inverse matrix, the product of these elementary matrices is precisely $A^{-1}$:

$$
E_k \cdots E_2 E_1 = A^{-1}.
$$

Because the same row operations are simultaneously applied to the right block $I$:

$$
(E_k \cdots E_2 E_1) I = A^{-1} I = A^{-1}.
$$

Thus, when the left block reaches $I$, the right block automatically becomes $A^{-1}$.

#### 4. Verification

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
-5 + 6 & 2 - 2 \\
-15 + 15 & 6 - 5 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$

---

## Exercise 5. A 3×3 Matrix

### Question

Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

### Solution

#### 1. Invertibility Check

Compute $\det A$ by cofactor expansion along row 1:

$$
\det A = 1 \cdot
\begin{vmatrix}
1 & 1 \\
0 & 1 \\
\end{vmatrix}
- 1 \cdot
\begin{vmatrix}
0 & 1 \\
1 & 1 \\
\end{vmatrix}
+ 0 = 1(1 - 0) - 1(0 - 1) = 1 - (-1) = 2.
$$

Since $\det A = 2 \neq 0$, the inverse $A^{-1}$ exists.

#### 2. Step-by-Step Gauss–Jordan Elimination

Set up the augmented matrix $[A \mid I]$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 & 0 & 1 & \mid & 0 & 0 & 1 \\
\end{pmatrix}.
$$

**Step 1:** Eliminate entry $(3,1)$ using $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & -1 & 1 & \mid & -1 & 0 & 1 \\
\end{pmatrix}.
$$

**Step 2:** Eliminate entry $(3,2)$ using $R_3 \leftarrow R_3 + R_2$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 2 & \mid & -1 & 1 & 1 \\
\end{pmatrix}.
$$

**Step 3:** Scale row 3 using $R_3 \leftarrow \frac{1}{2} R_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}.
$$

**Step 4:** Eliminate entry $(2,3)$ using $R_2 \leftarrow R_2 - R_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}.
$$

**Step 5:** Eliminate entry $(1,2)$ using $R_1 \leftarrow R_1 - R_2$:

$$
\begin{pmatrix}
1 & 0 & 0 & \mid & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}.
$$

The left block is $I$, so the right block is $A^{-1}$:

$$
A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
= \frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$

#### 3. Verification by Multiplication

$$
A A^{-1} =
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
\cdot \frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$

Evaluating the matrix product:

$$
\begin{aligned}
\mathrm{Row 1:} \quad
& 1(1) + 1(1) + 0(-1) = 2, \\
& 1(-1) + 1(1) + 0(1) = 0, \\
& 1(1) + 1(-1) + 0(1) = 0. \\
\mathrm{Row 2:} \quad
& 0(1) + 1(1) + 1(-1) = 0, \\
& 0(-1) + 1(1) + 1(1) = 2, \\
& 0(1) + 1(-1) + 1(1) = 0. \\
\mathrm{Row 3:} \quad
& 1(1) + 0(1) + 1(-1) = 0, \\
& 1(-1) + 0(1) + 1(1) = 0, \\
& 1(1) + 0(-1) + 1(1) = 2.
\end{aligned}
$$

Multiplying by the scalar $\frac{1}{2}$:

$$
A A^{-1} = \frac{1}{2}
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
= I.
$$

---

## Exercise 6. Solving a System Using the Inverse

### Question

Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

### Solution

#### 1. Invertibility Check and Finding $A^{-1}$

Compute $\det A$:

$$
\det A = (2)(3) - (1)(1) = 6 - 1 = 5.
$$

Since $\det A = 5 \neq 0$, $A$ is invertible. Using the $2\times 2$ inverse formula:

$$
A^{-1} = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

#### 2. Computing the Solution Vector $x = A^{-1}b$

$$
x = A^{-1} b = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}.
$$

Carrying out the matrix-vector multiplication:

$$
x = \frac{1}{5}
\begin{pmatrix}
3(5) + (-1)(7) \\
-1(5) + 2(7) \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
15 - 7 \\
-5 + 14 \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
8 \\
9 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix}.
$$

#### 3. Verification by Substitution

Substitute $x = \begin{pmatrix} 8/5 \\ 9/5 \end{pmatrix}$ into $Ax$:

$$
Ax =
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix}
= \begin{pmatrix}
2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) \\
1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) \\
\end{pmatrix}
= \begin{pmatrix}
\frac{16 + 9}{5} \\
\frac{8 + 27}{5} \\
\end{pmatrix}
= \begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5} \\
\end{pmatrix}
= \begin{pmatrix}
5 \\
7 \\
\end{pmatrix}
= b.
$$

The solution is verified.

---

## Exercise 7. Inverse of a Product

### Question

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

### Solution

#### 1. Method 1: Compute $(AB)^{-1}$ Directly

First, compute the product $AB$:

$$
AB =
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
= \begin{pmatrix}
1(2) + 1(0) & 1(0) + 1(3) \\
0(2) + 1(0) & 0(0) + 1(3) \\
\end{pmatrix}
= \begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}.
$$

Compute the determinant:

$$
\det(AB) = (2)(3) - (3)(0) = 6 \neq 0.
$$

Apply the $2\times 2$ inverse formula:

$$
(AB)^{-1} = \frac{1}{6}
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}.
$$

#### 2. Method 2: Compute $B^{-1}A^{-1}$

Find $A^{-1}$:
$\det A = 1(1) - 1(0) = 1$.

$$
A^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

Find $B^{-1}$:
$\det B = 2(3) - 0 = 6$.

$$
B^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}.
$$

Multiply $B^{-1}$ and $A^{-1}$:

$$
B^{-1} A^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2}(1) + 0(0) & \frac{1}{2}(-1) + 0(1) \\
0(1) + \frac{1}{3}(0) & 0(-1) + \frac{1}{3}(1) \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}.
$$

Both calculations yield the identical matrix:

$$
(AB)^{-1} = B^{-1} A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}.
$$

#### 3. Meaning of the Reversed Order

When applying composite transformations, $AB$ means "first apply $B$, then apply $A$":

$$
(AB)x = A(Bx).
$$

To reverse this composite process, one must undo the operations in reverse order: first undo $A$ by applying $A^{-1}$, and only then undo $B$ by applying $B^{-1}$:

$$
(B^{-1} A^{-1})(AB)x = B^{-1}(A^{-1} A) B x = B^{-1} I B x = B^{-1} B x = I x = x.
$$

This is the standard "socks and shoes" principle: if you put on socks ($B$) and then shoes ($A$), to undo the process you must take off shoes ($A^{-1}$) first, and then socks ($B^{-1}$).

---

## Exercise 8. Inverse of a Transformation

### Question

The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

### Solution

#### 1. Finding $S^{-1}$

Matrix $S$ is diagonal. Compute its determinant:

$$
\det S = (2)\left(\frac{1}{2}\right) - (0)(0) = 1.
$$

Since $\det S = 1 \neq 0$, the inverse exists. For a diagonal matrix, the inverse is obtained by inverting each non-zero diagonal entry:

$$
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}.
$$

#### 2. Geometric Interpretation

The matrix $S$ scales vectors in $\mathbb{R}^2$ by:
- stretching the horizontal component $x$ by a factor of $2$,
- compressing the vertical component $y$ by a factor of $\frac{1}{2}$.

The inverse transformation $S^{-1}$ reverses this action:
- compresses the horizontal component $x$ by a factor of $\frac{1}{2}$,
- stretches the vertical component $y$ by a factor of $2$.

Because $(2)(\frac{1}{2}) = 1$ along both coordinate axes, applying $S$ followed by $S^{-1}$ restores any point to its initial position.

#### 3. Verification on a Specific Vector

Choose the vector $v = \begin{pmatrix} 4 \\ 6 \end{pmatrix}$.

Apply $S$:

$$
Sv =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
\begin{pmatrix}
4 \\
6 \\
\end{pmatrix}
= \begin{pmatrix}
2(4) \\
\frac{1}{2}(6) \\
\end{pmatrix}
= \begin{pmatrix}
8 \\
3 \\
\end{pmatrix}.
$$

Apply $S^{-1}$ to the result:

$$
S^{-1}(Sv) =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
8 \\
3 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2}(8) \\
2(3) \\
\end{pmatrix}
= \begin{pmatrix}
4 \\
6 \\
\end{pmatrix}
= v.
$$

The original vector is completely restored.

---

## Exercise 9. Matrix Equation

### Question

Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

### Solution

#### 1. Algebraic Analysis: Which Side to Multiply

In the equation $AX = B$, matrix $A$ appears to the left of the unknown matrix $X$. Because matrix multiplication is non-commutative ($M_1 M_2 \neq M_2 M_1$ in general), we must multiply both sides on the **left** by $A^{-1}$:

$$
A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B.
$$

Multiplying on the right would give $AXA^{-1} = BA^{-1}$, which does not isolate $X$.

#### 2. Computation of $A^{-1}$

Compute $\det A$:

$$
\det A = (1)(1) - (2)(0) = 1.
$$

Since $\det A = 1 \neq 0$, $A$ is invertible:

$$
A^{-1} = \frac{1}{1}
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}.
$$

#### 3. Computation of $X = A^{-1}B$

$$
X =
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Evaluating entry by entry:

$$
\begin{aligned}
X_{11} &= 1(3) + (-2)(2) = 3 - 4 = -1, \\
X_{12} &= 1(1) + (-2)(4) = 1 - 8 = -7, \\
X_{21} &= 0(3) + 1(2) = 2, \\
X_{22} &= 0(1) + 1(4) = 4.
\end{aligned}
$$

Therefore:

$$
X =
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
$$

#### 4. Verification by Computing $AX$

$$
AX =
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
= \begin{pmatrix}
1(-1) + 2(2) & 1(-7) + 2(4) \\
0(-1) + 1(2) & 0(-7) + 1(4) \\
\end{pmatrix}
= \begin{pmatrix}
-1 + 4 & -7 + 8 \\
2 & 4 \\
\end{pmatrix}
= \begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}
= B.
$$

---

## Exercise 10. Inverse of a Diagonal Matrix

### Question

Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

### Solution

#### 1. Invertibility Criterion for Diagonal Matrices

The determinant of a diagonal matrix equals the product of its diagonal entries:

$$
\det D = (2)(-3)(5) = -30 \neq 0.
$$

$$
\det E = (2)(0)(5) = 0.
$$

- Matrix $D$ **is invertible** because all its diagonal entries are non-zero ($\det D \neq 0$).
- Matrix $E$ **is not invertible** because it contains a zero on its main diagonal ($\det E = 0$). Row 2 of $E$ consists entirely of zeros, so $\mathrm{rank}(E) \le 2 < 3$.

#### 2. Inverse of Matrix $D$

For any diagonal matrix with non-zero diagonal entries, the inverse is formed by taking the reciprocal of each diagonal entry:

$$
D^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}.
$$

#### 3. Verification by Multiplication

$$
D D^{-1} =
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}
= \begin{pmatrix}
2\left(\frac{1}{2}\right) & 0 & 0 \\
0 & (-3)\left(-\frac{1}{3}\right) & 0 \\
0 & 0 & 5\left(\frac{1}{5}\right) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
= I.
$$

---

## Exercise 11. Parameter and Invertibility

### Question

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

### Solution

#### 1. Invertibility Condition

Compute the determinant of $A(t)$:

$$
\det A(t) = (1)(1) - (t)(t) = 1 - t^2 = (1 - t)(1 + t).
$$

Matrix $A(t)$ is invertible if and only if $\det A(t) \neq 0$:

$$
1 - t^2 \neq 0 \iff t^2 \neq 1 \iff t \neq 1 \quad \mathrm{and} \quad t \neq -1.
$$

Therefore, $A(t)$ is invertible for all $t \in \mathbb{R} \setminus \{-1, 1\}$.

#### 2. Formula for $A(t)^{-1}$

For $t \neq \pm 1$, apply the $2\times 2$ inverse formula:

$$
A(t)^{-1} = \frac{1}{\det A(t)}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
= \frac{1}{1 - t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}.
$$

#### 3. Explanation of Excluded Values

At $t = 1$ and $t = -1$:
- The formula features division by $1 - t^2 = 0$, which is undefined.
- At $t = 1$:

$$
A(1) =
\begin{pmatrix}
1 & 1 \\
1 & 1 \\
\end{pmatrix}.
$$

Both rows are identical ($R_1 = R_2$). The columns are also identical, meaning the matrix has rank $1$. The linear transformation collapses the entire plane $\mathbb{R}^2$ onto the 1D line $y = x$.

- At $t = -1$:

$$
A(-1) =
\begin{pmatrix}
1 & -1 \\
-1 & 1 \\
\end{pmatrix}.
$$

The second row is the exact negative of the first ($R_2 = -R_1$). The matrix again has rank $1$, collapsing $\mathbb{R}^2$ onto the line $y = -x$.

In both cases, dimensional collapse destroys information, so no inverse matrix can exist.

---

## Exercise 12. Finding Inverses Without Starting from Scratch

### Question

It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

### Solution

#### 1. Computation of $(3A)^{-1}$

**Property:** For any non-zero scalar $c$ and invertible matrix $A$, $(cA)^{-1} = \frac{1}{c} A^{-1}$.

Here $c = 3$:

$$
(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3} \\
\end{pmatrix}.
$$

#### 2. Computation of $(A^T)^{-1}$

**Property:** Inversion and transposition commute: $(A^T)^{-1} = (A^{-1})^T$.

Transposing the given $A^{-1}$:

$$
(A^T)^{-1} =
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}^T
= \begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}.
$$

#### 3. Computation of $(A^2)^{-1}$

**Property:** The inverse of a power is the power of the inverse: $(A^k)^{-1} = (A^{-1})^k$.

For $k = 2$:

$$
(A^2)^{-1} = (A^{-1})^2 = A^{-1} A^{-1} =
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Evaluating entry by entry:

$$
\begin{aligned}
(A^{-1} A^{-1})_{11} &= 2(2) + (-1)(-3) = 4 + 3 = 7, \\
(A^{-1} A^{-1})_{12} &= 2(-1) + (-1)(2) = -2 - 2 = -4, \\
(A^{-1} A^{-1})_{21} &= -3(2) + 2(-3) = -6 - 6 = -12, \\
(A^{-1} A^{-1})_{22} &= -3(-1) + 2(2) = 3 + 4 = 7.
\end{aligned}
$$

Therefore:

$$
(A^2)^{-1} =
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}.
$$

---

## Exercise 13. Undoing a Composite Transformation

### Question

The matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

### Solution

#### 1. Method 1: Compute $T$ First, Then $T^{-1}$

Compute $T = HS$:

$$
T =
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1(2) + 1(0) & 1(0) + 1(1) \\
0(2) + 1(0) & 0(0) + 1(1) \\
\end{pmatrix}
= \begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Compute the determinant:

$$
\det T = (2)(1) - (1)(0) = 2.
$$

Since $\det T = 2 \neq 0$, the inverse is:

$$
T^{-1} = \frac{1}{2}
\begin{pmatrix}
1 & -1 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}.
$$

#### 2. Method 2: Use $(HS)^{-1} = S^{-1} H^{-1}$

Find $S^{-1}$:

$$
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

Find $H^{-1}$:

$$
H^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

Compute $S^{-1} H^{-1}$:

$$
S^{-1} H^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2}(1) + 0(0) & \frac{1}{2}(-1) + 0(1) \\
0(1) + 1(0) & 0(-1) + 1(1) \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}.
$$

Both methods yield the identical result:

$$
T^{-1} = (HS)^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}.
$$

#### 3. Computation of the Incorrect Order $H^{-1} S^{-1}$

$$
H^{-1} S^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1\left(\frac{1}{2}\right) + (-1)(0) & 1(0) + (-1)(1) \\
0\left(\frac{1}{2}\right) + 1(0) & 0(0) + 1(1) \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

Notice that:

$$
\begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1 \\
\end{pmatrix}
\neq
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}.
$$

The incorrect order produces a different matrix!

#### 4. Explanation of the Rule

The transformation $T = HS$ applies the scaling $S$ first, followed by the shear $H$:

$$
x \xrightarrow{S} Sx \xrightarrow{H} H(Sx) = Tx.
$$

To undo this sequence, we must first undo the most recently performed operation (the shear $H$) by applying $H^{-1}$. This returns us to the intermediate scaled state $Sx$:

$$
H^{-1}(Tx) = H^{-1}(HSx) = (H^{-1}H)Sx = Sx.
$$

Next, we undo the scaling $S$ by applying $S^{-1}$:

$$
S^{-1}(Sx) = (S^{-1}S)x = x.
$$

If one mistakenly applies $S^{-1}$ first, the unscaling operator acts on sheared coordinates rather than the original axes, distorting the vector rather than restoring it.

---

## Exercise 14. A Matrix That Is Its Own Inverse

### Question

Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

### Solution

#### 1. Proof that $A^{-1} = A$

By the formal definition of the matrix inverse, a matrix $B$ is the inverse of $A$ if:

$$
AB = I \quad \mathrm{and} \quad BA = I.
$$

We are given the condition:

$$
A^2 = A \cdot A = I.
$$

Setting $B = A$, we observe that $A \cdot A = I$. Since multiplying $A$ by $A$ yields the identity matrix, matrix $A$ satisfies the definition of its own inverse. Because the inverse of a square matrix is unique, it follows that:

$$
A^{-1} = A.
$$

Alternatively, multiplying both sides of $A^2 = I$ by $A^{-1}$ from the left:

$$
A^{-1}(A^2) = A^{-1} I \implies (A^{-1}A)A = A^{-1} \implies IA = A^{-1} \implies A = A^{-1}.
$$

Matrices that satisfy $A^2 = I$ (or equivalently $A = A^{-1}$) are called **involutory matrices**.

#### 2. Constructing a Non-Trivial $2\times2$ Example

We look for a matrix $A \neq \pm I$ satisfying $A^2 = I$. Geometrically, reflections across lines in $\mathbb{R}^2$ are involutions (reflecting twice returns to the original point).

Consider the reflection across the line $y = x$, represented by:

$$
A =
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

Clearly, $A \neq I$ and $A \neq -I$.

#### 3. Verification by Multiplication

Compute $A^2$:

$$
A^2 =
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
= \begin{pmatrix}
0(0) + 1(1) & 0(1) + 1(0) \\
1(0) + 0(1) & 1(1) + 0(0) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I.
$$

Since $A^2 = I$, we confirm that $A^{-1} = A$.

*(Another valid example is the reflection across the horizontal axis: $A = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$, which also satisfies $A^2 = I$.)*

---

## Exercise 15. Two Methods for Solving the Same System

### Question

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

### Solution

#### 1. Method 1: Using the Inverse Matrix $x = A^{-1}b$

**Step 1: Check invertibility and find $\det A$**

$$
\det A = (2)(3) - (1)(1) = 6 - 1 = 5 \neq 0.
$$

**Step 2: Form the inverse matrix $A^{-1}$**

$$
A^{-1} = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

**Step 3: Multiply by vector $b$**

$$
x = A^{-1} b = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
3(7) + (-1)(8) \\
-1(7) + 2(8) \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
21 - 8 \\
-7 + 16 \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
13 \\
9 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}.
$$

#### 2. Method 2: Using Gaussian Elimination

Set up the augmented matrix $[A \mid b]$:

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
1 & 3 & \mid & 8 \\
\end{pmatrix}.
$$

**Step 1: Swap rows to obtain a pivot of 1 ($R_1 \leftrightarrow R_2$):**

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 & 1 & \mid & 7 \\
\end{pmatrix}.
$$

**Step 2: Eliminate entry $(2,1)$ using $R_2 \leftarrow R_2 - 2R_1$:**

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & 1 - 2(3) & \mid & 7 - 2(8) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & -5 & \mid & -9 \\
\end{pmatrix}.
$$

**Step 3: Back substitution**
From the second row:

$$
-5 x_2 = -9 \implies x_2 = \frac{9}{5}.
$$

From the first row:

$$
x_1 + 3 x_2 = 8 \implies x_1 = 8 - 3\left(\frac{9}{5}\right) = \frac{40 - 27}{5} = \frac{13}{5}.
$$

Thus:

$$
x =
\begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}.
$$

#### 3. Comparison of the Two Methods

- **Consistency:** Both methods yield the identical solution $x_1 = \frac{13}{5}$, $x_2 = \frac{9}{5}$.
- **Computational Effort in this Example:**
  Gaussian elimination was simpler and faster. It required only one row swap, one row elimination step, and simple back substitution, dealing only with numbers directly involved in the system.
  The matrix inverse method required computing the determinant, finding the adjugate matrix, scalar division, and then performing a matrix-vector product.
- **General Principle:**
  For solving a **single system** $Ax = b$, Gaussian elimination is generally more efficient ($O(n^3/3)$ operations vs $O(n^3)$ for inversion).
  However, the matrix inverse method is advantageous when the same coefficient matrix $A$ is used to solve systems for **multiple different right-hand sides** $b_1, b_2, \dots, b_k$, as each subsequent solution requires only an $O(n^2)$ matrix-vector multiplication.
