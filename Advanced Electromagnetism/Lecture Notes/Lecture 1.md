**Date: 8/27/2024**

### Syllabus
Homework every week except exam weeks.


## Electrodynamics
Electricity & Magnetism is central to just about all areas of physics research.
Is it the core of plasma physics, and E&M with quantum mechanics is central to atomic, molecular, and optical physics.
Particle physics looks at other forces (strong & electroweak), but even then, Quantum Electrodynamics (QED) is important as well.
By introducing dynamics (time-dependence), we'll be able to discuss topics like circuits, radiation, electromagnetic waves, and relativity.


## Review of Static Electromagnetism
 - Solving Laplace's equation $\left(\vec{\nabla}^2V=0\right)$
 - Field-Potential relation $\left(\vec{E}=-\vec{\nabla}V\right)$
 - Coulomb's law $\left(\vec{E}=\dfrac{1}{4\pi\epsilon_0}\displaystyle\int\dfrac{\rho}{r^2}\hat{r}\ dr\right)$
 - Gauss's law
 - Biot-Savart Law $\left(\vec{B}=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{J}\times\hat{r}}{r^2}\ dr\right)$
 - Ampere's Law

### Maxwell's Equations
$$\begin{align}
\nabla\cdot \vec{E}&=\dfrac{\rho}{\epsilon_0} & \oint\vec{E}\cdot d\vec{A} &= \dfrac{q_\text{enc}}{\epsilon_0} & \text{(Gauss' Law)}\\
\nabla\cdot \vec{B}&=0 & \oint\vec{B}\cdot d\vec{A} &= 0 & \text{(No Monopoles)}\\
\nabla\times \vec{E}&=-\dfrac{\partial \vec{B}}{\partial t} & \oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A} & \text{(Faraday's Law)}\\
\nabla\times \vec{B}&=\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial \vec{E}}{\partial t} & \oint\vec{B}\cdot d\vec{l} &= \mu_0I + \epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A} & \text{(Ampere's Law)}
\end{align}$$

| Only True in Statics      | Always True              |
| ------------------------- | ------------------------ |
| Coulomb's Law             | Gauss' Law               |
| Biot-Savart Law           | Faraday's Law            |
| Ampere's Law              | Corrected Ampere's Law   |
| $\vec{E}=0$ in Conductors | $\vec{E}$ makes currents |
|                           | Lorentz Force Law        |

### Vector Calculus Review

Gradient = Covariant


Gradient: $\nabla f = \displaystyle\sum_i\partial_i f_i e_i$
Gradient is the inverse of a line integral.
$$V = -\int\vec{E}\cdot d\vec{l} \iff E=-\vec{\nabla}V$$
Divergence: $\vec{\nabla}\cdot\vec{F}= \displaystyle\sum_i\dfrac{\partial F_i}{\partial x_i}$
Curl:



### Kelvin-Stokes Theorem
$$\int_{\partial\Omega}\omega=\int_{\Omega}\mathrm{d}\omega$$

