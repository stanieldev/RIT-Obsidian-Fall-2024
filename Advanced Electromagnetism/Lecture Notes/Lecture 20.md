**Name:** Stanley Goodwin
**Date:** 11/5/2024

---

**Evanescent wave:** When we had total internal reflection, there was an EM field that made it into the second region, but this part wasn't a traveling wave, but rather an exponentially-decaying wave with distance. $\vec{S}\ne0$, but $\langle\vec{S}\rangle=0$, so no intensity is transmitted into the second region. Some energy is put into the evanescent wave, but the evanescent wave passes that right back into the reflected wave.

### Conductors
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho}{\epsilon_0} & 
\vec\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}\\
\vec\nabla\cdot\vec{B}&=0 & 
\vec\nabla\times\vec{B}&=\mu_0\sigma\vec{E}+\mu_0\epsilon_0\dfrac{\partial\vec{E}}{\partial t}
\end{align}$$
In a conductor $\rho_\text{free}$ quickly goes to zero, on the order of femtoseconds. For frequencies slower than approximately optical frequencies, the volume charge vanishes before the wave notices.
$$\begin{align}
\dfrac{\partial \rho}{\partial t}&=-\vec\nabla\cdot\vec{J}\\
&=-\sigma\vec\nabla\cdot\vec{E}\\
\Aboxed{\dfrac{\partial \rho}{\partial t}&=-\sigma\dfrac{\rho}{\epsilon_0}}\\
\end{align}$$
Lets take the curl of both sides again:
$$\begin{align}
\vec\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}\\
\vec\nabla\times\left(\vec\nabla\times\vec{E}\right)&=-\dfrac{\partial\left(\vec\nabla\times\vec{B}\right)}{\partial t}\\
\vec\nabla\left(\vec\nabla\cdot\vec{E}\right)-\vec\nabla^2\vec{E}&=-\dfrac{\partial\left(\vec\nabla\times\vec{B}\right)}{\partial t}\\
0-\vec\nabla^2\vec{E}&=-\mu_0\sigma\dfrac{\partial\vec{E}}{\partial t}-\mu_0\epsilon_0\dfrac{\partial^2\vec{E}}{\partial t^2}\\
\Aboxed{\vec\nabla^2\vec{E}&=\mu_0\sigma\dfrac{\partial\vec{E}}{\partial t}+\mu_0\epsilon_0\dfrac{\partial^2\vec{E}}{\partial t^2}}
\end{align}$$
Lets try a similar solution to before:
$$\vec{E}=\tilde{E}_0e^{i\left(\vec{k}\cdot\vec{x}-\omega t\right)}$$
So therefore:
$$\begin{align}
\vec\nabla^2\vec{E}&=\mu_0\sigma\dfrac{\partial\vec{E}}{\partial t}+\mu_0\epsilon_0\dfrac{\partial^2\vec{E}}{\partial t^2}\\
(i\vec{k})^2\vec{E}&=\mu_0\sigma(-i\omega)\vec{E}+\mu_0\epsilon_0(-i\omega)^2\vec{E}\\
-|\vec{k}|^2\vec{E}&=-i\mu_0\sigma\omega\vec{E}-\mu_0\epsilon_0\omega^2\vec{E}\\
|\vec{k}|^2&=\mu_0\epsilon_0\omega^2+i\mu_0\sigma\omega\\
\vec{k}&=\sqrt{\dfrac{\mu_0\epsilon_0\omega^2}{2}}\left(\sqrt{1+\sqrt{1+\left(\dfrac{i\mu_0\sigma\omega}{\mu_0\epsilon_0\omega^2}\right)^2}}+i\sqrt{-1+\sqrt{1+\left(\dfrac{i\mu_0\sigma\omega}{\mu_0\epsilon_0\omega^2}\right)^2}}\right)\\
&=\sqrt{\dfrac{\mu_0\epsilon_0\omega^2}{2}}\left(\sqrt{1+\sqrt{1-\dfrac{\sigma^2}{\epsilon_0^2\omega^2}}}+i\sqrt{-1+\sqrt{1-\dfrac{\sigma^2}{\epsilon_0^2\omega^2}}}\right)\\
\end{align}$$
Let's limit this to a very good conductor, where $\sigma\gg\epsilon\omega$.
$$\begin{align}
|\vec{k}|^2&=\mu_0\epsilon_0\omega^2+i\mu_0\sigma\omega\\
|\vec{k}|^2&\approx0+i\mu_0\sigma\omega\\
\tilde{k}&=\left(\dfrac{1+i}{\sqrt{2}}\right)\sqrt{\mu_0\sigma\omega}\\
&=(1+i)\sqrt{\dfrac{\mu_0\sigma\omega}{2}}\\
\Aboxed{\tilde{k}&=\sqrt{\dfrac{\mu_0\sigma\omega}{2}}+i\sqrt{\dfrac{\mu_0\sigma\omega}{2}}}
\end{align}$$
So we can write (assuming normal incidence for simplicity):
$$\begin{align}
\vec{E}&=\tilde{E}_0e^{i\left(\tilde{k}_z\cdot\vec{z}-\omega t\right)}\\
&=\tilde{E}_0\exp\left(iz\sqrt{\dfrac{\mu_0\sigma\omega}{2}}-z\sqrt{\dfrac{\mu_0\sigma\omega}{2}}-\omega t\right)\\
&=\tilde{E}_0\exp\left(-z\sqrt{\dfrac{\mu_0\sigma\omega}{2}}\right)\exp\left(iz\sqrt{\dfrac{\mu_0\sigma\omega}{2}}-\omega t\right)\\
\Aboxed{\vec{E}&=\tilde{E}_0e^{-z\sqrt{\tfrac{\mu_0\sigma\omega}{2}}}e^{i\left(z\sqrt{\tfrac{\mu_0\sigma\omega}{2}}-\omega t\right)}}
\end{align}$$
As the wave goes into the conductor, it has an exponential decay in field inside, because we have a $\vec{J}_\text{free}$ term. However, $\vec{J}_\text{free}$ is going to burn up power according to ohms law. The wave dies because it is dumping energy into the material.

Like a time constant, lets define $d$ to be when the E-field decays by:
$$\begin{align}
d&=\sqrt{\dfrac{2}{\mu_0\sigma\omega}}
\end{align}$$
This shows that metals at optical frequency are opaque.

### Maxwell's Equations in terms of $\vec{k}$ and $\omega$.
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho_\text{free}}{\epsilon_0} & 
\vec\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}\\
\vec\nabla\cdot\vec{B}&=0 & 
\vec\nabla\times\vec{B}&=\mu_0\sigma\vec{E}+\mu_0\epsilon_0\dfrac{\partial\vec{E}}{\partial t}
\end{align}$$
$$\begin{align}
i\vec{k}\cdot\vec{E}&=0\\
i\vec{k}\times\vec{E}&=i\omega\vec{B}\\
i\vec{k}\cdot\vec{B}&=0\\
i\vec{k}\times\vec{B}&=\mu_0\left(\sigma-i\omega\epsilon_0\right)\vec{E}\\
\end{align}$$
Yay!


