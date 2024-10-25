### Wave Equation
$$\begin{align}
c^2\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}\\
\end{align}$$
$$\begin{align}
\psi(0,t)=\psi(L,t)=0
\end{align}$$
$$\begin{align}
\psi(x,t)&=\sum_{n=1}^\infty\left(a_n\cos\left(cnt\right)+b_n\sin\left(cnt\right)\right)\sin\left(\dfrac{n\pi}{L}x\right)\\
\psi(x,0)&=\sum_{n=1}a_n\sin\left(\dfrac{n\pi}{L}x\right)\\
a_n&=\dfrac{2}{L}\int_{0}^L\psi(x,0)\cdot\sin\left(\dfrac{n\pi}{L}x\right)\ dx\\
b_n&=\dfrac{1}{n\pi}\dfrac{2}{L}\int_{0}^L\psi_t(x,0)\cdot\sin\left(\dfrac{n\pi}{L}x\right)\ dx
\end{align}$$

### Example
$$\begin{align}
\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}\\
\end{align}$$
$$\begin{align}
\psi_x(0,t)=\psi_x(1,t)=0\\
\psi(x,0)=x+1, \psi_t(x,0)=x^2,
\end{align}$$
$$\begin{align}
\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}\\
\dfrac{X''(x)}{X(x)}&=\dfrac{T''(t)}{T(t)}\\
X(x)&=A\sin(kx)+B\cos(kx)\\
T(t)&=C\sin(kt)+D\cos(kt)\\
X_n(x)&=\cos(n\pi x)\\
T_n(t)&=b_n\sin(n\pi t)+a_n\cos(n\pi t)\\
\psi(x,t)&=\sum_{n=1}^\infty\left(b_n\sin(n\pi t)+a_n\cos(n\pi t)\right)\cos(n\pi x)\\
\psi(x,0)&=\sum_{n=1}^\infty a_n\cos(n\pi x)\\
a_n&=\dfrac{2}{1}\int_{0}^1(x+1)\cdot\cos\left(n\pi x\right)\ dx\\
b_n&=\dfrac{1}{n\pi }\dfrac{2}{1}\int_{0}^Lx^2\cdot\cos\left(n\pi x\right)\ dx
\end{align}$$

### Example
$$\begin{align}
6\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}\\
\end{align}$$
$$\begin{align}
\psi(0,t)=\psi_x(\pi/2,t)=0\\
\psi(x,0), \psi_t(x,0)
\end{align}$$
$$\begin{align}
6\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}\\
\dfrac{X''(x)}{X(x)}&=\dfrac{T''(t)}{6T(t)}\\
X(x)&=A\sin(kx)+B\cos(kx)\\
T(t)&=C\sin(\sqrt{6}kx)+D\cos(\sqrt{6}kx)\\
X(0)&=B=0\\
X(\pi/2)&=Ak\cos(k\pi/2)\implies k = 2n+1\\
X_n(x)&=\sin((2n+1)x)\\
T_n(t)&=a_n\sin(\sqrt{6}(2n+1)t)+b_n\cos(2\sqrt{6}(2n+1)t)\\
u(x,t)&=\sum_{n=1}^\infty\left(a_n\sin(\sqrt{6}(2n+1)t)+b_n\cos(\sqrt{6}(2n+1)t)\right)\cdot \sin((2n+1)x)\\
u(x,0)&=\sum_{n=1}^\infty b_n\sin((2n+1)x)\\
b_n&=\dfrac{4}{\pi}\int_0^\tfrac{\pi}{2}u(x,0)\cdot\sin((2n+1)x)\ dx\\
a_n&=\dfrac{2}{(2n+1)\pi^2}\int_0^\tfrac{\pi}{2}u_t(x,0)\cdot\sin((2n+1)x)\ dx\\
\end{align}$$
