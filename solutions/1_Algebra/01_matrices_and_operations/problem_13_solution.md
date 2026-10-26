## Question

Let

$F=\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}.$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the Fibonacci sequence $0, 1, 1, 2, 3, 5, 8, \ldots$ and describe the relationship observed. Then compute $F\begin{pmatrix} a \\ b \end{pmatrix}$ and explain how this multiplication performs one recurrence step.

## Solution

### 1. Computing Powers of $F$

**Computing $F^2$:**

$F^2 = F \cdot F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}.$

- Entry $(1,1)$: $1 \cdot 1 + 1 \cdot 1 = 2$.
- Entry $(1,2)$: $1 \cdot 1 + 1 \cdot 0 = 1$.
- Entry $(2,1)$: $1 \cdot 1 + 0 \cdot 1 = 1$.
- Entry $(2,2)$: $1 \cdot 1 + 0 \cdot 0 = 1$.

$F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}.$

**Computing $F^3$:**

$F^3 = F^2 \cdot F = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}.$

- Entry $(1,1)$: $2 \cdot 1 + 1 \cdot 1 = 3$.
- Entry $(1,2)$: $2 \cdot 1 + 1 \cdot 0 = 2$.
- Entry $(2,1)$: $1 \cdot 1 + 1 \cdot 1 = 2$.
- Entry $(2,2)$: $1 \cdot 1 + 1 \cdot 0 = 1$.

$F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}.$

**Computing $F^4$:**

$F^4 = F^3 \cdot F = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}.$

- Entry $(1,1)$: $3 \cdot 1 + 2 \cdot 1 = 5$.
- Entry $(1,2)$: $3 \cdot 1 + 2 \cdot 0 = 3$.
- Entry $(2,1)$: $2 \cdot 1 + 1 \cdot 1 = 3$.
- Entry $(2,2)$: $2 \cdot 1 + 1 \cdot 0 = 2$.

$F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}.$

**Computing $F^5$:**

$F^5 = F^4 \cdot F = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}.$

- Entry $(1,1)$: $5 \cdot 1 + 3 \cdot 1 = 8$.
- Entry $(1,2)$: $5 \cdot 1 + 3 \cdot 0 = 5$.
- Entry $(2,1)$: $3 \cdot 1 + 2 \cdot 1 = 5$.
- Entry $(2,2)$: $3 \cdot 1 + 2 \cdot 0 = 3$.

$F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}.$

### 2. Comparison with the Fibonacci Sequence

Recall the Fibonacci sequence, indexed from $f_0$:

$f_0 = 0,\quad f_1 = 1,\quad f_2 = 1,\quad f_3 = 2,\quad f_4 = 3,\quad f_5 = 5,\quad f_6 = 8,\quad \ldots$

Listing the computed powers:

| Power $n$ | $F^n$ | Entries |
|-----------|-------|---------|
| $1$ | $\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$ | $f_2, f_1, f_1, f_0$ |
| $2$ | $\begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$ | $f_3, f_2, f_2, f_1$ |
| $3$ | $\begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$ | $f_4, f_3, f_3, f_2$ |
| $4$ | $\begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$ | $f_5, f_4, f_4, f_3$ |
| $5$ | $\begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$ | $f_6, f_5, f_5, f_4$ |

The pattern is clear:

$F^n = \begin{pmatrix} f_{n+1} & f_n \\ f_n & f_{n-1} \end{pmatrix},$

where $f_k$ denotes the $k$-th Fibonacci number. Each power of $F$ encodes four consecutive Fibonacci numbers arranged symmetrically (the matrix is symmetric), with the top-left entry being $f_{n+1}$.

### 3. One Recurrence Step via Matrix-Vector Multiplication

Compute $F\begin{pmatrix} a \\ b \end{pmatrix}$:

$F\begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 \cdot a + 1 \cdot b \\ 1 \cdot a + 0 \cdot b \end{pmatrix} = \begin{pmatrix} a + b \\ a \end{pmatrix}.$

**Interpretation:** If we think of the input vector $\begin{pmatrix} a \\ b \end{pmatrix}$ as encoding two consecutive Fibonacci numbers — with $a = f_{k+1}$ (the current term) and $b = f_k$ (the previous term) — then after multiplying by $F$ we obtain $\begin{pmatrix} a + b \\ a \end{pmatrix} = \begin{pmatrix} f_{k+2} \\ f_{k+1} \end{pmatrix}$.

This is exactly one step of the Fibonacci recurrence $f_{k+2} = f_{k+1} + f_k$:

- The new top entry is $a + b$, the next Fibonacci number.
- The new bottom entry is $a$, which becomes the "previous" term for the following step.

Applying $F$ repeatedly starting from $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$ generates the entire Fibonacci sequence:

$\begin{pmatrix} 1 \\ 0 \end{pmatrix} \xrightarrow{F} \begin{pmatrix} 1 \\ 1 \end{pmatrix} \xrightarrow{F} \begin{pmatrix} 2 \\ 1 \end{pmatrix} \xrightarrow{F} \begin{pmatrix} 3 \\ 2 \end{pmatrix} \xrightarrow{F} \begin{pmatrix} 5 \\ 3 \end{pmatrix} \xrightarrow{F} \cdots$

Thus, matrix multiplication by $F$ is an elegant linear-algebraic encoding of the Fibonacci recurrence.
