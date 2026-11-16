## Question

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

## Solution

### 1. Invertibility Check and Finding $A^{-1}$

Compute $\det A$:

$$
\det A = (2)(3) - (1)(1) = 6 - 1 = 5.
$$

Since $\det A = 5 \neq 0$, matrix $A$ is invertible. Using the $2\times 2$ inverse formula:

$$
A^{-1} = \frac{1}{\det A}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

### 2. Solving for $x$ via $x = A^{-1}b$

Multiply $A^{-1}$ by vector $b$:

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

### 3. Verification by Substitution

Substitute $x = \begin{pmatrix} 8/5 \\ 9/5 \end{pmatrix}$ back into $Ax$:

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
