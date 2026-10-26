## Question

The matrix for a rotation through an angle $\theta$ is

$R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}.$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that $R(\alpha)R(\beta) = R(\alpha+\beta)$. Explain the result geometrically.

## Solution

### 1. Writing Out Both Rotation Matrices

$R(\alpha) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix}, \qquad R(\beta) = \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix}.$

### 2. Computing the Product $R(\alpha)R(\beta)$

Multiply the two matrices row by column:

$R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix}.$

Computing each entry:

**Entry $(1,1)$:**

$\cos\alpha \cdot \cos\beta + (-\sin\alpha) \cdot \sin\beta = \cos\alpha\cos\beta - \sin\alpha\sin\beta.$

**Entry $(1,2)$:**

$\cos\alpha \cdot (-\sin\beta) + (-\sin\alpha) \cdot \cos\beta = -\cos\alpha\sin\beta - \sin\alpha\cos\beta = -(\sin\alpha\cos\beta + \cos\alpha\sin\beta).$

**Entry $(2,1)$:**

$\sin\alpha \cdot \cos\beta + \cos\alpha \cdot \sin\beta = \sin\alpha\cos\beta + \cos\alpha\sin\beta.$

**Entry $(2,2)$:**

$\sin\alpha \cdot (-\sin\beta) + \cos\alpha \cdot \cos\beta = \cos\alpha\cos\beta - \sin\alpha\sin\beta.$

Assembling the result:

$R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\sin\alpha\cos\beta + \cos\alpha\sin\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \cos\alpha\cos\beta - \sin\alpha\sin\beta \end{pmatrix}.$

### 3. Applying the Angle-Sum Formulas

The standard trigonometric angle-sum identities state:

$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta,$

$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta.$

Substituting these into the product computed above:

$R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha+\beta).$

Therefore:

$R(\alpha)R(\beta) = R(\alpha+\beta).$

### 4. Geometric Interpretation

A rotation matrix $R(\theta)$ rotates every vector in the plane by angle $\theta$ counterclockwise about the origin. When two rotations are composed (applied one after the other), the combined effect is a single rotation by the sum of the two angles.

Specifically, applying $R(\beta)$ first rotates by $\beta$, and then applying $R(\alpha)$ rotates by a further $\alpha$. The result is a total rotation by $\alpha + \beta$, which is exactly $R(\alpha + \beta)$.

This shows that the set of all rotation matrices is **closed under multiplication**, and that the group structure of rotations (the circle group $SO(2)$) is faithfully captured by matrix multiplication. The identity element corresponds to $R(0) = I$ (no rotation), and the inverse of $R(\theta)$ is $R(-\theta)$, since:

$R(\theta)R(-\theta) = R(\theta + (-\theta)) = R(0) = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.$

The angle-sum formula for trigonometric functions is therefore not just an analytic identity — it is the algebraic manifestation of the composition law for planar rotations.
