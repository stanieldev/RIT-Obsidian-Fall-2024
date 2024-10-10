**Name:** Stanley Goodwin
**Date:** 10/10/2024

# Practice Assignment #6

In this assignment, we consider the function $f(z)=\ln(z-(3+i))\tfrac{1}{z^2}$, where $\ln$ refers to the principle branch of the logarithm function. The goal is to explore the singularities of this function, its series expansion, and to compute contour integrals.

---
## Exercise 1
*Describe all singularities of $f(z)$ and classify each as either a pole, branch point, or other type of singularity. Additionally, provide a clear sketch indicating the location of each singularity in the complex plane.*

Given the function $f(z)=\ln(z-(3+i))\tfrac{1}{z^2}$, we can see the following:
 - Branch cut singularity at $z=x+i, x\lt3$.
 - Branch point at $z=3+i$.
 - Order 2 pole at $z=0+0i$.

![[HW6_Q1.png]]

---
## Exercise 2
Consider $z_0=2$. Determine whether it is possible to express $f(z)$ as a Laurent series (bilateral series) of the form:
$$f(z)=\sum_{n=-\infty}^\infty a_n(z-z_0)^n$$
*If such a series exists, determine the radius of convergence (i.e. the radius of it internal boundary $\rho_1$ and the radius of its external boundary $\rho_2$). Also, state explicitly if the series involves negative powers and what is the smallest value of $n$ such that $a_n\ne0$.*

About the point $z_0=2$, the closest singularity is the point $z=2+i$ on the branch cut of the natural log. The radius between $z_0$ and the closest singularity is 1.
$$\begin{align}
\Aboxed{\rho_1&=0}\\
\Aboxed{\rho_2&=1}
\end{align}$$
Since it doesn't enclose any poles at the origin, the Laurent series is equal to a Taylor series.
Put differently, the smallest $a_n\ne0$ is $n=0$.

---
## Exercise 3
Consider $z_0=0$. Determine whether it is possible to express $f(z)$ as a Laurent series (bilateral series) of the form:
$$f(z)=\sum_{n=-\infty}^\infty b_n(z-z_0)^n$$
*If such a series exists, determine the radius of convergence (i.e. the radius of it internal boundary $\rho_1$ and the radius of its external boundary $\rho_2$). Also, state explicitly if the series involves negative powers and what is the smallest value of $n$ such that $b_n\ne0$.*


About the point $z_0=0$, the closest singularity (that is not the center) is the point $z=0+i$ on the branch cut of the natural log. The radius between $z_0$ and the closest singularity is 1.
$$\begin{align}
\Aboxed{\rho_1&=0}\\
\Aboxed{\rho_2&=1}
\end{align}$$
Since this series expansion does enclose a pole at the origin, the Laurent series is necessary to express this function about the point $z=0$. Since the pole at the origin is of order $2$, then the smallest $b_n\ne0$ is $n=-2$, with the term $\dfrac{b_{-2}}{z^2}$.

---
## Exercise 4
Consider $z_0=3+i$. Determine whether it is possible to express $f(z)$ as a Laurent series (bilateral series) of the form:
$$f(z)=\sum_{n=-\infty}^\infty c_n(z-z_0)^n$$
*If such a series exists, determine the radius of convergence (i.e. the radius of it internal boundary $\rho_1$ and the radius of its external boundary $\rho_2$). Also, state explicitly if the series involves negative powers and what is the smallest value of $n$ such that $c_n\ne0$.*

About the point $z_0=3+i$, the closest singularity (that is not the center) is the point $z=3+i-\epsilon$ on the branch cut of the natural log. The radius between $z_0$ and the closest singularity is $\epsilon$.
$$\begin{align}
\Aboxed{\rho_1&=0}\\
\Aboxed{\rho_2&=\lim_{\epsilon\rightarrow0}|z-z_0|}
\end{align}$$
Therefore, there is **no series** (Laurent nor Taylor) expansion about $z_0=3+i$.

---
## Exercise 5
Consider a closed counter-clockwise curve $\gamma_1$ around the point $1−i$ with radius $1$.
*Compute the contour integral:*
$$I_1=\oint_{\gamma_1}f(z)\ dz$$
About the point $z_0=1-i$, there are no enclosed singularities within a circle of radius 1, and so:
$$\oint_{\gamma_1}f(z)\ dz=0\implies \boxed{I_1=0}$$
---
## Exercise 6
Consider a closed counter-clockwise curve $\gamma_2$ around the origin with radius $1$. Compute the contour integral:
$$I_2=\oint_{\gamma_2}f(z)\ dz$$
About the point $z_0=0$, there is only 1 enclosed singularity within a circle of radius 1, which is a pole of order 2. Therefore, we can write:
$$\begin{align}
I_2&=\oint_{\gamma_2}f(z)\ dz\\
&=2\pi i\cdot\lim_{z\rightarrow 0}\dfrac{d}{dz}\left(z^2f(z)\right)\\
&=2\pi i\cdot\lim_{z\rightarrow 0}\dfrac{d}{dz}\left(\ln(z-(3+i))\right)\\
&=2\pi i\cdot\lim_{z\rightarrow 0}\left(\dfrac{1}{z-(3+i)}\right)\\
&=-2\pi i\left(\dfrac{1}{3+i}\right)\\
&=-2\pi i\left(\dfrac{3-i}{3^2+1^2}\right)\\
\Aboxed{I_2&=-\dfrac{\pi}{5}-i\dfrac{3\pi}{5}}\\
\end{align}$$
I'm not 100% sure about this one, don't take this as fact.


## Continued Lecture
$$\begin{align}
\oint_{\gamma}\dfrac{1}{z}\ dz&\iff\int_{0}^{2\pi}\dfrac{1}{re^{i\theta}}\ ire^{i\theta}d\theta\\
\oint_{\gamma}\dfrac{1}{z}\ dz&\iff\int_{0}^{2\pi}i d\theta\\
\end{align}$$
So we want to find the inverse of converting to polar coordinates.
### Example 1
$$\begin{align}
I&=\int_{0}^{2\pi}\dfrac{1}{a+\sin\theta}\ d\theta, (a>1)
\end{align}$$
We can express $\sin\theta$ as a combination of complex exponentials:
$$\begin{align}
\sin\theta&=\dfrac{e^{i\theta}-e^{-i\theta}}{2i}=\left.\dfrac{z-\tfrac{1}{z}}{2i}\right|_{z=e^{i\theta}}
\end{align}$$
We can also do the same with our differential:
$$\begin{align}
z=e^{i\theta}\implies dz=ie^{i\theta}d\theta\implies d\theta=-i\dfrac{dz}{z}
\end{align}$$
So we can continue with our integral:
$$\begin{align}
I&=\int_{0}^{2\pi}\dfrac{1}{a+\sin\theta}\ d\theta\\
&=\int\dfrac{1}{a+\tfrac{z-\tfrac{1}{z}}{2i}}\cdot\dfrac{-i}{z}\ dz\\
&=2\int\dfrac{1}{z^2+(2ia)z-1}\ dz\\
&=2\int\dfrac{1}{(z-2ia+2\sqrt{1-a^2})}\dfrac{1}{(z-2ia-2\sqrt{1-a^2})}\ dz\\
\end{align}$$
$$\dfrac{1}{2b}\left(\dfrac{1}{z+a+b}-\dfrac{1}{z+a-b}\right)=\dfrac{1}{\left(z+a-b\right)\left(z+a+b\right)}$$
$$\begin{align}
&=2\int\dfrac{1}{(z-2ia+2\sqrt{1-a^2})}\dfrac{1}{(z-2ia-2\sqrt{1-a^2})}\ dz\\
&=\dfrac{2}{2\cdot2\sqrt{1-a^2}}\left(\int\dfrac{1}{z-2ia+2\sqrt{1-a^2}}\ dz-\int\dfrac{1}{z-2ia-2\sqrt{1-a^2}}\ dz\right)\\
&=\dfrac{1}{2\sqrt{1-a^2}}\left(\int\dfrac{1}{z-2ia+2\sqrt{1-a^2}}\ dz-\int\dfrac{1}{z-2ia-2\sqrt{1-a^2}}\ dz\right)\\
&=\dfrac{1}{2\sqrt{1-a^2}}\left(\ln\left|z-2ia+2\sqrt{1-a^2}\right|-\ln\left|z-2ia-2\sqrt{1-a^2}\right|\right)\\
&=\dfrac{1}{2\sqrt{1-a^2}}\ln\left|\dfrac{z-2ia+2\sqrt{1-a^2}}{z-2ia-2\sqrt{1-a^2}}\right|\\
&=\dfrac{1}{2\sqrt{1-a^2}}\ln\left|\dfrac{1+\dfrac{2\sqrt{1-a^2}}{z-2ia}}{1-\dfrac{2\sqrt{1-a^2}}{z-2ia}}\right|\\
&=\dfrac{1}{2\sqrt{1-a^2}}\dfrac{1}{2}\tanh^{-1}\left(\dfrac{2\sqrt{1-a^2}}{z-2ia}\right)\\
I&=\dfrac{1}{4\sqrt{1-a^2}}\tanh^{-1}\left(\dfrac{2\sqrt{1-a^2}}{z-2ia}\right)\\
\end{align}$$
