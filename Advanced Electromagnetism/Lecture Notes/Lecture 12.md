**Name:** Stanley Goodwin
**Date:** 10/3/2024

---

Exam details: 1 Page of my own notes!
## Field Boundary Conditions
Each of the following comes from one of Maxwell's equations.
### Ampere's Law
$$\oint\vec{B}\cdot d\vec{l}=\mu_0I+\epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}$$
Let's take an Amperian loop with a very small height:
$$\begin{align}
\oint\vec{B}\cdot d\vec{l}&=\int_\text{top}\vec{B}\cdot d\vec{l}+\int_\text{right}\vec{B}\cdot d\vec{l}+\int_\text{bottom}\vec{B}\cdot d\vec{l}+\int_\text{left}\vec{B}\cdot d\vec{l}\\
\mu_0I&=\int_\text{top}\vec{B}\cdot d\vec{l}+\int_\text{bottom}\vec{B}\cdot d\vec{l}+0\\
\mu_0I&=B^\parallel_\text{top}l-B^\parallel_\text{bottom}l\\
\dfrac{\mu_0I}{l}&=B^\parallel_\text{top}-B^\parallel_\text{bottom}\\
\Aboxed{B^\parallel_\text{top}-B^\parallel_\text{bottom}&=\mu_0\left(\vec{K}\times\hat{n}\right)}
\end{align}$$
Substituting $I_\text{enc}$ with $I_\text{free}$ to find $\vec{H}$:
$$\begin{align}
\Aboxed{H^\parallel_\text{top}-H^\parallel_\text{bottom}&=\vec{K}_\text{free}\times\hat{n}}
\end{align}$$
### Faraday's Law
$$\oint\vec{E}\cdot d\vec{l}=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}$$
Let's take an Gaussian loop with a very small height:
$$\begin{align}
\oint\vec{E}\cdot d\vec{l}&=\int_\text{top}\vec{E}\cdot d\vec{l}+\int_\text{right}\vec{E}\cdot d\vec{l}+\int_\text{bottom}\vec{E}\cdot d\vec{l}+\int_\text{left}\vec{E}\cdot d\vec{l}\\
0&=\int_\text{top}\vec{E}\cdot d\vec{l}+\int_\text{bottom}\vec{E}\cdot d\vec{l}+0\\
0&=E^\parallel_\text{top}l-E^\parallel_\text{bottom}l\\
0&=E^\parallel_\text{top}-E^\parallel_\text{bottom}\\
\Aboxed{E^\parallel_\text{top}-E^\parallel_\text{bottom}&=0}
\end{align}$$
### No Monopoles
$$\begin{align}
\oint\vec{B}\cdot d\vec{A}=0\\
\Aboxed{B^\perp_\text{top}-B^\perp_\text{bottom}&=0}
\end{align}$$
### Gauss' Law
$$\begin{align}
\oint\vec{E}\cdot d\vec{A}=0\\
\Aboxed{E^\perp_\text{top}-E^\perp_\text{bottom}&=\dfrac{\sigma}{\epsilon_0}}\\
\end{align}$$
Looking at the free charge:
$$\begin{align}
\Aboxed{D^\perp_\text{top}-D^\perp_\text{bottom}&=\sigma_\text{free}}\\
\end{align}$$

## Energy Conservation & Conserved Currents
Conserved current:
 - Global charge conservation is a statement that $\dfrac{d}{dt}\displaystyle\int\rho\ d\tau=0$.
 - If this all we knew, it would be possible for charge to vanish from on earth as long as a corresponding charge appears somewhere else in the universe.
 - A stronger statement shows local charge conservation: $\dfrac{d\rho}{dt}=-\vec\nabla\cdot\vec{J}$.
 - If the charge in a volume is changing, there must be a current flow from that volume's surface.

Any locally-conserved quantity will have a similar conservation law.
 - For a conserved quantity $X$, $\dfrac{dX}{dt}=-\vec\nabla\cdot\vec{S}$, where $\vec{S}$ is a volume current that carries $X$.
 - Some conserved quantities are Energy, Momentum, and Angular Momentum.


Energy density conservation:
$$\begin{align}
\mathcal{U}_E&=\dfrac{1}{2}\epsilon_0 E^2\\
\mathcal{U}_B&=\dfrac{1}{2\mu_0} B^2\\
\mathcal{U}_\text{EM}&=\dfrac{1}{2}\left(\epsilon_0 E^2+\dfrac{1}{\mu_0} B^2\right)\\
\dfrac{d}{dt}(\mathcal{U}_\text{EM})&=-\vec\nabla\cdot\phi
\end{align}$$
We can look at the work a little closer:
$$\begin{align}
dW_\text{EM}&=\vec{F}\cdot d\vec{l}\\
&=dq\left(\vec{E}+\vec{v}\times\vec{B}\right)\cdot \vec{v}\ dt\\
\dfrac{dW_\text{EM}}{dt}&=\vec{E}\cdot\left(\vec{v}\ dq\right)\\
&=\vec{E}\cdot\left(\vec{v}\rho\ d\tau\right)\\
\dfrac{dW_\text{EM}}{dt}&=\vec{E}\cdot\left(\vec{J}\ d\tau\right)\\
&=\int\vec{E}\cdot\vec{J}\ d\tau\\
&=\int\vec{E}\cdot\left(\dfrac{1}{\mu_0}\vec\nabla\times\vec{B}+\epsilon_0\dfrac{d\vec{E}}{dt}\right)\ d\tau\\
&=\dfrac{1}{\mu_0}\int\vec{E}\cdot\left(\vec\nabla\times\vec{B}\right)\ d\tau+\int\vec{E}\cdot\epsilon_0\dfrac{d\vec{E}}{dt}\ d\tau\\
&=\dfrac{1}{\mu_0}\int\left(\vec{B}\cdot\left(\vec\nabla\times\vec{E}\right)-\vec\nabla\cdot\left(\vec{E}\times\vec{B}\right)\right)\ d\tau+\int\vec{E}\cdot\epsilon_0\dfrac{d\vec{E}}{dt}\ d\tau\\
&=\dfrac{1}{\mu_0}\int\vec{B}\cdot\left(\vec\nabla\times\vec{E}\right)\ d\tau-\dfrac{1}{\mu_0}\int\vec\nabla\cdot\left(\vec{E}\times\vec{B}\right)\ d\tau+\int\vec{E}\cdot\epsilon_0\dfrac{d\vec{E}}{dt}\ d\tau\\
\dfrac{d\mathcal{U}_\text{q}}{dt}&=\dfrac{1}{\mu_0}\vec{B}\cdot\left(\vec\nabla\times\vec{E}\right)-\dfrac{1}{\mu_0}\vec\nabla\cdot\left(\vec{E}\times\vec{B}\right)+\vec{E}\cdot\epsilon_0\dfrac{d\vec{E}}{dt}\\
&=-\dfrac{1}{\mu_0}\vec{B}\cdot\dfrac{d\vec{B}}{dt}-\dfrac{1}{\mu_0}\vec\nabla\cdot\left(\vec{E}\times\vec{B}\right)+\vec{E}\cdot\epsilon_0\dfrac{d\vec{E}}{dt}\\
&=-\dfrac{1}{2\mu_0}B^2-\dfrac{1}{\mu_0}\vec\nabla\cdot\left(\vec{E}\times\vec{B}\right)-\dfrac{1}{2}\epsilon_0E^2\\
\Aboxed{-\vec\nabla\cdot\left(\dfrac{\vec{E}\times\vec{B}}{\mu_0}\right)&=\dfrac{d}{dt}\left(\mathcal{U}_\text{q}+\dfrac{1}{2\mu_0}B^2+\dfrac{1}{2}\epsilon_0E^2\right)}
\end{align}$$
The expression inside the divergence is called the Poynting vector:
$$\vec{S}=\dfrac{\vec{E}\times\vec{B}}{\mu_0}$$




