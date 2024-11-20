### Maxwell's Equations (Weber Convention)
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho_e}{\epsilon_0}&
\oint\vec{E}\cdot d\vec{A}&=\dfrac{q_\text{e}}{\epsilon_0}&
\text{(Gauss' Law)}\\
\vec\nabla\cdot\vec{H}&=\dfrac{\rho_m}{\mu_0}&
\oint\vec{H}\cdot d\vec{A}&=\dfrac{q_m}{\mu_0}&
\text{(Gauss' Law)}\\
-\vec\nabla\times\vec{E}&=\vec{J}_m+\mu_0\dfrac{\partial\vec{H}}{\partial t}&
-\oint\vec{E}\cdot d\vec{l}&=I_m+\mu_0\dfrac{d}{dt}\int\vec{H}\cdot d\vec{A}&
\text{(Faraday's Law)}\\
\vec\nabla\times\vec{H}&=\vec{J}_e+\epsilon_0\dfrac{\partial \vec{E}}{\partial t}&
\oint\vec{H}\cdot d\vec{l}&=I_e+\epsilon_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}&
\text{(Ampere's Law)}\\
\end{align}$$
$$\begin{align}
\vec{F}&=q_e\left(\vec{E}+\mu_0\vec{v}\times\vec{H}\right)+q_m\left(\vec{H}-\epsilon_0\vec{v}\times\vec{E}\right)&
\text{(Lorentz Force)}
\end{align}$$
### Boundary Conditions
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho_e}{\epsilon_0}&\implies&& \left.\left(\vec{E}_\text{above}^\perp-\vec{E}_\text{below}^\perp\right)\right|_\text{surface}&=\dfrac{\sigma_e}{\epsilon_0}\\
\vec\nabla\times\vec{E}&=-\vec{J}_m&\implies&&\left.\left(\vec{E}_\text{above}^\parallel-\vec{E}_\text{below}^\parallel\right)\right|_\text{surface}&=-\vec{K}_m\times\hat{n}\\
\vec\nabla\cdot\vec{H}&=\dfrac{\rho_m}{\mu_0}&\implies&&\left.\left(\vec{H}_\text{above}^\perp-\vec{H}_\text{below}^\perp\right)\right|_\text{surface}&=\dfrac{\sigma_m}{\mu_0}\\
\vec\nabla\times\vec{B}&=\vec{J}_e&\implies&& \left.\left(\vec{H}_\text{above}^\parallel-\vec{H}_\text{below}^\parallel\right)\right|_\text{surface}&=\vec{K}_e\times\hat{n}\\
\end{align}$$
### Scalar & Vector Potentials (Weber Convention)
$$\begin{align}
\dfrac{1}{c^2}\dfrac{\partial^2\vec{E}}{\partial t^2}-\vec\nabla^2\vec{E}&=-\vec\nabla\times\vec{J}_m-\mu_0\dfrac{\partial}{\partial t}\vec{J}_e-\dfrac{1}{\epsilon_0}\vec\nabla\rho_e&
\text{(Electric Wave Equation)}
\end{align}$$
TODO: ADD MAGNETISM


### Scalar & Vector Potentials (Weber Convention)
$$\begin{align}
\vec\nabla^2\phi_e-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\phi_e&=-\dfrac{\rho_e}{\epsilon_0}&
\text{(Electric Scalar Potential)}\\
\vec\nabla^2\vec{A}_e-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}_e&=-\mu_0\vec{J}_e&
\text{(Electric Vector Potential)}\\
\vec\nabla^2\phi_m-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\phi_m&=-\dfrac{\rho_m}{\mu_0}&
\text{(Magnetic Scalar Potential)}\\
\vec\nabla^2\vec{A}_m-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}_m&=-\epsilon_0\vec{J}_m&
\text{(Magnetic Vector Potential)}\\
\end{align}$$
### Lorenz Gauge Equations
$$\begin{align}
\dfrac{1}{c^2}\dfrac{\partial}{\partial t}\phi_e+\vec\nabla\cdot\vec{A}_e&=0&
\text{(Electric Condition)}\\
\dfrac{1}{c^2}\dfrac{\partial}{\partial t}\phi_m+\vec\nabla\cdot\vec{A}_m&=0&
\text{(Magnetic Condition)}\\
\end{align}$$
### Field Equations
$$\begin{align}
-\vec{E}&=\vec\nabla\phi_e+\dfrac{\partial}{\partial t}\vec{A}_e+\dfrac{1}{\epsilon_0}\vec\nabla\times\vec{A}_m&\text{(Electric Field)}\\
-\vec{H}&=\vec\nabla\phi_m+\dfrac{\partial}{\partial t}\vec{A}_m-\dfrac{1}{\mu_0}\vec\nabla\times\vec{A}_e&\text{(Magnetic Field)}\\
\end{align}$$
### Charge Quantization
$$\begin{align}
\dfrac{q_eq_m}{2\pi\hbar}&\in\mathbb{Z}&
\text{(Charge Relation)}\\
\end{align}$$
