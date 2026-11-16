## Question

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
$$

2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## Solution

### 1. Case 1: Triangular Coefficient Matrix

- **Chosen Method:** **Direct Back-Substitution**.
- **Justification:** The coefficient matrix is already upper triangular:

$$
\begin{pmatrix}
2 & -1 \\
0 & 4 \\
\end{pmatrix}.
$$

  Gaussian elimination is completely unnecessary because all entries below the main diagonal are already zero. We can immediately solve for the variables starting from the bottom equation.

- **Complete Execution:**
  From equation 2:

$$
4y = 8 \implies y = 2.
$$

  Substitute $y = 2$ into equation 1:

$$
2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2}.
$$

  The unique solution is:

$$
(x, y) = \left(\frac{5}{2}, 2\right).
$$

### 2. Case 2: Three Systems $Ax = b_i$ with Known $A^{-1}$

- **Chosen Method:** **Matrix Inversion Multiplication ($x_i = A^{-1}b_i$)**.
- **Justification and Plan:**
  Because $A^{-1}$ is already given, the solution to each system $Ax = b_i$ is found by computing the matrix-vector product:

$$
x_1 = A^{-1} b_1, \qquad x_2 = A^{-1} b_2, \qquad x_3 = A^{-1} b_3.
$$

- **Reusable vs. Unnecessary Parts:**
  The precomputed inverse $A^{-1}$ is reused three times. Each solution requires only an $O(n^2)$ matrix-vector multiplication. Re-running Gaussian elimination from scratch three times on $[A \mid b_1]$, $[A \mid b_2]$, and $[A \mid b_3]$ would needlessly repeat the elimination on $A$ three times.

### 3. Case 3: One $3\times 3$ System Without Given $A^{-1}$

- **Chosen Method:** **Gaussian Elimination with Back-Substitution**.
- **Justification and Plan:**
  The goal is to find only a single solution vector $x$ for one specific right-hand side $b$.
  Set up the single augmented matrix $[A \mid b]$ and reduce it to upper triangular form via elementary row operations, followed by back-substitution.
- **Reusable vs. Unnecessary Parts:**
  Computing the full inverse matrix $A^{-1}$ is equivalent to performing elimination on $[A \mid I]$, which solves for 3 separate unit column vectors and requires about $n^3 = 27$ scalar multiplications/divisions.
  In contrast, Gaussian elimination on $[A \mid b]$ requires only about $\frac{n^3}{3} = 9$ operations. Calculating $A^{-1}$ when only one single solution vector is needed would require roughly three times as much work, making the extra computation entirely unnecessary.
