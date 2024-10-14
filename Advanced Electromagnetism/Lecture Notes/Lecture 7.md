**Name:** Stanley Goodwin
**Date:** 9/17/2024

---

In dynamics, we can no longer define $\vec E$ as a gradient of a scalar function $\phi$.
Path integrals are no longer path-independent.

We can still define $\Delta V=-\displaystyle\int_\gamma\vec{E}\cdot d\vec{l}$, but is it entirely path-dependent.
### Inductance
Suppose we have 2 loops. There's a current $I$ flowing in loop 1.
Current flows in loop 1 which creates magnetic fields over all space.
That means there's magnetic flux on loop 2.
If I change the current in loop 1, there will be a time-varying flux in loop 2.
This implies there's an induced EMF in loop 2.

In principle, we can do it with Biot-Sovart.
 - Start with $\vec B_1(\vec{r})=\dfrac{\mu_0}{4\pi}\displaystyle\oint\dfrac{(I_1 d\vec{l}_1)\times\hat{r}}{r^2}$.
 - This only works with a very gently-changing magnetic field (quasi-static field).
 - The integral can be a pain, but is , in principle, solvable.

For calculating flux, we find the $\Phi_2=\displaystyle\iint\vec{B}_1\cdot d\vec{A}_2=M_{21}I_1$.
$$\vec{E}_2=-\dfrac{d\Phi_2}{dt}=-\dfrac{d(M_{21}I_1)}{dt}=-M_{21}\dfrac{dI_1}{dt}$$
$$\begin{align}
M_{21}&=\iint_\text{loop 2}\dfrac{\vec{B}_1\cdot d\vec{A}_2}{I_1}\\
&=\dfrac{\mu_0}{4\pi}\iint_\text{loop 2}\displaystyle\oint_\text{loop 1}\dfrac{d\vec{l}_1\times\hat{r}}{r^2}\cdot d\vec{A}_2\\
&=\dfrac{\mu_0}{4\pi}\oint_\text{loop 2}\displaystyle\oint_\text{loop 1}\dfrac{d\vec{l}_1\cdot d\vec{l}_2}{r}\\
\end{align}$$
In this form, it's easy to see that $M_{21}=M_{12}$, so there is *mutual induction* between the wires.
 - This often means we can solve an easier problem as a substitute for a harder one.



#### Example: Infinite Solenoid
Solenoid, $n$ turns per unit length, $4R$ radius.
In the center of the solenoid, a loop of radius $R$ in the plane normal to the solenoid axis.
If I run a current $I(t)=I_0+\alpha t$ in the little loop, what's the EMF of the solenoid?

This would be a pain if we first calculated $\vec B$ of the little loop and then integrate over the solenoid.
Instead, lets run the current in the solenoid and find the flux through the little loop.

$\vec{B}_\text{solenoid}=\mu_0nI$, $\vec{A}_\text{loop}=\pi R^2$, so $\Phi_\text{loop}=\mu_0nI\pi R^2$.
$\implies M_{21}=\dfrac{\Phi_\text{loop}}{I} = \mu_0n\pi R^2$
$\implies |\vec{E}|=-M_{21}\dfrac{dI}{dt} =-\mu_0n\pi R^2\alpha$.


### Self-Inductance
$$\Phi_1=M_{11}I_1$$
$$|\vec E_1|=-\dfrac{d\Phi_1}{dt}=-L\dfrac{dI_1}{dt}$$



### Energy in $\vec{B}$-Fields
$$\begin{align}
P&=\dfrac{dW}{dt}\\
&=\Delta V\cdot I\\
P &= L\cdot I\dfrac{dI}{dt}
\end{align}$$
$$\begin{align}
W &= \int P \ dt\\
&=\int L\cdot I\dfrac{dI}{dt} dt\\
\Aboxed{W&=\dfrac{1}{2}LI^2}
\end{align}$$
Recall for a capacitor: $W=\dfrac{1}{2}\dfrac{Q^2}{C}$.
Stored energy in the inductor, even though $\vec B$ doesn't do work.
 - We varied the current in the inductor, and time-varying $\vec{B}$ means that $\vec E$ is involved.

We looked at the energy stored in an inductor. Let's think more generally.
$$\begin{align}
W &= \dfrac{1}{2}LI^2\\
&= \dfrac{1}{2}I(LI)\\
&= \dfrac{1}{2}I\Phi_B\\
&= \dfrac{1}{2}\iint\vec{A}\cdot Id\vec{l}\\
&= \dfrac{1}{2}\iiint\left(\vec{A}\cdot\vec{J}\right)d\tau\\
&= \dfrac{1}{2\mu_0}\iiint \vec{A}\cdot\left(\vec\nabla\times\vec{B}\right)\ d\tau\\
&= \dfrac{1}{2\mu_0}\iiint \left(B^2-\vec\nabla\cdot\left(\vec{A}\times \vec{B}\right)\right)\ d\tau\\
&= \dfrac{1}{2\mu_0}\iiint B^2\ d\tau-\dfrac{1}{2\mu_0}\iiint \vec\nabla\cdot\left(\vec{A}\times \vec{B}\right)\ d\tau\\
&= \dfrac{1}{2\mu_0}\iiint B^2\ d\tau-\dfrac{1}{2\mu_0}\oint \vec{A}\times \vec{B}\ dA\\
\mathcal{W}_B&=\dfrac{1}{2\mu_0}B^2
\end{align}$$
Compare this to the energy stored by the electric field:
$$\mathcal{W}_E=\dfrac{1}{2}\epsilon_0E^2$$
Both electric and magnetic fields store energy per unit volume.
$$\begin{align}
\mathcal{W}_{EM}&=\dfrac{1}{2}\left(\epsilon_0E^2+\dfrac{1}{\mu_0}B^2\right)\\
&=\dfrac{1}{2\epsilon_0}\left(E^2+\dfrac{1}{\epsilon_0\mu_0}B^2\right)\\
\Aboxed{\mathcal{W}_{EM}&=\dfrac{1}{2\epsilon_0}\left(E^2+(cB)^2\right)}\\
\Aboxed{\mathcal{W}_{EM}&=\dfrac{1}{2\epsilon_0}\left(E^2-(icB)^2\right)}
\end{align}$$

Extras: Define $F=E+icB$.
$$\begin{align}
\mathcal{W}_{EM}&=\dfrac{1}{2\epsilon_0}\left(E+icB\right)\left(E-icB\right)\\
\Aboxed{\mathcal{W}_{EM}&=\dfrac{1}{2\epsilon_0}F^\dagger F}
\end{align}$$
