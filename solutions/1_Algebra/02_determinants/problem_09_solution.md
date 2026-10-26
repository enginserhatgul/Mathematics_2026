## Question

The vectors

$u = \begin{pmatrix} 3 \\ 1 \end{pmatrix},\qquad v = \begin{pmatrix} 1 \\ 4 \end{pmatrix}$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

## Solution

### 1. Geometric Definition of Area via the Determinant

In $\mathbb{R}^2$, the determinant of a $2\times 2$ matrix formed by two column vectors $u = \begin{pmatrix} u_1 \\ u_2 \end{pmatrix}$ and $v = \begin{pmatrix} v_1 \\ v_2 \end{pmatrix}$ represents the **oriented (signed) area** of the parallelogram spanned by $u$ and $v$:

$\mathrm{Area}(P) = |\det(u \mid v)| = \left| \begin{vmatrix} u_1 & v_1 \\ u_2 & v_2 \end{vmatrix} \right|.$

The sign of the determinant provides orientation information, while its absolute value gives the true geometric area.

### 2. Computation of the Determinant with Order $(u, v)$

Construct the matrix $M = (u \mid v)$ whose columns are $u$ and $v$:

$M = \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix}.$

Evaluating the determinant:

$\det M = \begin{vmatrix} 3 & 1 \\ 1 & 4 \end{vmatrix} = (3)(4) - (1)(1) = 12 - 1 = 11.$

Taking the absolute value, the geometric area of the parallelogram is:

$\mathrm{Area}(P) = |11| = 11.$

### 3. Computation of the Determinant with Reversed Order $(v, u)$

Now construct the matrix $N = (v \mid u)$ where the columns are reversed:

$N = \begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix}.$

Evaluating this determinant:

$\det N = \begin{vmatrix} 1 & 3 \\ 4 & 1 \end{vmatrix} = (1)(1) - (3)(4) = 1 - 12 = -11.$

### 4. Detailed Analysis: What Changes vs. What Does Not Change

#### What Changes: The Sign of the Determinant (Orientation)

- Swapping the columns of a matrix interchanges two vectors, which reverses the sign of the determinant according to the column-swap property:
  $\det(v \mid u) = -\det(u \mid v) = -11.$
- Geometrically, this sign change corresponds to a reversal in **orientation**:
  - The ordered pair $(u, v)$ forms a **counterclockwise** orientation (the angle sweeping from vector $u$ to vector $v$ through the interior of the parallelogram is positive/counterclockwise).
  - The ordered pair $(v, u)$ forms a **clockwise** orientation (sweeping from vector $v$ to vector $u$ is negative/clockwise).

#### What Does Not Change: The Geometric Area

- The physical, geometric surface area of the parallelogram depends solely on the shape and size of the boundary defined by $u$ and $v$. It is given by the formula $\mathrm{Area} = \|u\| \|v\| \sin\theta$, where $\theta$ is the angle between the vectors.
- Taking the absolute value of the determinant discards the directional orientation:
  $\mathrm{Area}(P) = |-11| = 11.$
- Therefore, the **geometric area remains completely invariant** under vector order reversal.
