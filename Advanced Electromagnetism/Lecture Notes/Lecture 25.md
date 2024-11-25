**Name:** Stanley Goodwin
**Date:** 11/21/2024

---
### Radiation
Last time, we saw how time-dependent $I(t)$ gave us an EM wave propagating outwards.
Time-varying charge distributions produce traveling EM waves.
In terms of energy flow, Poynting tells us that the EM power flowing "out to $\infty$":
$$\text{Power}=\oint\dfrac{\vec{E}\times\vec{B}}{\mu_0}\cdot d\vec{A}$$
In cases that $\vec{E}\times\vec{B}$ dies faster than surface area increases, there's no radiation at infinity.
An acceleration of charge is required to get radiation at some point out at infinity.
### Electric Dipole Radiation
The electric dipole moment is written as $\vec{p}=q\vec{d}$, but now $q$ is going to be an oscillating function in time, such that $q(t)=q_0(t)\cos(\omega t)$.
Lets consider the "flow" of how charges move, I.e. the current $I$:
$$I\hat{z}=\dfrac{dq}{dt}\hat{z}=\dfrac{\dot{\vec{p}}}{d}$$
Which can then be written as:
$$I\hat{z}=-q_0(t)\omega\sin(\omega t)\hat{z}$$
To find the voltage, we'll have to use the multipole expansion:
$$V(\vec{r})\approx\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{Q}{r}+\dfrac{\text{dipole}}{r^2}+\dfrac{\text{quadrupole}}{r^3}+\dots\right]$$
Or a more exact form in terms of a series:
$$V(\vec{r})\approx\dfrac{1}{4\pi\epsilon_0}\dfrac{1}{r}\sum_{n=0}^\infty\left(\dfrac{r'}{r}\right)^nP_n(\cos\theta_{r,r'})$$
### Power Flow
The total power of the system can be written as the following:
$$P=\oint\vec{S}\cdot d\vec{A}=\oint\dfrac{\vec{E}\times\vec{B}}{\mu_0}\cdot d\vec{A}$$
Integrating over a sphere, we can find the following power relationship:
$$\langle P_\text{total}\rangle=\dfrac{\mu_0p_0^2\omega^4}{12\pi c}$$
