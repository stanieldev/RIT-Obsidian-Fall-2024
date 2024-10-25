**Name:** Stanley Goodwin
**Date:** 10/24/2024

---
### Energy and Momentum
 - $\mathcal{U}_\text{EM}=\dfrac{1}{2}\epsilon_0E^2+\dfrac{1}{2\mu_0}B^2$
 - $\vec{S}=\dfrac{\vec{E}\times\vec{B}}{\mu_0}$
 - $\vec{\mathbb{P}}=\mu_0\epsilon_0\vec{S}$:
 For our EM waves:
  - $\left|\vec{E}\right|=E_0\left|\cos\left(\vec{k}\cdot\vec{x}-\omega t + \phi\right)\right|$
  - $\left|\vec{B}\right|=\dfrac{\left|\vec{E}\right|}{c}=\dfrac{E_0}{c}\left|\cos\left(\vec{k}\cdot\vec{x}-\omega t + \phi\right)\right|$
  - $\langle\mathcal{U}_\text{EM}\rangle=\dfrac{1}{2}\epsilon_0 E_0^2$
  - $\langle\vec{S}\rangle=\dfrac{1}{2}c\epsilon_0 E_0^2\hat{z}$
  - $\langle\vec{\mathbb{P}}\rangle=\mu_0\epsilon_0\langle\vec{S}\rangle=\mu_0\epsilon_0c\langle\mathcal{U}_\text{EM}\rangle\hat{z}=\dfrac{\langle\mathcal{U}_\text{EM}\rangle}{c}\hat{z}$
We can define the *intensity* as:
$$\text{Intensity}\equiv\dfrac{\langle P\rangle}{A}=\langle|\vec{S}|\rangle=c\langle|\mathcal{U}_\text{EM}|\rangle=\dfrac{1}{2}c\epsilon_0E_0^2$$
We found EM wave solutions to Maxwell's Equations in vacuum.
If we start from Maxwell's Equations in materials (but no free charges/currents):
$$\begin{align}
\vec\nabla\cdot\vec{D}&=0\\
\vec\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}\\
\vec\nabla\cdot\vec{B}&=0\\
\vec\nabla\times\vec{E}&=\dfrac{\partial\vec{D}}{\partial t}\\
\end{align}$$
We can get EM wave solutions in the materials.
**Note:** We'll restrict ourselves to linear, homogenous, materials. I.e.:
$$\begin{align}
\vec{D}&=\epsilon\vec{E}\\
\vec{B}&=\mu\vec{H}
\end{align}$$
Where $\epsilon$ and $\mu$ are scalar constants of the medium that are homogenous.
The only difference between material and vacuum is that waves propagate at speeds less than the speed of light in a vacuum: $c=\dfrac{1}{\sqrt{\mu\epsilon}}$.
This is because $\vec{P}$ points opposite to $\vec{E}$, so $\epsilon\ge\epsilon_0$.
Coefficient $\mu$ is allowed to be less than $\mu_0$, but when this happens, $\mu_0-\mu$ is very small.
$$v=\dfrac{1}{\sqrt{\mu\epsilon}}=\dfrac{1}{n\sqrt{\mu_0\epsilon_0}}$$
Where $n$ is the index of refraction in the material.

What happens at the interface between two, linear, materials?
We need our boundary conditions for this.
If there is no free charge or current at the interface, then:
$$\begin{align}
\vec{E}_\text{above}^\parallel-\vec{E}_\text{below}^\parallel&=0\\
\vec{B}_\text{above}^\perp-\vec{B}_\text{below}^\perp&=0\\
\vec{D}_\text{above}^\perp-\vec{D}_\text{below}^\perp&=0=\epsilon_\text{above}\vec{E}_\text{above}^\perp-\epsilon_\text{below}\vec{E}_\text{below}^\perp\\
\vec{H}_\text{above}^\parallel-\vec{H}_\text{below}^\parallel&=0=\dfrac{\vec{B}_\text{above}^\parallel}{\mu_\text{above}}-\dfrac{\vec{B}_\text{below}^\parallel}{\mu_\text{below}}\\
\end{align}$$
### Reflection & Transmission
$$\begin{align}
\tilde{E}_{0\text{T}}&=\dfrac{2}{1+\beta}\tilde{E}_{0\text{I}}\\
\tilde{E}_{0\text{R}}&=\dfrac{1-\beta}{1+\beta}\tilde{E}_{0\text{I}}\\
\beta&=\dfrac{n_2}{n_1}=\dfrac{v_1}{v_2}
\end{align}$$
How much power is transmitted:
$$\begin{align}
T=\dfrac{I_T}{I_0}&=\text{Transmission Coefficient}\\
R=\dfrac{I_R}{I_0}&=\text{Reflection Coefficient}\\
\end{align}$$
And so:
$$\begin{align}
T&=\dfrac{\epsilon_2v_2}{\epsilon_1v_1}\dfrac{E^2_{0\text{T}}}{E^2_{0\text{I}}}\\
R&=\dfrac{E^2_{0\text{R}}}{E^2_{0\text{I}}}\\
\end{align}$$
Plugging in the fields, we get:
$$\begin{align}
T&=\dfrac{\epsilon_2v_2}{\epsilon_1v_1}\dfrac{E^2_{0\text{T}}}{E^2_{0\text{I}}}\\
&=\dfrac{\epsilon_2}{\epsilon_1}\dfrac{1}{\beta}\dfrac{2^2}{(1+\beta)^2}\\
\end{align}$$
