## Question

Let

$A=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}.$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then assume the formula holds for $n$, multiply by $A$, and prove it holds for $n+1$.

## Solution

### 1. Computing $A^2$

$A^2 = A \cdot A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}.$

- Entry $(1,1)$: $1 \cdot 1 + 1 \cdot 0 = 1$.
- Entry $(1,2)$: $1 \cdot 1 + 1 \cdot 1 = 2$.
- Entry $(2,1)$: $0 \cdot 1 + 1 \cdot 0 = 0$.
- Entry $(2,2)$: $0 \cdot 1 + 1 \cdot 1 = 1$.

$A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}.$

### 2. Computing $A^3$

$A^3 = A^2 \cdot A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}.$

- Entry $(1,1)$: $1 \cdot 1 + 2 \cdot 0 = 1$.
- Entry $(1,2)$: $1 \cdot 1 + 2 \cdot 1 = 3$.
- Entry $(2,1)$: $0$.
- Entry $(2,2)$: $1$.

$A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}.$

### 3. Computing $A^4$

$A^4 = A^3 \cdot A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}.$

- Entry $(1,2)$: $1 \cdot 1 + 3 \cdot 1 = 4$.
- All other entries as before.

$A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}.$

### 4. Observing the Pattern and Formulating the Conjecture

Listing the results side by side:

| Power $n$ | $A^n$ |
|-----------|-------|
| $1$ | $\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$ |
| $2$ | $\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$ |
| $3$ | $\begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$ |
| $4$ | $\begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$ |

The diagonal entries are always $1$ and the lower-left entry is always $0$. The upper-right entry equals $n$ in each case.

**Conjecture:**

$A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \quad \text{for all integers } n \geq 1.$

### 5. Proof by Mathematical Induction

**Base case ($n = 1$):** We have $A^1 = A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$, which matches the formula with $n = 1$. The base case holds.

**Inductive step:** Assume the formula holds for some integer $n \geq 1$, that is, assume

$A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}. \quad (\star)$

We want to show it follows that $A^{n+1} = \begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}$.

Multiply both sides of $(\star)$ on the right by $A$:

$A^{n+1} = A^n \cdot A = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}.$

Computing each entry:

- Entry $(1,1)$: $1 \cdot 1 + n \cdot 0 = 1$.
- Entry $(1,2)$: $1 \cdot 1 + n \cdot 1 = 1 + n = n + 1$.
- Entry $(2,1)$: $0 \cdot 1 + 1 \cdot 0 = 0$.
- Entry $(2,2)$: $0 \cdot 1 + 1 \cdot 1 = 1$.

Therefore:

$A^{n+1} = \begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}.$

This is exactly the conjecture formula with $n$ replaced by $n + 1$. The inductive step holds.

**Conclusion:** By the principle of mathematical induction, for all integers $n \geq 1$:

$A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}.$

### 6. Geometric Interpretation

The matrix $A$ represents a horizontal shear by 1 unit. Each application adds one more unit of shear, so $A^n$ is a horizontal shear by $n$ units — confirming the upper-right entry grows linearly with $n$.
