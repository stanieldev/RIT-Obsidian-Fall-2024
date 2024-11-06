**Name:** Stanley Goodwin
**Date:** 10/29/2024
**Collaborators:** None

---

In this assignment, we will evaluate the integral:
$$I=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{-1}{(\omega-\omega_+)(\omega-\omega_-)}\dfrac{d\omega}{2\pi}$$
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
\Aboxed{\omega_\pm&=\dfrac{1}{2}i\left(-\gamma\pm\sqrt{\gamma^2-4\Omega_0^2}\right)}
\end{align}$$
https://www.desmos.com/calculator/epwvmwm8v5

When $4\Omega_0^2-\gamma^2>0$, changing $\gamma$ looks like it's moving along a circular arc in the bottom half of the complex plane.
When $4\Omega_0^2-\gamma^2=0$, both poles are on the imaginary axis on top of each other, once again in the bottom half of the complex plane.
When $4\Omega_0^2-\gamma^2<0$, the 2 poles are on the negative imaginary axis.

**Note:** The poles are always in the bottom half of the complex plane, with the most extreme case being when one of the poles is at $z=0$.

---
## Exercise 2
Next, evaluate the integral by choosing an appropriate integration contour. Explain clearly what integration contour is chosen depending on the sign of $t$ and why, using Jordon's lemma as discussed in class and in the lecture notes.
I'm using a half-circle that goes into the negative imaginary axis:
$$\begin{align}
\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}+\lim_{R\rightarrow\infty}\int_\pi^{2\pi} e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}\\
\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}+0\\
\Aboxed{\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}}
\end{align}$$
We can then just use the residue theorem:
$$\begin{align}
\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=2\pi i\left(\text{Res}(\omega=\omega_+)+\text{Res}(\omega=\omega_-)\right)
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
\oint e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}&=2\pi i\left(\text{Res}(\omega=\omega_+)+\text{Res}(\omega=\omega_-)\right)\theta(t)\\
&=2\pi i\left(-\dfrac{1}{\omega_+-\omega_-}\dfrac{e^{-i\omega_+t}}{2\pi}+\dfrac{1}{\omega_+-\omega_-}\dfrac{e^{-i\omega_-t}}{2\pi}\right)\theta(t)\\
&=\dfrac{i}{\omega_+-\omega_-}\left(e^{-i\omega_-t}-e^{-i\omega_+t}\right)\theta(t)\\
&=\theta(t)i\dfrac{e^{-i\omega_-t}-e^{-i\omega_+t}}{\omega_+-\omega_-}\\
\end{align}$$
By inspection, we can see that $\omega_\pm=i\lambda_\pm$, and so:
$$\begin{align}
&=\theta(t)i\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}\\
&=\theta(t)i\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{i\lambda_+-i\lambda_-}\\
\Aboxed{I&=\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}}
\end{align}$$
## Exercise 2 (Alternate)
$$\begin{align}
I(t)&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}\\
&=\int_{-\infty}^\infty e^{-i\omega t}\dfrac{-1}{(\omega-\omega_+)(\omega-\omega_-)}\dfrac{d\omega}{2\pi}\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}\left(\dfrac{1}{\omega-\omega_+}-\dfrac{1}{\omega-\omega_-}\right)\ d\omega\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\left(\int_{-\infty}^\infty\dfrac{e^{-i\omega t}}{\omega-\omega_+}\ d\omega-\int_{-\infty}^\infty\dfrac{e^{-i\omega t}}{\omega-\omega_-}\ d\omega\right)\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\left(\int_{-\infty}^\infty \dfrac{e^{-i(\omega+\omega_+)t}}{\omega}\ d\omega-\int_{-\infty}^\infty \dfrac{e^{-i(\omega+\omega_-)t}}{\omega}\ d\omega\right)\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\left(\int_{-\infty}^\infty e^{-i\omega_+t}\dfrac{e^{-i\omega t}}{\omega}\ d\omega-\int_{-\infty}^\infty e^{-i\omega_-t}\dfrac{e^{-i\omega t}}{\omega}\ d\omega\right)\\
&=\dfrac{1}{\omega_+-\omega_-}\dfrac{1}{2\pi}\left( e^{-i\omega_+t}-e^{-i\omega_-t}\right)\int_{-\infty}^\infty\dfrac{e^{-i\omega t}}{\omega}\ d\omega\\
&=\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}\dfrac{1}{2\pi}\int_{-\infty}^\infty\dfrac{1}{\omega}\cdot e^{-i\omega t}\ d\omega\\
&=\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}\dfrac{2\pi i}{2\pi}\\
\Aboxed{I(t)&=\theta(t)i\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}}
\end{align}$$
By inspection, we can see that $\omega_\pm=i\lambda_\pm$, and so:
$$\begin{align}
I(t)&=\theta(t)i\dfrac{e^{-i\omega_+t}-e^{-i\omega_-t}}{\omega_+-\omega_-}\\
&=\theta(t)i\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{i\lambda_+-i\lambda_-}\\
\Aboxed{I(t)&=\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}}
\end{align}$$
It actually wasn't necessary to use a contour integration, since we can use Partial Fraction Decomposition to find the function. The particularity at of the time is something that can be inferred by observation.

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
