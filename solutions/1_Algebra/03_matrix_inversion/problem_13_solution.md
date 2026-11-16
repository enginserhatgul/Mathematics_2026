## Question

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

## Solution

### 1. Method 1: Compute $T$ First, Then Its Inverse

First, find $T = HS$:

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
\det T = (2)(1) - (1)(0) = 2 \neq 0.
$$

Apply the $2\times 2$ inverse formula:

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

### 2. Method 2: Use $(HS)^{-1} = S^{-1} H^{-1}$

Find the individual inverses:

$$
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix},
\qquad
H^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

Multiply $S^{-1}$ and $H^{-1}$:

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

Both methods produce the identical matrix:

$$
T^{-1} = (HS)^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}.
$$

### 3. Computation of the Incorrect Order $H^{-1} S^{-1}$

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

Multiplying in the wrong order yields an incorrect matrix.

### 4. Explanation of the Rule

The transformation $T = HS$ acts on a vector $x$ as:

$$
x \xrightarrow{S} Sx \xrightarrow{H} H(Sx) = Tx.
$$

To reverse this sequence, we must undo the operations in reverse chronological order:
1. First undo the last operation $H$ by applying $H^{-1}$:
   $H^{-1}(Tx) = H^{-1}(HSx) = (H^{-1}H)Sx = Sx$.
2. Next undo the scaling $S$ by applying $S^{-1}$:
   $S^{-1}(Sx) = (S^{-1}S)x = x$.

If we attempted to apply $S^{-1}$ first, the unscaling would act on sheared coordinates, which distorts the geometry and fails to return to the original vector.
