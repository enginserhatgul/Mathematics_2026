## Question

Without expanding the determinant, compute

$\det \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}.$

State the rule for an arbitrary triangular matrix and explain it using this example.

## Solution

### 1. Statement of the General Rule for Triangular Matrices

A square matrix is called **upper triangular** if all entries below the main diagonal are zero ($t_{ij} = 0$ for $i > j$), and **lower triangular** if all entries above the main diagonal are zero ($t_{ij} = 0$ for $i < j$). A **diagonal matrix** is both upper and lower triangular.

**Rule:** The determinant of any triangular (or diagonal) matrix equals the product of its main diagonal entries:

$\det T = \prod_{i=1}^n t_{ii} = t_{11} t_{22} \cdots t_{nn}.$

### 2. Application to the Given Matrix

The matrix

$T = \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}$

is upper triangular because all entries strictly below the main diagonal are zero ($t_{21} = 0$, $t_{31} = 0$, $t_{32} = 0$).

Applying the diagonal product rule directly:

$\det T = \begin{vmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{vmatrix} = (2) \cdot (-3) \cdot (7) = -42.$

### 3. Theoretical Explanation: Why Off-Diagonal Terms Vanish

To understand why only the diagonal entries contribute to the determinant, we can analyze the structure through two perspectives:

#### Perspective A: Successive Laplace Expansion

Expanding along the first column, which contains zeros in all positions below the first entry:

$\begin{vmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{vmatrix} = 2 \cdot \begin{vmatrix} -3 & 5 \\ 0 & 7 \end{vmatrix} - 0 \cdot \begin{vmatrix} 4 & 1 \\ 0 & 7 \end{vmatrix} + 0 \cdot \begin{vmatrix} 4 & 1 \\ -3 & 5 \end{vmatrix}.$

The only non-zero contribution comes from the $(1,1)$ entry. The remaining $2\times 2$ minor is again upper triangular:

$\begin{vmatrix} -3 & 5 \\ 0 & 7 \end{vmatrix} = (-3)(7) - (5)(0) = -21.$

Multiplying by the leading element:

$\det T = 2 \cdot (-21) = -42.$

#### Perspective B: The Permutation (Leibniz) Formula

The complete expansion of an $n\times n$ determinant is given by the sum over all permutations $\sigma \in S_n$:

$\det T = \sum_{\sigma \in S_n} \mathrm{sgn}(\sigma) \prod_{i=1}^n t_{i, \sigma(i)}.$

For any permutation $\sigma$ other than the identity permutation ($\sigma \neq \mathrm{id}$), there must exist at least one index $i$ such that $\sigma(i) < i$. In an upper triangular matrix, every entry with $\sigma(i) < i$ lies strictly below the main diagonal and is therefore equal to $0$.

Consequently, every term in the sum corresponding to a non-identity permutation contains at least one zero factor and vanishes completely. The only surviving term is the one corresponding to the identity permutation $\sigma(i) = i$:

$\det T = \mathrm{sgn}(\mathrm{id}) \cdot t_{11} t_{22} t_{33} = (1) \cdot (2) \cdot (-3) \cdot (7) = -42.$
