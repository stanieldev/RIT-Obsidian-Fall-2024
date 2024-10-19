### Example:
$$\begin{align}
2\dfrac{\partial^2u}{\partial x^2}+1&=\dfrac{\partial u}{\partial t}\\
\end{align}$$
$$u(0,t)=0, \ \ \ u(\pi,t)=3, \ \ \ u(x,0)=x$$
Let $u(x,t)=W(x,t)+V(x)$

| $W$                                                                      | $V$                                           |
| ------------------------------------------------------------------------ | --------------------------------------------- |
| $2\cdot\dfrac{\partial^2W}{\partial x^2}=\dfrac{\partial W}{\partial t}$ | $2\cdot\dfrac{\partial^2V}{\partial x^2}+1=0$ |
| $W(0,t)=0$                                                               | $V(0)=0$                                      |
| $W(\pi,t)=0$                                                             | $V(\pi)=3$                                    |
| $W(x,0)=x-V(x)$                                                          |                                               |
$$\begin{align}
0&=2\cdot\dfrac{\partial^2V}{\partial x^2}+1\\
V(x)&=-\dfrac{1}{4}x^2+Ax+B\\
\end{align}$$
Apply boundary conditions:
$$\begin{align}
V(0)&=B=0\\
V(\pi)&=-\dfrac{1}{4}\pi^2+A\pi=3\\
A&=\dfrac{3}{\pi}+\dfrac{1}{4}\pi\\
\end{align}$$
For $W$:
$$\begin{align}
2\cdot\dfrac{\partial^2W}{\partial x^2}&=\dfrac{\partial W}{\partial t}\\
2\cdot X''(x)T(t)&=X(x)T'(t)\\
\dfrac{X''(x)}{X(x)}&=\dfrac{1}{2}\dfrac{T'(t)}{T(t)}\\
X_n(x)&=\sin\left(\dfrac{n\pi}{\pi}x\right)=\sin\left(nx\right)\\
\lambda_n&=n^2, n\ge1\\
T(t)&=e^{-2n^2t}\\
W(x,t)&=\sum_{n=1}^\infty c_n\sin\left(nx\right)e^{-2n^2t}\\
c_n&=\dfrac{2}{\pi}\int_0^\pi(x-V(x))\sin(nx)\ dx\\
\end{align}$$
$$\begin{align}
u_n(x,t)&=-\dfrac{1}{4}x^2+\left(\dfrac{3}{\pi}+\dfrac{1}{4}\pi\right)x+\sum_{n=1}^\infty c_n\sin\left(nx\right)e^{-2n^2t}\\
c_n&=\dfrac{2}{\pi}\int_0^\pi(x-V(x))\sin(nx)\ dx\\
\end{align}$$


### Heat Equation in 2 Dimensions
$$\begin{align}
k\vec\nabla^2u(\vec{x},t)=\dfrac{\partial u(\vec{x},t)}{\partial t}
\end{align}$$
$$\begin{align}
u(0,y,t)&=0,&u(L,y,t)&=0\\
u(x,0,t)&=0,&u(x,H,t)&=0\\
\end{align}$$
Let $u(\vec{x},t)=X(x)Y(y)T(t)$:
$$\begin{align}
k\vec\nabla^2u(\vec{x},t)&=\dfrac{\partial u(\vec{x},t)}{\partial t}\\
kX''(x)Y(y)T(t)+kX(x)Y(y)''T(t)&=X(x)Y(y)T'(t)\\
\dfrac{X''(x)}{X(x)}+\dfrac{Y''(x)}{Y(x)}&=\dfrac{1}{k}\dfrac{T'(t)}{T(t)}=-\lambda\\
\end{align}$$
Creating the following differential equations:
$$\begin{align}
X''(x)+\mu X(x)&=0\\
Y''(y)+(\lambda-\mu) Y(y)&=0\\
T'(t)+k\lambda T(t)&=0
\end{align}$$
With the following solutions:
$$\begin{align}
X_n(x)&=\sin\left(\dfrac{n\pi}{L}x\right) & \mu_n&=\left(\dfrac{n\pi}{L}\right)^2\\
Y_m(y)&=\sin\left(\dfrac{m\pi}{H}y\right) & \lambda_{nm}&=\left(\dfrac{m\pi}{H}\right)^2-\left(\dfrac{n\pi}{L}\right)^2\\
T_{nm}(t)&=\exp\left(-k\lambda_{nm}t\right)
\end{align}$$
Therefore, we can find $u(\vec{x},t)$:
$$\begin{align}
u(\vec{x},t)&=X_n(x)Y_m(y)T(t)\\
&=\sum_{n=1}^\infty\sum_{m=1}^\infty c_{nm}\sin\left(\dfrac{n\pi}{L}x\right)\sin\left(\dfrac{m\pi}{H}y\right)\exp\left(-k\left(\left(\dfrac{m\pi}{H}\right)^2-\left(\dfrac{n\pi}{L}\right)^2\right)t\right)\\
c_{nm}&=\dfrac{2}{L}\dfrac{2}{H}\int_0^H\int_0^Lf(x,y)\sin\left(\dfrac{n\pi}{L}x\right)\sin\left(\dfrac{m\pi}{H}y\right)\ dx\ dy
\end{align}$$


### Example in 2D
$$\begin{align}
3\vec\nabla^2u(\vec{x},t)=\dfrac{\partial u(\vec{x},t)}{\partial t}
\end{align}$$
$$\begin{align}
u(0,y,t)&=0,&u(1,y,t)&=0\\
u(x,0,t)&=0,&u(x,2,t)&=0\\
u(x,y,0)&=f(x,y)
\end{align}$$
Let $u(\vec{x},t)=X(x)Y(y)T(t)$:
$$\begin{align}
3\vec\nabla^2u(\vec{x},t)&=\dfrac{\partial u(\vec{x},t)}{\partial t}\\
3X''(x)Y(y)T(t)+3X(x)Y(y)''T(t)&=X(x)Y(y)T'(t)\\
\dfrac{X''(x)}{X(x)}+\dfrac{Y''(x)}{Y(x)}&=\dfrac{1}{3}\dfrac{T'(t)}{T(t)}=-\lambda\\
\end{align}$$
Creating the following differential equations:
$$\begin{align}
X''(x)+\mu X(x)&=0\\
Y''(y)+(\lambda-\mu) Y(y)&=0\\
T'(t)+3\lambda T(t)&=0
\end{align}$$
With the following solutions:
$$\begin{align}
X_n(x)&=\sin\left(n\pi x\right) & \mu_n&=\left(n\pi\right)^2\\
Y_m(y)&=\sin\left(\dfrac{m\pi}{2}y\right) & \lambda_{nm}&=\left(\dfrac{m\pi}{2}\right)^2-\left(n\pi\right)^2\\
T_{nm}(t)&=\exp\left(-3\lambda_{nm}t\right)
\end{align}$$
Therefore, we can find $u(\vec{x},t)$:
$$\begin{align}
\Aboxed{u(\vec{x},t)&=\sum_{n=1}^\infty\sum_{m=1}^\infty c_{nm}\sin\left(n\pi x\right)\sin\left(\dfrac{m\pi}{2}y\right)\exp\left(-3\pi^2\left(\dfrac{m^2}{4}-n^2\right)t\right)}\\
\Aboxed{c_{nm}&=2\int_0^2\int_0^1f(x,y)\sin\left(n\pi x\right)\sin\left(\dfrac{m\pi}{2}y\right)\ dx\ dy}
\end{align}$$
