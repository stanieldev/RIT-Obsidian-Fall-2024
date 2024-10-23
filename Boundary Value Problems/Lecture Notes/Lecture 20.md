**Name:** Stanley Goodwin
**Date:** 10/16/2024

---

Non-homogenous Boundary Conditions and/or the extra heating source for the heat equation.
$$k\dfrac{\partial^2u}{\partial x^2}+h(x)=\dfrac{\partial u}{\partial t}$$
With boundary conditions:
$$u(0,t)=A, \ \ \ u(L,t)=B$$
Using separation of variables:
$$\begin{align}
k\dfrac{\partial^2u}{\partial x^2}+h(x)&=\dfrac{\partial u}{\partial t}\\
k\cdot X''(x)T(t)+h(x)&=X(x)T'(t)\\
k\cdot \dfrac{X''(x)}{X(x)}+\dfrac{h(x)}{X(x)T(t)}&=\dfrac{T'(t)}{T(t)}\\
\end{align}$$
Consider $u(x,t)=w(x,t)+v(x)$
$$\begin{align}
k\dfrac{\partial^2u}{\partial x^2}+h(x)&=\dfrac{\partial u}{\partial t}\\
k\cdot \left(W''(x,t)+V''(x)\right)+h(x)&=\dfrac{\partial W}{\partial t}\\
\end{align}$$
Looking at the boundary conditions:
$$\begin{align}
A&=u(0,t)\\
A&=W(0,t)+V(x)\\
B&=u(L,t)\\
B&=W(L,t)+V(L)\\
u(x,0)&=W(x,0)+V(x)
\end{align}$$
So we get 2 equations we need to solve (homogenous and particular):
$$\begin{align}
k\dfrac{\partial^2W}{\partial x^2}&=\dfrac{\partial W}{\partial t}\\
k\dfrac{\partial^2V}{\partial x^2}+h(x)&=0\\
\end{align}$$



### Example:
$$\begin{align}
6\dfrac{\partial^2u}{\partial x^2}+e^x&=\dfrac{\partial u}{\partial t}\\
\end{align}$$
$$u(0,t)=2, \ \ \ u(1,t)=4, \ \ \ u(x,0)=x$$
Let $u(x,t)=W(x,t)+V(x)$

| $W$                                                                      | $V$                                             |
| ------------------------------------------------------------------------ | ----------------------------------------------- |
| $6\cdot\dfrac{\partial^2W}{\partial x^2}=\dfrac{\partial W}{\partial t}$ | $6\cdot\dfrac{\partial^2V}{\partial x^2}+e^x=0$ |
| $W(0,t)=0$                                                               | $V(0)=2$                                        |
| $W(1,t)=0$                                                               | $V(0)=4$                                        |
| $W(x,0)=x-V(x)$                                                          |                                                 |
$$\begin{align}
6\cdot\dfrac{\partial^2V}{\partial x^2}+e^x&=0\\
\dfrac{\partial^2V}{\partial x^2}&=-\dfrac{1}{6}e^x\\
V(x)&=-\dfrac{1}{6}e^x+Ax+B\\
\end{align}$$
Apply boundary conditions:
$$\begin{align}
V(x)&=-\dfrac{1}{6}e^x+Ax+B\\
V(0)&=-\dfrac{1}{6}+B=2\\
V(1)&=-\dfrac{1}{6}e+A+B=4\\
\end{align}$$
And so:
$$\begin{align}
u(x,t)=V(x)+\sum c_nw_n(x,t)
\end{align}$$
Where you'd solve $w_n(x,t)$ using power series expansion, I think.


### Example:
$$\begin{align}
2\dfrac{\partial^2u}{\partial x^2}&=\dfrac{\partial u}{\partial t}\\
\end{align}$$
$$u(0,t)=1, \ \ \ u(\pi,t)=2, \ \ \ u(x,0)=f(x)$$
Let $u(x,t)=w(x,t)+v(x)$

| $W$                                                                      | $V$                                         |
| ------------------------------------------------------------------------ | ------------------------------------------- |
| $2\cdot\dfrac{\partial^2w}{\partial x^2}=\dfrac{\partial w}{\partial t}$ | $2\cdot\dfrac{\partial^2V}{\partial x^2}=0$ |
| $W(0,t)=0$                                                               | $V(0)=1$                                    |
| $W(\pi,t)=0$                                                             | $V(\pi)=2$                                  |
| $W(x,0)=f(x)-V(x)$                                                       |                                             |
$$\begin{align}
V(x)&=Ax+B\\
V(0)&=B=1\\
V(\pi)&=A\pi+B=2\\
\Aboxed{A=\dfrac{1}{\pi} & \ \ \ B=1}
\end{align}$$
Therefore:
$$\begin{align}
u(x,t)=\dfrac{1}{\pi}x+1+\sum c_nw_n(x,t)
\end{align}$$



### Example:
$$\begin{align}
\dfrac{\partial^2u}{\partial x^2}+x^2&=\dfrac{\partial u}{\partial t}\\
\end{align}$$
$$u(0,t)=0, \ \ \ u(5,t)=0, \ \ \ u(x,0)=f(x)$$
Let $u(x,t)=w(x,t)+v(x)$

| $W$                                                                | $V$                                       |
| ------------------------------------------------------------------ | ----------------------------------------- |
| $\dfrac{\partial^2w}{\partial x^2}=\dfrac{\partial w}{\partial t}$ | $\dfrac{\partial^2V}{\partial x^2}+x^2=0$ |
| $W(0,t)=0$                                                         | $V(0)=0$                                  |
| $W(5,t)=0$                                                         | $V(5)=0$                                  |
| $W(x,0)=f(x)-V(x)$                                                 |                                           |
$$\begin{align}
V(x)&=-\dfrac{1}{12}x^4+Ax+B\\
V(0)&=B=0\\
V(5)&=-\dfrac{625}{12}+5A=0\\
\Aboxed{A=\dfrac{125}{12} & \ \ \ B=0}
\end{align}$$
Therefore:
$$\begin{align}
u(x,t)=-\dfrac{1}{12}x^4+\dfrac{125}{12}x+\sum c_nw_n(x,t)
\end{align}$$

