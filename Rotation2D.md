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
\cos\\alpha & \sin\\alpha \\
-\sin\\alpha & \cos\\alpha
\end{bmatrix}
$$

This matrix can be derived from **counterclockwise** rotation matrix by replacing $\alpha$ with $-\alpha$, like this:

$$
\begin{bmatrix}
\cos(-\alpha) & -\sin(-\alpha) \\
\sin(-\alpha) & \cos(-\alpha)
\end{bmatrix} =
\begin{bmatrix}
\cos\\alpha & \sin\\alpha \\
-\sin\\alpha & \cos\\alpha
\end{bmatrix}
$$

because:

$$\cos(-\alpha) = \cos\alpha$$

and

$$\sin(-\alpha) = -\sin\alpha$$ 

## Using the rotation matrix

Having a vector

$\vec{v}=\begin{bmatrix}x\\y\end{bmatrix}$

the new vector $\vec{w}$
after **counterclockwise** rotation by angle $\alpha$ is calculated by:

$$
\vec{w}=R(\alpha)\cdot\vec{v}=
\begin{bmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha
\end{bmatrix}
\begin{bmatrix} x \\ y \end{bmatrix}=
\begin{bmatrix} x\cdot\cos\alpha-y\cdot\sin\alpha \\ x\cdot\sin\alpha+ y\cdot\cos\alpha \end{bmatrix}
$$

The new vector $\vec{z}$ after **clockwise** rotation by angle $\alpha$ is calculated by:

$$
\vec{z}=R(\alpha)\cdot\vec{v}=
\begin{bmatrix}
\cos\alpha & \sin\alpha \\
-\sin\alpha & \cos\alpha
\end{bmatrix}
\begin{bmatrix} x \\ y \end{bmatrix}=
\begin{bmatrix} x\cdot\cos\alpha+y\cdot\sin\alpha \\ -x\cdot\sin\alpha+ y\cdot\cos\alpha \end{bmatrix}
$$
