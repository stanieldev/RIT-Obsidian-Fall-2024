**Name:** Stanley Goodwin
**Date:** 09/27/2024
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
f(z)&=e^z=e^{x+iy}=e^x\left(\cos y + i\sin y\right)\\
f(x,y)&=\left(e^x\cos y \right)+i\left(e^x\sin y\right)
\end{align}$$
$$\begin{align}
\dfrac{\partial \Im\left(f(x,y)\right)}{dx}&=-\dfrac{\partial \Re\left(f(x,y)\right)}{dy}\\
\dfrac{\partial\left(e^x\sin y\right)}{dx}&=-\dfrac{\partial\left(e^x\cos y \right)}{dy}\\
e^x\sin y&=-\left(-e^x\sin y \right)\\
\Aboxed{e^x\sin y&=e^x\sin y}
\end{align}$$

---
## Exercise 4
Compute the contour integral of $f(z)=\dfrac{1}{z-1}$ over a square contour $\Gamma$, oriented counter-clockwise, centered at the origin with a side length B. The contour integral is:
$$I=\oint\dfrac{1}{z-1}\ dz$$
So I'm going to use a trick:
$$\begin{align}
\oint\dfrac{1}{z-1}\ dz&=2\pi i\cdot\text{Res}(z=1)\\
&=2\pi i\cdot\lim_{z\rightarrow 1}(z-1)\cdot\dfrac{1}{z-1}\\
\Aboxed{\oint\dfrac{1}{z-1}&=2\pi i}
\end{align}$$
Alternatively, I'll do as the question asked instead:
For $B\ge2$:
$$\begin{align}
\oint\dfrac{1}{z-1}\ dz&=\int_{-\tfrac{B}{2}}^{\tfrac{B}{2}}\dfrac{1}{\tfrac{B}{2}+iy-1}\ idy+\int_{\tfrac{B}{2}}^{-\tfrac{B}{2}}\dfrac{1}{-\tfrac{B}{2}+iy-1}\ idy\\
&+\int_{-\tfrac{B}{2}}^{\tfrac{B}{2}}\dfrac{1}{x-i\tfrac{B}{2}-1}\ dx+\int_{\tfrac{B}{2}}^{-\tfrac{B}{2}}\dfrac{1}{x+i\tfrac{B}{2}-1}\ dx\\
\Aboxed{\oint\dfrac{1}{z-1}\ dz&=2\pi i}
\end{align}$$
