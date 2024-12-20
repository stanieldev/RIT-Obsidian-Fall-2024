**Name:** Stanley Goodwin
**Date:** 10/29/2024
**Collaborators:** None

---

In this assignment, we will evaluate the integral:
$$\begin{align}
I&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}
\end{align}$$
where $\Omega_0$ and $\gamma$ are both positive. This integral will be used later in the context of the inverse Fourier transform and the polarization response of dielectric systems to an external electric field.

---
## Exercise 1
First, calculate the roots $\omega_\pm$ of the denominator and factor it accordingly:
$$\Omega_0^2-\omega^2-i\gamma\omega=-(\omega-\omega_+)(\omega-\omega_-)$$
Determine the position of these poles on the complex plane, particularly focusing on whether they lie within the upper or lower half-plane, given that we assumed $\gamma\gt 0$.
$$\begin{align}
0&=\omega^2+i\gamma\omega-\Omega_0^2\\
\omega_\pm&=\dfrac{-(i\gamma)\pm\sqrt{(i\gamma)^2-4(1)(-\Omega_0^2)}}{2(1)}\\
&=\dfrac{-i\gamma\pm\sqrt{-\gamma^2+4\Omega_0^2}}{2}\\
\Aboxed{\omega_\pm&=\dfrac{-i\gamma\pm i\sqrt{\gamma^2-4\Omega_0^2}}{2}}\\
-i\omega_\pm&=-i\dfrac{-i\gamma\pm i\sqrt{\gamma^2-4\Omega_0^2}}{2}\\
&=\dfrac{-\gamma\pm \sqrt{\gamma^2-4\Omega_0^2}}{2}\\
\Aboxed{\lambda_\pm&=\dfrac{1}{2}\left(-\gamma\pm \sqrt{\gamma^2-4\Omega_0^2}\right)}\\
\Aboxed{\lambda_\pm&=-i\omega_\pm}\\
\end{align}$$
https://www.desmos.com/calculator/epwvmwm8v5

When $4\Omega_0^2-\gamma^2>0$, changing $\gamma$ looks like it's moving along a circular arc in the bottom half of the complex plane.
When $4\Omega_0^2-\gamma^2=0$, both poles are on the imaginary axis on top of each other, once again in the bottom half of the complex plane.
When $4\Omega_0^2-\gamma^2<0$, the 2 poles are on the negative imaginary axis.

**Note:** The poles are always in the bottom half of the complex plane, with the most extreme case being when one of the poles is at $z=0$.

---
## Exercise 2 (Using $\lambda$)
Next, evaluate the integral by choosing an appropriate integration contour. Explain clearly what integration contour is chosen depending on the sign of $t$ and why, using Jordon's lemma as discussed in class and in the lecture notes.
$$\begin{align}
I&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}\\
&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{-1}{(\omega-\omega_+)(\omega-\omega_-)}\dfrac{d\omega}{2\pi}\\
&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{-i^2}{(i\omega-i\omega_+)(i\omega-i\omega_-)}\dfrac{d\omega}{2\pi}\\
&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{(i\omega+\lambda_+)(i\omega+\lambda_-)}\dfrac{d\omega}{2\pi}\\
&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{(-i)^2}{(\omega-i\lambda_+)(\omega-i\lambda_-)}\dfrac{d\omega}{2\pi}\\
&=-\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{(\omega-i\lambda_+)(\omega-i\lambda_-)}d\omega\\
\end{align}$$
I'm using a half-circle that loops around the negative half-plane:
$$\begin{align}
\oint e^{-i\omega t}\dfrac{\theta(t)}{(\omega-i\lambda_+)(\omega-i\lambda_-)}d\omega&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{(\omega-i\lambda_+)(\omega-i\lambda_-)}d\omega\\
&
+\lim_{R\rightarrow\infty}\int_{0}^{-\pi} e^{-i\omega(R)t}\dfrac{1}{(\omega(R)-i\lambda_+)(\omega(R)-i\lambda_-)}d\phi\\
&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{(\omega-i\lambda_+)(\omega-i\lambda_-)}d\omega+0\\
\Aboxed{\oint e^{-i\omega t}\dfrac{\theta(t)}{(\omega-i\lambda_+)(\omega-i\lambda_-)}d\omega&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{(\omega-i\lambda_+)(\omega-i\lambda_-)}d\omega}
\end{align}$$
Using the residue theorem on the contour integral, we find the two residue components:
$$\begin{align}
-\dfrac{1}{2\pi}\oint e^{-i\omega t}\dfrac{\theta(t)}{(\omega-i\lambda_+)(\omega-i\lambda_-)}d\omega
&=-\dfrac{2\pi}{2\pi i}\theta(t)\left(\text{Res}(\omega=i\lambda_+)+\text{Res}(\omega=i\lambda_-)\right)\\
\Aboxed{I&=i\theta(t)\left(\text{Res}(\omega=i\lambda_+)+\text{Res}(\omega=i\lambda_-)\right)}
\end{align}$$
We can then find the residues with the following:
$$\begin{align}
\text{Res}(\omega=i\lambda_+)
&=\lim_{\omega\rightarrow i\lambda_+}(\omega-i\lambda_+)\left(e^{-i\omega t}\dfrac{1}{(\omega-i\lambda_+)(\omega-i\lambda_-)}\right)\\
&=\lim_{\omega\rightarrow i\lambda_+}\dfrac{(\omega-i\lambda_+)}{(\omega-i\lambda_+)}\left(\dfrac{e^{-i\omega t}}{\omega-i\lambda_-}\right)\\
&=\lim_{\omega\rightarrow i\lambda_+}\dfrac{e^{-i\omega t}}{\omega-i\lambda_-}\\
&=\dfrac{e^{-i(i\lambda_+) t}}{i\lambda_+-i\lambda_-}\\
\Aboxed{\text{Res}(\omega=i\lambda_+)&=\dfrac{1}{i}\dfrac{e^{\lambda_+t}}{\lambda_+-\lambda_-}}\\\\
\text{Res}(\omega=i\lambda_-)
&=\lim_{\omega\rightarrow i\lambda_-}(\omega-i\lambda_-)\left(e^{-i\omega t}\dfrac{1}{(\omega-i\lambda_+)(\omega-i\lambda_-)}\right)\\
&=\lim_{\omega\rightarrow i\lambda_-}\dfrac{(\omega-i\lambda_-)}{(\omega-i\lambda_-)}\left(\dfrac{e^{-i\omega t}}{\omega-i\lambda_+}\right)\\
&=\lim_{\omega\rightarrow i\lambda_-}\dfrac{e^{-i\omega t}}{\omega-i\lambda_+}\\
&=\dfrac{e^{-i(i\lambda_-) t}}{i\lambda_--i\lambda_+}\\
\Aboxed{\text{Res}(\omega=i\lambda_-)&=-\dfrac{1}{i}\dfrac{e^{\lambda_-t}}{\lambda_+-\lambda_-}}
\end{align}$$
Combining them, we get the final expression:
$$\begin{align}
I&=i\theta(t)\left(\text{Res}(\omega=i\lambda_+)+\text{Res}(\omega=i\lambda_-)\right)\\
&=\dfrac{i}{i}\theta(t)\left(\dfrac{e^{\lambda_+t}}{\lambda_+-\lambda_-}-\dfrac{e^{\lambda_-t}}{\lambda_+-\lambda_-}\right)\\
&=\theta(t)\left(\dfrac{e^{\lambda_+t}}{\lambda_+-\lambda_-}-\dfrac{e^{\lambda_-t}}{\lambda_+-\lambda_-}\right)\\
\Aboxed{I&=\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}}
\end{align}$$
---
## Exercise 3
Plot the function for two cases: $\gamma>2\Omega_0$ and $\gamma<2\Omega_0$.
Make sure that the interval for $t$ includes both a portion where $t<0$ and $t>0$.
$$\begin{align}
\Aboxed{I(t)&=\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}}
\Aboxed{\lambda_\pm&=\dfrac{1}{2}\left(-\gamma\pm\sqrt{\gamma^2-4\Omega_0^2}\right)}
\end{align}$$
Case I: $\gamma>2\Omega_0$:
$$\begin{align}
\Aboxed{\lambda_\pm&=\dfrac{1}{2}\left(-\gamma\pm\sqrt{\gamma^2-4\Omega_0^2}\right)}
\end{align}$$
$$\begin{align}
I(t)&=\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}\\
&=\theta(t)e^{-\tfrac{1}{2}\gamma t}\dfrac{e^{\sqrt{\gamma^2-4\Omega_0^2}t}-e^{-\sqrt{\gamma^2-4\Omega_0^2}t}}{\sqrt{\gamma^2-4\Omega_0^2}}\\
\Aboxed{I(t)&=\dfrac{2\cdot\theta(t)}{\sqrt{\gamma^2-4\Omega_0^2}}e^{-\tfrac{1}{2}\gamma t}\sinh\left(\sqrt{\gamma^2-4\Omega_0^2}t\right)}
\end{align}$$
![[HW8_Q3_1.png]]
https://www.desmos.com/calculator/drgx6xupvz


Case II: $\gamma<2\Omega_0$:
$$\begin{align}
\Aboxed{\lambda_\pm&=\dfrac{1}{2}\left(-\gamma\pm i\sqrt{4\Omega_0^2-\gamma^2}\right)}
\end{align}$$
$$\begin{align}
I(t)&=\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}\\
&=\theta(t)e^{-\tfrac{1}{2}\gamma t}\dfrac{e^{i\sqrt{4\Omega_0^2-\gamma^2}t}-e^{-i\sqrt{4\Omega_0^2-\gamma^2}t}}{i\sqrt{4\Omega_0^2-\gamma^2}}\\
&=\dfrac{2i\cdot\theta(t)e^{-\tfrac{1}{2}\gamma t}}{i\sqrt{4\Omega_0^2-\gamma^2}}\sin\left(\sqrt{4\Omega_0^2-\gamma^2}t\right)\\
\Aboxed{I(t)&=\dfrac{2\cdot\theta(t)}{\sqrt{4\Omega_0^2-\gamma^2}}e^{-\tfrac{1}{2}\gamma t}\sin\left(\sqrt{4\Omega_0^2-\gamma^2}t\right)}
\end{align}$$
![[HW8_Q3_2.png]]
https://www.desmos.com/calculator/m0ztcmalkk
