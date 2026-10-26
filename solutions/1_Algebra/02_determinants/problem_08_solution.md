## Question

Let $A, B$ be square matrices such that $\det A = 3$ and $\det B = -5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB \neq BA$.

## Solution

### 1. Computation of $\det(AB)$ and $\det(BA)$

**Multiplicative Property of Determinants:** For any square matrices $A$ and $B$ of matching dimensions, the determinant of their matrix product equals the product of their individual determinants:

$\det(AB) = \det A \cdot \det B.$

Applying this formula to $\det(AB)$:

$\det(AB) = (3) \cdot (-5) = -15.$

Applying the formula to the reversed product $\det(BA)$:

$\det(BA) = \det B \cdot \det A = (-5) \cdot (3) = -15.$

### 2. Explanation of Why $\det(AB) = \det(BA)$ While $AB \neq BA$

In general linear algebra, matrix multiplication is **non-commutative**:

$AB \neq BA.$

The composite linear transformation $AB$ (which applies $B$ first, then $A$) produces different geometric mappings and different matrix entries than $BA$ (which applies $A$ first, then $B$).

However, the determinant is a scalar-valued function mapping matrices into the field of real numbers $\mathbb{R}$:

$\det: \mathbb{R}^{n\times n} \to \mathbb{R}.$

While matrices do not commute, multiplication of real scalars **is commutative**:

$\det A \cdot \det B = \det B \cdot \det A$ in $\mathbb{R}$.

Geometrically, the determinant measures the factor by which an operator scales volume. When transformations are composed, their volume scaling factors multiply together. Whether space is scaled by factor $3$ and then by factor $-5$, or by factor $-5$ and then by factor $3$, the net volume scaling factor of both composite transformations is identically $-15$.

### 3. Existence and Computation of $\det(A^{-1}B)$

#### Step 1: Verification of Invertibility

A matrix inverse $A^{-1}$ exists if and only if $\det A \neq 0$. Because $\det A = 3 \neq 0$, matrix $A$ is non-singular and its inverse $A^{-1}$ is guaranteed to exist.

#### Step 2: Determinant of an Inverse Matrix

Using the identity $A \cdot A^{-1} = I$ and taking determinants of both sides:

$\det(A \cdot A^{-1}) = \det(I) \implies \det A \cdot \det(A^{-1}) = 1 \implies \det(A^{-1}) = \frac{1}{\det A}.$

Substituting $\det A = 3$:

$\det(A^{-1}) = \frac{1}{3}.$

#### Step 3: Computation of the Product

Applying the multiplicative property to $A^{-1}B$:

$\det(A^{-1}B) = \det(A^{-1}) \cdot \det B = \left(\frac{1}{3}\right) \cdot (-5) = -\frac{5}{3}.$
