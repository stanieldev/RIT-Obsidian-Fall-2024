**Name:** Stanley Goodwin
**Date:** 9/20/2024

---

$$\begin{align}
I(n) &= \int_0^\pi x^n\cos(kx)\ dx\\
&=x^n\dfrac{\sin(kx)}{k}-\int_0^\pi nx^{n-1}\dfrac{\sin(kx)}{k}\ dx\\
&=x^n\dfrac{\sin(kx)}{k}+nx^{n-1}\dfrac{\cos(kx)}{k^2}-\int_0^\pi n(n-1)x^{n-2}\dfrac{\cos(kx)}{k^2}\ dx\\
&=x^n\dfrac{\sin(kx)}{k}+nx^{n-1}\dfrac{\cos(kx)}{k^2}-\dfrac{n(n-1)}{k^2}\int_0^\pi x^{n-2}\cos(kx)\ dx\\
&=\pi^n\dfrac{\sin(k\pi)}{k}+n\pi^{n-1}\dfrac{\cos(k\pi)}{k^2}-\dfrac{n(n-1)}{k^2}I(n-2)\\
I(n)&=n\pi^{n-1}\dfrac{(-1)^k}{k^2}-\dfrac{n(n-1)}{k^2}I(n-2)\\
\end{align}$$
Suppose $n$ is even:
$$\begin{align}
I(n)&=n\pi^{n-1}\dfrac{(-1)^k}{k^2}-\dfrac{n(n-1)}{k^2}I(n-2)\\
&=n\pi^{n-1}\dfrac{(-1)^k}{k^2}-\dfrac{n(n-1)}{k^2}(n-2)\pi^{n-3}\dfrac{(-1)^k}{k^2}+\dfrac{n(n-1)}{k^2}\dfrac{(n-2)(n-3)}{k^2}I(n-4)\\
&=\dfrac{n!}{(n-1)!}\pi^{n-1}\dfrac{(-1)^k}{k^2}-\dfrac{n!}{(n-3)!}\pi^{n-3}\dfrac{(-1)^k}{k^4}+\dfrac{n!}{(n-4)!}\dfrac{1}{k^4}I(n-4)\\
&=\dfrac{1}{k}\sum_{i=1,3,5,\dots} \dfrac{n!}{(n-i)!}k^{-i}(-1)^k
\end{align}$$
