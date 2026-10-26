## Question

For

$A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## Solution

### 1. Computation of the Determinant in Terms of the Parameter $t$

The given matrix is a $2\times 2$ matrix depending on the real parameter $t$:

$A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}.$

Using the formula for the determinant of a $2\times 2$ matrix:

$\det A(t) = \begin{vmatrix} t & 1 \\ 2 & t \end{vmatrix} = (t)(t) - (1)(2) = t^2 - 2.$

### 2. Criterion for Invertibility and Finding the Critical Values

A square matrix is **invertible** if and only if its determinant is non-zero ($\det M \neq 0$). Conversely, a matrix is **not invertible** (singular) if and only if its determinant vanishes:

$\det A(t) = 0.$

Setting our expression equal to zero:

$t^2 - 2 = 0 \iff t^2 = 2 \iff t = \sqrt{2} \quad \mathrm{or} \quad t = -\sqrt{2}.$

Therefore, the matrix $A(t)$ is not invertible for:

$t \in \{-\sqrt{2}, \sqrt{2}\}.$

For all other real numbers $t \notin \{-\sqrt{2}, \sqrt{2}\}$, we have $\det A(t) \neq 0$, meaning $A(t)$ is invertible with explicit inverse:

$A(t)^{-1} = \frac{1}{t^2 - 2}\begin{pmatrix} t & -1 \\ -2 & t \end{pmatrix}.$

### 3. Connection to Linear Dependence and Geometric Collapse

The vanishing of the determinant directly reflects the loss of linear independence among the rows and columns:

#### Case 1: $t = \sqrt{2}$

Substituting $t = \sqrt{2}$ into the matrix gives:

$A(\sqrt{2}) = \begin{pmatrix} \sqrt{2} & 1 \\ 2 & \sqrt{2} \end{pmatrix}.$

Notice the relationship between the rows:

$R_2 = (2, \sqrt{2}) = \sqrt{2} \cdot (\sqrt{2}, 1) = \sqrt{2} R_1.$

Because row 2 is a scalar multiple of row 1, the row vectors are collinear. They span only a 1-dimensional subspace (a straight line passing through the origin) rather than the full 2-dimensional plane $\mathbb{R}^2$. The linear map maps the entire plane into this 1D line, crushing 2D area down to zero. Since distinct input vectors map to the same output vector, the mapping is not injective and cannot be inverted.

#### Case 2: $t = -\sqrt{2}$

Substituting $t = -\sqrt{2}$ into the matrix gives:

$A(-\sqrt{2}) = \begin{pmatrix} -\sqrt{2} & 1 \\ 2 & -\sqrt{2} \end{pmatrix}.$

Notice the relationship between the rows:

$R_2 = (2, -\sqrt{2}) = -\sqrt{2} \cdot (-\sqrt{2}, 1) = -\sqrt{2} R_1.$

The rows are once again linearly dependent, leading to the same geometric dimensional collapse and confirming that no inverse mapping can exist.
