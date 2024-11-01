
### Dirichlet Conditions (2D)
$$\vec\nabla^2\psi=\dfrac{1}{c^2}\dfrac{\partial^2\psi}{\partial t^2}$$
$$\begin{align}
\psi(0,y,t)&=0 & \psi(L_x,y,t)&=0\\
\psi(x,0,t)&=0 & \psi(x,L_y,t)&=0\\
\end{align}$$
Separations of variables:
$$\begin{align}
\vec\nabla^2\psi&=\dfrac{1}{c^2}\dfrac{\partial^2\psi}{\partial t^2}\\
\dfrac{X''}{X}+\dfrac{Y''}{Y}&=\dfrac{1}{c^2}\dfrac{T''}{T}=-\lambda\\
\dfrac{X''}{X}&=-\lambda-\dfrac{Y''}{Y}=-\mu\\
\end{align}$$
Ordinary differential equations:
$$\begin{align}
T''(t)&=-c^2\lambda T(t)&
T(t)&=A\sin(c\sqrt{\lambda}t)+B\cos(c\sqrt{\lambda}t)\\
X''(x)&=-\mu X(x)&
X(x)&=C\sin(\sqrt{\mu}x)+D\cos(\sqrt{\mu}x)\\
Y''(y)&=-(\lambda-\mu)Y(y)&
Y(y)&=E\sin(\sqrt{\lambda-\mu}y)+F\cos(\sqrt{\lambda-\mu}y)\\
\end{align}$$
Applying boundary conditions:
$$\begin{align}
X(0)&=C\sin(\sqrt{\mu}0)+D\cos(\sqrt{\mu}0)\\
0&=D\\
X(L_x)&=C\sin(\sqrt{\mu}L_x)+D\cos(\sqrt{\mu}L_x)\\
\mu_{nx}&=\left(\dfrac{n_x\pi}{L_x}\right)^2\\
Y(0)&=E\sin(\sqrt{\lambda-\mu}0)+F\cos(\sqrt{\lambda-\mu}0)\\
0&=F\\
Y(L_y)&=E\sin(\sqrt{\lambda-\mu}L_y)+F\cos(\sqrt{\lambda-\mu}L_y)\\
\lambda_{nx,ny}&=\left(\dfrac{n_y\pi}{L_y}\right)^2+\left(\dfrac{n_x\pi}{L_x}\right)^2
\end{align}$$
Simplifying solutions:
$$\begin{align}
T(t)&=A\sin(c|\vec{n}|t)+B\cos(c|\vec{n}|t)\\
X(x)&=C\sin\left(\dfrac{n_x\pi}{L_x}x\right)\\
Y(y)&=E\sin\left(\dfrac{n_y\pi}{L_y}y\right)\\
\end{align}$$
Combining all solutions:
$$\begin{align}
\psi(x,y,t)&=\sum_{n_x=1}^\infty\sum_{n_y=1}^\infty\left(A_{n_x,n_y}\sin(c|\vec{n}|t)+B_{n_x,n_y}\cos(c|\vec{n}|t)\right)\sin\left(\dfrac{n_x\pi}{L_x}x\right)\sin\left(\dfrac{n_y\pi}{L_y}y\right)\\
A_{n_x,n_y}&=\dfrac{2}{L_x}\dfrac{2}{L_y}\int_0^{L_y}\int_0^{L_y} \psi_0(x,y)\cdot\sin\left(\dfrac{n_x\pi}{L_x}x\right)\sin\left(\dfrac{n_y\pi}{L_y}y\right)\ dx\ dy\\
B_{n_x,n_y}&=\dfrac{1}{c|\vec{n}|}\dfrac{2}{L_x}\dfrac{2}{L_y}\int_0^{L_y}\int_0^{L_y} \psi_{0t}(x,y)\cdot\sin\left(\dfrac{n_x\pi}{L_x}x\right)\sin\left(\dfrac{n_y\pi}{L_y}y\right)\ dx\ dy\\
\end{align}$$



### Transverse Wave (1D)
Using traveling waves $v=x+ct$ and $w=x-ct$.
$$\begin{align}
\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{1}{c^2}\dfrac{\partial^2\psi}{\partial t^2}\\
\psi_{vv}+2\psi_{vw}+\psi_{ww}&=\psi_{vv}-2\psi_{vw}+\psi_{ww}\\
\psi_{vw}&=0\\
\dfrac{\partial}{\partial v}\dfrac{\partial\psi}{\partial w}&=\dfrac{\partial}{\partial w}\dfrac{\partial\psi}{\partial v}=0\\
\dfrac{\partial\psi}{\partial w}=A\ \ &\ \ \dfrac{\partial\psi}{\partial v}=B\\
\psi(x,t)&=f(v)+f(w)\\
\psi(x,t)&=f(x+ct)+g(x-ct)\\
\end{align}$$