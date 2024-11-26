**Name:** Stanley Goodwin
**Date:** 11/26/2024

---
### Electric Dipole Radiation
For an oscillating electric dipole at the origin, the Poynting vector far away from the origin was:
$$\vec{S}(r,t)=\dfrac{\mu_0}{c(4\pi)^2}\left(\dfrac{p_0\omega}{r}\right)^2\sin^2\theta\cos^2\left(\omega(t-r/c)\right)\hat{r}$$
$$\langle P_\text{total}\rangle=\dfrac{\mu_0p_0^2\omega^4}{12\pi c}$$
Where $p_0$ is the magnitude of the dipole moment.
Radiation fields come from accelerating charges.

Since power must be conserved, there must be energy added to the dipole to keep it oscillating.
There is a "radiation reaction force" on the charges of the dipole arising from the Electromagnetic Field. We must work against this force in order to sustain dipole oscillation.

The Poynting vector has an angular dependence, where the $P\propto\sin^2\theta$, so that no power flows to the poles of the dipole.

Electrical Engineers talk about an effective radiation resistance:
$$R_\text{rad}=\dfrac{\langle P_\text{radiation}\rangle}{I^2_\text{rms}}$$
This is the equivalent resistance that would dissipate the same energy as the dipole.
For us, we used $I(t)=-q_0\omega\sin\left(\omega t\right)$, $I_\text{rms}^2=\dfrac{q_0^2\omega^2}{2}$.
$$\begin{align}
R_\text{rad}
&=\dfrac{\langle P_\text{radiation}\rangle}{I^2_\text{rms}}\\
&=\dfrac{\tfrac{\mu_0p_0^2\omega^4}{12\pi c}}{\tfrac{q_0^2\omega^2}{2}}\\
&=\dfrac{\mu_0q_0^2d^2\omega^2}{6\pi cq_0^2}\\
&=\dfrac{\mu_0ck^2d^2}{6\pi}\\
&=\sqrt{\dfrac{\mu_0}{\epsilon_0}}\dfrac{(kd)^2}{6\pi}\\
\Aboxed{R_\text{rad}&\approx377\ \Omega}
\end{align}$$
This is the impedance of free space.

If we want to make a proper antenna, we would superpose a bunch of dipoles.
Real antennas typically have $d=\lambda/2$ or $d=\lambda/4$, but our approximations break down there.

For our result, we can see that $P\propto\omega^4\implies P\propto1/\lambda^4$. Higher frequencies radiate more power.

This $\omega$ dependence is (partly) responsible for the blue sky. Incoming white light, light of all visible angular frequencies, excite molecules in the sky, making oscillating dipoles. These dipoles re-radiate in a process we call *scattering*, and we get lots more power from higher frequencies.

Also, due to the $\sin^2\theta$ factor, most light reaching you through scattering will carry a particular electromagnetic polarization state.

**For a singular charge:**
$$P=\dfrac{\mu_0}{6\pi c}q^2\vec{a}^2$$
Where $\vec{a}$ is the acceleration of the charge.

If the charges are moving very fast (relative to $c$), we'll need relativistic corrections.

### Special Relativity
Follows from two simple postulates:
 - The laws of physics should be the same in all *inertial reference frames*.
 - The speed of light, in all inertial reference frames, is *homogenous*.
*Inertial reference frames:* Frames where Newton's 1st law of motion is satisfied.
#### Lorentz Transformation
Say an event happens at $(\vec{x},t)$ in frame $S$, and $(\vec{x}',t')$ observed in frame $S'$.

In Galilean Relativity, we can transform between the frames with:
$$\begin{align}
x'&=x-v_xt&y'&=y-v_yt&z'&=z-v_zt&t'&=t
\end{align}$$
Unfortunately, this is incorrect for our universe, even though it is common sense.

In Lorentzian Relativity, we can transform start with a general equation:
$$\begin{align}
x'&=ax+bt&t'&=cx+dt
\end{align}$$
First off, the origin of $x'$ moves at speed $v$ in frame $S$, which means if $x'=0$, then $x=vt$.
$$\begin{align}
x'&=ax+bt\\
0&=avt+bt\\
b&=-av\\
\Aboxed{x'&=a(x-vt)}
\end{align}$$
Einstein's First Postulate says there is no preferred frame of reference.
In other words, the transform $(x,t)\iff(x',t')$ should give the same physics.
$$\begin{align}
\Aboxed{x&=a(x'+vt)}
\end{align}$$
Einstein's First Postulate says the speed of light is homogenous in a vacuum.
Effectively, both $S$ and $S'$ must see the speed of light be $c$. I.e. $x=ct$ and $x'=ct'$.
$$\begin{align}
x'&=a(x-vt)\\
ct'&=a(ct-vt)\\
ct'&=a(c-v)t\\
\\
x&=a(x'+vt')\\
ct&=a(ct'+vt')\\
ct&=a(c+v)t'\\
\\
c^2tt'&=a^2(c-v)(c+v)tt'\\
a^2&=\dfrac{c^2}{c^2-v^2}\\
a&=\dfrac{1}{\sqrt{1-v^2/c^2}}
\end{align}$$
This is the Lorentz Factor $\gamma(v)$ for time dilation and length contraction.

The complete Lorentz Transformation is then:
$$\begin{align}
x'&=\gamma(v)(x-vt)=\dfrac{x-vt}{\sqrt{1-v^2/c^2}}\\
t'&=\gamma(v)\left(t-\tfrac{v}{c^2}x\right)=\dfrac{t-\tfrac{v}{c^2}x}{\sqrt{1-v^2/c^2}}\\
\end{align}$$
