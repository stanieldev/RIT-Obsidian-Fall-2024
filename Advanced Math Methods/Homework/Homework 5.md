**Name:** Stanley Goodwin
**Date:** 10/01/2024
**Collaborators:** None

---

In this assignment, we will use the Cauchy Integral Formula to calculate the electrostatic potential $u(x,y)$ at the center of a disk of radius $R$, given the potential at its boundary.
The boundary condition for the potential on the circle of radius $r=R$ is given by:
$$u(R\cos\phi,R\sin\phi)=b(\phi)$$
To solve this problem, we'll assume (with no loss of generality) that $u(x,y)$ is the real part of a holomorphic function $f(z)=u(x,y)+iv(x,y)$ inside the disk, where $z=re^{i\phi}$.

---
## Question 1
### 1.1
*Calculate the potential $u(x,y)$ at the center of a disk of radius $R$, centered at the origin, in terms of the value of the potential at the boundary (a circle of radius $R$).*
**Note:** Use the right-hand side of the Cauchy Integral Formula: $f(\zeta)=\dfrac{1}{2\pi i}\displaystyle\oint\dfrac{f(z)}{z-\zeta}\ dz$, by interpreting $u(x,y)$ as the real part of $f(z)=u(x,y)+iv(x,y)$. 
$$\begin{align}
f(0+0i)&=\dfrac{1}{2\pi i}\oint\dfrac{f(z)}{z}\ dz\\
&=\dfrac{1}{2\pi i}\oint\dfrac{u(x,y)+iv(x,y)}{x+iy}\cdot\left(dx+idy\right)\\
&=\dfrac{1}{2\pi i}\oint\dfrac{u(R\cos\phi,R\sin\phi)}{Re^{i\phi}}\ iRe^{i\phi}\ d\phi+\dfrac{1}{2\pi i}\oint\dfrac{iv(R\cos\phi,R\sin\phi)}{Re^{i\phi}}\ iRe^{i\phi}\ d\phi\\
&=\dfrac{1}{2\pi }\oint u(R\cos\phi,R\sin\phi)\ d\phi+i\dfrac{1}{2\pi }\oint v(R\cos\phi,R\sin\phi)\ d\phi\\
\Re\left(f(0+0i)\right)&=\dfrac{1}{2\pi }\oint u(R\cos\phi,R\sin\phi)\ d\phi\\
\Aboxed{u(0,0)&=\dfrac{1}{2\pi }\oint b(\phi)\ d\phi}
\end{align}$$
### 1.2
*Write the contour integral explicitly by parametrizing it with polar coordinates centered around the origin, proving the following formula:* $u(0,0)=\dfrac{1}{2\pi}\displaystyle\int_0^{2\pi} b(\phi)\ d\phi$
$$\begin{align}
f(0+0i)&=\dfrac{1}{2\pi i}\oint\dfrac{f(z)}{z}\ dz\\
&=\dfrac{1}{2\pi i}\int_0^{2\pi}\dfrac{f(Re^{i\phi})}{Re^{i\phi}}\ d\left(Re^{i\phi}\right)\\
&=\dfrac{1}{2\pi i}\int_0^{2\pi}\dfrac{(b(\phi)+i\tilde{b}(\phi))\cdot iRe^{i\phi}}{Re^{i\phi}}\ d\phi\\
&=\dfrac{1}{2\pi}\int_0^{2\pi}(b(\phi)+i\tilde{b}(\phi))\ d\phi\\
&=\dfrac{1}{2\pi}\int_0^{2\pi}b(\phi)\ d\phi+i\dfrac{1}{2\pi}\int_0^{2\pi}\tilde{b}(\phi)\ d\phi\\
\Re(f(0))&=\Re\left(\dfrac{1}{2\pi}\int_0^{2\pi}b(\phi)\ d\phi+i\dfrac{1}{2\pi}\int_0^{2\pi}\tilde{b}(\phi)\ d\phi\right)\\
\Aboxed{u(0,0)&=\dfrac{1}{2\pi}\int_0^{2\pi}b(\phi)\ d\phi}
\end{align}$$
---
## Question 2
Choose $f(z)=z^2$. Evaluate the value of $u(x,y)$ at the boundary of the disk of radius $R$ (i.e. the function $b(\phi)$) and apply the formula derived in Exercise 1 to verify explicitly that the value of the potential $u$ at its center is consistent with Eq. (2).
$$\begin{align}
f(z)&=z^2\\
&=(x+iy)^2\\
&=(x^2-y^2)+i(2xy)\\
f\left(re^{i\phi}\right)&=\left(R^2\cos^2\phi-R^2\sin^2\phi\right)+i\left(R^2\cos\phi\sin\phi\right)\\
\Re\left(f\left(Re^{i\phi}\right)\right)&=R^2\cos^2\phi-R^2\sin^2\phi\\
u(R,\phi)&=R^2\cos2\phi\\
\Aboxed{b(\phi)&=R^2\cos2\phi}
\end{align}$$
$$\begin{align}
u(0,0)&=\dfrac{1}{2\pi }\int_{0}^{2\pi} b(\phi)\ d\phi\\
&=\dfrac{1}{2\pi }\int_{0}^{2\pi} R^2\cos2\phi\ d\phi\\
&=\dfrac{R^2}{4\pi }\left.\sin2\phi\right|_{0}^{2\pi}\\
&=\dfrac{R^2}{4\pi }\left(\sin4\pi-\sin0\right)\\
\Aboxed{u(0,0)&=0}
\end{align}$$


