**Name:** Stanley Goodwin
**Date:** 11/14/2024

---

### Quantum Example
Given a Hamiltonian ($\hat{H}_0$) at thermal equilibrium (temperature $T$):
$$\hat\rho\propto e^{-\tfrac{1}{k_bT}\hat{H}}$$
Out of equilibrium, $\hat{H}(t)=\hat{H}_0+a(t)\hat{A}$ we can write:
$$i\hbar\dfrac{\partial}{\partial t}\hat\rho(t)=\left[\hat{H}(t),\hat\rho(t)\right]$$
$$b(t)=\mathrm{Tr}\left(\hat\rho(t)\hat{B}\right)=\langle\hat{B}\rangle$$
When looking at the linear response, then (assuming $\chi=0$ for negative $t$'s):
$$\begin{align}
b(t)&=\int_0^\infty\chi(t-\tau)a(t)\ dt\\
\end{align}$$

### Classical Model of Dielectric
We have a volume of dielectric, with an applied electric field in the $\hat{x}$ direction.
$$\vec{P}(t)=-n|e|\cdot x(t)\hat{x}$$
Where $x(t)$ is the deviation of the volumes from their state with no electric field.
Assuming a very crude model of electrons, then we can say:
$$\begin{align}
\left[m\dfrac{d^2}{dt^2}+\beta\dfrac{d}{dt}+k\right]x(t)\hat{x}=-|e|\cdot \vec{E}(t)\\
\Aboxed{\left[\dfrac{d^2}{dt^2}+\gamma\dfrac{d}{dt}+\Omega_0^2\right]\vec{P}(t)=-\dfrac{ne^2}{m}\vec{E}(t)}
\end{align}$$
Where $\gamma=\beta/m$ and $\Omega_0^2=k/m$, also substituting in polarization density.
We can then take the Fourier transform of the differential equation:
$$\begin{align}
\left[(-i\omega)^2+\gamma(-i\omega)+\Omega_0^2\right]\tilde{P}(\omega)=-\dfrac{ne^2}{m}\tilde{E}(\omega)\\
\tilde{P}(\omega)=\left(\dfrac{ne^2}{m}\dfrac{1}{\omega^2+i\gamma\omega-\Omega_0^2}\right)\tilde{E}(\omega)\\
\tilde{\chi}(\omega)=\dfrac{ne^2}{m}\dfrac{1}{\omega^2+i\gamma\omega-\Omega_0^2}\\
\end{align}$$
### Lanata's Example
Start with a definition:
$$\begin{align}
\chi(\omega)&=\int_0^\infty\chi(t)e^{i\omega t}\ dt=\int_{-\infty}^\infty \theta(t)\chi(t)e^{i\omega t}\ dt\\
\end{align}$$
**Observation:** If $\chi(t)$ is causal, then the expression if $\chi(\omega)$ is well-defined such that:
$$\forall\omega\ | \ \chi=a+bi, \ \ \ b>0$$
We can then write the integral as:
$$\begin{align}
\chi(\omega)&=\int_{-\infty}^\infty \theta(t)\chi(t)e^{iat}e^{-bt}\ dt\\
\end{align}$$
**Theorem:** $\chi(\omega)$ is holomorphic $\forall\omega\ | \ \omega=a+bi, \ \ \ b>0$.
**Observation:** Since $\chi(\omega)\in\mathbb{R}$, then $\chi^*(\omega)=\chi(-\omega^*)$.
**Observation:** If $\omega=\omega^*$, then $a(\omega)=a(-\omega^*)$ and $b(\omega)=-b(-\omega^*)$.

### Dispersion Relations
A special case of the Titchmarsh theorem.
$$\oint_\Gamma\dfrac{\chi(\nu)}{\nu-\omega}\ d\nu=-i\pi\chi(\omega)+\int_{-\infty}^\omega\dfrac{\chi(\nu)}{\nu-\omega}\ d\nu+\int_{\omega}^\infty\dfrac{\chi(\nu)}{\nu-\omega}\ d\nu$$
Since we have a contour integral on the other side, we can use residue theorem:
$$0=-i\pi\chi(\omega)+\int_{-\infty}^\omega\dfrac{\chi(\nu)}{\nu-\omega}\ d\nu+\int_{\omega}^\infty\dfrac{\chi(\nu)}{\nu-\omega}\ d\nu$$
We can then simplify the integral to be the following:
$$\boxed{\chi(\omega)=\dfrac{1}{i\pi}\int_{-\infty}^\infty\dfrac{\chi(\nu)}{\nu-\omega}\ d\nu}$$
We can then separate it into a real and imaginary component:
$$\begin{align}
\Re[\chi(\omega)]&=+\dfrac{1}{\pi}\int_{-\infty}^\infty\dfrac{\Im[\chi(\nu)]}{\nu-\omega}\ d\nu\\
\Im[\chi(\omega)]&=-\dfrac{1}{\pi}\int_{-\infty}^\infty\dfrac{\Re[\chi(\nu)]}{\nu-\omega}\ d\nu\\
\end{align}$$
The integrals mentioned above are the "principle part integrals".

