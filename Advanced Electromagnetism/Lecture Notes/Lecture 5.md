**Name:** Stanley Goodwin
**Date:** 9/10/2024

---
### Resistor Review
 - Ohmic Materials $\vec{J}=\sigma\vec{E}$
 - Resistance $V=IR$
 - $\Delta V = -\displaystyle\oint\vec{E}\cdot d\vec{l}$
 - $I = \displaystyle\oint\vec{J}\cdot d\vec{A}$
 - Boundary Conditions: $\vec{E}\perp V$.

### Electromotive Force (EMF)
EMF - What Drives Current?

Given a circuit with current running:
 - This cannot be electrostatic, since $\oint\vec{E}\cdot d\vec{l} = 0$.
 - The current needs to be driven by something else. We call this:
$$\mathrm{EMF} = \oint\vec{f}\cdot d\vec{l}$$
Where $\vec{f}$ is the force per unit charge.
This integral is taken at a point in time, rather than following a charge around the loop.
$\mathrm{EMF}$ has units of voltage $V$.

There are all sorts of things that provide EMF.
For magnetic forces, $\vec{f}=\vec{v}\times\vec{B}$.
For batteries: $\vec{f}=\dfrac{\vec{F}_\mathrm{chemical}}{q}$.
$$\mathrm{EMF}=\oint\vec{f}_\mathrm{total}\cdot d\vec{l} = \int_B^A\left(\vec{f}_\mathrm{battery}+\vec{E}\right)\cdot d\vec{l}+\int_A^B\vec{E}\cdot d\vec{l}$$
$$\vec{f}_\mathrm{battery}+\vec{E} = 0\implies \boxed{\mathrm{EMF}=\int_A^B\vec{E}\cdot d\vec{l}=\int_B^A\vec{f}_\mathrm{battery}\cdot d\vec{l}}$$
The EMF is exactly equal to the voltage drop across the battery!

Now, lets look at a particular source of EMF - make a conductor move through a magnetic field.
This is called a *Motional EMF*.

When a conductor moves through a magnetic field, the Lorentz Force drives a current.
The EMF due to this motion is:
$$\mathrm{EMF}=-\dfrac{d\Phi_B}{dt}$$
The external magnetic field exerts a force on the induced currents.
The net force on the loop is then a force that opposes the motion of the wire.

Another way to think about the current direction is that the induced current attempts to add (or subtract) magnetic field lines to oppose the change in flux that induced the current.
This is Lenz's Law, being the minus sign in the flux rule.

### Energy, $\vec F_B$ and Induced Current
$$I=\dfrac{vBL}{R}$$
$$\begin{align}
-\dfrac{\partial}{\partial t}\int_{x_0}^{x_1}\vec{F}\cdot d\vec{l} + I^2R &= 0\\
\int_{x_0}^{x_1}\vec{F}\cdot d\vec{v}&=\dfrac{(vBL)^2}{R}\\
\end{align}$$
Power is conserved during this process.