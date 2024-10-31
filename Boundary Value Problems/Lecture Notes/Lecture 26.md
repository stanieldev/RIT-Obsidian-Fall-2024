### Example
$$\begin{align}
5\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}+\dfrac{\partial\psi}{\partial t}\\
\end{align}$$
$$\begin{align}
\psi(0,t)=\psi(\pi,t)=0
\end{align}$$
Separation of Variables:
$$\begin{align}
\dfrac{X''(x)}{X(x)}&=\dfrac{1}{5}\dfrac{T''(t)}{T(t)}+\dfrac{1}{5}\dfrac{T(t)}{T(t)}
\end{align}$$
Function of $x$:
$$\begin{align}
X''(x)&=-\lambda X(x)\\
X(x)&=A\sin\left(\sqrt{\lambda}x\right)+B\cos\left(\sqrt{\lambda}x\right)\\
X(0)&=B=0\\
X(\pi)&=A\sin\left(\sqrt{\lambda}\pi\right)=0\\
\sqrt{\lambda}\pi&=n\pi\\
\lambda_n&=n^2\\
X(x)&=A\sin\left(nx\right)\\
\end{align}$$
Function of $t$:
$$\begin{align}
0&=T''(t)+T'(t)+5\lambda T(t)\\
T(t)&=e^{-\tfrac{1}{2}t}\left(C\sin\left(\dfrac{\sqrt{20n^2-1}}{2}t\right)+D\cos\left(\dfrac{\sqrt{20n^2-1}}{2}t\right)\right)\\
\end{align}$$
Total function component:
$$\begin{align}
u_n(x,t)&=e^{-\tfrac{1}{2}t}\left(a_n\sin\left(\dfrac{\sqrt{20n^2-1}}{2}t\right)+b_n\cos\left(\dfrac{\sqrt{20n^2-1}}{2}t\right)\right)\sin\left(nx\right)\\
u_t(x,t)&=e^{-\tfrac{1}{2}t}\left(-\tfrac{1}{2}b_n\cos\left(\dfrac{\sqrt{20n^2-1}}{2}t\right)+\dfrac{\sqrt{20n^2-1}}{2}a_n\cos\left(\dfrac{\sqrt{20n^2-1}}{2}t\right)\right)\sin\left(nx\right)\\
u(x,0)&=b_n\sin\left(nx\right)\\
u_t(x,0)&=\left(-\tfrac{1}{2}b_n+\dfrac{\sqrt{20n^2-1}}{2}a_n\right)\sin\left(nx\right)\\
\end{align}$$
Total function:
$$\begin{align}
u(x,t)&=\sum_{n=1}^\infty e^{-\tfrac{1}{2}t}\left(a_n\sin\left(\dfrac{\sqrt{20n^2-1}}{2}t\right)+b_n\cos\left(\dfrac{\sqrt{20n^2-1}}{2}t\right)\right)\sin\left(nx\right)\\
u(x,0)&=\sum_{n=1}^\infty b_n\sin\left(nx\right)\\
u_t(x,0)&=\sum_{n=1}^\infty \left(-\tfrac{1}{2}b_n+\dfrac{\sqrt{20n^2-1}}{2}a_n\right)\sin\left(nx\right)\\
\end{align}$$
Then find the coefficients:
$$\begin{align}
b_n&=\dfrac{2}{\pi}\int_0^\pi\sin(mx)\sin(nx)\ dx\\
&=\dfrac{2}{\pi}\int_0^\pi\sin^2(nx)\ dx\\
&=\dfrac{1}{\pi}\int_0^\pi1-\cos(2nx)\ dx\\
&=\dfrac{1}{\pi}\left(x-\dfrac{1}{2n}\sin(2nx)\right|_0^\pi\\
&=\pi\\
a_n&=\dfrac{2}{\pi}\int_0^\pi\sin(mx)\sin(nx)\ dx\\
u(x,0)&=b_n\sin\left(nx\right)\\
u_t(x,0)&=\left(-\tfrac{1}{2}b_n+\dfrac{\sqrt{20n^2-1}}{2}a_n\right)\sin\left(nx\right)\\
\end{align}$$
Who cares...



### 2D Wave Equation
$$\begin{align}
c^2\vec\nabla^2\psi&=\dfrac{\partial^2\psi}{\partial t^2}\\
\end{align}$$
$$\begin{align}
\psi(0,y,t)=\psi(L,y,t)=0\\
\psi(x,0,t)=\psi(0,H,t)=0\\
\end{align}$$
Separation of Variables:
$$\begin{align}
\dfrac{X''(x)}{X(x)}+\dfrac{Y''(y)}{Y(y)}&=\dfrac{1}{c^2}\dfrac{T''(t)}{T(t)}=-\lambda\\
\end{align}$$
$$\begin{align}
\dfrac{X''(x)}{X(x)}&=-\lambda-\dfrac{Y''(y)}{Y(y)}=-\mu\\
\end{align}$$
3 Differential Equations:
$$\begin{align}
\dfrac{T''(t)}{T(t)}&=-c^2\lambda\\
\dfrac{X''(x)}{X(x)}&=-\mu\\
\dfrac{Y''(y)}{Y(y)}&=\mu-\lambda
\end{align}$$
...


