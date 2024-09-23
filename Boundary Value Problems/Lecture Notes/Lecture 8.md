**Name:** Stanley Goodwin
**Date:** 9/13/2024

---
### General S-L Problems
The general Sturm-Liouville differential equation takes the following form:
$$\left(y'(x)\cdot p(x)\right)'+y(x)\cdot q(x)+\lambda_n\cdot y(x)\cdot r(x)=0$$
Properties of $\lambda_n$ & $y_n(x)$:
1) $\lambda_n$ is an increasing sequence.
2) $\lambda_n \rightarrow y_n(x)\ne0$.
3) $y_n(x)$ forms an orthogonal basis$\iff \displaystyle\int_a^by_i(x)\cdot y_j(x) \ \mathrm{d}x=C_i\delta_{ij}$.

Recall: $y''(x)+\lambda y(x)=0$ with $y(0)=0$ and $y(a)=0$.
$$\begin{align}\implies \lambda_n&=(n\pi)^2 & y_n(x)&=\sin\left(\dfrac{n\pi}{a}x\right)\end{align}$$
$$\begin{align}
\int_{c_1}^{c_2}y_n(x)\cdot y_m(x)\ \mathrm{d}x &=\int_{0}^{a}\sin\left(\dfrac{n\pi}{a}x\right)\sin\left(\dfrac{m\pi}{a}x\right)\ \mathrm{d}x\\
&=\int_{0}^{a}\sin\left(\dfrac{n\pi}{a}x\right)\left(\sin\left(\dfrac{(m=n)\pi}{a}x\right)+\sin\left(\dfrac{(m\ne n)\pi}{a}x\right)\right)\ \mathrm{d}x\\
&=\int_{0}^{a}\sin\left(\dfrac{n\pi}{a}x\right)\sin\left(\dfrac{(m=n)\pi}{a}x\right)\ \mathrm{d}x
+\int_{0}^{a}\sin\left(\dfrac{n\pi}{a}x\right)\sin\left(\dfrac{(m\ne n)\pi}{a}x\right)\ \mathrm{d}x\\
&=\int_{0}^{a}\sin^2\left(\dfrac{n\pi}{a}x\right)\ \mathrm{d}x + 0\\
&=\dfrac{a}{n\pi}\int_{x=0}^{x=a}\sin^2\left(u\right)\ \mathrm{d}u\\
c_n&=\dfrac{a^2}{2n\pi}\\
\end{align}$$

### Fourier Analysis
$$\begin{align}
F(k)&=\int_{-\infty}^{\infty} f(x)e^{-ikx}\ \mathrm{d}x &&\text{(Position)}\\
F(\omega)&=\int_{-\infty}^{\infty} f(t)e^{-i\omega t}\ \mathrm{d}t &&\text{(Time)}\\
\end{align}$$
Recall: $T=\dfrac{2\pi}{\omega}$ and $\lambda=\dfrac{2\pi}{k}$. For momentum, $p=\hbar k$, $E=\hbar\omega$.
This shows that ($x,p$) and $(t,E)$ are Fourier inverses.
$$[p,x]=i(\hbar k)x = i\hbar[k,x] \implies [x,p]=-i\hbar$$
