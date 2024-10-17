**Name:** Stanley Goodwin
**Date:** 10/17/2024

---
### Lorentzian Distribution
Consider a function $L(x)=N^{-1}\dfrac{1}{x^2+a^2}$, named the Lorentzian Distribution.
The value of $N$ is calculated as $N=\displaystyle\int_{-\infty}^{\infty}\dfrac{1}{x^2+a^2}\ dx$.

Given $\Gamma$ as a semi-circle of the upper lane and $\bar\gamma$ as the arc of the semicircle:
$$\begin{align}
\lim_{R\rightarrow\infty}\int_{-R}^{R}\dfrac{1}{x^2+a^2}\ dx
&=\lim_{R\rightarrow\infty}\oint_\Gamma\dfrac{1}{z^2+a^2}\ dz-\lim_{R\rightarrow\infty}\int_\bar\gamma\dfrac{1}{z^2+a^2}\ dz\\
&=\lim_{R\rightarrow\infty}\oint_\Gamma\dfrac{1}{z^2+a^2}\ dz-\lim_{R\rightarrow\infty}\int_0^{\pi}\dfrac{iRe^{i\phi}}{R^2e^{2i\phi}+a^2}\ d\phi\\
\Aboxed{\lim_{R\rightarrow\infty}\int_{-R}^{R}\dfrac{1}{x^2+a^2}\ dx&=\lim_{R\rightarrow\infty}\oint_\Gamma\dfrac{1}{z^2+a^2}\ dz}
\end{align}$$
We can solve the right-hand side using our techniques in complex analysis:
$$\begin{align}
\lim_{R\rightarrow\infty}\oint_\Gamma\dfrac{1}{z^2+a^2}\ dz
&=\lim_{R\rightarrow\infty}\oint_\Gamma\dfrac{1}{(z-ia)(z+ia)}\ dz\\
&=2\pi i\cdot \mathrm{Res}(z=ia)\\
&=2\pi i\cdot \lim_{z\rightarrow ia}(z-ia)\dfrac{1}{(z-ia)(z+ia)}\\
&=2\pi i\cdot \lim_{z\rightarrow ia}\dfrac{1}{(z+ia)}\\
&=2\pi i\cdot \dfrac{1}{2ia}\\
\Aboxed{\lim_{R\rightarrow\infty}\oint_\Gamma\dfrac{1}{z^2+a^2}\ dz&=\dfrac{\pi}{a}}
\end{align}$$
Therefore, we can say that:
$$\begin{align}
\Aboxed{\lim_{R\rightarrow\infty}\int_{-R}^{R}\dfrac{1}{x^2+a^2}\ dx&=\dfrac{\pi}{a}}
\end{align}$$
Which means we can write the Lorentzian Distribution as:
$$\begin{align}
\Aboxed{L(x)=\dfrac{a}{\pi}\cdot\dfrac{1}{x^2+a^2}}
\end{align}$$
### Darboux Theorem
$$\begin{align}
\text{If } z\cdot f(z) \rightarrow 0 \text{ as }|z|\rightarrow\infty\\
\text{Then } \int_{\gamma}f(z)\ dz \rightarrow 0 \text{ as }R\rightarrow\infty\\
\end{align}$$
