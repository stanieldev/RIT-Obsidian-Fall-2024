### Wave Equation
$$\begin{align}
c^2\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}\\
\end{align}$$
$$\begin{align}
\psi(0,t)=\psi(L,t)=0
\end{align}$$
$$\begin{align}
\psi(x,t)&=\sum_{n=1}^\infty\left(a_n\cos\left(\dfrac{n\pi}{L}ct\right)+b_n\sin\left(\dfrac{n\pi}{L}ct\right)\right)\sin\left(\dfrac{n\pi}{L}x\right)\\
\psi(x,0)&=\sum_{n=1}a_n\sin\left(\dfrac{n\pi}{L}x\right)\\
a_n&=\dfrac{2}{L}\int_{0}^L\psi(x,0)\cdot\sin\left(\dfrac{n\pi}{L}x\right)\ dx\\
b_n&=\dfrac{1}{n\pi}\dfrac{2}{L}\int_{0}^L\psi_t(x,0)\cdot\sin\left(\dfrac{n\pi}{L}x\right)\ dx
\end{align}$$
$$\begin{align}
\psi(x,t)&=\sum_{n=1}^\infty\left(a_n\cos\left(\dfrac{n\pi}{L}ct\right)+b_n\sin\left(\dfrac{n\pi}{L}ct\right)\right)\sin\left(\dfrac{n\pi}{L}x\right)\\
\psi(x,0)&=a_n\sin\left(\dfrac{n\pi}{L}x\right)\\

a_n&=\dfrac{2}{L}\int_{0}^L\sum_{m=1}\sin\left(\dfrac{m\pi}{L}x\right)\cdot\sin\left(\dfrac{n\pi}{L}x\right)\ dx\\
&=\dfrac{2}{L}\int_{0}^L\sin^2\left(\dfrac{n\pi}{L}x\right)\ dx\\
&=\dfrac{1}{L}\int_{0}^L1-\cos\left(\dfrac{n\pi}{L}x\right)\ dx\\
&=\dfrac{1}{L}\left.x-\dfrac{L}{n\pi}\sin\left(\dfrac{n\pi}{L}x\right)\right|_{0}^L\\

b_n&=\dfrac{1}{n\pi}\dfrac{2}{L}\int_{0}^L\dfrac{L}{cn\pi}\sum_{m=1}\sin\left(\dfrac{m\pi}{L}x\right)\cdot\sin\left(\dfrac{n\pi}{L}x\right)\ dx\\
&=\dfrac{2}{c(n\pi)^2}\int_{0}^L\sin^2\left(\dfrac{n\pi}{L}x\right)\ dx\\
&=\dfrac{2}{c(n\pi)^2}\int_{0}^L\dfrac{1-\cos\left(\dfrac{2n\pi}{L}x\right)}{2}\ dx\\
&=\dfrac{1}{c(n\pi)^2}\left.x-\dfrac{L}{2n\pi}\sin\left(\dfrac{2n\pi}{L}x\right)\right|_{0}^L\\
b_n&=\dfrac{L}{c(n\pi)^2}\\
\end{align}$$
It's incomplete, but enough.


### Non-Homogenous
$$\begin{align}
c^2\dfrac{\partial^2\psi}{\partial x^2}+h(x)&=\dfrac{\partial^2\psi}{\partial t^2}\\
\end{align}$$
$$\begin{align}
\psi(0,t)=A, \psi(L,t)=B
\end{align}$$

| $W$                                                                      | $V$                                           |
| ------------------------------------------------------------------------ | --------------------------------------------- |
| $c^2\dfrac{\partial^2W}{\partial x^2}=\dfrac{\partial^2W}{\partial t^2}$ | $c^2\dfrac{\partial^2V}{\partial x^2}+h(x)=0$ |
| $W(0,t)=0$                                                               | $V(0,t)=A$                                    |
| $W(L,t)=0$                                                               | $V(L,t)=B$                                    |
| $W(x,0)=\psi(x,0)-V(x)$                                                  |                                               |
| $W_t(x,0)=\psi_t(x,0)$                                                   |                                               |


### Example
$$\begin{align}
3\dfrac{\partial^2\psi}{\partial x^2}+e^x&=\dfrac{\partial^2\psi}{\partial t^2}\\
\end{align}$$
$$\begin{align}
\psi(0,t)=0, \psi(1,t)=2\\
\psi(x,0)=x, \psi_t(x,0)=x^2
\end{align}$$

| $W$                                                                    | $V$                                        |
| ---------------------------------------------------------------------- | ------------------------------------------ |
| $3\dfrac{\partial^2W}{\partial x^2}=\dfrac{\partial^2W}{\partial t^2}$ | $3\dfrac{\partial^2V}{\partial x^2}+e^x=0$ |
| $W(0,t)=0$                                                             | $V(0,t)=0$                                 |
| $W(1,t)=0$                                                             | $V(1,t)=2$                                 |
| $W(x,0)=x-V(x)$                                                        |                                            |
| $W_t(x,0)=x^2$                                                         |                                            |
$$\begin{align}
V(x)&=-\dfrac{1}{3}e^x+ax+b\\
b&=0\\
a&=2+\dfrac{1}{3}e\\
V(x)&=-\dfrac{1}{3}e^x+\left(2+\dfrac{e}{3}\right)x
\end{align}$$

### Other Hyperbolic PDEs
Telegraph Equation
$$\begin{align}
c^2\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}+\dfrac{\partial\psi}{\partial t}+\psi\\
c^2X''(x)T(t)&=X(x)T''(t)+X(x)T'(t)+X(x)T(t)\\
c^2\dfrac{X''(x)}{X(x)}&=\dfrac{T''(t)}{T(t)}+\dfrac{T'(t)}{T(t)}+1\\
X(x)&=A\sin\left(\dfrac{n\pi}{L}x\right)+B\cos\left(\dfrac{n\pi}{L}x\right)\\
T(t)&=
\end{align}$$
