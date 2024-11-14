**Name:** Stanley Goodwin
**Date:** XX/XX/2024
**Collaborators:** None

In this assignment, we will analyze a model for the response of a dielectric to an external electric field. Consider the following differential equation for the polarization density $P(t)$:
$$\left[\dfrac{d^2}{dt^2}+\gamma\dfrac{d}{dt}+\Omega_0^2\right]P(t)=\dfrac{ne^2}{m}E(t)$$
where $\gamma$ and $\Omega_0$ are positive constants, $n$ is the density of atoms per volume, $e$ is the electron charge and $m$ is the electron mass. Following similar steps as we did for the RL circuit, we will solve this equation using the Green's function method, where in this context the Green's function is traditionally called the electric susceptibility $\chi(t)$.

---
## Exercise 1
Formally seek a solution expressing $P(t)$ and $E(t)$ as continuous linear combinations of plane waves:
$$\begin{align}
P(t)&=\int e^{-i\omega t}\tilde{P}(\omega)\ \dfrac{d\omega}{2\pi}\\
E(t)&=\int e^{-i\omega t}\tilde{E}(\omega)\ \dfrac{d\omega}{2\pi}\\
\end{align}$$
Substitute these expressions into the differential equation and identify the electric susceptibility $\tilde{\chi}(\omega)$ through the definition $\tilde{P}(\omega)=\tilde{\chi}(\omega)\tilde{E}(\omega)$. 
$$\begin{align}
\left[\dfrac{d^2}{dt^2}+\gamma\dfrac{d}{dt}+\Omega_0^2\right]P(t)&=\dfrac{ne^2}{m}E(t)\\
\left[\dfrac{d^2}{dt^2}+\gamma\dfrac{d}{dt}+\Omega_0^2\right]\int e^{-i\omega t}\tilde{P}(\omega)\ \dfrac{d\omega}{2\pi}&=\dfrac{ne^2}{m}\int e^{-i\omega t}\tilde{E}(\omega)\ \dfrac{d\omega}{2\pi}\\
\int \left[\dfrac{d^2}{dt^2}+\gamma\dfrac{d}{dt}+\Omega_0^2\right]e^{-i\omega t}\tilde{P}(\omega)\ \dfrac{d\omega}{2\pi}&=\dfrac{ne^2}{m}\int e^{-i\omega t}\tilde{E}(\omega)\ \dfrac{d\omega}{2\pi}\\
\int \left[(-i\omega)^2-i\omega\gamma+\Omega_0^2\right]e^{-i\omega t}\tilde{P}(\omega)\ \dfrac{d\omega}{2\pi}&=\dfrac{ne^2}{m}\int e^{-i\omega t}\tilde{E}(\omega)\ \dfrac{d\omega}{2\pi}\\
\left[-\omega^2-i\omega\gamma+\Omega_0^2\right]\tilde{P}(\omega)&=\dfrac{ne^2}{m}\tilde{E}(\omega)\\
\tilde{P}(\omega)&=-\dfrac{ne^2}{m}\dfrac{1}{\omega^2+i\omega\gamma-\Omega_0^2}\tilde{E}(\omega)\\
\Aboxed{\tilde{\chi}(\omega)&=-\dfrac{ne^2}{m}\dfrac{1}{\omega^2+i\omega\gamma-\Omega_0^2}}
\end{align}$$
Factor each denominator of $\tilde{\chi}(\omega)$ and determine the position of its poles in the complex $\omega$-plane.
$$\begin{align}
\tilde{\chi}(\omega)&=-\dfrac{ne^2}{m}\dfrac{1}{\omega^2+i\omega\gamma-\Omega_0^2}\\
\omega_\pm&=-\dfrac{i\gamma}{2}\pm\sqrt{-\dfrac{\gamma^2}{4}+\Omega_0^2}\\
\Aboxed{\omega_\pm&=\dfrac{i}{2}\left(-\gamma\pm\sqrt{\gamma^2-4\Omega_0^2}\right)}\\
\Aboxed{\tilde{\chi}(\omega)&=\dfrac{ne^2}{m}\dfrac{-1}{(\omega-\omega_+)(\omega-\omega_-)}}
\end{align}$$
The poles are at the 2 points $\omega_\pm$, which looks like the following graph:
INSERT_GRAPH_HERE

---
## Exercise 2
Calculate $\chi(t)$ by evaluating:
$$\begin{align}
\chi(t)&=\int e^{-i\omega t}\tilde{\chi}(\omega)\ \dfrac{d\omega}{2\pi}
\end{align}$$
following the same contour integration approach used for the RL circuit. Explain clearly what integration contour you choose depending on the sign of $t$ and why, using Jordon's lemma.

---
## Exercise 3
Using the expression you found for $\chi(t)$, explain whether the response of the dielectric satisfies causality, specifically:
 - What is the physical significance of the $\theta(t)$ factor?
 - How is causality reflected in the analytic properties of $\tilde{\chi}(\omega)$?

---
## Exercise 4
Consider an electric field pulse of the form:
$$E_T(t)=\begin{cases}\tfrac{1}{T},&-\tfrac{T}{2}<t<\tfrac{T}{2}\\0,& \text{otherwise}\end{cases}$$
and the corresponding polarization $P_T(t)$, using the general convolution formula:
$$P(t)=\int_{-\infty}^\infty\chi(t-\tau)E(\tau)\ d\tau$$
Determine the value of $P_T(t)$ for all $t\ne0$ in the limit for $T\rightarrow0$.
