## Question

Given

$A=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix},\qquad B=\begin{pmatrix} a & b \\ c & d \end{pmatrix}.$

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

## Solution

### 1. Compute $AB$

Multiply $A$ on the left by $B$ on the right:

$AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} a & b \\ c & d \end{pmatrix}.$

Applying row-by-column multiplication:

- Entry $(1,1)$: $1 \cdot a + 1 \cdot c = a + c$.
- Entry $(1,2)$: $1 \cdot b + 1 \cdot d = b + d$.
- Entry $(2,1)$: $0 \cdot a + 1 \cdot c = c$.
- Entry $(2,2)$: $0 \cdot b + 1 \cdot d = d$.

Therefore:

$AB = \begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix}.$

### 2. Compute $BA$

Now multiply $B$ on the left by $A$ on the right:

$BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}.$

Applying row-by-column multiplication:

- Entry $(1,1)$: $a \cdot 1 + b \cdot 0 = a$.
- Entry $(1,2)$: $a \cdot 1 + b \cdot 1 = a + b$.
- Entry $(2,1)$: $c \cdot 1 + d \cdot 0 = c$.
- Entry $(2,2)$: $c \cdot 1 + d \cdot 1 = c + d$.

Therefore:

$BA = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}.$

### 3. Set $AB = BA$ and Derive the Conditions

Two matrices are equal if and only if all their corresponding entries are equal. Equating $AB$ and $BA$ entry by entry:

| Position | $AB$ entry | $BA$ entry | Equation |
|----------|-----------|-----------|----------|
| $(1,1)$ | $a + c$ | $a$ | $a + c = a$ |
| $(1,2)$ | $b + d$ | $a + b$ | $b + d = a + b$ |
| $(2,1)$ | $c$ | $c$ | $c = c$ (always true) |
| $(2,2)$ | $d$ | $c + d$ | $d = c + d$ |

Simplifying the non-trivial equations:

- From $(1,1)$: $a + c = a \implies c = 0$.
- From $(1,2)$: $b + d = a + b \implies d = a$.
- From $(2,2)$: $d = c + d \implies c = 0$ (same condition again).

### 4. General Form of All Matrices $B$ That Commute with $A$

The conditions are $c = 0$ and $d = a$, while $a$ and $b$ are free parameters. Substituting back:

$B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix},$

where $a, b \in \mathbb{R}$ are arbitrary.

This is the set of all upper-triangular matrices with equal diagonal entries (scalar multiples of the identity plus an upper off-diagonal term). Geometrically, these matrices represent the same family as $A$ itself — shear transformations combined with uniform scaling. It is no coincidence that $A$ commutes with matrices of its own type, since powers of $A$ all share this structure.

### 5. Verification

Let $B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$. Then:

$AB = \begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}, \qquad BA = \begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}.$

Indeed $AB = BA$, confirming the result.
