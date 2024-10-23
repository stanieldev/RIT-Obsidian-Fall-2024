**Name:** Stanley Goodwin
**Date:** 10/22/2024

---
### Waves
In 1D, $f(x,t)=A\cos(kx-\omega t+\phi)$. There are other solutions, but we're starting with the cosine since we can build any other solution from a linear combination of these cosine solutions.

In 3D, $f(\vec{x},t)=\vec{A}\cos(\vec{k}\cdot\vec{x}-\omega t+\phi)$.
### Energy and Momentum in Waves
More generally, $\mathcal{U}_\text{EM}=\dfrac{1}{2}\epsilon_0E_0^2+\dfrac{1}{2\mu_0}B_0^2$
For our plane wave,
$$\vec{E}(\vec{x},t)=\Re\left(\vec{\tilde{E}}(\vec{x},t)\right)=E_0\cos\left(\vec{k}\cdot\vec{x}-\omega t+\phi\right)$$
For a linearly polarized wave, $\vec{E}_0=E_0\hat{n}$, as well as $\vec{B}=\dfrac{\hat{k}\times\vec{E}}{c}$.
$$\begin{align}
\mathcal{U}_\text{EM}
&=\dfrac{1}{2}\epsilon_0E_0^2\cos^2\left(\dots\right)+\dfrac{1}{2\mu_0c^2}E_0^2\cos^2\left(\dots\right)\\
&=\epsilon_0E_0^2\cos^2\left(\vec{k}\cdot\vec{x}-\omega t+\phi\right)\\
\Aboxed{\langle\mathcal{U}_\text{EM}\rangle&=\dfrac{1}{2}\epsilon_0E_0^2}
\end{align}$$
Taking a look at the Poynting Vector: $\vec{S}=\dfrac{\vec{E}\times\vec{B}}{\mu_0}$:
$$\begin{align}
\vec{S}
&=\dfrac{\vec{E}\times\vec{B}}{\mu_0}\\
&=\dfrac{E\tfrac{E}{c}}{\mu_0}\hat{k}\\
&=\dfrac{E^2}{c\mu_0}\hat{k}\\
&=c\epsilon_0E^2\hat{k}\\
\Aboxed{\langle\vec{S}\rangle&=c\langle\mathcal{U}_\text{EM}\rangle\hat{k}}
\end{align}$$
We can compare this to:
$$\begin{align}
\langle\vec{S}\rangle&=\langle\mathcal{U}_\text{EM}\rangle c\hat{k}\\
\vec{J}&=\rho\vec{v}
\end{align}$$
