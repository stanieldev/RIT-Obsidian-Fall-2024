**Name:** Stanley Goodwin
**Date:** XX/XX/2024
**Collaborators:** None

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
&=\dfrac{1}{\lambda_+-\lambda_-}\int_{-\infty}^\infty e^{i\omega t}\theta(t)\left(e^{\lambda_+t}-e^{\lambda_-t}\right)\ dt\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left[\int_{-\infty}^\infty e^{i\omega t}\theta(t)e^{\lambda_+t}\ dt-\int_{-\infty}^\infty e^{i\omega t}\theta(t)e^{\lambda_-t}\ dt\right]\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left[\int_{-\infty}^0 e^{(\lambda_++i\omega )t}\ dt-\int_{-\infty}^0 e^{(\lambda_-+i\omega)t}\ dt\right]\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left[\dfrac{e^{(\lambda_++i\omega)t}}{\lambda_++i\omega}-\dfrac{e^{(\lambda_-+i\omega)t}}{\lambda_-+i\omega}\right]_{-\infty}^0\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left[\dfrac{e^{0}}{\lambda_++i\omega}-\dfrac{e^{0}}{\lambda_-+i\omega}\right]\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left[\dfrac{1}{\lambda_++i\omega}-\dfrac{1}{\lambda_-+i\omega}\right]\\
&=\dfrac{1}{\lambda_+-\lambda_-}\left[\dfrac{\lambda_--\lambda_+}{(\lambda_++i\omega)(\lambda_-+i\omega)}\right]\\
&=\dfrac{-1}{(\lambda_++i\omega)(\lambda_-+i\omega)}\\
\Aboxed{\tilde{G}(\omega)&=\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}}
\end{align}$$
---
## Exercise 2

---
## Exercise 3
