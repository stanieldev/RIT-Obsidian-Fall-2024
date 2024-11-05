**Name:** Stanley Goodwin
**Date:** 10/29/2024
**Collaborators:** None

---

In this assignment, we will evaluate the integral:
$$I=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}$$
where $\Omega_0$ and $\gamma$ are both positive. This integral will be used later in the context of the inverse Fourier transform and the polarization response of dielectric systems to an external electric field.

---
## Exercise 1
First, calculate the roots $\omega_\pm$ of the denominator and factor it accordingly:
$$\Omega_0^2-\omega^2-i\gamma\omega=-(\omega-\omega_+)(\omega-\omega_-)$$
Determine the position of these poles on the complex plane, particularly focusing on whether they lie within the upper or lower half-plane, given that we assumed $\gamma\gt 0$.
$$\begin{align}
0&=\omega^2+i\gamma\omega-\Omega_0^2\\
\omega_\pm&=-\left(\dfrac{i\gamma}{2}\right)\pm\sqrt{\left(\dfrac{i\gamma}{2}\right)^2-\dfrac{-\Omega_0^2}{1}}\\
&=-\left(\dfrac{i\gamma}{2}\right)\pm\dfrac{1}{2}\sqrt{4\Omega_0^2-\gamma^2}\\
\Aboxed{\omega_\pm&=-\dfrac{1}{2}\left(i\gamma\pm\sqrt{4\Omega_0^2-\gamma^2}\right)}
\end{align}$$
https://www.desmos.com/calculator/fkkp6d98hz
When $4\Omega_0^2-\gamma^2>0$, changing $\gamma$ looks like it's moving along a circular arc in the bottom half of the complex plane.
When $4\Omega_0^2-\gamma^2=0$, both poles are on the imaginary axis on top of each other, once again in the bottom half of the complex plane.
When $4\Omega_0^2-\gamma^2<0$, the 2 poles are on the negative imaginary axis.

**Note:** The poles are always in the bottom half of the complex plane, with the most extreme case being when one of the poles is at $z=0$.

---
## Exercise 2
Next, evaluate the integral by choosing an appropriate integration contour. Explain clearly what integration contour is chosen depending on the sign of $t$ and why, using Jordon's lemma as discussed in class and in the lecture notes.
$$\begin{align}
I&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}\\
&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{-1}{(\omega-\omega_+)(\omega-\omega_-)}\dfrac{d\omega}{2\pi}\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}\left(\dfrac{1}{\omega-\omega_+}-\dfrac{1}{\omega-\omega_-}\right)\ d\omega\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\left(\int_{-\infty}^\infty\dfrac{e^{-i\omega t}}{\omega-\omega_+}\ d\omega-\int_{-\infty}^\infty\dfrac{e^{-i\omega t}}{\omega-\omega_-}\ d\omega\right)\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\left(\int_{-\infty}^\infty \dfrac{e^{-i(\omega+\omega_+)t}}{\omega}\ d\omega-\int_{-\infty}^\infty \dfrac{e^{-i(\omega+\omega_-)t}}{\omega}\ d\omega\right)\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\left(\int_{-\infty}^\infty e^{-i\omega_+t}\dfrac{e^{-i\omega t}}{\omega}\ d\omega-\int_{-\infty}^\infty e^{-i\omega_-t}\dfrac{e^{-i\omega t}}{\omega}\ d\omega\right)\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\left( e^{-i\omega_+t}-e^{-i\omega_-t}\right)\int_{-\infty}^\infty\dfrac{e^{-i\omega t}}{\omega}\ d\omega\\
&=\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}\dfrac{1}{2\pi}\int_{-\infty}^\infty\dfrac{1}{\omega}\cdot e^{-i\omega t}\ d\omega\\
\Aboxed{I&=\theta(t)\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}}
\end{align}$$
---
## Exercise 3
Plot the function for two cases: $\gamma>2\Omega_0$ and $\gamma<2\Omega_0$.
Make sure that the interval for $t$ includes both a portion where $t<0$ and $t>0$.

Case I: $\gamma>2\Omega_0$:
$$\begin{align}
\omega_\pm&=-\dfrac{1}{2}\left(i\gamma\pm i\sqrt{4\Omega_0^2-\gamma^2}\right)\\
I&=\theta(t)\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}\\
&=\theta(t)e^{-i}\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}\\
\end{align}$$
Case II: $\gamma<2\Omega_0$:
$$\begin{align}
\Aboxed{I&=\theta(t)\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}}
\end{align}$$








$$\begin{align}
I_\Gamma&=\int_a^b e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}+\int_0^\tfrac{\pi}{2} e^{-ibe^{i\phi}t}\dfrac{ibe^{i\phi}}{\Omega_0^2-b^2e^{2i\phi}-i\gamma be^{i\phi}}\dfrac{d\phi}{2\pi}\\
&+\int_b^a e^{\omega t}\dfrac{i}{\Omega_0^2+\omega^2+\gamma\omega}\dfrac{d\omega}{2\pi}+\int_\tfrac{\pi}{2}^0 e^{-iae^{i\phi}t}\dfrac{iae^{i\phi}}{\Omega_0^2-a^2e^{2i\phi}-i\gamma ae^{i\phi}}\dfrac{d\phi}{2\pi}\\
\end{align}$$
