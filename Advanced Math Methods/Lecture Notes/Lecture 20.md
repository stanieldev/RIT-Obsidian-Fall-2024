**Name:** Stanley Goodwin
**Date:** 11/5/2024

---

### Fourier Transforms
$$\begin{align}
\tilde{f}(k)&=\int_{-\infty}^\infty e^{-ikx}f(x)\ dx 
&\iff&& 
f(x)&=\int_{-\infty}^\infty e^{+ikx}\tilde{f}(k)\ \dfrac{dk}{2\pi}\\
\tilde{f}(\omega)&=\int_{-\infty}^\infty e^{+i\omega t}f(t)\ dt 
&\iff&& 
f(t)&=\int_{-\infty}^\infty e^{-i\omega t}\tilde{f}(\omega)\ \dfrac{d\omega}{2\pi}\\
\end{align}$$
### Fourier Transforms with Differentials
$$\begin{align}
\dfrac{\partial^n}{\partial t^n}f(t)&=\dfrac{\partial^n}{\partial t^n}\int_{-\infty}^\infty e^{-i\omega t}\tilde{f}(\omega)\ \dfrac{d\omega}{2\pi}\\
&=\int_{-\infty}^\infty \dfrac{\partial^n}{\partial t^n}e^{-i\omega t}\tilde{f}(\omega)\ \dfrac{d\omega}{2\pi}\\
&=\int_{-\infty}^\infty (-i\omega)^n e^{-i\omega t}\tilde{f}(\omega)\ \dfrac{d\omega}{2\pi}\\
&=(-i)^n\int_{-\infty}^\infty e^{-i\omega t}\left(\omega^n\tilde{f}(\omega)\right)\ \dfrac{d\omega}{2\pi}\\
\end{align}$$
For any derivative, if $\tilde{f}(\omega)$ and $\omega^n\tilde{f}(\omega)$ is XXX, then the $n$-th derivative has a Fourier Transform.

### Definition of Convolution
The integral form of the convolution can be written as the following:
$$\begin{align}
(f_1*f_2)(t)&=\int_{-\infty}^\infty f_1(t-t')f_2(t')\ dt'
\end{align}$$
#### Time-Translational Invariance
$$\begin{align}
\vec{P}(t)&=\int_{-\infty}^\infty \delta(t-t')\vec{E}(t')\ dt'
\end{align}$$
#### Causality
$$\begin{align}
\vec{P}(t)&=\int_{-\infty}^t \delta(t-t')\vec{E}(t')\ dt'\\
\vec{P}(t)&=\int_0^\infty \delta(t)\vec{E}(t'-\tau)\ d\tau\\
\end{align}$$
