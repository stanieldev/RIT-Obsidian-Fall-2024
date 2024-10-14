**Name:** Stanley Goodwin
**Date:** 9/12/2024

---
### Magnetic Fields & Work
We know that magnetic fields don't do work, and yet we saw that it looks like it does work when we remove a loop of metal from a magnetic field.

By removing the loop from the magnetic field, it redirects where the charges are doing, and so is technically not doing any work. The driving the current isn't directly the reduction of energy from the system.


### Motional EMF and Faraday's Law
1. Induced EMF can be accounted for by the Lorentz Force.
2. Induced EMF is symmetric under who is moving. 
   Can't be the Lorentz Force since the B-field moves instead.
3. Changing Magnetic Field (Magnitude) also creates EMF.

This tells us something deeper about flux.
This led to Faraday postulating that $\vec{E}=-\dfrac{d\Phi_B}{dt}$.
Time-varying Magnetic Flux provides a force that pushes static charges.
Field $\vec E$ looks like an electric field, but is not proven until relativity.

In dynamics, we no longer have a $V$ for $\vec E$ because $\vec\nabla\times\vec{E}\ne0$.
For a full picture of $\vec E$, we need Gauss's Law for the divergence and Faraday's Law for the curl.
Also need a boundary condition, as always.

Where static charges are not present, $\vec\nabla\cdot\vec{E}=0$, we can calculate Faraday's law to calculate $\vec E$ much the same way as Ampere's Law calculated $\vec B$.
$$\oint\vec{E}\cdot d\vec{l}=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}$$
compared to:
$$\oint\vec{B}\cdot d\vec{l}=\mu_0\int\vec{J}\cdot d\vec{A}$$


### Differential Form of Faradays' Law
$$\oint\vec{E}\cdot d\vec{l}=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A} \implies \vec\nabla\times\vec{E} = -\dfrac{\partial\vec{B}}{\partial t}$$
Note: $\vec E$ only curls on changing $\vec B$, but $\vec E$ having loops just means there's curl in the interior of the loop, not necessarily on the loop itself.
For the solenoid example, the exterior field $\vec E=\dfrac{cR^2}{2s}\hat{\phi}$, has 0 curl $\left(\vec\nabla\times\dfrac{\hat{\phi}}{s}\propto \delta(s)\right)$, but the fact that I have loops in $\vec{E}_\text{external}$ tells me there's curl in $E$ somewhere inside the loop (i.e. inside the solenoid, where $\partial_t\vec{B}\ne0$).
