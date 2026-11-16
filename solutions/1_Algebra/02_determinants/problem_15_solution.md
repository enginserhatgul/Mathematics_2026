## Question

Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

## Solution

### 1. Properties Used

1. **Multiplicativity:** $\det(XY) = \det X \cdot \det Y$ for square matrices of the same size.
2. **Transpose:** $\det(A^T) = \det A$.
3. **Inverse:** $\det(B^{-1}) = \dfrac{1}{\det B}$ for an invertible matrix $B$.

### 2. Computation

Apply multiplicativity to the three factors:

$$
\det\left(B^{-1}A^TB\right) = \det\left(B^{-1}\right)\cdot\det\left(A^T\right)\cdot\det B.
$$

Apply the transpose and inverse properties:

$$
\det\left(B^{-1}\right)\cdot\det\left(A^T\right)\cdot\det B = \frac{1}{\det B}\cdot\det A\cdot\det B.
$$

Substitute the given values:

$$
\frac{1}{3}\cdot(-2)\cdot 3 = -2.
$$

### 3. Why the Factors Involving $B$ Cancel

The determinant of a product is a product of ordinary numbers, and multiplication of numbers is commutative. Therefore $\det B^{-1}$ and $\det B$ can be brought next to each other, and

$$
\det\left(B^{-1}\right)\cdot\det B = \frac{1}{\det B}\cdot\det B = 1.
$$

This reflects the fact that $B^{-1}A^TB$ is a similarity transformation of $A^T$, and similar matrices have equal determinants, so

$$
\det\left(B^{-1}A^TB\right) = \det\left(A^T\right) = \det A.
$$

### 4. Conclusion

$$
\det\left(B^{-1}A^TB\right) = -2.
$$
