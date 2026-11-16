## Question

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

## Solution

### 1. Method 1: Compute $(AB)^{-1}$ Directly

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

Compute $\det(AB)$:

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

### 2. Method 2: Compute $B^{-1}A^{-1}$

Find $A^{-1}$:
Since $\det A = (1)(1) - (1)(0) = 1$:

$$
A^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

Find $B^{-1}$:
Since $\det B = (2)(3) - 0 = 6$:

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

Both calculations give the identical result:

$$
(AB)^{-1} = B^{-1} A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}.
$$

### 3. Meaning of the Reversed Order

When linear transformations are composed, $AB$ means applying $B$ first, then applying $A$:

$$
(AB)x = A(Bx).
$$

To undo this sequence, we must undo the operations in reverse order: first undo the last operation $A$ by applying $A^{-1}$, and then undo the first operation $B$ by applying $B^{-1}$:

$$
(B^{-1} A^{-1})(AB)x = B^{-1}(A^{-1} A) B x = B^{-1} I B x = B^{-1} B x = x.
$$

This is the classic "socks and shoes" principle: to undo putting on socks ($B$) and then shoes ($A$), one must take off shoes ($A^{-1}$) first, then socks ($B^{-1}$).
