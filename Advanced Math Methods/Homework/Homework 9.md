
**Name:** Stanley Goodwin
**Date:** 11/12/2024
**Collaborators:** Chris

In this assignment, we will explore the Fourier inversion formula by directly calculating Fourier transforms and their inverses, verifying the consistency of the results.

---
## Exercise 1
In Assignment 7, we calculated the inverse Fourier transform of the function:
$$\tilde{G}(\omega)=\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}$$
and obtained the result:
$$G(t)=\int_{-\infty}^\infty e^{-i\omega t}\tilde{G}(\omega)\dfrac{d\omega}{2\pi}=\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}$$
where:
$$\lambda_\pm=\dfrac{1}{2}\left(-\gamma\pm\sqrt{\gamma^2-4\Omega_0^2}\right)$$
Now, verify the consistency with the Fourier inversion theorem by calculating the Fourier transform of $G(t)$ and checking that you recover $\tilde{G}(\omega)$.
$$\begin{align}
\tilde{G}(\omega)&=\int_{-\infty}^\infty e^{i\omega t}G(t)\ dt\\
&=\int_{-\infty}^\infty e^{i\omega t}\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}\ dt\\
&=\dfrac{1}{\lambda_+-\lambda_-}\int_{-\infty}^\infty e^{i\omega t}\theta(t)\left[e^{\lambda_+t}-e^{\lambda_-t}\right]\ dt\\
&=\dfrac{1}{\lambda_+-\lambda_-}\int_{-\infty}^0 e^{i\omega t}\left[e^{\lambda_+t}-e^{\lambda_-t}\right]\ dt\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left(\int_{-\infty}^0 e^{i\omega t}e^{\lambda_+t}\ dt-\int_{-\infty}^0 e^{i\omega t}e^{\lambda_-t}\ dt\right)\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left(\int_{-\infty}^0 e^{(\lambda_++i\omega)t}\ dt-\int_{-\infty}^0 e^{(\lambda_-+i\omega)t}\ dt\right)\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left(\dfrac{e^{(\lambda_++i\omega)t}}{\lambda_++i\omega}-\dfrac{e^{(\lambda_-+i\omega)t}}{\lambda_-+i\omega}\right|_{-\infty}^0\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left(\dfrac{e^{0}}{\lambda_++i\omega}-\dfrac{e^{0}}{\lambda_-+i\omega}\right)\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left(\dfrac{1}{\lambda_++i\omega}-\dfrac{1}{\lambda_-+i\omega}\right)\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left(\dfrac{(\lambda_-+i\omega)-(\lambda_++i\omega)}{(\lambda_++i\omega)(\lambda_-+i\omega)}\right)\\
&=-\dfrac{1}{\lambda_+-\lambda_-}\left(\dfrac{\lambda_+-\lambda_-}{(\lambda_++i\omega)(\lambda_-+i\omega)}\right)\\
&=-\dfrac{1}{(\lambda_++i\omega)(\lambda_-+i\omega)}\\
&=-\dfrac{(-i)^2}{(\omega-i\lambda_+)(\omega-i\lambda_-)}\\
&=\dfrac{1}{(\omega-\omega_+)(\omega-\omega_-)}\\
\Aboxed{\tilde{G}(\omega)&=\dfrac{-1}{\Omega_0^2-\omega^2-i\gamma\omega}}
\end{align}$$
---
## Exercise 2
In a previous example, we calculated the inverse Fourier transform of the function:
$$\tilde{W}(\omega)=\dfrac{\sin(\kappa\omega)}{\kappa\omega},\ \ \ \kappa=T/2$$
And found:
$$W(t)=\dfrac{1}{2\kappa}\chi[-\kappa,\kappa],\ \ \ \kappa=T/2{}$$
In this exercise, check that if we take the Fourier transform of $W(t)$, we get back $\tilde{W}(\omega)$.
$$\begin{align}
\tilde{W}(\omega)&=\int_{-\infty}^\infty e^{i\omega t}W(t)\ dt\\
&=\int_{-\infty}^\infty e^{i\omega t}\dfrac{1}{2\kappa}\chi[-\kappa,\kappa]\ dt\\
&=\dfrac{1}{2\kappa}\int_{-\kappa}^\kappa e^{i\omega t}\ dt\\
&=\dfrac{1}{2i\kappa\omega}\left.e^{i\omega t}\right|_{-\kappa}^\kappa\\
&=\dfrac{2}{2i\kappa\omega}\left(e^{i\omega\kappa}-e^{-i\omega\kappa}\right)\\
&=\dfrac{2i}{2i\kappa\omega}\sin(\kappa\omega)\\
\tilde{W}(\omega)&=\dfrac{\sin(\kappa\omega)}{\kappa\omega}\\
\Aboxed{\tilde{W}(\omega)&=\dfrac{\sin(\kappa\omega)}{\kappa\omega},\ \ \ \kappa=T/2}
\end{align}$$
---
## Exercise 3
Next, consider the function $G(t)=\theta(t)e^{-\alpha t}$, where $\alpha>0$. Perform the following steps:

First, calculate the Fourier Transform of $G(t)$:
$$\begin{align}
\tilde{G}(\omega)
&=\int_{-\infty}^\infty e^{i\omega t}G(t)\ dt\\
&=\int_{-\infty}^\infty e^{i\omega t}\theta(t)e^{-\alpha t}\ dt\\
&=\int_{0}^\infty e^{i\omega t}e^{-\alpha t}\ dt\\
&=\int_{0}^\infty e^{(-\alpha+i\omega)t}\ dt\\
&=\dfrac{1}{-\alpha+i\omega}\left.e^{(-\alpha+i\omega)t}\right|_{0}^\infty\\
&=\dfrac{1}{-\alpha+i\omega}\left(0-1\right)\\
\Aboxed{\tilde{G}(\omega)&=\dfrac{1}{\alpha-i\omega}}
\end{align}$$
Then, apply the inverse Fourier transform to $\tilde{G}(\omega)$, and verify using the residue theorem that it gives back the original function $G(t)$.
$$\begin{align}
G(t)
&=\int_{-\infty}^\infty e^{-i\omega t}\tilde{G}(\omega)\ \dfrac{d\omega}{2\pi}\\
&=\dfrac{1}{2\pi}\int_{-\infty}^\infty\dfrac{e^{-i\omega t}}{\alpha-i\omega}\ d\omega\\
&=-\dfrac{1}{2\pi}\oint_\mathbb{C}\dfrac{e^{-i\omega t}}{\alpha-i\omega}\ d\omega\\
&=\dfrac{1}{2\pi i}\oint_\mathbb{C}\dfrac{e^{-i\omega t}}{\omega+i\alpha}\ d\omega\\
&=\dfrac{2\pi i}{2\pi i}\theta(t)\lim_{\omega\rightarrow-i\alpha}e^{-i\omega t}\\
&=\theta(t)e^{-i(-i\alpha)t}\\
\Aboxed{G(t)&=\theta(t)e^{-\alpha t}}
\end{align}$$
