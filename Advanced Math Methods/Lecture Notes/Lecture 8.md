**Name:** Stanley Goodwin
**Date:** 9/19/2024

---
### Exercise 1
**Definition:** $\ln(z)=\ln\left(re^{i\theta}\right)=\ln(r)+i\theta$.
Q1) Radius Independence
$$\begin{align}
&\lim_{\epsilon\rightarrow0^+}\left(\ln\left(re^{i(\pi+\epsilon)}\right)-\ln\left(re^{i(\pi-\epsilon)}\right)\right)\\
=&\lim_{\epsilon\rightarrow0^+}\ln\left(\dfrac{re^{i(\pi+\epsilon)}}{re^{i(\pi-\epsilon)}}\right)\\
=&\lim_{\epsilon\rightarrow0^+}\ln\left(e^{i(\pi+\epsilon-\pi+\epsilon)}\right)\\
=&2i\lim_{\epsilon\rightarrow0^+}(\epsilon)\\
=&0\mod 2\pi i
\end{align}$$
Q2) Logarithm $\theta \le \tfrac{\pi}{2}$
$$\begin{align}
\ln\left(e^{i(\pi/3)}\cdot e^{i(\pi/3)}\right)&=\ln\left(e^{i(\pi/3)}\right)+\ln\left(e^{i(\pi/3)}\right)\\
\ln\left( e^{i(2\pi/3)}\right)&=\ln\left(e^{i(\pi/3)}\right)+\ln\left(e^{i(\pi/3)}\right)\\
\Aboxed{\dfrac{2\pi}{3}i&=\dfrac{\pi}{3}i+\dfrac{\pi}{3}i}
\end{align}$$
Q3) Logarithm $\theta \gt \tfrac{\pi}{2}$
$$\begin{align}
\ln\left(e^{i(2\pi/3)}\cdot e^{i(2\pi/3)}\right)&=\ln\left(e^{i(2\pi/3)}\right)+\ln\left(e^{i(2\pi/3)}\right)\\
\ln\left( e^{i(4\pi/3)}\right)&=\ln\left(e^{i(2\pi/3)}\right)+\ln\left(e^{i(2\pi/3)}\right)\\
\Aboxed{-\dfrac{2\pi}{3}i&\ne\dfrac{2\pi}{3}i+\dfrac{2\pi}{3}i }
\end{align}$$

### Complex Integration
Theorem: Let $f(z)=\dfrac{dF}{dz}$, where $F$ is holomorphic on $\Omega\in\mathbb{C}$, then:
$$\int_\gamma f(z)\ dz=\int_\gamma \dfrac{dF(z)}{dz}dz=F(\gamma_f)-F(\gamma_i)$$
This is the Fundamental Theorem of Calculus for complex variables.

Proof:
$$\begin{align}
\int_\gamma f(z)\ dz&=\int_\gamma \dfrac{dF}{dz}dz\\
&=\int_\gamma\left(\dfrac{dF}{dz}dx+i\dfrac{dF}{dz}dy\right)\\
&=\int_\gamma\left(\dfrac{dF}{dx}dx+\dfrac{dF}{dy}dy\right)\\
&=\int_\gamma\vec\nabla F\\
\Aboxed{\int_\gamma f(z)\ dz&=F(\gamma_f)-F(\gamma_i)}
\end{align}$$

### Integration over Closed Contours
Let $f(z)=(z-z_0)^k$, where $k\in\mathbb{Z}$, and $\gamma$ is some contour including $z=z_0$.
$$\begin{align}
\oint_\gamma f(z)dz&=\oint_\gamma (z-z_0)^k\ dz\\
&=\begin{cases}\left.\dfrac{(z-z_0)^{k+1}}{k+1}\right|_\gamma,& k\ne-1\\
\ln|z-z_0|_\gamma,&k=-1\end{cases}\\
\oint_\gamma f(z)dz&=\begin{cases}0,& k\ne-1\\
2\pi i,&k=-1\end{cases}
\end{align}$$
Using a Laurent Series $f(z)=\displaystyle\sum_{k=1}^\infty c_n(z-z_0)^{-k}$, then:
$$\begin{align}
\oint_\gamma f(z)dz&=\oint_\gamma \sum_{k=1}^\infty c_k(z-z_0)^{-k}\ dz\\
&=\sum_{k=1}^\infty c_k\oint_\gamma (z-z_0)^{-k}\ dz\\
\Aboxed{\oint_\gamma f(z)dz&=2\pi i c_1}
\end{align}$$
