To do list:
 - Maxwell in vacuum
 - Maxwell standard
 - Maxwell with $P$ and $M$ polarizations.

### Maxwell's Equations ($\vec{E}$ and $\vec{B}$)
$$\begin{align}
\nabla\cdot\vec{E}&=\dfrac{\rho}{\epsilon_0}&
\oint\vec{E}\cdot d\vec{A}&=\dfrac{q_\text{enc}}{\epsilon_0}&
\text{(Gauss' Law)}\\
\nabla\cdot\vec{B}&=0&
\oint\vec{B}\cdot d\vec{A}&=0&
\text{(No Monopoles)}\\
\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}&
\oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}&
\text{(Faraday's Law)}\\
\nabla\times\vec{B}&=\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial\vec{E}}{\partial t}&
\oint\vec{B}\cdot d\vec{l}&=\mu_0I+\epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}&
\text{(Ampere's Law)}\\
\nabla\cdot\vec{J}&=-\dfrac{\partial\rho}{\partial t}&
\oint\vec{J}\cdot d\vec{A}&=-\dfrac{\partial q_\text{enc}}{\partial t}&
\text{(Continuity)}
\end{align}$$
$$\begin{align}
\vec{F}&=q_e\left(\vec{E}+\vec{v}\times\vec{B}\right)&
\text{(Lorentz Force)}\\
\dfrac{1}{c^2}\dfrac{\partial^2\vec{E}}{\partial t^2}-\nabla^2\vec{E}&=-\dfrac{1}{c\epsilon_0}\left(\dfrac{1}{c}\dfrac{\partial\vec{J}}{\partial t}+c\nabla\rho\right)&
\text{(Electric Wave Equation)}\\
\dfrac{1}{c^2}\dfrac{\partial^2\vec{B}}{\partial t^2}-\nabla^2\vec{B}&=\mu_0\left(\nabla\times\vec{J}\right)&
\text{(Magnetic Wave Equation)}
\end{align}$$
### Maxwell's Equations (Vacuum)
$$\begin{align}
\nabla\cdot\vec{E}&=0&
\oint\vec{E}\cdot d\vec{A}&=0&
\text{(Gauss' Law)}\\
\nabla\cdot\vec{B}&=0&
\oint\vec{B}\cdot d\vec{A}&=0&
\text{(No Monopoles)}\\
\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}&
\oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}&
\text{(Faraday's Law)}\\
\nabla\times\vec{B}&=\dfrac{1}{c^2}\dfrac{\partial\vec{E}}{\partial t}&
\oint\vec{B}\cdot d\vec{l}&=\dfrac{1}{c^2}\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}&
\text{(Ampere's Law)}
\end{align}$$
$$\begin{align}
\dfrac{1}{c^2}\dfrac{\partial^2\vec{E}}{\partial t^2}-\nabla^2\vec{E}&=0&
\text{(Electric Wave Equation)}\\
\dfrac{1}{c^2}\dfrac{\partial^2\vec{B}}{\partial t^2}-\nabla^2\vec{B}&=0&
\text{(Magnetic Wave Equation)}
\end{align}$$
























### Symmetric Maxwell's Equations ($\vec{E}$ & $\vec{B}$)
$$\begin{align}
\nabla\cdot \vec{E}&=\dfrac{\rho_e}{\epsilon_0}&
\oint\vec{E}\cdot d\vec{A} &= \dfrac{q_\text{e}}{\epsilon_0}&
\text{(Gauss' Law)}\\
\nabla\cdot \vec{B}&=\mu_0\rho_m&
\oint\vec{B}\cdot d\vec{A}&=\mu_0q_m&
\text{(Bauss' Law)}\\
\nabla\times \vec{E}&=-\mu_0\vec{J}_m-\dfrac{\partial \vec{B}}{\partial t}&
\oint\vec{E}\cdot d\vec{l}&=-\mu_0I_m-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}&
\text{(Faraday's Law)}\\
\nabla\times \vec{B}&=\mu_0\vec{J}_e+\epsilon_0\mu_0\dfrac{\partial \vec{E}}{\partial t}&
\oint\vec{B}\cdot d\vec{l} &= \mu_0I_e + \epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}&
\text{(Ampere's Law)}\\
\end{align}$$
$$\begin{align}
\vec{F}&=q_e\left(\vec{E}+\vec{v}\times\vec{B}\right)+q_m\left(\vec{B}-v\times\dfrac{1}{c^2}\vec{E}\right)&
\text{(Lorentz Force)}\\
\epsilon_0\mu_0\dfrac{\partial^2 \vec{E}}{\partial t^2}-\nabla^2E&=-\dfrac{1}{\epsilon_0c^2}\left(\dfrac{\partial \vec{J}_e}{\partial t}+c^2\nabla\rho_e+\nabla\times\vec{J}_m\right)&
\text{(Electric Wave Equation)}\\
\dfrac{1}{c^2}\dfrac{\partial^2 \vec{B}}{\partial t^2}-\nabla^2\vec{B}&=-\mu_0\left(\dfrac{1}{c^2}\dfrac{\partial\vec{J}_m}{\partial t}+\nabla\rho_m-\nabla\times\vec{J}_e\right)&
\text{(Magnetic Wave Equation)}\\
\end{align}$$




### Single Field Symmetric Equations
$$\begin{align}
F&=\vec{E}\pm ic\vec{B}\\
\rho&=c\rho_e\pm i\rho_m
\end{align}$$

$$\begin{align}
\nabla\cdot F&=\dfrac{\rho}{c\epsilon_0}\\
\end{align}$$

$$\begin{align}
\nabla\times F&=\nabla\times\vec{E}-ic\nabla\times\vec{B}\\
&=\dfrac{1}{\epsilon_0c^2}\left(-\vec{J}_m-c^2\dfrac{\partial \vec{B}}{\partial t}\pm ic\left(\vec{J}_e+\epsilon_0\dfrac{\partial \vec{E}}{\partial t}\right)\right)
\end{align}$$

