**Name:** Stanley Goodwin
**Date:** 9/3/2024

---
### Conductors in Equilibrium
 - In equilibrium, $\vec{E}=0$ inside the conducting material.
 - This also implies, by $\vec{E} = -\vec\nabla V$, that $V$ is uniform within the conducting material.
 - In static equilibrium, all charges are distributed on the surface.
	 - This is shown by Gauss's law, since $\vec\nabla\cdot\vec{E}=\dfrac{\rho}{\epsilon_0} = 0$.
 - If there's a cavity within the conductor with a charge inside, an induced charge forms on the inner surface to "screen" that charge. We can see the value of the charge due to charge conservation $(q_\text{inner}=-q_\text{cavity}$ and $q_\text{outer}-q_\text{inner}=q_\text{net})$, but you can't tell anything about the distribution of the charge from the outside because of the conductor that screens the cavity.

## Magnetostatics
Static $\vec{B}$ arises due to currents.
$$\vec{F}_B=q\vec{v}\times\vec{B}=\int Id\vec{l}\times\vec{B}=\int \left(\vec{K}\times\vec{B}\right)dA=\int \left(\vec{J}\times\vec{B}\right)d\tau$$
If we know where all the currents are (and they are steady currents), we can use the Biot-Savart law to calculate $\vec{B}$.

### Biot-Sovart & Ampere
If we know where all the currents are, (and they are steady currents), we can use the Biot-Sovart Law to calculate the magnetic field $\vec{B}$.

In general:
$$\vec{B}=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\left(I\ d\vec{l}\right)\times\hat{r}}{r^2}$$
For surface currents:
$$\vec{B}=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{K}\times\hat{r}}{r^2}\ dA$$
For volume currents:
$$\vec{B}=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{J}\times\hat{r}}{r^2}\ d\tau$$
In principle, this is our solution for a known distribution of steady currents.
Can be onerous to actually compute (use a computer lol).

An alternative would be something like Ampere's Law. If we have sufficient symmetry in the current distribution, it is much simpler to compute.
$$\begin{align}
\nabla\times \vec{B}&=\mu_0\vec{J} & \oint\vec{B}\cdot d\vec{l} &= \mu_0I & \text{(Ampere's Law)}
\end{align}$$
If we can choose a path where $\vec B$ is parallel or perpendicular at every point on a path and $B$ is uniform everywhere that $\vec{B}\parallel d\vec{l}$.
It technically holds true in most cases, but isn't always so useful for calculating things.

### Vector Potential
Since $\vec{B}$ is divergence-less $\left(\vec\nabla\cdot\vec{B}=0\right)$, we can write it as the curl of a vector $\vec{A}$.
$$\vec\nabla\times\vec{A}=\vec{B}$$
For a scalar potential, we can always add a constant term without effecting the field.
For a vector potential, we can add the gradient of an arbitrary scalar function $\phi$.
$$\vec\nabla\times\vec{A} = \vec\nabla\times\left(\vec{A}+\vec\nabla\phi\right)$$
This flexibility is called *gauge symmetry*. We'll return to this later in the semester.
In statics, we typically use the *coulomb gauge*, defined as $\vec\nabla\cdot\vec{A}=0$.
This is identical to saying that $\vec\nabla^2\phi = 0$, which looks very familiar...

If we can get $\vec{A}$, then we can find $\vec{B}$ from $\vec\nabla\times\vec{A}=\vec{B}$.

### Finding Vector Potential
Example 1:
$$\begin{align}
\int\vec{B}\cdot d\vec{A}&=\int\left(\vec\nabla\times\vec{A}\right)\cdot d\vec{A}\\
\Aboxed{\int\vec{B}\cdot d\vec{A}&=\oint\vec{A}\cdot d\vec{l}}
\end{align}$$
Example 2:
$$\begin{align}
& \vec\nabla\times\vec{B} = \vec\nabla\times\left(\vec\nabla\times\vec{A}\right)
\end{align}$$
$$\vec{A}=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}}{r}d\tau$$

