**Name:** Stanley Goodwin
**Date:** 8/27/2024

---
## Syllabus
Homework every week except exam weeks.

## Electrodynamics
Electricity & Magnetism is central to just about all areas of physics research.
 - Is it the core of plasma physics.
 - E&M with quantum mechanics is central to atomic, molecular, and optical physics.
 - Particle physics looks at other forces (strong & electroweak), but even then, Quantum Electrodynamics (QED) is important as well.

By introducing dynamics (time-dependence), we'll be able to discuss topics like circuits, radiation, electromagnetic waves, and relativity.

## Review of Static Electromagnetism
What do we remember doing last semester?
 - Solving Laplace's equation $\left(\vec{\nabla}^2V=0\right)$
 - Field-Potential relation $\left(\vec{E}=-\vec{\nabla}V\right)$
 - Coulomb's law $\left(\vec{E}=\dfrac{1}{4\pi\epsilon_0}\displaystyle\int\dfrac{\rho}{r^2}\hat{r}\ d\tau\right)$
 - Biot-Savart Law $\left(\vec{B}=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{J}\times\hat{r}}{r^2}\ d\tau\right)$
 - Gauss' Law / Ampere's Law

### Comparison of Electrostatic and Electrodynamics
| *Only True in Statics*    | *Always True*            |
| ------------------------- | ------------------------ |
| Coulomb's Law             | Gauss' Law               |
| Biot-Savart Law           | Faraday's Law            |
| Ampere's Law              | Maxwell-Ampere's Law     |
| $\vec{E}=0$ in Conductors | $\vec{E}$ makes currents |
|                           | Lorentz Force Law        |
### Maxwell's Equations
$$\begin{align}
\vec\nabla\cdot \vec{E}&=\dfrac{\rho}{\epsilon_0} & \oint\vec{E}\cdot d\vec{A} &= \dfrac{q_\text{enc}}{\epsilon_0} & \text{(Gauss' Law)}\\
\vec\nabla\cdot \vec{B}&=0 & \oint\vec{B}\cdot d\vec{A} &= 0 & \text{(No Monopoles)}\\
\vec\nabla\times \vec{E}&=-\dfrac{\partial \vec{B}}{\partial t} & \oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A} & \text{(Faraday's Law)}\\
\vec\nabla\times \vec{B}&=\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial \vec{E}}{\partial t} & \oint\vec{B}\cdot d\vec{l} &= \mu_0I_\text{enc} + \epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A} & \text{(Ampere's Law)}
\end{align}$$

## Vector Calculus Review
### Gradient
Tells us the directional derivative of the scalar function $f$.
$$\vec\nabla f = \displaystyle\sum_i\dfrac{\partial f}{\partial x_i}\cdot e_i$$
Is it also the inverse operation of a line integral.
$$f = -\int\vec{F}\cdot d\vec{l} \iff \vec{F}=-\vec{\nabla}f$$
### Divergence
Tells us about an "outflow" from a point of a vector field $F$.
$$\vec{\nabla}\cdot\vec{F}= \displaystyle\sum_i\dfrac{\partial F_i}{\partial x_i}$$
It also relates to the flux of a closed surface with the following relation:
$$\int\vec\nabla\cdot\vec{F}\ d\tau = \oint\vec{F}\cdot d\vec{A}$$
This relationship is called the *Divergence Theorem*.
### Curl
Tells us about a "curl" of vector field $F$ at a point.
$$\vec{\nabla}\times\vec{F}=\left|\begin{array}{ccc}\hat{x}&\hat{y}&\hat{z}\\\partial_x&\partial_y&\partial_z\\F_x&F_y&F_z\end{array}\right|$$
It also relates to the curl of a closed contour with the following relation:
$$\int\left(\vec\nabla\times\vec{F}\right)\cdot d\vec{A} = \oint\vec{F}\cdot d\vec{l}$$
This relationship is called *Green's Theorem*.

