**Name:** Stanley Goodwin
**Date:** 10/8/2024

---
### Conserved Energy
Last time, we found the Poynting vector:
$$\vec{S}=\dfrac{\vec{E}\times\vec{B}}{\mu_0}=\vec{E}\times\vec{H}$$
It has the units of energy per area per unit time.


### Relativistic E&M
For moving charges, Coulomb's and Biot-Sovart's laws are not absolutely true.
However, the directions for $\vec E$ and $\vec B$ are more or less what you'd expect.
The fields are compressed in the direction of motion, not uniform.

When you draw it out classically, Newton's 3rd law is violated.
There is a part of momentum that's lost, and it's actually stored in the field.

### Conserved Momentum
Perhaps, instead of just momentum being stored in particles alone, the electromagnetic field may be responsible for making up for the non-conserved momentum.
$$\begin{align}
-\vec\nabla\cdot\phi&=\dfrac{\partial}{\partial t}\left(\mathbb{\vec P}+\mathbb{\vec P}_\text{fields}\right)\\
\int\left(\vec\nabla\cdot T\right)\ d\tau&=\dfrac{\partial\mathbb{\vec P}}{\partial t}+\dfrac{\partial}{\partial t}\int\epsilon_0\mu_0\vec{S}\ d\tau\\
\oint T\cdot d\vec{A}&=\dfrac{\partial\mathbb{\vec P}}{\partial t}+\dfrac{\partial}{\partial t}\int\epsilon_0\mu_0\vec{S}\ d\tau\\
\end{align}$$
