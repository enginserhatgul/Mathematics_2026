## Question

Given

$A=\begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix},\quad B=\begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix},\quad C=\begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}.$

Compute $(AB)C$ and $A(BC)$ step-by-step. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## Solution

### 1. Checking Dimensions

Before computing, verify that all products are defined:

- $A$ is $2 \times 3$, $B$ is $3 \times 2$: $AB$ is $2 \times 2$.
- $(AB)$ is $2 \times 2$, $C$ is $2 \times 2$: $(AB)C$ is $2 \times 2$.
- $B$ is $3 \times 2$, $C$ is $2 \times 2$: $BC$ is $3 \times 2$.
- $A$ is $2 \times 3$, $(BC)$ is $3 \times 2$: $A(BC)$ is $2 \times 2$.

All products are well-defined and both paths yield a $2 \times 2$ result.

---

### Path 1: Computing $(AB)C$

#### Step 1a: Compute $AB$

$AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}.$

Computing each entry row-by-column:

- $(AB)_{11}$: $1 \cdot 1 + 2 \cdot 2 + 0 \cdot (-1) = 1 + 4 + 0 = 5$.
- $(AB)_{12}$: $1 \cdot 0 + 2 \cdot 1 + 0 \cdot 3 = 0 + 2 + 0 = 2$.
- $(AB)_{21}$: $0 \cdot 1 + 1 \cdot 2 + 1 \cdot (-1) = 0 + 2 - 1 = 1$.
- $(AB)_{22}$: $0 \cdot 0 + 1 \cdot 1 + 1 \cdot 3 = 0 + 1 + 3 = 4$.

$AB = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix}.$

#### Step 1b: Compute $(AB)C$

$(AB)C = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}.$

Computing each entry:

- $((AB)C)_{11}$: $5 \cdot 2 + 2 \cdot 0 = 10 + 0 = 10$.
- $((AB)C)_{12}$: $5 \cdot 1 + 2 \cdot (-1) = 5 - 2 = 3$.
- $((AB)C)_{21}$: $1 \cdot 2 + 4 \cdot 0 = 2 + 0 = 2$.
- $((AB)C)_{22}$: $1 \cdot 1 + 4 \cdot (-1) = 1 - 4 = -3$.

$(AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.$

---

### Path 2: Computing $A(BC)$

#### Step 2a: Compute $BC$

$BC = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}.$

Computing each entry:

- $(BC)_{11}$: $1 \cdot 2 + 0 \cdot 0 = 2$.
- $(BC)_{12}$: $1 \cdot 1 + 0 \cdot (-1) = 1$.
- $(BC)_{21}$: $2 \cdot 2 + 1 \cdot 0 = 4$.
- $(BC)_{22}$: $2 \cdot 1 + 1 \cdot (-1) = 2 - 1 = 1$.
- $(BC)_{31}$: $(-1) \cdot 2 + 3 \cdot 0 = -2$.
- $(BC)_{32}$: $(-1) \cdot 1 + 3 \cdot (-1) = -1 - 3 = -4$.

$BC = \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}.$

#### Step 2b: Compute $A(BC)$

$A(BC) = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}.$

Computing each entry:

- $(A(BC))_{11}$: $1 \cdot 2 + 2 \cdot 4 + 0 \cdot (-2) = 2 + 8 + 0 = 10$.
- $(A(BC))_{12}$: $1 \cdot 1 + 2 \cdot 1 + 0 \cdot (-4) = 1 + 2 + 0 = 3$.
- $(A(BC))_{21}$: $0 \cdot 2 + 1 \cdot 4 + 1 \cdot (-2) = 0 + 4 - 2 = 2$.
- $(A(BC))_{22}$: $0 \cdot 1 + 1 \cdot 1 + 1 \cdot (-4) = 0 + 1 - 4 = -3$.

$A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.$

---

### 3. Comparing the Results

Both computation paths yield the same result:

$(AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix} = A(BC).$

This confirms the **associativity of matrix multiplication**: $(AB)C = A(BC)$.

### 4. Counting Intermediate Operations

Each entry of a matrix product of a $p \times q$ matrix with a $q \times r$ matrix requires $q$ multiplications and $q-1$ additions, giving $2q - 1$ arithmetic operations per entry, across $p \cdot r$ entries total.

| Step | Dimensions | Entries to compute | Operations per entry | Total (approx.) |
|------|-----------|-------------------|---------------------|-----------------|
| $AB$ (Path 1) | $(2 \times 3)(3 \times 2) \to 2 \times 2$ | 4 | $2 \cdot 3 - 1 = 5$ | $\approx 20$ |
| $(AB)C$ (Path 1) | $(2 \times 2)(2 \times 2) \to 2 \times 2$ | 4 | $2 \cdot 2 - 1 = 3$ | $\approx 12$ |
| **Path 1 total** | | | | **$\approx 32$** |
| $BC$ (Path 2) | $(3 \times 2)(2 \times 2) \to 3 \times 2$ | 6 | $2 \cdot 2 - 1 = 3$ | $\approx 18$ |
| $A(BC)$ (Path 2) | $(2 \times 3)(3 \times 2) \to 2 \times 2$ | 4 | $2 \cdot 3 - 1 = 5$ | $\approx 20$ |
| **Path 2 total** | | | | **$\approx 38$** |

In this example, Path 1 (grouping $AB$ first) is slightly more efficient because the intermediate matrix is smaller. This illustrates that while associativity guarantees **the result is always the same**, the **computational cost can differ** depending on the chosen grouping. In practice — especially for very large matrices or chains of many matrices — choosing the optimal parenthesization (the *matrix chain multiplication* problem) can dramatically reduce computation time.

### 5. What Associativity Means

Associativity means that when multiplying a chain of matrices, the **order of operations** (which pair is multiplied first) does **not affect the final result** — only the **order of the matrices themselves** matters. We can freely regroup the multiplications for computational convenience without changing the answer.

This property distinguishes matrix multiplication from operations where grouping changes the result (e.g., matrix subtraction: $(A - B) - C \neq A - (B - C)$ in general).
