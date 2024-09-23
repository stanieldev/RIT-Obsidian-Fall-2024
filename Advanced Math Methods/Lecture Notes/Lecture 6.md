**Name:** Stanley Goodwin
**Date:** 9/12/2024

---
### Power Series
$$\begin{align}
S(z)&=\sum_{n=0}^\infty a_n(z-z_0)^n & \rho&=\limsup_{n\rightarrow\infty} |a_n|^{-1/n}
\end{align}$$
This series converges for $|z-z_0|\lt\rho$.
#### Exercise 1
Given $e^z=\displaystyle\sum_{n=0}^\infty\dfrac{z^n}{n!}$, find $\dfrac{de^z}{dz}=e^z$.
$$\begin{align}
\dfrac{de^z}{dz}&=\dfrac{d}{dz}\displaystyle\sum_{n=0}^\infty\dfrac{z^n}{n!}&& \text{(Substitution)}\\
&=\displaystyle\sum_{n=0}^\infty\dfrac{\partial}{\partial z}\dfrac{z^n}{n!}&& \text{(Fubini's Theorem)}\\
&=\displaystyle\sum_{n=0}^\infty\dfrac{n\cdot z^{n-1}}{n!}&& \text{(Derivative Power Rule)}\\
&=\displaystyle\sum_{n=1}^\infty\dfrac{z^{n-1}}{(n-1)!}+0&& \text{(n=0 contributes 0 to sum)}\\
&=\displaystyle\sum_{n=0}^\infty\dfrac{z^{n}}{n!}&& \text{(Reindexing the sum)}\\
\Aboxed{\dfrac{de^z}{dz}&=e^z}&& \text{(Q.E.D.)}
\end{align}$$
---

### Inverse Power Series
$$\begin{align}
L(z)&=\sum_{n=1}^\infty b_n(z-z_0)^{-n} \implies S\left(w=\dfrac{1}{z-z_0}\right)=\sum_{n=1}^\infty b_nw^{n}
\end{align}$$
This series converges for $|z-z_0|\gt\dfrac{1}{\rho}$.

### Laurent Series
$$\begin{align}
F(z)&=\displaystyle\sum_{n=-\infty}^\infty a_n(z-z_0)^n\\
&=S_+(z)+S_-(z)
\end{align}$$
Given radii of convergence of $\rho_+$ and $\rho_-$, then $F(z)$ converges on $\rho_-\lt|z-z_0|\lt\rho_+$.



Theorem: If $f(z)$ is holomorphic on $\Omega\subset\mathbb{C}$, $g\left(w\right)\equiv f^{-1}(z)$ is holomorphic, with:
$$\dfrac{dg(w)}{dw}=\left(\dfrac{df(g(w))}{dz}\right)^{-1}$$


### Finding the inverse of $e^z$
Let $f(z)=e^z$, which is known to be holomorphic on $z\in\mathbb{C}$.
It makes sense to find an inverse on $\Im(z)=0$, but there is cyclicity for imaginary numbers.
Let the region that is invertible: $\Omega=\left\{re^{i\theta}, r\in\mathbb{R}, \theta\in[-\pi,\pi)\right\}$.

**Principle-branch complex logarithm**
$$\forall z\in\Omega, f(z)=e^z=w \implies f^{-1}(w)=\ln(r)+i\theta=z$$
$$\begin{align}
w&=\ln(z)\\
&=\ln\left(re^{i\theta}\right)\\
&=\ln(r)+\ln\left(e^{i\theta}\right)\\
\Aboxed{w&=\ln(r)+i\theta}
\end{align}$$
There is a singularity at $\theta=\pi$, with limit of $2\pi i$, which is why there are infinitely many solutions.
Any integer multiple of that limit gives us different branches of the complex logarithm.

For any branch of the logarithm:
$$\ln_n(z)=|z|e^{i\left(\arg(z)+2\pi n\right)},\arg(z)\ne\pi, n\in\mathbb{Z}$$
The singularity at $\arg(z)=\pi$ is called a *branch cut singularity*.
