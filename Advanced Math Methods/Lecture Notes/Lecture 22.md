**Name:** Stanley Goodwin
**Date:** 11/12/2024

---
### RL Circuit
Consider an LR circuit with a resistor and inductor in series,
$$\begin{align}
\left[\dfrac{d}{dt}+\alpha\right]I(t)&=W(t)
\end{align}$$
where $\alpha=R/L$ and $W(t)=V(t)/L$.
$$\begin{align}
\left[\dfrac{d}{dt}+\alpha\right]G(t)&=\delta(t)\\
\mathcal{F}\left\{\left[\dfrac{d}{dt}+\alpha\right]G(t)\right\}&=\mathcal{F}\left\{\delta(t)\right\}\\
\mathcal{F}\left\{\dfrac{d}{dt}G(t)\right\}+\alpha\mathcal{F}\left\{G(t)\right\}&=\mathcal{F}\left\{\delta(t)\right\}\\
-i\omega\tilde{G}(\omega)+\alpha\tilde{G}(\omega)&=1\\
\left(\alpha-i\omega\right)\tilde{G}(\omega)&=1\\
\Aboxed{\tilde{G}(\omega)&=\dfrac{1}{\alpha-i\omega}}
\end{align}$$
We can then find $G(t)$ using the inverse Fourier transform:
$$\begin{align}
G(t)&=\mathcal{F}^{-1}\left\{\tilde{G}(\omega)\right\}\\
&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\alpha-i\omega}\ \dfrac{d\omega}{2\pi}\\
&=-\dfrac{1}{2\pi i}\int_{-\infty}^\infty \dfrac{e^{-i\omega t}}{\omega+i\alpha}\ d\omega\\
&=\dfrac{1}{2\pi i}\oint_\mathbb{C} \dfrac{e^{-i\omega t}}{\omega+i\alpha}\ d\omega\\
&=\dfrac{1}{2\pi i}2\pi i\cdot\theta(t)\lim_{\omega\rightarrow-i\alpha}e^{-i\omega t}\\
\Aboxed{G(t)&=\theta(t)e^{-\alpha t}}
\end{align}$$
Therefore, the solution then takes the following form:
$$\begin{align}
I(t)&=\int_{-\infty}^\infty G(t-\tau)W(\tau)\ d\tau\\
&=\int_{-\infty}^\infty \theta(t-\tau)e^{-\alpha(t-\tau)}W(\tau)\ d\tau\\
&=e^{-\alpha t}\int_{-\infty}^\infty \theta(t-\tau)e^{\alpha\tau}W(\tau)\ d\tau\\
\Aboxed{I(t)&=e^{-\alpha t}\int_{-\infty}^{t}e^{\alpha\tau}W(\tau)\ d\tau}\\
\end{align}$$
















smelly smell that smells... smelly