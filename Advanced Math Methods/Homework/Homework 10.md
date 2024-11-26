**Name:** Stanley Goodwin
**Date:** 11/14/2024
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
![[HW10_Q1.png]]
https://www.desmos.com/calculator/4mieh458km

---
## Exercise 2
Calculate $\chi(t)$ by evaluating:
$$\begin{align}
\chi(t)&=\int e^{-i\omega t}\tilde{\chi}(\omega)\ \dfrac{d\omega}{2\pi}
\end{align}$$
following the same contour integration approach used for the RL circuit. Explain clearly what integration contour you choose depending on the sign of $t$ and why, using Jordon's lemma.

I'm using a half-circle that goes into the negative imaginary axis:
$$\begin{align}
\dfrac{ne^2}{m}\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=\dfrac{ne^2}{m}\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}+\lim_{R\rightarrow\infty}\dfrac{ne^2}{m}\int_\pi^{2\pi} e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}\\
\dfrac{ne^2}{m}\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=\dfrac{ne^2}{m}\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}+0\\
\Aboxed{\dfrac{ne^2}{m}\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=\dfrac{ne^2}{m}\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}}
\end{align}$$
We can then just use the residue theorem:
$$\begin{align}
\dfrac{ne^2}{m}\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=2\pi i\dfrac{ne^2}{m}\left(\text{Res}(\omega=\omega_+)+\text{Res}(\omega=\omega_-)\right)
\end{align}$$
So we can calculate the residues:
$$\begin{align}
\text{Res}(\omega=\omega_+)&=\lim_{\omega\rightarrow\omega_+}(\omega-\omega_+)\left(\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{e^{-i\omega t}}{2\pi}\right)\\
&=\lim_{\omega\rightarrow\omega_+}(\omega-\omega_+)\left(\dfrac{-1}{(\omega-\omega_+)(\omega-\omega_-)}\dfrac{e^{-i\omega t}}{2\pi}\right)\\
&=\lim_{\omega\rightarrow\omega_+}\left(\dfrac{-1}{\omega-\omega_-}\dfrac{e^{-i\omega t}}{2\pi}\right)\\
\Aboxed{\text{Res}(\omega=\omega_+)&=-\dfrac{1}{\omega_+-\omega_-}\dfrac{e^{-i\omega_+t}}{2\pi}}\\
\text{Res}(\omega=\omega_-)&=\lim_{\omega\rightarrow\omega_-}(\omega-\omega_-)\left(\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{e^{-i\omega t}}{2\pi}\right)\\
&=\lim_{\omega\rightarrow\omega_-}(\omega-\omega_-)\left(\dfrac{-1}{(\omega-\omega_+)(\omega-\omega_-)}\dfrac{e^{-i\omega t}}{2\pi}\right)\\
&=\lim_{\omega\rightarrow\omega_-}\left(\dfrac{-1}{\omega-\omega_+}\dfrac{e^{-i\omega t}}{2\pi}\right)\\
\Aboxed{\text{Res}(\omega=\omega_+)&=\dfrac{1}{\omega_+-\omega_-}\dfrac{e^{-i\omega_-t}}{2\pi}}\\
\end{align}$$
Substituting, we get:
$$\begin{align}
\dfrac{ne^2}{m}\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=2\pi i\dfrac{ne^2}{m}\left(\text{Res}(\omega=\omega_+)+\text{Res}(\omega=\omega_-)\right)\theta(t)\\
&=2\pi i\dfrac{ne^2}{m}\left(-\dfrac{1}{\omega_+-\omega_-}\dfrac{e^{-i\omega_+t}}{2\pi}+\dfrac{1}{\omega_+-\omega_-}\dfrac{e^{-i\omega_-t}}{2\pi}\right)\theta(t)\\
&=\dfrac{i}{\omega_+-\omega_-}\dfrac{ne^2}{m}\left(e^{-i\omega_-t}-e^{-i\omega_+t}\right)\theta(t)\\
&=\theta(t)i\dfrac{ne^2}{m}\dfrac{e^{-i\omega_-t}-e^{-i\omega_+t}}{\omega_+-\omega_-}\\
\end{align}$$
By inspection, we can see that $\omega_\pm=i\lambda_\pm$, and so:
$$\begin{align}
&=\theta(t)i\dfrac{ne^2}{m}\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}\\
&=\theta(t)i\dfrac{ne^2}{m}\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{i\lambda_+-i\lambda_-}\\
\Aboxed{\chi(t)&=\dfrac{ne^2}{m}\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}}\\
\Aboxed{\lambda_\pm&=\dfrac{1}{2}\left(-\gamma\pm\sqrt{\gamma^2-4\Omega_0^2}\right)}
\end{align}$$
---
## Exercise 3
Using the expression you found for $\chi(t)$, explain whether the response of the dielectric satisfies causality, specifically:
 - What is the physical significance of the $\theta(t)$ factor?
 - How is causality reflected in the analytic properties of $\tilde{\chi}(\omega)$?

The response is causal because of the $\theta(t)$ component, making it zero for all times up to the integration are allowed to influence the present, but the future is not.

The physical significance of $\theta(t)$ is that it enforces causality on the definition of the function, relating to the above comment.

I assume by the analytic properties is that it comes from the function being holomorphic in the upper half complex plane, and so then leads to causality directly.

---
## Exercise 4
Consider an electric field pulse of the form:
$$E_T(t)=\begin{cases}\tfrac{1}{T},&-\tfrac{T}{2}<t<\tfrac{T}{2}\\0,& \text{otherwise}\end{cases}$$
and the corresponding polarization $P_T(t)$, using the general convolution formula:
$$P(t)=\int_{-\infty}^\infty\chi(t-\tau)E(\tau)\ d\tau$$
Determine the value of $P_T(t)$ for all $t\ne0$ in the limit for $T\rightarrow0$.
$$\begin{align}
P(t)
&=\lim_{T\rightarrow0}\int_{-\infty}^\infty\chi(t-\tau)E_T(\tau)\ d\tau\\
&=\int_{-\infty}^\infty\chi(t-\tau)\delta(\tau)\ d\tau\\
&=\chi(t)\\
\Aboxed{P(t)&=\dfrac{ne^2}{m}\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}}
\end{align}$$







