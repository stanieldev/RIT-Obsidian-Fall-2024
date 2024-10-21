### Example
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

### Example
$$\begin{align}
6\vec\nabla^2u(\vec{x},t)=\dfrac{\partial u(\vec{x},t)}{\partial t}
\end{align}$$
$$\begin{align}
u(0,y,t)&=0,&u(2,y,t)&=0\\
\dfrac{\partial u}{\partial y}(x,0,t)&=0,&\dfrac{\partial u}{\partial y}(x,4,t)&=0\\
u(x,y,0)&=f(x,y)
\end{align}$$
Let $u(\vec{x},t)=X(x)Y(y)T(t)$:
$$\begin{align}
6\vec\nabla^2u(\vec{x},t)&=\dfrac{\partial u(\vec{x},t)}{\partial t}\\
6X''(x)Y(y)T(t)+6X(x)Y(y)''T(t)&=X(x)Y(y)T'(t)\\
\dfrac{X''(x)}{X(x)}+\dfrac{Y''(x)}{Y(x)}&=\dfrac{1}{6}\dfrac{T'(t)}{T(t)}=-\lambda\\
\end{align}$$
Creating the following differential equations:
$$\begin{align}
X''(x)+\mu X(x)&=0&
X_n(x)&=A\sin\left(\sqrt{\mu}x\right)+B\cos\left(\sqrt{\mu}x\right)\\
Y''(y)+(\lambda-\mu) Y(y)&=0&
Y_m(y)&=C\sin\left(\sqrt{\lambda-\mu}y\right)+D\cos\left(\sqrt{\lambda-\mu}y\right)\\
T'(t)+6\lambda T(t)&=0&
T(t)&=Ee^{-6\lambda t}
\end{align}$$
With the following boundary conditions:
$$\begin{align}
X_n(0)&=B\cos\left(0\right)=0\\
X_n(2)&=A\sin\left(\sqrt{\mu}x\right)=0\\
Y'_m(y)&=\sqrt{\lambda-\mu}\left(C\cos\left(\sqrt{\lambda-\mu}y\right)-D\sin\left(\sqrt{\lambda-\mu}y\right)\right)\\
Y'_m(0)&=\sqrt{\lambda-\mu}C=0\\
Y'_m(4)&=\left(D\sin\left(\sqrt{\lambda-\mu}y\right)\right)=0\\
\end{align}$$
Therefore, the values come to be:
$$\begin{align}
\mu_n&=\left(\dfrac{n\pi}{2}\right)^2\\
\lambda_{mn}&=\left(\dfrac{m\pi}{4}\right)^2+\left(\dfrac{n\pi}{2}\right)^2
\end{align}$$
So we find the following equations:
$$\begin{align}
X_n(x)&=A\sin\left(\sqrt{\mu_n}x\right)\\
Y_m(y)&=D\cos\left(\sqrt{\lambda_{mn}-\mu_n}y\right)\\
T_{nm}(t)&=Ee^{-6\lambda_{mn} t}
\end{align}$$
Therefore, we can find $u(\vec{x},t)$:
$$\begin{align}
\Aboxed{u(\vec{x},t)&=\sum_{n=0}^\infty\sum_{m=0}^\infty c_{nm}\sin\left(\dfrac{n\pi}{2}x\right)\cos\left(\dfrac{m\pi}{4}y\right)\exp\left(-6\pi^2\left(\left(\dfrac{m}{4}\right)^2+\left(\dfrac{n}{2}\right)^2\right)t\right)}\\
\Aboxed{c_{nm}&=\dfrac{1}{2}\int_0^4\int_0^2f(x,y)\sin\left(\dfrac{n\pi}{2}x\right)\cos\left(\dfrac{m\pi}{4}y\right)\ dx\ dy}
\end{align}$$
