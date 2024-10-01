**Name:** Stanley Goodwin
**Date:** 10/01/2024
**Collaborators:** None

---

In this assignment, we will use the Cauchy Integral Formula to calculate the electrostatic potential $u(x,y)$ at the center of a disk of radius $R$, given the potential at its boundary.
The boundary condition for the potential on the circle of radius $r=R$ is given by:
$$u(r\cos\phi,r\sin\phi)=b(\phi)$$
To solve this problem, we ill assume (with no loss of generality) that $u(x,y)$ is the real part of a holomorphic function $f(z)=u(x,y)+iv(x,y)$ inside the disk, where $z=re^{i\phi}$.

---
## Question 1
### 1.1
*Calculate the potential $u(x,y)$ at the center of a disk of radius $R$, centered at the origin, in terms of the value of the potential at the boundary (a circle of radius $R$).*
**Note:** Use the right-hand side of the Cauchy Integral Formula: $f(\zeta)=\dfrac{1}{2\pi i}\displaystyle\oint\dfrac{f(z)}{z-\zeta}\ dz$, by interpreting $u(x,y)$ as the real part of $f(z)=u(x,y)+iv(x,y)$. 
$$\begin{align}
f(0)&=\dfrac{1}{2\pi i}\oint\dfrac{f(z)}{z}\ dz\\
&=\dfrac{1}{2\pi i}\int_0^{2\pi}\dfrac{f(Re^{i\phi})}{Re^{i\phi}}\ d\left(Re^{i\phi}\right)\\
&=\dfrac{1}{2\pi i}\int_0^{2\pi}\dfrac{b(\phi)\cdot iRe^{i\phi}}{Re^{i\phi}}\ d\theta\\
f(0)&=\dfrac{1}{2\pi}\int_0^{2\pi}b(\phi)\ d\theta\\
\Re(f(0))&=\dfrac{1}{2\pi}\int_0^{2\pi}b(\phi)\ d\theta\\
\Aboxed{u(0,0)&=\dfrac{1}{2\pi}\int_0^{2\pi}b(\phi)\ d\theta}
\end{align}$$
### 1.2
Write the contour integral explicitly by parametrizing it with polar coordinates centered around the origin, proving the following formula: $u(0,0)=\dfrac{1}{2\pi}\displaystyle\int_0^{2\pi} b(\phi)\ d\phi$
$$\begin{align}
...
\end{align}$$
---
## Question 2
