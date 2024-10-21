**Name:** Stanley Goodwin
**Date:** XX/XX/2024
**Collaborators:** None
**Time Taken:** XXX Hours

---
## Question 1
Let’s look at the coax again, but this time with the current constant in time. Like last week, the coax has a small central wire $(a\ll b)$ and a *thin* outer shell $(c-b\ll b)$. Constant current $I$ flows in the $+z$ direction on the inner wire and total current $I$ flows in the opposite direction in the outer shell. Assume that the coax cable (wire plus shell) is net neutral, and neglect fringe fields. 
**Note:** There is a constant voltage difference $V_0$ between the wire and the shell (see the figure).
### 1.A
*Find the electric and magnetic fields $\vec{E}(s)$ and $\vec{B}(s)$ in the “coax region” $a<s<b$, where $s$ is the usual radial coordinate.* 
$$\begin{align}
\oint\vec{E}(s)\cdot d\vec{A}&=\dfrac{q_\text{enc}}{\epsilon_0}\\
\vec{E}(s)\cdot2\pi s&=\dfrac{CV}{\epsilon_0}\hat{s}\\
\vec{E}(s)&=\dfrac{2\pi\epsilon_0V}{2\pi s\epsilon_0\ln(b/a)}\hat{s}\\
\Aboxed{\vec{E}(s)&=\dfrac{V}{\ln(b/a)}\dfrac{1}{s}\hat{s}}
\end{align}$$
$$\begin{align}
\oint\vec{B}(s)\cdot d\vec{l}&=\mu_0I\\
\Aboxed{\vec{B}(s)&=\dfrac{\mu_0I}{2\pi s}\hat\phi, \ \ \ a<s<b}
\end{align}$$
### 1.B
*Calculate the Poynting vector $\vec{S}(s)$ in the coax region.* The magnitude of $\vec{S}$ gives the energy flux density and represents the power per area moving through space. *Does its direction make sense for the coax?*
$$\begin{align}
\vec{S}(s)&=\dfrac{\vec{E}(s)\times\vec{B}(s)}{\mu_0}\\
&=\dfrac{\vec{E}(s)\times\vec{B}(s)}{\mu_0}\\
&=\dfrac{V}{\ln(b/a)}\dfrac{1}{s}\hat{s}\times\dfrac{I}{2\pi s}\hat\phi\\
&=\left(\dfrac{V}{\ln(b/a)}\dfrac{1}{s}\dfrac{I}{2\pi s}\right)\hat{s}\times\hat\phi\\
&=\dfrac{1}{2\ln(b/a)}\dfrac{IV}{\pi s^2}\hat{z}\\
\Aboxed{\vec{S}(s)&=\dfrac{1}{2\ln(b/a)}\dfrac{P}{A}\hat{z}}\\
\Aboxed{|\vec{S}(s)|&=\dfrac{1}{2\ln(b/a)}\dfrac{P}{A}}
\end{align}$$
Looks like I got the right expression, since it's some factor of power over area. The directional also makes sense since it means that power is traveling in the direction of current flow.
### 1.C
Integrate this flux through the cross-sectional area of the coax to find the power transported down the coax line (be clear/careful about what your "$d\vec{A}$" element is). Does your answer make sense relative to the circuit maintaining the current and voltage? Briefly comment.
$$\begin{align}
\int\vec{S}(s)\cdot d\vec{A}&=\int\dfrac{1}{2\ln(b/a)}\dfrac{IV}{\pi s^2}\hat{z}\cdot dA\ \hat{z}\\
&=\int_0^{2\pi}\int_a^b\dfrac{1}{2\ln(b/a)}\dfrac{IV}{\pi s^2}\hat{z}\cdot sdsd\phi\ \hat{z}\\
&=\dfrac{2\pi IV}{2\pi\ln(b/a)}\int_a^b\dfrac{1}{s^2}\cdot sds\\
&=\dfrac{2\pi IV}{2\pi\ln(b/a)}\cdot\ln\left|s\right|_a^b\\
&=\dfrac{2\pi\ln(b/a)}{2\pi\ln(b/a)}IV\\
\Aboxed{\int\vec{S}(s)\cdot d\vec{A}&=IV=P}
\end{align}$$
This completely adds up, since the total power the circuit would be running with the fields that are within the coaxial region. It looks as if the Power in the circuit is the Poynting Vector Flux.

---
## Question 2
A capacitor with circular plates of radius $R$ separated by distance $d\ll R$ is being charged by a steady current $I$. The plates are sufficiently close that fringe effects can be ignored. Assume that at $t=0$, the plate is uncharged.
### 2.A
In class we did an activity (this was Worksheet 11) to compute the magnitude of the magnetic field between the plates at all distances $s$ from the center of the plates (for both $s<R$ and $s>R$). Reconstruct that argument (show me your work) and then use it to compute the Poynting vector $\vec{S}$ (magnitude and direction) on the rim of the capacitor, between the plates, at $s=R$ (the "rim" is the ribbon of area at $s=R$ between the plates; see the diagram). Express your answer in terms of given quantities only.

### 2.B
Compute the stored energy $U$ in the capacitor as function of time in terms of given quantities. Then show that the rate at which the capacitor's stored energy is increasing $(dU/dt)$ is equal to the rate at which field energy is entering through the rim. Comment on the sign conventions you used, and the basic physics— what is going on here?

---
## Question 3
Consider a very long solenoid of length $L$, radius $R$, and turns per length $n$. The current $I$ in the solenoid is linearly ramped from $I=0$ to $I=I_0$ over a period $t_0$ as shown in the graph. Assume as usual the “quasistatic” approximation—the ramping is gentle enough that we can ignore the displacement current’s contribution to the magnetic field.
### 3.A
Integrate the magnetic field energy density to derive a formula for the total field energy
stored in the solenoid at times $t>t_0$.
### 3.B
Solve for the electric field everywhere in space at times $0<t<t_0$
### 3.C
Solve for the Poynting vector $\vec{S}$ (direction and magnitude) at $s=R$ (just inside the walls
of the solenoid) as a function of time $t$.
### 3.D
Show that the integral from $t=0$ to $t=t_0$ of the total power entering at the surface of the solenoid is equal to the total energy stored in the solenoid you calculated in part a.

---
## Question 4
Consider the electric field $\vec{E}(x,y,z,t)=E_0\cos\left(k(x-ct)\right)\hat{y}$, where $k$ and $c$ are constants.
### 3.A
*What is the charge density $\rho(x,y,z)$ required to produce such a field?*
*And what are the units of $k$ and $c$?*
$$\begin{align}
\vec\nabla\cdot\vec{E}(x,y,z,t)&=\dfrac{\rho(x,y,z)}{\epsilon_0}\\
\dfrac{\partial}{\partial x}\vec{E}_x(x,y,z,t)&=\dfrac{\rho(x,y,z)}{\epsilon_0}\\
0&=\dfrac{\rho(x,y,z)}{\epsilon_0}\\
\Aboxed{\rho(x,y,z)&=0}
\end{align}$$
The units of $k$ are $\dfrac{1}{\text{m}}$ and the units of $c$ are $\dfrac{\text{m}}{\text{s}}$ in SI units.
### 3.B
Come up with the simplest possible $\vec{B}$-field that satisfies Faraday’s Law for this $\vec{E}$ . Then check that all of the remaining free space (i.e. no charge and no current) Maxwell’s Equations are satisfied by these fields, if you make the right choice for the constant 𝑐. What does 𝑐 need to be equal to? And what is the amplitude of the $\vec{B}$-field?
$$\begin{align}
\oint\vec{B}\cdot d\vec{l}&=\mu_0I+\epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}\\
&=0+\epsilon_0\mu_0\dfrac{d}{dt}\int E_0\cos\left(k(x-ct)\right)\hat{y}\cdot d\vec{A}\\
&=\epsilon_0\mu_0\dfrac{d}{dt}E_0A\cos\left(k(x-ct)\right)\\
&=-\epsilon_0\mu_0E_0A\sin\left(k(x-ct)\right)\left(k(-c)\right)\\
\vec{B}(x,y,z,t)&=\dfrac{\epsilon_0\mu_0E_0Akc}{2\pi\sqrt{x^2+z^2}}\sin\left(k(x-ct)\right)\hat\phi\\
\end{align}$$
### 3.C
What is the Poynting Vector $\vec{S}$ associated with these fields?
#### 3.C.I
What is the energy density at any point in space, $\mathcal{U}_\text{EM}(x,y,z,t)$?
How is it related to $|\vec{S}|$?
#### 3.C.II
Describe in words what this $\vec{E}$ and $\vec{B}$ field look like.
Can you “interpret” them physically? What does the constant “k” tell you?
