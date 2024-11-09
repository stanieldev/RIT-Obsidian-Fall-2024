**Name:** Stanley Goodwin
**Date:** 11/7/2024

---
### EM Waves in Conductors
EM waves in a conducting medium propagating in the $+\hat{z}$-direction:
$$\begin{align}
\vec{E}&=E_0e^{-k_\text{Im}z}e^{i(k_\text{Re}z-\omega t+\phi)}\hat{x}\\
\vec{B}&=\left(\dfrac{k_\text{Re}+ik_\text{Im}}{\omega}\right)E_0e^{-k_\text{Im}z}e^{i(k_\text{Re}z-\omega t+\phi)}\hat{y}\\
\end{align}$$
In a good conductor:
$$\begin{align}
\vec{E}&=E_0e^{-\sqrt{\tfrac{\mu\sigma\omega}{2}}z}\cos\left(\sqrt{\tfrac{\mu\sigma\omega}{2}}z-\omega t+\phi\right)\hat{x}\\
\vec{B}&=\left(\dfrac{\sqrt{\mu\sigma\omega}}{\omega}e^{i\pi/4}\right)E_0e^{-k_\text{Im}z}e^{i(k_\text{Re}z-\omega t+\phi)}\hat{y}\\
&=\sqrt{\dfrac{\sigma}{\epsilon\omega}}E_0e^{-\sqrt{\tfrac{\mu\sigma\omega}{2}}z}\cos\left(\sqrt{\tfrac{\mu\sigma\omega}{2}}z-\omega t+\phi+\dfrac{\pi}{4}\right)\hat{y}\\
\Aboxed{|B_0|&=\dfrac{|E_0|}{c}\sqrt{\dfrac{\sigma}{\epsilon\omega}}}
\end{align}$$
For a good conductor, $\vec{B}$ lags $\vec{E}$ by $1/8$ of a cycle. The magnitude of $\vec{B}$ is also pretty large compared to the vacuum.

When in a vacuum, both $\vec{E}$ and $\vec{B}$ carry equal shares of energy.
In a good conductor, most  of the energy is carried by the $\vec{B}$ field.

A consequence of the $\vec{B}$ lag makes a large force on the charge carries that points in the direction of propagation, adding momentum to the charge. This is called *radiation pressure*.

### Reflection off Metals
$$\begin{align}
\epsilon_1E_1^\perp-\epsilon_2E_2^\perp&=\sigma_\text{free} &
\vec{E}_1^\parallel&=\vec{E}_2^\parallel\\
\dfrac{B_1^\perp}{\mu_1}-\dfrac{B_2^\perp}{\mu_2}&=\vec{J}_\text{free}=0 &
\vec{B}_1^\perp&=\vec{B}_2^\perp\\
\end{align}$$
To include a $\vec{J}_\text{free}=\sigma\vec{E}$, the $\vec{E}$ field must be a delta function at the interface so that there's no free current density. We can have $\vec{J}_\text{free}$ inside the material, but we cannot have a $\vec{K}_\text{free}$ confined to the surface.

Using the boundary conditions, we find that:
$$\begin{align}
\tilde{E}_{0\text{R}}&=\left(\dfrac{n_1-\tilde{n}_2}{n_1+\tilde{n}_2}\right)\tilde{E}_{0\text{I}}\\
\tilde{n}_2&=c\dfrac{\tilde{k}}{\omega}
\end{align}$$
For a good conductor and $k_\text{R}\gg\dfrac{\omega}{c}=k_1$:
$$\begin{align}
\tilde{E}_{0\text{R}}&=\left(\dfrac{k_1-\tilde{k}_2}{k_1+\tilde{k}_2}\right)\tilde{E}_{0\text{I}}\\
&=\left(\dfrac{k_1-k_\text{Re}-ik_\text{Im}}{k_1+k_\text{Re}+ik_\text{Im}}\right)\tilde{E}_{0\text{I}}\\
\end{align}$$
Since it's a good conductor:
$$\begin{align}
\tilde{E}_{0\text{R}}&\approx-\tilde{E}_{0\text{I}}\\
R&\approx1
\end{align}$$
For a good conductor, essentially it has perfect reflection, showing why metals are shiny. Almost everything is reflected, and the tiny bit that's transmitted rapidly dies (as an exponential). For good conductors, it has a small *skin depth*.

### Maxwell's Equations and Potentials
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho}{\epsilon_0}\\
\vec\nabla\cdot\vec{B}&=0\\
\vec\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}\\
\vec\nabla\times\vec{B}&=\mu_0\vec{J}+\mu_0\epsilon_0\dfrac{\partial\vec{E}}{\partial t}\\
\end{align}$$
We found EM waves from vacuum solutions, but we want to be able to get a general solution in the presence of charges and currents.
$$\begin{align}
\vec\nabla\times\vec\nabla\times\vec{E}&=-\dfrac{\partial}{\partial t}\vec\nabla\times\vec{B}\\
\vec\nabla\left(\vec\nabla\cdot\vec{E}\right)-\vec\nabla^2\vec{E}&=-\dfrac{\partial}{\partial t}\vec\nabla\times\vec{B}\\
\dfrac{1}{\epsilon_0}\vec\nabla\rho-\vec\nabla^2\vec{E}&=-\dfrac{\partial}{\partial t}\left(\mu_0\vec{J}+\mu_0\epsilon_0\dfrac{\partial\vec{E}}{\partial t}\right)\\
\dfrac{1}{\epsilon_0}\vec\nabla\rho-\vec\nabla^2\vec{E}&=-\mu_0\dfrac{\partial\vec{J}}{\partial t}-\mu_0\epsilon_0\dfrac{\partial^2\vec{E}}{\partial t^2}\\
\dfrac{1}{c^2}\dfrac{\partial^2\vec{E}}{\partial t^2}-\vec\nabla^2\vec{E}&=-\left(\mu_0\dfrac{\partial\vec{J}}{\partial t}+\dfrac{1}{\epsilon_0}\vec\nabla\rho\right)\\
\end{align}$$
