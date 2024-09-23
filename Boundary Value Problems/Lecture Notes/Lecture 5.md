**Name:** Stanley Goodwin
**Date:** 9/6/2024

---

Example: $u_x=u_{xx}+3u_y$
$$u(x,y)=Ae^{kx}e^{-\tfrac{3}{2}y}\left(Be^{\sqrt{\left(\tfrac{9}{4}+k\right)}y}+Ce^{-\sqrt{\left(\tfrac{9}{4}+k\right)}y}\right)$$
There are 3 kinds of solutions as always. Just be smart about it.
It's the same as before, blah blah blah.


Example: $u_{xx}-u_{xy}+u_{yy}=0$
$$\begin{align}
X''(x)Y(y)-X'(x)Y'(y)+X(x)Y''(y) &= 0\\
\dfrac{X''(x)}{X(x)}-\dfrac{X'(x)}{X(x)}\dfrac{Y'(y)}{Y(y)}+\dfrac{Y''(y)}{Y(y)} &= 0\\
\dfrac{\dfrac{d}{dx}\left(\dfrac{X''(x)}{X(x)}\right)}{\dfrac{d}{dx}\left(\dfrac{X'(x)}{X(x)}\right)} = \dfrac{Y'(y)}{Y(y)} &= k\\
X''(x)-kX'(x)+k^2X(x) &= 0\\
\end{align}$$
$$u(x,y)=Ae^{\tfrac{k}{2}x}\left(Ae^{i\tfrac{\sqrt{3}}{2}kx}+e^{-i\tfrac{\sqrt{3}}{2}kx}\right)e^{ky}$$

### Boundary Conditions
Given $ay''+by'+cy=0$:
 - The initial conditions are $y(0)=A$ and $y'(0)=B$ (1 point).
 - The boundary conditions are $y(a)=A$ and $y(b) = B$ (2 points).

Dirichlet Conditions: $y(a) = A$ and $y(a) = B$.
Neumann Conditions: $y'(a) = A$ and $y'(b) = B$.
Robin Conditions: $y(a) = A$ and $y'(b) = B$.


### Sturm-Liouville Problems
Eigenvalues / Eigenfunctions : $A\vec{x}=\lambda\vec{x} \implies \left(A-\lambda\mathbb{I}\right)\vec{x}=0$.
Eigenfunction $y$ and Eigenvalue $\lambda$.

Example: $y''+\lambda y = 0$, with $y(0)=y(1)=0$ (Dirichlet Conditions).
$$\begin{align}
y(x)&=Ae^{i\sqrt{\lambda}x}+Be^{-i\sqrt{\lambda}x}\\
y(0)&=A+B\\
y(1)&=A\sin(\sqrt{\lambda})=0\\
\end{align}$$
Either $\lambda=\left(\pi n\right)^2$ or $A=B=0$.
$$\begin{align}
y(x)&=Ae^{i(\pi n)x}-Ae^{-i(\pi n)x}\\
y_n(x)&= A\sin((n\pi)x)
\end{align}$$
