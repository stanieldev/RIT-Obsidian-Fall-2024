### Uniqueness of the Solution
Below is the heat equation:
$$ku_{xx}=u_t$$
Maximum Principle: $u(x,t)$ satisfies the heat equation and boundary condition, therefore the maximum value of $u(x,t)$ on its domain, there is a $x_0$ where $u(x_0,0)$.




### Example
$$\begin{align}
k\dfrac{\partial^2u}{\partial x^2}+h(x)&=\dfrac{\partial u}{\partial t}\\
\end{align}$$
$$u(0,t)=a, \ \ \ u(L,t)=b, \ \ \ u(x,0)=f(x)$$
Let $u(x,t)=w(x,t)+v(x)$

| $W$                                                                 | $V$                                         |
| ------------------------------------------------------------------- | ------------------------------------------- |
| $k\dfrac{\partial^2W}{\partial x^2}=\dfrac{\partial W}{\partial t}$ | $k\dfrac{\partial^2V}{\partial x^2}+h(x)=0$ |
| $W(0,t)=0$                                                          | $V(0)=a$                                    |
| $W(5,t)=0$                                                          | $V(L)=b$                                    |
| $W(x,0)=f(x)-V(x)$                                                  |                                             |

$$\begin{align}
u(x,t)=V(x)+\sum c_nW_n(x,t)
\end{align}$$
