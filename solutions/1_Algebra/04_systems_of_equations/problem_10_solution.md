## Question

Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

## Solution

### 1. Setting Up the System of Equations

The polynomial is $p(x) = ax^2 + bx + c$.
Requiring the graph of $p(x)$ to pass through the given points yields three linear equations in the unknowns $a, b, c$:

1. Passes through $(0, 1)$:

$$
p(0) = a(0)^2 + b(0) + c = 1 \implies c = 1.
$$

2. Passes through $(1, 3)$:

$$
p(1) = a(1)^2 + b(1) + c = 3 \implies a + b + c = 3.
$$

3. Passes through $(2, 9)$:

$$
p(2) = a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9.
$$

Writing this as a linear system:

$$
\begin{cases}
c = 1, \\
a + b + c = 3, \\
4a + 2b + c = 9.
\end{cases}
$$

### 2. Solving the System

Substitute $c = 1$ into equations 2 and 3:

$$
\begin{cases}
a + b + 1 = 3 \implies a + b = 2, \\
4a + 2b + 1 = 9 \implies 4a + 2b = 8 \implies 2a + b = 4.
\end{cases}
$$

Subtract the first equation from the second:

$$
(2a + b) - (a + b) = 4 - 2 \implies a = 2.
$$

Now solve for $b$ using $a + b = 2$:

$$
2 + b = 2 \implies b = 0.
$$

Thus, the unique coefficients are:

$$
a = 2, \qquad b = 0, \qquad c = 1.
$$

The required polynomial is:

$$
p(x) = 2x^2 + 1.
$$

### 3. Verification by Substituting the Given Points

- Point $(0, 1)$: $p(0) = 2(0)^2 + 1 = 0 + 1 = 1$. (Matches $y = 1$)
- Point $(1, 3)$: $p(1) = 2(1)^2 + 1 = 2(1) + 1 = 3$. (Matches $y = 3$)
- Point $(2, 9)$: $p(2) = 2(2)^2 + 1 = 2(4) + 1 = 8 + 1 = 9$. (Matches $y = 9$)

All three points lie on the graph of $p(x) = 2x^2 + 1$, confirming the result.
