**Name:** Stanley Goodwin
**Date:** 11/21/2024

---
## Coulomb Potential in $N$ Dimensions
We start with Laplace's Equation for electromagnetism:
$$\begin{align}
\vec\nabla^2\phi(\vec{x})&=-4\pi\rho(\vec{x})\\
\phi(\vec{x})&=\int\dfrac{\rho(\vec{x}')}{|\vec{x}-\vec{x}'|}\ d^n\vec{x}'\\
&=\int\dfrac{1}{|\vec{x}-\vec{x}'|}\rho(\vec{x}')\ d^n\vec{x}'\\
&=\int G(\vec{x}-\vec{x}')\rho(\vec{x}')\ d^n\vec{x}'\\
\end{align}$$
Which leads to the Green's function equation:
$$\begin{align}
\vec\nabla^2G(\vec{x})&=-4\pi\delta(\vec{x})\\
G(\vec{x})&=\dfrac{1}{|\vec{x}|}
\end{align}$$
### Solving for the Green's Function
We will consider the Green's function as a limit of $\epsilon$.
$$\begin{align}
\vec\nabla^2G_\epsilon(\vec{x})&=-4\pi\delta_\epsilon(\vec{x})\\
\end{align}$$
In this case, we'll look at isotropic solutions, where $G_\epsilon(\vec{x})=f_\epsilon(r)$, where $r=|\vec{x}|$.
$$\begin{align}
\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial f_\epsilon(r)}{\partial r}\right)&=-4\pi\delta_\epsilon(r)
\end{align}$$
For integrating over spheres in $N$ dimensions, we can notice that the determinant Jacobian of $N$-spherical space, after integrating over all except $r$, will take the form $|J|=C_n r^{n-1}$
$$\begin{align}
-4\pi\int\delta_\epsilon(r)\ dr&=\iint\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial f_\epsilon(r)}{\partial r}\right)|J|\ dr\ d\Omega\\
&=C_n\int\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial f_\epsilon(r)}{\partial r}\right)r^{n-1}\ dr\\
-4\pi\int_0^\infty\delta_\epsilon(r)\ dr&=\iint\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial f_\epsilon(r)}{\partial r}\right)|J|\ dr\ d\Omega\\
\Aboxed{-\dfrac{2\pi}{C_n}&=\int r^{n-3}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial f_\epsilon(r)}{\partial r}\right)\ dr}
\end{align}$$
We can pull some trickery where we take the derivative of both sides:
$$\begin{align}
0&=r^{n-3}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial f_\epsilon(r)}{\partial r}\right)\\
0&=\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial f_\epsilon(r)}{\partial r}\right)\\
A/r^2&=\dfrac{\partial f_\epsilon(r)}{\partial r}\\
\Aboxed{f_\epsilon(r)&=\dfrac{A}{r}+B}
\end{align}$$
I don't know if this is correct, but works for 3D.

## Coulomb Potential in 1 Dimension
$$\begin{align}
\dfrac{\partial^2}{\partial x^2}G_\epsilon(x)&=\delta_\epsilon(x)\\
\iint \dfrac{\partial^2}{\partial x^2}G_\epsilon(x)\ dx^2&=\int\left(\int_0^\infty\delta_\epsilon(x)\ dx\right)dx\\
G_\epsilon(x)&=\int\dfrac{1}{2}dx\\
\Aboxed{G_\epsilon(x)&=\dfrac{1}{2}x+C_0}
\end{align}$$
Taking the limit as $\epsilon\rightarrow0$, then:
$$\begin{align}
\Aboxed{G(x)&=\dfrac{1}{2}x+C_0}
\end{align}$$
