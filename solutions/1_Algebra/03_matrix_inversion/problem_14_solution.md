## Question

Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

## Solution

### 1. Proof that $A^{-1} = A$

By the definition of matrix inverse, a matrix $B$ is the inverse of $A$ if:

$$
AB = I \qquad \mathrm{and} \qquad BA = I.
$$

We are given that $A^2 = I$, which means:

$$
A \cdot A = I.
$$

Setting $B = A$, we see that $A$ itself satisfies the definition of the inverse matrix. Because the inverse of an invertible matrix is unique, it follows directly that:

$$
A^{-1} = A.
$$

Alternatively, multiplying both sides of $A^2 = I$ by $A^{-1}$ from the left:

$$
A^{-1}(A^2) = A^{-1} I \implies (A^{-1}A)A = A^{-1} \implies IA = A^{-1} \implies A = A^{-1}.
$$

A matrix satisfying $A^2 = I$ is known as an **involutory matrix**.

### 2. Example of a Non-Trivial $2\times 2$ Involutory Matrix

Geometrically, reflections across lines through the origin in $\mathbb{R}^2$ are involutory transformations (reflecting twice across the same line returns any vector to itself).

Consider the reflection across the line $y = x$, given by the permutation matrix:

$$
A =
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

Notice that $A \neq I$ and $A \neq -I$.

### 3. Verification by Multiplication

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

Since $A^2 = I$, we conclude that $A^{-1} = A$.
