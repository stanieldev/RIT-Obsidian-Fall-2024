**Name:** Stanley Goodwin
**Date:** 11/7/2024

---
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
