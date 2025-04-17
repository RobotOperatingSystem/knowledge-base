# Rotations in 2D

To rotate a point or vector about origin in 2D space, a rotation matrix is used.

## Counterclockwise rotation

The general form of the 2D rotation matrix $R$ for a **counterclockwise** rotation by an angle $\alpha$ is:

$$
R(\alpha) =
\begin{bmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha
\end{bmatrix}
$$

## Clockwise rotation

The general form of the 2D rotation matrix $R$ for a **clockwise** rotation by an angle $\alpha$ is:

$$
R(\alpha) =
\begin{bmatrix}
\cos\alpha & \sin\alpha \\
-\sin\alpha & \cos\alpha
\end{bmatrix}
$$

> [!TIP]
> *Clockwise* rotation matrix can be derived from **counterclockwise** rotation matrix
> by replacing $\alpha$ with $-\alpha$, like shown below:

$$
\begin{bmatrix}
\cos(-\alpha) & -\sin(-\alpha) \\
\sin(-\alpha) & \cos(-\alpha)
\end{bmatrix} =
\begin{bmatrix}
\cos\alpha & \sin\alpha \\
-\sin\alpha & \cos\alpha
\end{bmatrix}
$$

while $\cos(-\alpha) = \cos\alpha$ and $\sin(-\alpha) = -\sin\alpha$ 

## Using the rotation matrix

Having a vector $\vec{v}$:

$$
\vec{v}=
\begin{bmatrix}
x \\
y 
\end{bmatrix}
$$

the new vector $\vec{w}$
after **counterclockwise** rotation by angle $\alpha$ is calculated by:

$$
\vec{w}=R(\alpha)\cdot\vec{v}=
\begin{bmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}=
\begin{bmatrix}
x\cdot\cos\alpha-y\cdot\sin\alpha \\
x\cdot\sin\alpha+ y\cdot\cos\alpha
\end{bmatrix}
$$

The new vector $\vec{z}$ after **clockwise** rotation by angle $\alpha$ is calculated by:

$$
\vec{z}=R(\alpha)\cdot\vec{v}=
\begin{bmatrix}
\cos\alpha & \sin\alpha \\
-\sin\alpha & \cos\alpha
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}=
\begin{bmatrix}
x\cdot\cos\alpha+y\cdot\sin\alpha \\
-x\cdot\sin\alpha+ y\cdot\cos\alpha
\end{bmatrix}
$$

## Example

> [!WARNING]
> The following example is a little bit weird, so be careful!

Let's have a vector $\vec{u}$:

$$
\vec{u}=
\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$

and a vector $\vec{v}$:

$$
\vec{v}=
\begin{bmatrix}
1 \\
2
\end{bmatrix}
$$

Vector $\vec{v}$ is a **counterclockwise** rotated vector $\vec{u}$ about the origin by angle $\alpha$.

**Question**: What is the value of the angle $\alpha$? 

**Answer**:

$$
\begin{bmatrix}
1 \\
2
\end{bmatrix}=
\begin{bmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha
\end{bmatrix}
\begin{bmatrix}
2 \\
1
\end{bmatrix}=
\begin{bmatrix}
2\cdot\cos\alpha-\sin\alpha \\
2\cdot\sin\alpha+ \cos\alpha
\end{bmatrix}
$$

So we have two equations:

$$
1 = 2\cdot\cos\alpha-\sin\alpha
$$
$$
2 = 2\cdot\sin\alpha+\cos\alpha
$$

From the first one we calculate $\sin\alpha$:

$$
\sin\alpha=2\cdot\cos\alpha-1
$$

and substitute $\sin\alpha$ in the second equation:

$$
2=2\cdot(2\cdot\cos\alpha-1) + \cos\alpha=4\cdot\cos\alpha-2+\cos\alpha=5\cdot\cos\alpha-2
$$

We calculate now the value of $\alpha$:

$$
2=5\cdot\cos\alpha-2
$$

$$
4=5\cdot\cos\alpha
$$

$$
\cos\alpha = \frac{4}{5}
$$

$$
\alpha = \cos^{-1}(\frac{4}{5})\thickapprox0.6435011087932843\ rad\thickapprox36.86989764584401^{\circ}
$$
