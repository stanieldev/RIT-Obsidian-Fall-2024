### Electrostatics & Magnetostatics
$$\begin{align}
\vec{E}_\mathrm{net}&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho}{r^2}\hat{r}\ d\tau&\text{(Coulomb's Law)}\\
V_\mathrm{net}&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho}{r}\ d\tau&\text{(Scalar Potential)}\\
\vec{B}_\mathrm{net}&=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{J}\times\hat{r}}{r^2}\ d\tau&\text{(Biot-Savart Law)}\\
\vec{A}_\mathrm{net}&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}}{r}\ d\tau&\text{(Vector Potential)}
\end{align}$$
### Maxwell's Equations $\left(\vec{E}\ \&\ \vec{B}\right)$
$$\begin{align}
\nabla\cdot\vec{E}&=\dfrac{\rho}{\epsilon_0}&
\oint\vec{E}\cdot d\vec{A}&=\dfrac{q_\text{enc}}{\epsilon_0}&
\text{(Gauss' Law)}\\
\nabla\cdot\vec{B}&=0&
\oint\vec{B}\cdot d\vec{A}&=0&
\text{(No Monopoles)}\\
\nabla\cdot\vec{J}&=-\dfrac{\partial\rho}{\partial t}&
\oint\vec{J}\cdot d\vec{A}&=-\dfrac{\partial q_\text{enc}}{\partial t}&
\text{(Continuity)}\\
\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}&
\oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}&
\text{(Faraday's Law)}\\
\nabla\times\vec{B}&=\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial\vec{E}}{\partial t}&
\oint\vec{B}\cdot d\vec{l}&=\mu_0I+\epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}&
\text{(Ampere's Law)}
\end{align}$$
$$\begin{align}
\vec{F}&=q_e\left(\vec{E}+\vec{v}\times\vec{B}\right)&
\text{(Lorentz Force)}\\
\vec\nabla^2\vec{E}&=\dfrac{1}{c^2}\dfrac{\partial^2\vec{E}}{\partial t^2}&
\text{(Electric Wave Equation)}\\
\vec\nabla^2\vec{B}&=\dfrac{1}{c^2}\dfrac{\partial^2\vec{B}}{\partial t^2}&
\text{(Magnetic Wave Equation)}
\end{align}$$
### Boundary Conditions
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho}{\epsilon_0}&\implies&& \left.\left(\vec{E}_\text{above}^\perp-\vec{E}_\text{below}^\perp\right)\right|_\text{surface}&=\dfrac{\sigma}{\epsilon_0}\\
\vec\nabla\times\vec{E}&=0&\implies&&\left.\left(\vec{E}_\text{above}^\parallel-\vec{E}_\text{below}^\parallel\right)\right|_\text{surface} &=0\\
\vec\nabla\cdot\vec{B}&=0&\implies&&\left.\left(\vec{B}_\text{above}^\perp-\vec{B}_\text{below}^\perp\right)\right|_\text{surface}&=0\\
\vec\nabla\times\vec{B}&=\mu_0\vec{J}&\implies&& \left.\left(\vec{B}_\text{above}^\parallel-\vec{B}_\text{below}^\parallel\right)\right|_\text{surface}&=\mu_0\left(\vec{K}\times\hat{n}\right)\\
\end{align}$$
### Alternate Fields
$$\begin{align}
\vec{D}&=\epsilon_0\vec{E}+\vec{P}&\implies&&\rho_\text{free}&=\rho-\rho_\text{bound}\\
\vec{H}&=\dfrac{1}{\mu_0}\vec{B}-\vec{M}&\implies&&\vec{J}_\text{free}&=\vec{J}-\vec{J}_\text{bound}-\dfrac{\partial\vec{D}}{\partial t}\\
\end{align}$$
$$\begin{align}
\left.\left(\vec{D}_\text{above}^\perp-\vec{D}_\text{below}^\perp\right)\right|_\text{surface}&=\sigma_\text{free}\\
\left.\left(\vec{D}_\text{above}^\parallel-\vec{D}_\text{below}^\parallel\right)\right|_\text{surface}&=0\\
\left.\left(\vec{H}_\text{above}^\perp-\vec{H}_\text{below}^\perp\right)\right|_\text{surface}&=0\\
\left.\left(\vec{H}_\text{above}^\parallel-\vec{H}_\text{below}^\parallel\right)\right|_\text{surface}&=\vec{K}_\text{free}\times\hat{n}\\
\end{align}$$
### Electrodynamics
$$\begin{align}
\mathrm{EMF}&=\oint\vec{E}\cdot d\vec{l}=-\dfrac{d\Phi_B}{dt}\\
M_{ij}&=\dfrac{\mu_0}{4\pi}\oint_{\gamma_i}\oint_{\gamma_j}\dfrac{d\vec{l}_i\cdot d\vec{l}_j}{r}
\end{align}$$
### Electromagnetic Energy
$$\begin{align}
\mathcal{W}_E=\dfrac{1}{2}\epsilon_0E^2, \ \ \ \mathcal{W}_B=\dfrac{1}{2\mu_0}B^2\\
\mathcal{W}_{EM}=\dfrac{1}{2}\left(\epsilon_0E^2+\dfrac{1}{\mu_0}B^2\right)\\
\end{align}$$











---
### Symmetric Maxwell's Equations ($\vec{E}$ & $\vec{B}$)
$$\begin{align}
\vec\nabla\cdot \vec{E}&=\dfrac{\rho_e}{\epsilon_0}&
\oint\vec{E}\cdot d\vec{A} &= \dfrac{q_\text{e}}{\epsilon_0}&
\text{(Gauss' Law)}\\
\vec\nabla\cdot \vec{B}&=\mu_0\rho_m&
\oint\vec{B}\cdot d\vec{A}&=\mu_0q_m&
\text{(Bauss' Law)}\\
\vec\nabla\times \vec{E}&=-\mu_0\vec{J}_m-\dfrac{\partial \vec{B}}{\partial t}&
\oint\vec{E}\cdot d\vec{l}&=-\mu_0I_m-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}&
\text{(Faraday's Law)}\\
\vec\nabla\times \vec{B}&=\mu_0\vec{J}_e+\dfrac{1}{c^2}\dfrac{\partial \vec{E}}{\partial t}&
\oint\vec{B}\cdot d\vec{l} &= \mu_0I_e + \dfrac{1}{c^2}\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}&
\text{(Ampere's Law)}\\
\end{align}$$
$$\begin{align}
\vec{F}&=q_e\left(\vec{E}+\vec{v}\times\vec{B}\right)+q_m\left(\vec{B}-v\times\dfrac{1}{c^2}\vec{E}\right)&
\text{(Lorentz Force)}\\
\dfrac{1}{c^2}\dfrac{\partial^2 \vec{E}}{\partial t^2}-\nabla^2E&=-\dfrac{1}{\epsilon_0c^2}\left(\dfrac{\partial \vec{J}_e}{\partial t}+c^2\nabla\rho_e+\nabla\times\vec{J}_m\right)&
\text{(Electric Wave Equation)}\\
\dfrac{1}{c^2}\dfrac{\partial^2 \vec{B}}{\partial t^2}-\nabla^2\vec{B}&=-\mu_0\left(\dfrac{1}{c^2}\dfrac{\partial\vec{J}_m}{\partial t}+\nabla\rho_m-\nabla\times\vec{J}_e\right)&
\text{(Magnetic Wave Equation)}\\
\end{align}$$
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho_e}{\epsilon_0}&\implies&& \left.\left(\vec{E}_\text{above}^\perp-\vec{E}_\text{below}^\perp\right)\right|_\text{surface}&=\dfrac{\sigma}{\epsilon_0}\\
\vec\nabla\times\vec{E}&=-\mu_0\vec{J}_m&\implies&&\left.\left(\vec{E}_\text{above}^\parallel-\vec{E}_\text{below}^\parallel\right)\right|_\text{surface} &=-\mu_0\left(\vec{K}_m\times\hat{n}\right)\\
\vec\nabla\cdot \vec{B}&=\mu_0\rho_m&\implies&&\left.\left(\vec{B}_\text{above}^\perp-\vec{B}_\text{below}^\perp\right)\right|_\text{surface}&=\mu_0\sigma_m\\
\vec\nabla\times\vec{B}&=\mu_0\vec{J}&\implies&& \left.\left(\vec{B}_\text{above}^\parallel-\vec{B}_\text{below}^\parallel\right)\right|_\text{surface}&=\mu_0\left(\vec{K}_e\times\hat{n}\right)\\
\end{align}$$

