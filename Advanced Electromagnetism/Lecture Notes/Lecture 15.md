**Name:** Stanley Goodwin
**Date:** 10/17/2024

---
### Conserved Momentum
Last time, we showed that the electromagnetic field can store momentum in order to make sure momentum is conserved in all inertial frames.

In terms of tensors and momentum flux:
$$\begin{align}
\oint T\cdot d\vec{A}&=\dfrac{\partial\mathbb{\vec P}}{\partial t}+\dfrac{\partial}{\partial t}\int\epsilon_0\mu_0\vec{S}\ d\tau\\
\end{align}$$
Where $T$ is the *Maxwell Stress Tensor*, coming from momentum flux per unit area.
The on-diagonals are pressures, the off-diagonals are sheers.

Our electromagnetic field can also store angular momentum w/density:
$$\begin{align}
\mathbb{\vec{L}}_\text{EM}=\vec{r}\times\mathbb{\vec{P}}_\text{EM}=\epsilon_0\mu_0\cdot \vec{r}\times\vec{S}
\end{align}$$
Otherwise, the Lorentz force violates Newton's 3rd law and momentum conservation.
Photons (quantized electromagnetic fields) are massless, but do carry energy and momentum.
$$\begin{align}
\dfrac{\text{Energy Flow}}{\text{Area}\cdot\text{Time}}\cdot\dfrac{1}{c^2}&=\text{Momentum Density}\\
\left|\vec{S}\right|\cdot\dfrac{1}{c^2}&=\left|\mathbb{\vec{P}}_\text{EM}\right|
\end{align}$$
### Electromagnetic Waves
To begin, what is a wave? A *traveling disturbance* that satisfies the wave equation.
$$\vec\nabla^2\phi=\dfrac{1}{c^2}\dfrac{\partial^2\phi}{\partial t^2}$$
To set a solution, start with any function $\phi_0$. A wave solution would be $\phi(\vec{x},t)=\phi_0(\vec{x}-\vec{v}t)$
Another solution is a wave in the opposite direction: $\phi(\vec{x},t)=\phi_0(\vec{x}+\vec{v}t)$

Stationary solutions of the wave equation are the mean of 2 equal and opposite traveling waves.
It is also a solution to the wave equation, since the wave equation is linear.

It doesn't necessarily have to be periodic, but it can be written as a linear combination of sines and cosines using the *Fourier transform*.

Most the future work we do will be with *transverse waves*, and specifically *plane waves*.