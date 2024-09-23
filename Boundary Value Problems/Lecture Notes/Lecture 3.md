**Name:** Stanley Goodwin
**Date:** 8/30/2024

---

Classify $u_{xx}-2u_{xy}+\dfrac{1}{4}u_{yy}=0$
$(-2)^2-4(1)(1/4) > 0 \implies$Hyperbolic.


Step I: Separation of Variables
$$\begin{align}
u(x,y)&=X(x)\cdot Y(y)\\
u_x(x,y)&=X'(x)\cdot Y(y)\\
u_y(x,y)&=X(x)\cdot Y'(y)\\
u_{xx}(x,y)&=X''(x)\cdot Y(y)\\
u_{xy}(x,y)&=X'(x)\cdot Y'(y)\\
u_{yy}(x,y)&=X(x)\cdot Y''(y)\\
\end{align}$$


Ex: Solve $u_x+u_y=u$
$$\begin{align}
u_x(x,y)+u_y(x,y)&=u(x,y)\\
X'(x)Y(y)+X(x)Y'(y)&=X(x)Y(y)\\
\dfrac{X'(x)}{X(x)}+\dfrac{Y'(y)}{Y(y)}&=1\\
\dfrac{Y'(y)}{Y(y)} &= 1 - \dfrac{X'(x)}{X(x)}\\
\end{align}$$
$$X'(x)=(1-k)X(x) \implies X(x)=Ae^{(1-k)x}$$
$$Y'(y)=kY(y) \implies Y(y)=Ae^{ky}$$
$$\boxed{u(x,y)=Ae^{(1-k)x+ky}}$$
Ex: Solve $u_{xy}=u$
$$\begin{align}
u_{xy}(x,y)&=u(x,y)\\
X'(x)Y'(y)&=X(x)Y(y)\\
\dfrac{X'(x)}{X(x)}&=\dfrac{Y(y)}{Y'(y)}=k\\
X(x)=Ae^{kx} \ \ & \ \ Y(y)=Be^{y/k}\\
\Aboxed{u(x,y)&=Ae^{kx+y/k}}
\end{align}$$

Ex: Solve $y\cdot u_x + x\cdot u_y = 0$
$$\begin{align}
y\cdot X'(x)Y(y)&=-x\cdot X(x)Y'(y)\\
\dfrac{Y'(y)}{y\cdot Y(y)} &= -\dfrac{X'(x)}{x\cdot X(x)}=k\\
\dfrac{Y'(y)}{Y(y)}=ky \ \ \ & \ \ \ \dfrac{X'(x)}{X(x)}=-kx \\
\ln|Y(y)|=\dfrac{ky^2}{2} + C \ \ \ & \ \ \ \ln|X(x)|=-\dfrac{kx^2}{2} + C \\
Y(y)=Ae^{\tfrac{ky^2}{2}} \ \ \ & \ \ \ X(x)=Ae^{-\tfrac{kx^2}{2}}\\
\Aboxed{u(x,y)&=Ae^{k(y^2-x^2)}}
\end{align}$$

Ex: $u_{xx} = u_y$
$$\begin{align}
X''(x)Y(y)&=X(x)Y'(Y)\\
\dfrac{X''(x)}{X(x)}&=\dfrac{Y'(Y)}{Y(Y)}=k
\end{align}$$
Blahblahblah same stuff over and over.

Ex: Solve $u_{xx}+u_{yy} = 0$
$$X''=kX \implies X(x)=Ae^{\sqrt kx}+Be^{-\sqrt kx}$$
$$Y''=-kY \implies Y(y)=Ce^{i\sqrt kx}+De^{-i\sqrt kx}$$
$$\boxed{u(x,y)=\left(Ae^{\sqrt kx}+Be^{-\sqrt kx}\right)\left(Ce^{i\sqrt kx}+De^{-i\sqrt kx}\right)}$$
