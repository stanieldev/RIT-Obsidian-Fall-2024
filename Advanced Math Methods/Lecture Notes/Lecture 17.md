**Name:** Stanley Goodwin
**Date:** 10/24/2024

---
### Tricks for solving
Didn't use, they're typical solution techniques from calculus.

### Example
We want to find this integral:
$$\begin{align}
I&=\int_{-\infty}^\infty\dfrac{\sin(x)}{x}\ dx\\
\end{align}$$
So let's break this up into a closed complex integral:
$$\begin{align}
\oint_\Gamma\dfrac{\sin(z)}{z}\ dz&=\int_{\epsilon}^R\dfrac{\sin(x)}{x}\ dx+\int_{-\pi}^0\dfrac{\sin\left(Re^{i\phi}\right)}{Re^{i\phi}}iRe^{i\phi}\ d\phi+\int_{\epsilon}^R\dfrac{\sin(x)}{x}\ dx+\int_{-\pi}^0\dfrac{\sin\left(\epsilon e^{i\phi}\right)}{\epsilon e^{i\phi}}i\epsilon e^{i\phi}\ d\phi\\
\Aboxed{\oint_\Gamma\dfrac{\sin(z)}{z}\ dz&=2\int_{\epsilon}^R\dfrac{\sin(x)}{x}\ dx}
\end{align}$$
We can calculate the complex integral using:







$$\begin{align}
I&=\int_{-\infty}^\infty\dfrac{\sin(x)}{x}\ dx\\
&=\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}I(\epsilon, R)\\
I(\epsilon, R)&=\dfrac{1}{2i}\left[\int_\Omega\dfrac{e^{ix}}{x}\ dx-\int_\Omega\dfrac{e^{-ix}}{x}\ dx\right]\\
&=
\end{align}$$