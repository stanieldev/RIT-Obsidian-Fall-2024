### Electrostatics & Magnetostatics
$$\begin{align}
\vec{E}_\mathrm{net}&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho}{r^2}\hat{r}\ d\tau&\text{(Coulomb's Law)}\\
V_\mathrm{net}&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho}{r}\ d\tau&\text{(Scalar Potential)}\\
\vec{B}_\mathrm{net}&=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{J}\times\hat{r}}{r^2}\ d\tau&\text{(Biot-Savart Law)}\\
\vec{A}_\mathrm{net}&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}}{r}\ d\tau&\text{(Vector Potential)}
\end{align}$$
### Maxwell's Equations $\left(\vec{E}\ \&\ \vec{B}\right)$
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho}{\epsilon_0}&
\oint\vec{E}\cdot d\vec{a}&=\dfrac{q_\text{enc}}{\epsilon_0}&
\text{(Gauss' Law)}\\
\vec\nabla\cdot\vec{B}&=0&
\oint\vec{B}\cdot d\vec{a}&=0&
\text{(No Monopoles)}\\
\vec\nabla\cdot\vec{J}&=-\dfrac{\partial\rho}{\partial t}&
\oint\vec{J}\cdot d\vec{a}&=-\dfrac{\partial q_\text{enc}}{\partial t}&
\text{(Continuity)}\\
\vec\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}&
\oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{a}&
\text{(Faraday's Law)}\\
\vec\nabla\times\vec{B}&=\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial\vec{E}}{\partial t}&
\oint\vec{B}\cdot d\vec{l}&=\mu_0I_\text{enc}+\epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{a}&
\text{(Ampere's Law)}
\end{align}$$
$$\begin{align}
\vec{F}&=q\left(\vec{E}+\vec{v}\times\vec{B}\right)&
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
### Electromagnetic Induction
$$\begin{align}
\mathrm{EMF}&=\oint\vec{E}\cdot d\vec{l}=-\dfrac{d\Phi_B}{dt}
&\text{(Electromotive "Force")}\\
M_{ij}&=\dfrac{\mu_0}{4\pi}\oint_{\gamma_i}\oint_{\gamma_j}\dfrac{d\vec{l}_i\cdot d\vec{l}_j}{r}=M_{ji}
&\text{(Mutual Induction)}
\end{align}$$
### Electromagnetic Energy
$$\begin{align}
\mathcal{U}_{EM}&=\dfrac{1}{2}\left(\epsilon_0\vec{E}^2+\dfrac{1}{\mu_0}\vec{B}^2\right)\\
\vec{S}&=\dfrac{\vec{E}\times\vec{B}}{\mu_0}\\
\vec{\mathbb{P}}_\text{EM}&=\mu_0\epsilon_0\vec{S}\\
\end{align}$$
### Electromagnetic Waves
$$\begin{align}
\vec{k}&=\sqrt{k_x^2+k_y^2+k_z^2}\ \hat{k}\\
\vec{E}&=\tilde{E_0}\cos\left(\vec{k}\cdot\vec{x}-\omega t\right)\hat{E}_0\\
\vec{B}&=\dfrac{\tilde{E_0}}{c}\cos\left(\vec{k}\cdot\vec{x}-\omega t\right)\left(\hat{k}\times\hat{E}_0\right)=\dfrac{\hat{k}\times\vec{E}}{c}\\
\end{align}$$
### Interfaces
$$\begin{align}
n_1\sin(\theta_I)&=n_2\sin(\theta_T) & \theta_B&=\tan^{-1}\left(\beta\right)\\
\beta&=\dfrac{n_2}{n_1} & \alpha&=\dfrac{\cos\theta_T}{\cos\theta_I}
\end{align}$$
$$\begin{align}
&\text{Parallel (P)} && \text{Perpendicular (S)}\\
\tilde{E}_{0\text{T}}&=\dfrac{2}{\alpha+\beta}\tilde{E}_{0\text{I}} &
\tilde{E}_{0\text{T}}&=\dfrac{2}{1+\alpha\beta}\tilde{E}_{0\text{I}}\\
\tilde{E}_{0\text{R}}&=\dfrac{\alpha-\beta}{\alpha+\beta}\tilde{E}_{0\text{I}} & 
\tilde{E}_{0\text{R}}&=\dfrac{1-\alpha\beta}
{1+\alpha\beta}\tilde{E}_{0\text{I}}\\
T&=\dfrac{4\alpha\beta}{(\alpha+\beta)^2} & 
T&=\dfrac{4\alpha\beta}{(1+\alpha\beta)^2}\\
R&=\dfrac{(\alpha-\beta)^2}{(\alpha+\beta)^2} & 
R&=\dfrac{(1-\alpha\beta)^2}{(1+\alpha\beta)^2}\\
\end{align}$$
### Conductors
$$\begin{align}
k_\text{Re}&=\omega\sqrt{\dfrac{\mu\epsilon}{2}}\sqrt{1+\sqrt{1+\left(\tfrac{\sigma}{\epsilon\omega}\right)^2}}\\
k_\text{Im}&=\omega\sqrt{\dfrac{\mu\epsilon}{2}}\sqrt{-1+\sqrt{1+\left(\tfrac{\sigma}{\epsilon\omega}\right)^2}}\\
\end{align}$$
### Electromagnetic Gauge
$$\begin{align}
\phi'&=\phi-\partial_t\lambda&\vec{E}&=-\vec\nabla\phi-\partial_t\vec{A}\\
\vec{A}'&=\vec{A}+\vec\nabla\lambda&\vec{B}&=\vec\nabla\times\vec{A}\\
\end{align}$$
$$\begin{align}
\vec\nabla^2V+\dfrac{\partial}{\partial t}\left(\vec\nabla\cdot\vec{A}\right)&=-\dfrac{\rho}{\epsilon_0}\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(\vec\nabla\cdot\vec{A}+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)&=-\mu_0\vec{J}
\end{align}$$
#### Coulomb Gauge
$$\begin{align}
\vec\nabla\cdot\vec{A}&=0\\
\vec\nabla^2V&=-\dfrac{\rho}{\epsilon_0}\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\dfrac{1}{c^2}\dfrac{\partial}{\partial t}\left(\vec\nabla V\right)&=-\mu_0\vec{J}
\end{align}$$
#### Lorenz Gauge
$$\begin{align}
\vec\nabla\cdot\vec{A}&=-\mu_0\epsilon_0\dfrac{\partial\phi}{\partial t}\\
\dfrac{1}{c^2}\partial_t^2\phi-\vec\nabla^2\phi&=\dfrac{\rho}{\epsilon_0}\\
\dfrac{1}{c^2}\partial_t^2\vec{A}-\vec\nabla^2\vec{A}&=\mu_0\vec{J}\\
\end{align}$$
#### Jefimenko's Equations
$$\begin{align}
V(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho(\vec{r}', t_R)}{|\vec{r}-\vec{r}'|}\ d\tau'\\
\vec{A}(\vec{r},t)&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}(\vec{r}', t_R)}{|\vec{r}-\vec{r}'|}\ d\tau'\\
t_R&=t-\dfrac{|\vec{r}-\vec{r}'|}{c}
\end{align}$$
$$\begin{align}
\vec{E}(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\left[\dfrac{\rho(\vec{r}', t_R)}{|\mathscr{r}|^2}\hat{r}+\dfrac{\dot\rho(\vec{r}', t_R)}{c|\mathscr{r}|}\hat{r}-\dfrac{\vec{J}(\vec{r},t_R)}{c^2|\mathscr{r}|}\right]d\tau'\\
\vec{B}(\vec{r},t)&=\dfrac{\mu_0}{4\pi}\int\left[\dfrac{\vec{J}(\vec{r},t_R)}{|\mathscr{r}|^2}+\dfrac{\dot{\vec{J}}(\vec{r},t_R)}{c|\mathscr{r}|}\right]\times\hat{\mathscr{r}}\ d\tau'
\end{align}$$
### Relativistic Point Charge
$$\begin{align}
V(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\dfrac{qc}{\mathscr{r}c-\vec{\mathscr{r}}\cdot\vec{v}}\\
\vec{A}(\vec{r},t)&=\dfrac{\vec{v}}{c^2}V(\vec{r},t)\\
\end{align}$$
### Dipole Radiation
$$\begin{align}
\langle P_\text{total}\rangle&=\dfrac{\mu_0p_0^2\omega^4}{12\pi c}\\
&=\dfrac{\mu_0q^2a^2}{6\pi c}\\
\end{align}$$
### Lorentz Transform
$$\begin{align}
\left[\begin{array}{c}ct'\\x'\\y'\\z'\end{array}\right]&=
\left[\begin{array}{c}\gamma&-\gamma\beta&0&0\\-\gamma\beta&\gamma&0&0\\0&0&1&0\\0&0&0&1\end{array}\right]\left[\begin{array}{c}ct\\x\\y\\z\end{array}\right]\\
\end{align}$$
$$\begin{align}
E'_x&=E_x & E'_y&=\gamma(E_y-vB_z) & E'_z&=\gamma(E_z+vB_y)\\
B'_x&=B_x & B'_y&=\gamma(B_y+vE_z/c^2) & B'_z&=\gamma(B_z-vE_y/c^2)\\
\end{align}$$
