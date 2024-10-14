**Name:** Stanley Goodwin
**Date:** 9/5/2024

---
## Boundary Conditions
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho}{\epsilon_0} &\implies& \left.\left(\vec{E}_\text{above}^\perp-\vec{E}_\text{below}^\perp\right)\right|_\text{surface} = \dfrac{\sigma}{\epsilon_0}\\
\vec\nabla\times\vec{E}&=0 &\implies& \left.\left(\vec{E}_\text{above}^\parallel-\vec{E}_\text{below}^\parallel\right)\right|_\text{surface} = 0\\
\vec\nabla\cdot\vec{B}&=0 &\implies& \left.\left(\vec{B}_\text{above}^\perp-\vec{B}_\text{below}^\perp\right)\right|_\text{surface} = 0\\
\vec\nabla\times\vec{B}&=\mu_0\vec{J} &\implies& \left.\left(\vec{B}_\text{above}^\parallel-\vec{B}_\text{below}^\parallel\right)\right|_\text{surface} = \vec{K}\times\hat{n}\\
\end{align}$$
## Current & Resistance
What makes current flow in the first place? In most materials we find:
$$\vec{J}=\sigma\vec{f} \ \ \ \text{or} \ \ \ \rho\vec{J}=\vec{f}$$
Where $\sigma$ is the conductivity of the material, $\rho$ is the resistivity, and $\vec{f}$ is the force per unit charge.
Ohm's Law isn't fundamental like Newton's Laws are, but is it effectively true for *most* materials.

Recall that $\vec{J} = nq\vec{v}_\text{drift}$, Ohm's law says that:
$$\begin{align}
nq\vec{v}_\text{drift} &= \sigma\vec{f}\\
\Aboxed{\vec{v}_\text{drift}&=\dfrac{\sigma}{nq}\vec{f}}
\end{align}$$
The chargers are bouncing all over, encountering a resistive force, losing energy to scattering and thermalization. That $\vec{f}$ is necessary to keep charges drifting in 1 particular direction.
$\vec{v}_\text{drift}$ for any given charge (like you have a swarm of bees being pushed by a gentle breeze).

Recall that $\vec{F} = q\left(\vec{E}+\vec{v}\times\vec{B}\right)$.
Generally, $\vec{v}$ and $\vec{B}$ are small enough that $\vec{f}=\vec{E}$.
 - Bigger $\sigma$, less $\vec{E}$ is need to drive a given $\vec{J}$.
 - For a "good conductor," like copper, $\sigma_\text{cu}=6\cdot10^7\ \Omega^{-1}\mathrm{m}^{-1}$.
 - For a "insulator," like wood, $\sigma_\text{wood}\approx10^{-8}\ \Omega^{-1}\mathrm{m}^{-1}$.
 - For a resistor in a circuit, $\sigma_\text{wood}\sim10^3\ \Omega^{-1}\mathrm{m}^{-1}$.
Ohm's Law: $\vec{J}=\sigma\vec{f} \implies \vec{J}=\sigma\vec{E}$.

When we have current in a wire, there is an electric field in the wire ($\vec{E}=0$ in static equilibrium).
If $\sigma \rightarrow \infty$, we could have finite current, even with $\vec{E}=0$.
But for real conductors, $\sigma$ is big, but finite, so some small $\vec{E}$ will be present.
Power dissipated in wire: $P = \Delta V\cdot I$.

### Resistance of Wires
For a cylindrical resistor:
$$\begin{align}
\vec{J}=\sigma\vec{E} \implies \dfrac{I}{A}=\sigma\dfrac{\Delta V}{L}\\
\dfrac{\Delta V}{I} = \Aboxed{R = \rho\dfrac{L}{A}}
\end{align}$$
We see here that $R$ is a geometric quantity. It depends on the shape and material of the resistor, not the current flowing through the resistor.

In calculating $R$ for the wire, I assumed a uniform $\vec{E}$. Why?
The continuity equation & ohm's law $\implies$ $\vec{E}$ is parallel to the surface.
$$\vec\nabla\cdot\vec{J}+\dfrac{\partial\rho}{\partial t}=0$$
1) $\vec\nabla\cdot\vec{E}=0$ for a steady current, since in a steady state $\partial_t\rho=0 \implies \vec\nabla\cdot\vec{J}=0$.
   Using ohms law, $\vec\nabla\cdot\vec{E}=0$ as well.

2) At the edges of the resistor, $\vec{E}\cdot\hat{n}=0$ ($\vec{E}$ is $\parallel$ to the surface)
   If this weren't the case, $\vec{J}$ would gain charges, so $\vec{J}$ is also $\parallel$ to the surface.

What we have now is a boundary condition. Can (in principle) solve $\vec{E}$ with the usual tricks.
Use $\vec{J}=\sigma\vec{E}$ and $I=\oint\vec{J}\cdot d\vec{A}$, we always find that $\Delta V=\int\vec{E}\cdot d\vec{l}\propto I$, and therefore $\Delta V = IR$.

