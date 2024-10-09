**Name:** Stanley Goodwin
**Date:** 10/01/2024

---

#### Example 1
$$\begin{align}
\text{Let }f(z)&=\dfrac{1}{z}e^z\\
\oint f(z)\ dz &= \oint \dfrac{1}{z}e^z\ dz \\
&= \oint\dfrac{1}{z}\sum_n\dfrac{z^n}{n!}\ dz \\
&= \oint\sum_n\dfrac{z^{n-1}}{n!}\ dz \\
&= \oint\sum_{n=0}\dfrac{z^{n-1}}{n!}\ dz+\oint\sum_{n\ge1}\dfrac{z^{n-1}}{n!}\ dz \\
&= \dfrac{1}{0!}\oint\dfrac{1}{z}+0 \\
\Aboxed{\oint f(z)\ dz &= 2\pi i}
\end{align}$$
#### Example 2
$$\begin{align}
\text{Let }f(z)&=\dfrac{1}{z}\sin(z)\\
\oint f(z)\ dz &= \oint \dfrac{1}{z}\sin(z)\ dz \\
&= \oint\dfrac{1}{z}\sum_n\dfrac{(-1)^n\cdot z^{2n+1}}{(2n+1)!}\ dz \\
&= \oint\sum_n\dfrac{(-1)^n\cdot z^{2n}}{(2n+1)!}\ dz \\
&= \sum_n\dfrac{(-1)^n}{(2n+1)!}\oint z^{2n}\ dz \\
\Aboxed{\oint f(z)\ dz &= 0}
\end{align}$$
### Cauchy Integral Formula
Consider $f(z)$ holomorphic in $\Omega\subset\mathbb{C}$, where $\forall t, \Gamma(t)\in\Omega$, and $z_0\in\Gamma$:
$$\begin{align}
\oint_{\Gamma}\dfrac{f(z)}{z-z_0}\ dz=2\pi i f(z_0)
\end{align}$$
#### Cauchy Integral Proof
$$\begin{align}
\text{Let }z&=z_0+re^{i\theta}\\
\oint_{\Gamma}\dfrac{f(z)}{z-z_0}\ dz
&=\oint_{\Gamma}\dfrac{f(z_0+re^{i\theta})}{z_0+re^{i\theta}-z_0}\ d\left(z_0+re^{i\theta}\right)\\
&=\oint_{\Gamma}\dfrac{f(z_0+re^{i\theta})}{re^{i\theta}}\cdot ire^{i\theta} d\theta\\
&=\oint_{\Gamma}f(z_0+re^{i\theta})\cdot i d\theta\\
\lim_{r\rightarrow 0}\oint_{\Gamma}\dfrac{f(z)}{z-z_0}\ dz
&=
\lim_{r\rightarrow 0}\oint_{\Gamma}f(z_0+re^{i\theta})\cdot i d\theta\\
&=\oint_{\Gamma}\lim_{r\rightarrow 0}f(z_0+re^{i\theta})\cdot i d\theta\\
&=\oint_{\Gamma}f(z_0)\ i d\theta\\
&=if(z_0)\oint_{\Gamma}d\theta\\
&=if(z_0)(2\pi)\\
\Aboxed{\oint_{\Gamma}\dfrac{f(z)}{z-z_0}\ dz&=2\pi i f(z_0)}
\end{align}$$

