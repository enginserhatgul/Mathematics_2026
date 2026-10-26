## Question

For

$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

## Solution

### 1. Computation of $\det A$

We compute the determinant of $A$ using Sarrus' rule:

$\det A = \begin{vmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{vmatrix}.$

- **Downward diagonal products:**
  - $(1) \cdot (3) \cdot (1) = 3$
  - $(2) \cdot (1) \cdot (2) = 4$
  - $(0) \cdot (0) \cdot (1) = 0$
  - Sum $= 3 + 4 + 0 = 7$.

- **Upward anti-diagonal products:**
  - $(0) \cdot (3) \cdot (2) = 0$
  - $(1) \cdot (1) \cdot (1) = 1$
  - $(2) \cdot (0) \cdot (1) = 0$
  - Sum $= 0 + 1 + 0 = 1$.

Subtracting the anti-diagonal sum:

$\det A = 7 - 1 = 6.$

### 2. Theoretical Prediction for $\det B$

Matrix $B$ is obtained from $A$ by performing the elementary row operation $R_1 \leftrightarrow R_2$:

$B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}.$

**Determinant Property:** Interchanging any two rows (or columns) of an $n\times n$ matrix reverses the orientation of the row vectors, which negates the value of the determinant:

$\det B = -\det A.$

Since $\det A = 6$, we predict that:

$\det B = -6.$

### 3. Verification by Direct Calculation of $\det B$

We evaluate the determinant of matrix $B$ directly:

$\det B = \begin{vmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{vmatrix}.$

Applying Sarrus' rule:

- **Downward diagonal products:**
  - $(0) \cdot (2) \cdot (1) = 0$
  - $(3) \cdot (0) \cdot (2) = 0$
  - $(1) \cdot (1) \cdot (1) = 1$
  - Sum $= 0 + 0 + 1 = 1$.

- **Upward anti-diagonal products:**
  - $(1) \cdot (2) \cdot (2) = 4$
  - $(0) \cdot (1) \cdot (1) = 0$
  - $(3) \cdot (1) \cdot (1) = 3$
  - Sum $= 4 + 0 + 3 = 7$.

Subtracting the anti-diagonal sum:

$\det B = 1 - 7 = -6.$

The direct calculation yields $\det B = -6$, which precisely confirms the theoretical prediction $\det B = -\det A$.
