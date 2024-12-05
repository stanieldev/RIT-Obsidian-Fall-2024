**Name:** Stanley Goodwin
**Date:** 12/04/2024
**Collaborators:** Chris

In this Assignment, we consider the phenomenological model for the Green's function of the electronic temperature in a material after a laser pulse. The electronic temperature $T(t)$ is related to the power input $P(t)$ from the laser by the relation:
$$T(t)=\int G(t-\tau)P(\tau)\ d\tau$$
The Green's function in the frequency domain is given by:
$$\tilde{G}(\omega)=\dfrac{1}{C_e+C_p}\left[\dfrac{1}{\eta-i\omega}+\dfrac{C_p}{C_e}\dfrac{1}{\kappa-i\omega}\right], \ \ \ \kappa=\eta+g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)$$
---
## Exercise 1
Determine the conditions on the parameters $\eta$, $C_e$, $C_p$, and $g$ under which $\tilde{G}(\omega)$ corresponds to a causal Green's function. Explain this from perspective of the analytic properties of $\tilde{G}(\omega)$ in the complex plane, focusing on the location of its poles and their implications for causality.

In order to maintain causality, there must not be any singularities in the upper-half plane $\Im(z)<0$.
$$\begin{align}
\tilde{G}(\omega)&=\dfrac{i}{C_e+C_p}\left[\dfrac{1}{\omega+i\eta}+\dfrac{C_p}{C_e}\dfrac{1}{\omega+i\kappa}\right], \ \ \ \kappa=\eta+g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)\\
\end{align}$$
We see there are singularity holes at:
$$\begin{align}
\Im\left(\dfrac{1}{\omega+i\eta}\right)&<0\\
\Im\left(\dfrac{\omega-i\eta}{\omega^2+\eta^2}\right)&<0\\
\Im\left(\omega-i\eta\right)&<0\\
\Aboxed{\eta&>0}\\
\\
\Im\left(\dfrac{1}{\omega+i\kappa}\right)&<0\\
\Im\left(\dfrac{\omega-i\kappa}{\omega^2+\kappa^2}\right)&<0\\
\Im\left(\omega-i\kappa\right)&<0\\
\kappa&>0\\
\eta+g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)&>0\\
\Aboxed{\eta>-g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)}
\end{align}$$
Overall, then:
$$\begin{align}
\text{If }&g>0:&\eta&>0\\
\text{If }&g<0:&\eta&>-g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)\\ 
\end{align}$$
---
## Exercise 2
Calculate explicitly the inverse Fourier transform $\tilde{G}(\omega)$ to obtain $G(t)$, assuming the parameters satisfy the conditions for causality determined in Exercise 1. Provide a detailed explanation of the integration contour and how the causality conditions ensure the correct result.
$$\begin{align}
G(t)&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}\tilde{G}(\omega)\ d\omega\\
&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}\dfrac{1}{C_e+C_p}\left[\dfrac{1}{\eta-i\omega}+\dfrac{C_p}{C_e}\dfrac{1}{\eta+g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)-i\omega}\right]\ d\omega\\
&=\dfrac{1}{2\pi}\dfrac{1}{C_e+C_p}\int_{-\infty}^\infty e^{-i\omega t}\left[\dfrac{1}{\eta-i\omega}+\dfrac{C_p}{C_e}\dfrac{1}{\kappa-i\omega}\right]\ d\omega\\
&=\dfrac{1}{2\pi}\dfrac{1}{C_e+C_p}\int_{-\infty}^\infty \dfrac{e^{-i\omega t}}{\eta-i\omega}\ d\omega+\dfrac{1}{2\pi}\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\int_{-\infty}^\infty\dfrac{e^{-i\omega t}}{\kappa-i\omega}\ d\omega\\
&=\dfrac{1}{2\pi}\dfrac{1}{C_e+C_p}\oint_\mathbb{H^-}\dfrac{e^{-i\omega t}}{\eta-i\omega}\ d\omega+\dfrac{1}{2\pi}\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\oint_\mathbb{H^-}\dfrac{e^{-i\omega t}}{\kappa-i\omega}\ d\omega\\
&=\dfrac{2\pi i}{2\pi}\dfrac{1}{C_e+C_p}\lim_{\omega\rightarrow-i\eta}\dfrac{\omega+i\eta}{\eta-i\omega}e^{-i\omega t}+\dfrac{2\pi i}{2\pi}\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\lim_{\omega\rightarrow-i\kappa}\dfrac{\omega+i\eta}{\eta-i\omega}e^{-i\omega t}\\
&=\dfrac{2\pi i}{2\pi i}\dfrac{1}{C_e+C_p}\lim_{\omega\rightarrow-i\eta}e^{-i\omega t}+\dfrac{2\pi i}{2\pi i}\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\lim_{\omega\rightarrow-i\kappa}e^{-i\omega t}\\
&=\dfrac{1}{C_e+C_p}e^{-\eta t}+\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}e^{-\kappa t}\\
\Aboxed{G(t)&=\dfrac{\theta(t)e^{-\eta t}}{C_e+C_p}\left(1+\dfrac{C_p}{C_e}e^{-g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)t}\right)}
\end{align}$$
---
## Exercise 3
Take the Green's function $G(t)$ obtained in Exercise 2 and Fourier transform it explicitly.
Verify the inversion formula:
$$\begin{align}
\tilde{G}(\omega)&=\int_{-\infty}^\infty e^{i\omega t}G(t)\ dt\\
&=\int_{-\infty}^\infty e^{i\omega t}\dfrac{\theta(t)}{C_e+C_p}\left(e^{-\eta t}+\dfrac{C_p}{C_e}e^{-\kappa t}\right)\ dt\\
&=\dfrac{1}{C_e+C_p}\int_0^\infty e^{i\omega t}\left(e^{-\eta t}+\dfrac{C_p}{C_e}e^{-\kappa t}\right)\ dt\\
&=\dfrac{1}{C_e+C_p}\int_0^\infty e^{i\omega t}e^{-\eta t}\ dt+\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\int_0^\infty e^{i\omega t}e^{-\kappa t}\ dt\\
&=\dfrac{1}{C_e+C_p}\int_0^\infty e^{(-\eta+i\omega)t}\ dt+\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\int_0^\infty e^{(-\kappa+i\omega)t}\ dt\\
&=\dfrac{1}{C_e+C_p}\dfrac{e^{-\infty}-1}{-\eta+i\omega}+\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\dfrac{e^{-\infty}-1}{-\kappa+i\omega}\\
&=\dfrac{1}{C_e+C_p}\dfrac{1}{\eta-i\omega}+\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\dfrac{1}{\kappa-i\omega}\\
&=\dfrac{1}{C_e+C_p}\left(\dfrac{1}{\eta-i\omega}+\dfrac{C_p}{C_e}\dfrac{1}{\kappa-i\omega}\right)\\
\Aboxed{\tilde{G}(\omega)&=\dfrac{1}{C_e+C_p}\left[\dfrac{1}{\eta-i\omega}+\dfrac{C_p}{C_e}\dfrac{1}{\kappa-i\omega}\right], \ \ \ \kappa=\eta+g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)}
\end{align}$$
---
## Exercise 4
Three candidate pairs of plots for the real and imaginary parts of $\tilde{G}(\omega)$ are shown in Figure 1, but only one of these pairs is valid. Based on the principle of causality (in particular, the dispersion relations), determine which pair of plots corresponds to an actual causal Green's function.
Explain your answer.
$$\tilde{G}(\omega)=\dfrac{1}{C_e+C_p}\left[\dfrac{\eta}{\eta^2+\omega^2}+\dfrac{C_p}{C_e}\dfrac{\kappa}{\kappa^2+\omega^2}\right]+i\dfrac{1}{C_e+C_p}\left[\dfrac{\omega}{\eta^2+\omega^2}+\dfrac{C_p}{C_e}\dfrac{\omega}{\kappa^2+\omega^2}\right]$$
The only pair of plots that match the above expression are the middle 2 plots (2nd from the top).
I know this since the distribution of the real part is like $\dfrac{1}{a^2+x^2}$ and the imaginary part $\dfrac{x}{a^2+x^2}$.

---
## Exercise 5
Calculate the explicit expressions for the real and imaginary parts of $\tilde{G}(\omega)$ in terms of the model parameters. Use these expressions to verify the relationship by the dispersion relations under the assumption of causality.
$$\tilde{G}(\omega)=\dfrac{1}{C_e+C_p}\left[\dfrac{1}{\eta-i\omega}+\dfrac{C_p}{C_e}\dfrac{1}{\kappa-i\omega}\right], \ \ \ \kappa=\eta+g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)$$
We can rationalize the denominators to get:
$$\tilde{G}(\omega)=\dfrac{1}{C_e+C_p}\left[\dfrac{\eta+i\omega}{\eta^2+\omega^2}+\dfrac{C_p}{C_e}\dfrac{\kappa+i\omega}{\kappa^2+\omega^2}\right], \ \ \ \kappa=\eta+g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)$$
Separating, we find that:
$$\tilde{G}(\omega)=\dfrac{1}{C_e+C_p}\left[\dfrac{\eta}{\eta^2+\omega^2}+\dfrac{C_p}{C_e}\dfrac{\kappa}{\kappa^2+\omega^2}\right]+i\dfrac{1}{C_e+C_p}\left[\dfrac{\omega}{\eta^2+\omega^2}+\dfrac{C_p}{C_e}\dfrac{\omega}{\kappa^2+\omega^2}\right]$$
### Dispersion Relations
$$\begin{align}
\Re(\chi(\omega))
&=\dfrac{1}{\pi}\displaystyle\int_{-\infty}^\infty\dfrac{\Im(\chi(\nu))}{\nu-\omega}\ d\nu\\
&=\dfrac{1}{C_e+C_p}\dfrac{1}{\pi}\int_{-\infty}^\infty\dfrac{\nu}{\eta^2+\nu^2}\dfrac{1}{\nu-\omega}\ d\nu+\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\dfrac{1}{\pi}\int_{-\infty}^\infty\dfrac{\nu}{\kappa^2+\nu^2}\dfrac{1}{\nu-\omega}\ d\nu\\
&=\dfrac{1}{C_e+C_p}\dfrac{1}{\pi}\dfrac{\eta\pi}{\eta^2+\nu^2}+\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\dfrac{1}{\pi}\dfrac{\kappa\pi}{\eta^2+\nu^2}\\
\Aboxed{\Re(\chi(\omega))&=\dfrac{1}{C_e+C_p}\left[\dfrac{\eta}{\eta^2+\nu^2}+\dfrac{C_p}{C_e}\dfrac{\kappa}{\eta^2+\nu^2}\right], \ \ \ \kappa=\eta+g\left(\tfrac{1}{C_e}+\tfrac{1}{C_p}\right)}
\end{align}$$
$$\begin{align}
\Im(\chi(\omega))
&=-\dfrac{1}{\pi}\int_{-\infty}^\infty\dfrac{\Re(\chi(\nu))}{\nu-\omega}\ d\nu\\
&=-\dfrac{1}{C_e+C_p}\dfrac{1}{\pi}\int_{-\infty}^\infty\dfrac{\eta}{\eta^2+\omega^2}\dfrac{1}{\nu-\omega}\ d\nu-\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\dfrac{1}{\pi}\int_{-\infty}^\infty\dfrac{\kappa}{\kappa^2+\omega^2}\dfrac{1}{\nu-\omega}\ d\nu\\
&=-\dfrac{1}{C_e+C_p}\dfrac{1}{\pi}\left(-\dfrac{\pi\omega}{\eta^2+\omega^2}\right)-\dfrac{1}{C_e+C_p}\dfrac{C_p}{C_e}\dfrac{1}{\pi}\left(-\dfrac{\pi\omega}{\kappa^2+\omega^2}\right)\\
\Aboxed{\Im(\chi(\omega))&=\dfrac{1}{C_e+C_p}\left(\dfrac{\omega}{\eta^2+\omega^2}+\dfrac{C_p}{C_e}\dfrac{\omega}{\kappa^2+\omega^2}\right)}
\end{align}$$














