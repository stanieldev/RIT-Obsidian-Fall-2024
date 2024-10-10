**Name:** Stanley Goodwin
**Date:** 10/01/2024
**Collaborators:** None

In this assignment, we will compute contour integrals of holomorphic functions, both directly and using the theorems introduced in this chapter until now. Remember that contour integrals are defined as follows:
$$I=\oint_\Gamma f(z)\ dz = \int_{t_0}^{t_f}f(z(t))\dfrac{dz(t)}{dt}\ dt$$

---
## Exercise 1
*Calculate the contour integral of $f(z)=e^z$ over the contour $\Gamma$, which consists of the following three segments.*

For the sake of convenience, I chose parametrizations that are straight lines.
### 1.1 : $z=0+0i$ to $z=1+1i$
$$\begin{align}
\Gamma_1(t)&=(0+0i)(1-t)+(1+1i)(t)\\
\Aboxed{\Gamma_1(t)&=t+ti}\\
\oint_{\Gamma_1} f(z)\ dz&=\int_{0}^{1}f(\Gamma_1(t))\dfrac{d\Gamma_1(t)}{dt}\ dt\\
&=\int_{0}^{1}f(t+ti)\cdot(1+i)\ dt\\
&=\int_{0}^{1}e^{(1+i)t}\cdot(1+i)\ dt\\
&=\dfrac{(1+i)}{(1+i)}\left.e^{(1+i)t}\right|_0^1\\
&=e^{1+i}-e^{0}\\
\Aboxed{\oint_{\Gamma_1} f(z)\ dz&=e^{1+i}-1}
\end{align}$$
### 1.2 : $z=1+1i$ to $z=1+0i$
$$\begin{align}
\Gamma_2(t)&=(1+1i)(1-t)+(1+0i)(t)\\
\Aboxed{\Gamma_2(t)&=1+i(1-t)}\\
\oint_{\Gamma_2} f(z)\ dz&=\int_{0}^{1}f(\Gamma_2(t))\dfrac{d\Gamma_2(t)}{dt}\ dt\\
&=\int_{0}^{1}f(1+i(1-t))\cdot(-i)\ dt\\
&=\int_{0}^{1}e^{1+i-it}\cdot(-i)\ dt\\
&=\dfrac{(-i)}{(-i)}\left.e^{1+i-it}\right|_0^1\\
&=e^{1}-e^{1+i}\\
\Aboxed{\oint_{\Gamma_2} f(z)\ dz&=e-e^{1+i}}
\end{align}$$
### 1.3 : $z=1+0i$ to $z=0+0i$
$$\begin{align}
\Gamma_3(t)&=(1+0i)(1-t)+(0+0i)(t)\\
\Aboxed{\Gamma_3(t)&=1-t}\\
\oint_{\Gamma_3} f(z)\ dz&=\int_{0}^{1}f(\Gamma_3(t))\dfrac{d\Gamma_3(t)}{dt}\ dt\\
&=\int_{0}^{1}f(1-t)\cdot(-1)\ dt\\
&=\int_{0}^{1}e^{1-t}\cdot(-1)\ dt\\
&=\dfrac{(-1)}{(-1)}\left.e^{1-t}\right|_0^1\\
&=e^{0}-e^{1}\\
\Aboxed{\oint_{\Gamma_3} f(z)\ dz&=1-e}
\end{align}$$

---
## Exercise 2
Compute the same contour integral of $f(z)=e^z$ over the contour $\Gamma$ using the fundamental theorem of calculus for holomorphic functions, and verify that the result is consistent with the answer from Exercise 1.
$$\begin{align}
&&\int_\gamma f(z)\ dz &= F(\gamma_f)-F(\gamma_0)\\
\implies&&\oint_\gamma f(z)\ dz &= 0
\end{align}$$
From exercise 1, we can see that the integral can be written as:
$$\begin{align}
\oint_\gamma f(z)\ dz &= \oint_{\Gamma_1} f(z)\ dz+\oint_{\Gamma_2} f(z)\ dz+\oint_{\Gamma_3} f(z)\ dz\\
&=\left(e^{1+i}-1\right)+\left(e-e^{1+i}\right)+\left(1-e\right)\\
&=\left(e^{1+i}-e^{1+i}\right)+\left(e-e\right)+\left(1-1\right)\\
\Aboxed{\oint_\gamma f(z)\ dz &= 0}
\end{align}$$

---
## Exercise 3
Compute the same contour integral of $f(z)=e^z$ over the contour $\Gamma$ using Cauchy’s theorem, and verify that the result is consistent with the answer from Exercise 1.
$$\begin{align}
f(z)=e^z \implies \dfrac{df(z)}{dz}=e^z
\end{align}$$
Since $f(z)$ is differentiable (holomorphic) over all space, then $\displaystyle\oint_\gamma f(z)\ dz=0$.


---
## Exercise 4
Compute the contour integral of $f(z)=\dfrac{1}{z-1}$ over a square contour $\Gamma$, oriented counter-clockwise, centered at the origin with a side length B. The contour integral is:
$$I=\oint\dfrac{1}{z-1}\ dz$$
For the sake of convenience, I'm going to break the contour into the following:
$$\begin{align}
\oint\dfrac{1}{z-1}\ dz&=\int_{\Gamma_1}\dfrac{1}{z-1}\ dz+\int_{\Gamma_2}\dfrac{1}{z-1}\ dz+\int_{\Gamma_3}\dfrac{1}{z-1}\ dz+\int_{\Gamma_4}\dfrac{1}{z-1}\ dz\\
&+\int_{\Gamma_5}\dfrac{1}{z-1}\ dz+\int_{\Gamma_6}\dfrac{1}{z-1}\ dz+\int_{\Gamma_7}\dfrac{1}{z-1}\ dz+\int_{\Gamma_8}\dfrac{1}{z-1}\ dz\\
\end{align}$$
Here's a graph of the contour breakup (as $R\rightarrow 0$):
![[HW4_Q4.png]]
Doing a bit of simplification, we can see that:
$$\begin{align}
\int_{\Gamma_1}\dfrac{1}{z-1}\ dz+\int_{\Gamma_2}\dfrac{1}{z-1}\ dz+\int_{\Gamma_3}\dfrac{1}{z-1}\ dz+\int_{\Gamma_4}\dfrac{1}{z-1}\ dz+\int_{\Gamma_5}\dfrac{1}{z-1}\ dz &=0\\
\int_{\Gamma_6}\dfrac{1}{z-1}\ dz+\int_{\Gamma_8}\dfrac{1}{z-1}\ dz&=0
\end{align}$$
Therefore, the original expression simplifies to the following:
$$\begin{align}
\oint\dfrac{1}{z-1}\ dz&=\lim_{R\rightarrow0}\int_{\Gamma_7}\dfrac{1}{\left(Re^{i\theta}+1\right)-1}\ d\left(Re^{i\theta}+1\right)\\
&=\lim_{R\rightarrow0}\int_{0}^{2\pi}\dfrac{iRe^{i\theta}}{Re^{i\theta}}\ d\theta\\
&=i\int_{0}^{2\pi}\ d\theta\\
\Aboxed{\oint\dfrac{1}{z-1}\ dz&=2\pi i}
\end{align}$$
