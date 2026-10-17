## Question

For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Solution

Here $A$ is a $2\times 2$ matrix. The matching $2\times 2$ identity matrix and zero matrix are:

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad 0=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}.
$$

### 1. Operations with Identity Matrix $I$

Computing $AI$:

$$
\begin{aligned}
AI &=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2(1)+1(0) & 2(0)+1(1) \\
0(1)+2(0) & 0(0)+2(1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= A.
\end{aligned}
$$

Computing $IA$:

$$
\begin{aligned}
IA &=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1(2)+0(0) & 1(1)+0(2) \\
0(2)+1(0) & 0(1)+1(2) \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= A.
\end{aligned}
$$

### 2. Operation with Zero Matrix $0$

Computing $A+0$:

$$
\begin{aligned}
A+0 &=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} +
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2+0 & 1+0 \\
0+0 & 2+0 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= A.
\end{aligned}
$$

### 3. Successive Powers of $A$

Computing $A^2 = AA$:

$$
\begin{aligned}
A^2 &=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2(2)+1(0) & 2(1)+1(2) \\
0(2)+2(0) & 0(1)+2(2) \\
\end{pmatrix} \\
&= \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}.
\end{aligned}
$$

Computing $A^3 = A^2 A$:

$$
\begin{aligned}
A^3 &=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
4(2)+4(0) & 4(1)+4(2) \\
0(2)+4(0) & 0(1)+4(2) \\
\end{pmatrix} \\
&= \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
\end{aligned}
$$

### 4. Roles of $I$ and $0$

- Identity Matrix $I$: Acts as the multiplicative neutral element in the ring of square matrices. For any compatible square matrix $A$, multiplying by $I$ on the left or on the right leaves the matrix invariant: $AI = IA = A$.
- Zero Matrix $0$: Acts as the additive neutral element in the space of matrices. Adding $0$ to any matrix leaves the matrix unchanged: $A + 0 = A$.

### 5. Observed Pattern in Successive Powers

Examining the computed powers:

$$
\begin{aligned}
A^1 &=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
2^1 & 1\cdot 2^0 \\
0 & 2^1 \\
\end{pmatrix}, \\
A^2 &=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix} =
\begin{pmatrix}
2^2 & 2\cdot 2^1 \\
0 & 2^2 \\
\end{pmatrix}, \\
A^3 &=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix} =
\begin{pmatrix}
2^3 & 3\cdot 2^2 \\
0 & 2^3 \\
\end{pmatrix}.
\end{aligned}
$$

The general formula for power $n \ge 1$ is:

$$
A^n=
\begin{pmatrix}
2^n & n 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
$$

### 6. Mathematical Justification

We can decompose $A$ into a scalar matrix plus a strictly upper-triangular nilpotent matrix:

$$
A= 2I + N,
$$

where

$$
N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}.
$$

Notice that $N^2 = 0$. Because $2I$ commutes with any matrix, we can apply the binomial theorem:

$$
A^n = (2I + N)^n = (2I)^n + \binom{n}{1}(2I)^{n-1}N + 0 = 2^n I + n 2^{n-1}N.
$$

Substituting back yields precisely the general formula for $A^n$:

$$
\begin{aligned}
A^n &=
\begin{pmatrix}
2^n & 0 \\
0 & 2^n \\
\end{pmatrix} +
\begin{pmatrix}
0 & n 2^{n-1} \\
0 & 0 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2^n & n 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
\end{aligned}
$$
