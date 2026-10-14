## Question

Let

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For

$$
x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

### 1. Computation of $RSx$ (Scale, Then Rotate)

First, apply the scaling transformation $S$ to vector $x$:

$$
Sx=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
2(1)+0(2) \\
0(1)+1(2) \\
\end{pmatrix}
= \begin{pmatrix}
2 \\
2 \\
\end{pmatrix}.
$$

Next, apply the rotation matrix $R$ to the scaled vector $Sx$:

$$
RSx=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
0(2)+(-1)(2) \\
1(2)+0(2) \\
\end{pmatrix}
= \begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}.
$$

### 2. Computation of $SRx$ (Rotate, Then Scale)

First, apply the rotation transformation $R$ to vector $x$:

$$
Rx=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
0(1)+(-1)(2) \\
1(1)+0(2) \\
\end{pmatrix}
= \begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}.
$$

Next, apply the scaling matrix $S$ to the rotated vector $Rx$:

$$
SRx=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
= \begin{pmatrix}
2(-2)+0(1) \\
0(-2)+1(1) \\
\end{pmatrix}
= \begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}.
$$

### 3. Verification via Composite Matrices

We can verify the products using the composite transformation matrices:

$$
RS=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix},
$$

$$
(RS)x=
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}.
$$

For $SR$:

$$
SR=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
= \begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix},
$$

$$
(SR)x=
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}.
$$

Both calculation routes yield identical outcomes.

### 4. Comparison of Transformations

Comparing the outputs:

$$
RSx =
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
\neq
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
= SRx.
$$

### 5. Geometric Interpretation

The scaling matrix $S$ is anisotropic (nonuniform): it stretches vectors strictly along the horizontal $x$-axis by a factor of $2$, while leaving vertical $y$-coordinates untouched.

- In the sequence $RSx$:
  The vector $(1, 2)$ is first stretched horizontally to $(2, 2)$. Rotating this vector by $90^\circ$ counterclockwise turns the horizontal component $2$ into the new vertical component, and the vertical component $2$ into the negative horizontal component, producing $(-2, 2)$.

- In the sequence $SRx$:
  The initial vector $(1, 2)$ is rotated first by $90^\circ$ counterclockwise into $(-2, 1)$. This rotation interchanges the axes: the original vertical component $y=2$ is placed onto the horizontal axis as $-2$. When horizontal scaling $S$ is applied afterwards, it stretches this newly horizontal component by a factor of $2$, turning $-2$ into $-4$, while leaving the new vertical component $1$ unchanged. This produces $(-4, 1)$.

Because rotation alters the alignment of the vector relative to the fixed coordinate axes where the scaling acts, the two geometric operations do not commute.
