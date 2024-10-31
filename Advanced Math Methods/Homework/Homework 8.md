**Name:** Stanley Goodwin
**Date:** 10/29/2024
**Collaborators:** None

---

In this assignment, we will evaluate the integral:
$$I=\int e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}$$
where $\Omega_0$ and $\gamma$ are both positive. This integral will be used later in the context of the inverse Fourier transform and the polarization response of dielectric systems to an external electric field.
## Exercise 1
First, calculate the roots $\omega_\pm$ of the denominator and factor it accordingly:
$$\Omega_0^2-\omega^2-i\gamma\omega=-(\omega-\omega_+)(\omega-\omega_-)$$
Determine the position of these poles on the complex plane, particularly focusing on whether they lie within the upper or lower half-plane, given that we assumed $\gamma\gt 0$.
## Exercise 2
Next, evaluate the integral by choosing an appropriate integration contour. Explain clearly what integration contour is chosen depending on the sign of $t$ and why, using Jordon's lemma as discussed in class and in the lecture notes.




**Note:** If everything is done correctly, you should find that:
$$\begin{align}
\int e^{-i\omega t}\dfrac{1}{\Omega_0^2-\omega^2-i\gamma\omega}\dfrac{d\omega}{2\pi}=\theta(t)\dfrac{e^{\lambda_+t}-e^{\lambda_-t}}{\lambda_+-\lambda_-}
\end{align}$$
$$\begin{align}
\lambda_\pm=\dfrac{1}{2}\left(-\gamma\pm\sqrt{\gamma^2-4\Omega_0^2}\right)
\end{align}$$


## Exercise 3
Plot the function for two cases: $\gamma>2\Omega_0$ and $\gamma<2\Omega_0$.
Make sure that the interval for $t$ includes both a portion where $t<0$ and $t>0$.

