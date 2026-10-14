## Question

The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Solution

### 1. Dimension Compatibility Condition

For the matrix product $X Y$ to be defined, the number of columns in the left matrix $X$ must equal the number of rows in the right matrix $Y$.

If matrix $X$ has size $m\times k$ and matrix $Y$ has size $k\times n$, the inner dimensions match ($k=k$). The product $X Y$ is defined and produces a matrix of size $m\times n$ (the outer dimensions):

$$
(m\times k)\cdot (k\times n)\implies m\times n.
$$

If the inner dimensions differ, the product is undefined.

### 2. Evaluation of Each Product

1. Product $AB$:
   - Sizes: $A_{2\times 3}$ and $B_{3\times 4}$.
   - Inner dimensions: $3 = 3$ (match).
   - Conclusion: Defined, resulting in size $2\times 4$.

2. Product $BA$:
   - Sizes: $B_{3\times 4}$ and $A_{2\times 3}$.
   - Inner dimensions: $4 \neq 2$ (mismatch).
   - Conclusion: Undefined.

3. Product $BC$:
   - Sizes: $B_{3\times 4}$ and $C_{4\times 2}$.
   - Inner dimensions: $4 = 4$ (match).
   - Conclusion: Defined, resulting in size $3\times 2$.

4. Product $CB$:
   - Sizes: $C_{4\times 2}$ and $B_{3\times 4}$.
   - Inner dimensions: $2 \neq 3$ (mismatch).
   - Conclusion: Undefined.

5. Product $AC$:
   - Sizes: $A_{2\times 3}$ and $C_{4\times 2}$.
   - Inner dimensions: $3 \neq 4$ (mismatch).
   - Conclusion: Undefined.

6. Product $CA$:
   - Sizes: $C_{4\times 2}$ and $A_{2\times 3}$.
   - Inner dimensions: $2 = 2$ (match).
   - Conclusion: Defined, resulting in size $4\times 3$.

7. Product $AD$:
   - Sizes: $A_{2\times 3}$ and $D_{2\times 2}$.
   - Inner dimensions: $3 \neq 2$ (mismatch).
   - Conclusion: Undefined.

8. Product $DA$:
   - Sizes: $D_{2\times 2}$ and $A_{2\times 3}$.
   - Inner dimensions: $2 = 2$ (match).
   - Conclusion: Defined, resulting in size $2\times 3$.

### 3. Summary Table

| Product | Left Matrix | Right Matrix | Inner Check | Status | Result Size |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $AB$ | $2\times 3$ | $3\times 4$ | $3 = 3$ | Defined | $2\times 4$ |
| $BA$ | $3\times 4$ | $2\times 3$ | $4 \neq 2$ | Undefined | — |
| $BC$ | $3\times 4$ | $4\times 2$ | $4 = 4$ | Defined | $3\times 2$ |
| $CB$ | $4\times 2$ | $3\times 4$ | $2 \neq 3$ | Undefined | — |
| $AC$ | $2\times 3$ | $4\times 2$ | $3 \neq 4$ | Undefined | — |
| $CA$ | $4\times 2$ | $2\times 3$ | $2 = 2$ | Defined | $4\times 3$ |
| $AD$ | $2\times 3$ | $2\times 2$ | $3 \neq 2$ | Undefined | — |
| $DA$ | $2\times 2$ | $2\times 3$ | $2 = 2$ | Defined | $2\times 3$ |

### 4. Mathematical Explanation

Every entry $(X Y)_{ij}$ of a matrix product is defined as the scalar dot product of row $i$ of $X$ and column $j$ of $Y$:

$$
(XY)_{ij}=\sum_{r=1}^k x_{ir} y_{rj}.
$$

For this sum to exist, the number of components in row vector $x_i$ (the column dimension of $X$) must equal the number of components in column vector $y_j$ (the row dimension of $Y$). When these dimensions do not match, the dot product cannot be formed.
