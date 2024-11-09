**Name:** Stanley Goodwin
**Date:** 10/31/2024

---
### Review of Square Roots of Complex Numbers
$$\begin{align}
a+ib&=\sqrt{a^2+b^2}e^{i\tan^{-1}\left(\tfrac{b}{a}\right)}\\
\sqrt{a+ib}&=\sqrt[\leftroot{-2}\uproot{2}4]{a^2+b^2}e^{i\tfrac{1}{2}\tan^{-1}\left(\tfrac{b}{a}\right)}
\end{align}$$
### Back to Insulators
The Fresnel Equations for oblique incidence (for polarization in the plane of incidence.)
$$\begin{align}
\vec{E}_{0T}&=\dfrac{2}{\alpha+\beta}\vec{E}_{0I}\\
\vec{E}_{0R}&=\dfrac{\alpha-\beta}{\alpha+\beta}\vec{E}_{0I}\\
\beta\approx\dfrac{n_2}{n_1}, \ \alpha=\dfrac{\cos\theta_T}{\cos\theta_I}
\end{align}$$
 - If $\theta_I=0$, Snell's Law gives $\theta_R=\theta_T=0$ and $\alpha=1$, recovering the normally-incident case.
 - $\vec{E}_{0T}$ is always in-phase with $\vec{E}_{0I}$.
 - $\vec{E}_{0R}$ may be out of phase $(\alpha<\beta)$. The phase shift depends not just on the indices of refraction, but also on the angles.
 - For normal incidence, we only got 0 reflection for $\beta=1$ $(n_2=n_1)$. This time, we also get 0 reflection for $\alpha=\beta$, and the angle that makes it happen is called *Brewster's Angle*.

### Relationship to other things
$$\begin{align}
I_I&=\langle\vec{S}_I\rangle\cos(\theta_I)\\
I_R&=\langle\vec{S}_R\rangle\cos(\theta_R)\\
I_T&=\langle\vec{S}_T\rangle\cos(\theta_T)\\
R&\equiv\dfrac{I_R}{I_I}=\dfrac{E^2_{0R}}{E^2_{0I}}=\dfrac{(\alpha-\beta)^2}{(\alpha+\beta)^2}\\
T&\equiv\dfrac{I_T}{I_I}=\dfrac{n_2}{n_1}\dfrac{E^2_{0R}}{E^2_{0I}}\dfrac{\cos\theta_T}{\cos\theta_I}=\dfrac{4\alpha\beta}{(\alpha+\beta)^2}\\
\end{align}$$

If $n_2>n_1$, there exists a critical angle for which the transmitted angle is $90$ degrees.
This is called Total Internal Reflection. If the incident angle is greater than this critical angle, there will be 0 transmission.

For the transmitted wave, we have a part propagating $\parallel$ to the boundary, but also a part does propagate into the 2nd region. Since the component of the wavevector transmitted is imaginary, the part that is transmitted is 2 exponential decays instead of 2 oscillations. This "evanescent wave" has a nonzero Electric Field, but transmits 0 power.
