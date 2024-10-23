**Name:** Stanley Goodwin
**Date:** 10/22/2024
**Collaborators:** Chris, Hasan
**Time Taken:** 6 Hours

---
## Question 1
Let’s look at the coax again, but this time with the current constant in time. Like last week, the coax has a small central wire $(a\ll b)$ and a *thin* outer shell $(c-b\ll b)$. Constant current $I$ flows in the $+z$ direction on the inner wire and total current $I$ flows in the opposite direction in the outer shell. Assume that the coax cable (wire plus shell) is net neutral, and neglect fringe fields. 
**Note:** There is a constant voltage difference $V_0$ between the wire and the shell (see the figure).
### 1.A
*Find the electric and magnetic fields $\vec{E}(s)$ and $\vec{B}(s)$ in the “coax region” $a<s<b$, where $s$ is the usual radial coordinate.*
$$\begin{align}
\oint\vec{E}(s)\cdot d\vec{A}&=\dfrac{q_\text{enc}}{\epsilon_0}\\
E(s)\cdot2\pi s&=\dfrac{CV}{\epsilon_0}\\
E(s)&=\dfrac{2\pi\epsilon_0}{\ln(b/a)}\dfrac{V}{2\pi s\epsilon_0}\\
\Aboxed{\vec{E}(s)&=\dfrac{V}{\ln(b/a)}\dfrac{1}{s}\hat{s}, \ \ \ a<s<b}
\end{align}$$
$$\begin{align}
\oint\vec{B}(s)\cdot d\vec{l}&=\mu_0I\\
B(s)\cdot 2\pi s&=\mu_0I\\
\Aboxed{\vec{B}(s)&=\dfrac{\mu_0I}{2\pi s}\hat\phi, \ \ \ a<s<b}
\end{align}$$
### 1.B
*Calculate the Poynting vector $\vec{S}(s)$ in the coax region.* The magnitude of $\vec{S}$ gives the energy flux density and represents the power per area moving through space. *Does its direction make sense for the coax?*
$$\begin{align}
\vec{S}(s)&=\dfrac{\vec{E}(s)\times\vec{B}(s)}{\mu_0}\\
&=\dfrac{V}{\ln(b/a)}\dfrac{1}{s}\hat{s}\times\dfrac{I}{2\pi s}\hat\phi\\
&=\left(\dfrac{V}{\ln(b/a)}\dfrac{1}{s}\dfrac{I}{2\pi s}\right)\hat{s}\times\hat\phi\\
&=\dfrac{1}{2\ln(b/a)}\dfrac{IV}{\pi s^2}\hat{z}\\
\Aboxed{\vec{S}(s)&=\dfrac{1}{2\ln(b/a)}\dfrac{IV}{\pi s^2}\hat{z}}\\
\end{align}$$
Looks like I got the right expression, since it's some factor of power over area. The directional also makes sense since it means that power is traveling in the direction of current flow, which is expected for DC current.
### 1.C
*Integrate this flux through the cross-sectional area of the coax to find the power transported down the coax line* (be clear/careful about what your "$d\vec{A}$" element is). *Does your answer make sense relative to the circuit maintaining the current and voltage? Briefly comment.*
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
$$\begin{align}
\oint\vec{B}\cdot d\vec{l}&=\mu_0I+\epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}\\
B\cdot 2\pi s&=\mu_00+\epsilon_0\mu_0\dfrac{d}{dt}\left(E\pi s^2\right)\\
B&=\dfrac{\epsilon_0\mu_0\pi s^2}{2\pi s}\dfrac{dE}{dt}\\
B&=\dfrac{\epsilon_0\mu_0\pi s^2}{2\pi s}\dfrac{I}{\epsilon_0\pi R^2}\\
\Aboxed{\vec{B}&=\dfrac{\mu_0Is}{2\pi R^2}\hat\phi, \ \ \ s<R}
\end{align}$$
$$\begin{align}
\oint\vec{B}\cdot d\vec{l}&=\mu_0I+\epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A}\\
B\cdot 2\pi s&=\mu_00+\epsilon_0\mu_0\dfrac{d}{dt}\left(E\pi R^2\right)\\
B&=\dfrac{\epsilon_0\mu_0\pi R^2}{2\pi s}\dfrac{dE}{dt}\\
B&=\dfrac{\epsilon_0\mu_0\pi R^2}{2\pi s}\dfrac{I}{\epsilon_0\pi R^2}\\
\Aboxed{\vec{B}&=\dfrac{\mu_0I}{2\pi s}\hat\phi, \ \ \ s>R}
\end{align}$$
$$\begin{align}
\vec{B}&=\begin{cases}
\dfrac{\mu_0Is}{2\pi R^2}\hat\phi, & s<R\\
\dfrac{\mu_0I}{2\pi s}\hat\phi, & s>R\\
\end{cases}
\end{align}$$
We can then calculate the Poynting Vector:
$$\begin{align}
\vec{S}&=\dfrac{\tfrac{Q(t)\pi R^2}{\epsilon_0}\hat{z}\times\dfrac{\mu_0Is}{2\pi R^2}\hat\phi}{\mu_0}\\
&=\dfrac{Q(t)\pi R^2\mu_0Is\cdot \hat{z}\times\hat\phi}{2\pi R^2\mu_0\epsilon_0}\\
&=\dfrac{Q(t)I(t)R}{2\epsilon_0}\hat{s}\\
&=\dfrac{I^2Rt}{2\epsilon_0}\hat{s}\\
\Aboxed{\vec{S}&=\dfrac{I^2Rt}{2\epsilon_0}\hat{s}}
\end{align}$$
### 2.B
Compute the stored energy $U$ in the capacitor as function of time in terms of given quantities. Then show that the rate at which the capacitor's stored energy is increasing $(dU/dt)$ is equal to the rate at which field energy is entering through the rim. Comment on the sign conventions you used, and the basic physics— what is going on here?
$$\begin{align}
U(t)&=\dfrac{1}{2}\dfrac{Q^2}{C}\\
\Aboxed{U(t)&=\dfrac{1}{2}\dfrac{I^2t^2d}{\epsilon_0\pi R^2}}\\
\dfrac{\partial U(t)}{\partial t}&=\dfrac{\partial}{\partial t}\left(\dfrac{1}{2}\dfrac{I^2t^2d}{\epsilon_0\pi R^2}\right)\\
&=\dfrac{1}{2}\dfrac{I^2d}{\epsilon_0\pi R^2}\dfrac{\partial}{\partial t}\left(t^2\right)\\
\Aboxed{U'(t)&=\dfrac{I^2d}{\epsilon_0\pi R^2}t}
\end{align}$$
The rate of change is positive since we're looking from the perspective of the capacitor, which is gaining energy. However, since the energy flows inward, it would be a negative value for the source of the energy, like the battery.

---
## Question 3
Consider a very long solenoid of length $L$, radius $R$, and turns per length $n$. The current $I$ in the solenoid is linearly ramped from $I=0$ to $I=I_0$ over a period $t_0$ as shown in the graph. Assume as usual the “quasistatic” approximation—the ramping is gentle enough that we can ignore the displacement current’s contribution to the magnetic field.
### 3.A
Integrate the magnetic field energy density to derive a formula for the total field energy
stored in the solenoid at times $t>t_0$.
$$\begin{align}
\int\mathcal{U}_\text{B}\ d\tau&=\int\dfrac{B^2}{2\mu_0}\ d\tau\\
&=\int\dfrac{(\mu_0nI)^2}{2\mu_0}\ d\tau\\
&=\dfrac{\mu_0n^2}{2}I^2(t)\int d\tau\\
&=\dfrac{\mu_0n^2}{2}I^2(t)\cdot\pi R^2L\\
&=\dfrac{\mu_0\pi R^2Ln^2}{2}I^2(t)\\
\Aboxed{U(t)&=\dfrac{\mu_0\pi R^2Ln^2I^2}{2t_0^2}t^2}
\end{align}$$
### 3.B
Solve for the electric field everywhere in space at times $0<t<t_0$.
Region $s<R$:
$$\begin{align}
\oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}\\
E\cdot2\pi s&=-\dfrac{d}{dt}\left(B\cdot\pi s^2\right)\\
E&=-\dfrac{\pi s^2}{2\pi s}\dfrac{dB}{dt}\\
E&=-\dfrac{\mu_0 ns}{2}\dfrac{dI}{dt}\\
\Aboxed{\vec{E}&=-\dfrac{\mu_0 ns}{2}\dfrac{I_0}{t_0}\hat\phi}
\end{align}$$
Region $s>R$:
$$\begin{align}
\oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}\\
E\cdot2\pi s&=-\dfrac{d}{dt}\left(B\cdot\pi R^2\right)\\
E&=-\dfrac{\pi R^2}{2\pi s}\dfrac{dB}{dt}\\
E&=-\dfrac{\mu_0 nR^2}{2s}\dfrac{dI}{dt}\\
\Aboxed{\vec{E}&=-\dfrac{\mu_0 nR^2}{2s}\dfrac{I_0}{t_0}\hat\phi}
\end{align}$$
$$\begin{align}
\vec{E}(t)&=\begin{cases}
-\dfrac{\mu_0 ns}{2}\dfrac{I_0}{t_0}\hat\phi, & s<R\\
-\dfrac{\mu_0 nR^2}{2s}\dfrac{I_0}{t_0}\hat\phi, & s>R\\
\end{cases}
\end{align}$$
### 3.C
Solve for the Poynting vector $\vec{S}$ (direction and magnitude) at $s=R$ (just inside the walls
of the solenoid) as a function of time $t$.
$$\begin{align}
\vec{S}&=\dfrac{-\dfrac{\mu_0 ns}{2}\dfrac{I_0}{t_0}\hat\phi\times\mu_0nI\hat{z}}{\mu_0}\\
\vec{S}&=\dfrac{-\mu_0n^2I_0^2R}{2t_0^2}t\cdot\hat\phi\times\hat{z}\\
\Aboxed{\vec{S}&=\dfrac{-\mu_0n^2I_0^2R}{2t_0^2}t\cdot\hat{s}}
\end{align}$$
The Poynting Vector points inward toward the center of the solenoid.
### 3.D
Show that the integral from $t=0$ to $t=t_0$ of the total power entering at the surface of the solenoid is equal to the total energy stored in the solenoid you calculated in part a.
$$\begin{align}
\iint\vec{S}\cdot d\vec{A}\ dt&=\pi R^2\int_0^{t_0}|\vec{S}|\ dt\\
&=-\pi R^2\int_0^{t_0}\dfrac{\mu_0n^2I_0^2R}{2t_0^2}t\ dt\\
&=-\dfrac{\pi\mu_0n^2I_0^2R^3}{2t_0^2}\dfrac{t_0^2}{2}\\
\Aboxed{U&=-\dfrac{\mu_0n^2I_0^2\pi R^3}{4}}
\end{align}$$

---
## Question 4
Consider the electric field $\vec{E}(x,y,z,t)=E_0\cos\left(k(x-ct)\right)\hat{y}$, where $k$ and $c$ are constants.
### 4.A
*What is the charge density $\rho(x,y,z)$ required to produce such a field?*
*And what are the units of $k$ and $c$?*
$$\begin{align}
\vec\nabla\cdot\vec{E}(x,y,z,t)&=\dfrac{\rho(x,y,z)}{\epsilon_0}\\
\dfrac{\partial}{\partial x}\vec{E}_x(x,y,z,t)&=\dfrac{\rho(x,y,z)}{\epsilon_0}\\
0&=\dfrac{\rho(x,y,z)}{\epsilon_0}\\
\Aboxed{\rho(x,y,z)&=0}
\end{align}$$
The units of $k$ are $\dfrac{1}{\text{m}}$ and the units of $c$ are $\dfrac{\text{m}}{\text{s}}$ in SI units.
### 4.B
Come up with the simplest possible $\vec{B}$-field that satisfies Faraday’s Law for this $\vec{E}$ . Then check that all of the remaining free space (i.e. no charge and no current) Maxwell’s Equations are satisfied by these fields, if you make the right choice for the constant 𝑐. What does 𝑐 need to be equal to? And what is the amplitude of the $\vec{B}$-field?

Maxwell's Laws in Vacuum.
$$\begin{align}
\nabla\cdot\vec{E}&=0\\
\nabla\cdot\vec{B}&=0\\
\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}\\
\nabla\times\vec{B}&=\epsilon_0\mu_0\dfrac{\partial\vec{E}}{\partial t}
\end{align}$$
To find our $\vec{B}$, we have:
$$\begin{align}
\dfrac{\partial\vec{B}}{\partial t}&=-\nabla\times\vec{E}\\
\int_0^t\dfrac{\partial\vec{B}}{\partial t}\ dt&=-\int_0^t\nabla\times\vec{E}\ dt\\
\vec{B}-\vec{B}_0&=\int_0^tkE_0\sin\left(k(x-ct)\right)\hat{z}\ dt\\
&=-\dfrac{kE_0}{-kc}\cos\left(k(x-ct)\right|_0^t\hat{z}\\
\vec{B}-\vec{B}_0&=-\dfrac{kE_0}{-kc}\left(\cos(k(x-ct))-\cos(kx)\right)\hat{z}\\
\Aboxed{\vec{B}(x,y,z,t)&=\dfrac{E_0}{c}\cos(k(x-ct))\hat{z}}\\
\Aboxed{|B_0|&=\dfrac{E_0}{c}}
\end{align}$$
As for Maxwell's Laws:
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\partial E_x}{\partial x}+\dfrac{\partial E_y}{\partial y}+\dfrac{\partial E_z}{\partial z}\\
&=0+0+0\\
\Aboxed{\vec\nabla\cdot\vec{E}&=\rho(x,y,z)=0}
\end{align}$$
$$\begin{align}
\vec\nabla\cdot\vec{B}&=\dfrac{\partial B_x}{\partial x}+\dfrac{\partial B_y}{\partial y}+\dfrac{\partial B_z}{\partial z}\\
&=0+0+0\\
\Aboxed{\vec\nabla\cdot\vec{B}&=0}
\end{align}$$
$$\begin{align}
\vec\nabla\times\vec{E}
&=\dfrac{\partial}{\partial x}\left(E_0\cos\left(k(x-ct)\right)\right)\hat{z}\\
&=-kE_0\sin\left(k(x-ct)\right)\hat{z}\\
-\dfrac{\partial\vec{B}}{\partial t}
&=-\dfrac{\partial}{\partial t}\left(\dfrac{E_0}{c}\cos(k(x-ct))\hat{z}\right)\\
&=\dfrac{E_0}{c}\left(-kc\right)\sin(k(x-ct))\hat{z}\\
&=-kE_0\sin(k(x-ct))\hat{z}\\
\Aboxed{\vec\nabla\times\vec{E}&=-\dfrac{\partial\vec{B}}{\partial t}}
\end{align}$$
$$\begin{align}
\vec\nabla\times\vec{B}
&=-\dfrac{\partial}{\partial x}\left(\dfrac{E_0}{c}\cos(k(x-ct))\right)\hat{y}\\
&=\dfrac{E_0}{c}\left(k\right)\sin(k(x-ct))\hat{y}\\
&=\dfrac{kE_0}{c}\sin(k(x-ct))\hat{y}\\
\epsilon_0\mu_0\dfrac{\partial\vec{E}}{\partial t}
&=\epsilon_0\mu_0\dfrac{\partial}{\partial t}\left(E_0\cos\left(k(x-ct)\right)\hat{y}\right)\\
&=-\epsilon_0\mu_0E_0\left(-kc\right)\sin\left(k(x-ct)\right)\hat{y}\\
&=\epsilon_0\mu_0kcE_0\sin\left(k(x-ct)\right)\hat{y}\\
\Aboxed{\dfrac{kE_0}{c}\sin(k(x-ct))\hat{y}&=\epsilon_0\mu_0kcE_0\sin\left(k(x-ct)\right)\hat{y}}\\
kE_0\sin(k(x-ct))\hat{y}&=\epsilon_0\mu_0kc^2E_0\sin\left(k(x-ct)\right)\hat{y}\\
\dfrac{1}{\epsilon_0\mu_0}&=c^2\\
\end{align}$$
In order for our equations to be satisfied, we require that $c^2=(\epsilon_0\mu_0)^{-1}$.
### 4.C
What is the Poynting Vector $\vec{S}$ associated with these fields?
$$\begin{align}
\vec{E}(x,y,z,t)&=E_0\cos\left(k(x-ct)\right)\hat{y}\\
\vec{B}(x,y,z,t)&=\dfrac{E_0}{c}\cos(k(x-ct))\hat{z}\\
\vec{S}(x,y,z,t)
&=\dfrac{E_0\cos\left(k(x-ct)\right)\hat{y}\times\dfrac{E_0}{c}\cos(k(x-ct))\hat{z}}{\mu_0}\\
&=\dfrac{E_0^2\cos^2\left(k(x-ct)\right)\hat{y}\times\hat{z}}{c\mu_0}\\
\Aboxed{\vec{S}(x,y,z,t)&=\dfrac{E_0^2}{\mu_0c}\cos^2\left(k(x-ct)\right)\hat{x}}
\end{align}$$
#### 4.C.I
What is the energy density at any point in space, $\mathcal{U}_\text{EM}(x,y,z,t)$?
How is it related to $|\vec{S}|$?
$$\begin{align}
\vec{E}(x,y,z,t)&=E_0\cos\left(k(x-ct)\right)\hat{y}\\
\vec{B}(x,y,z,t)&=\dfrac{E_0}{c}\cos(k(x-ct))\hat{z}\\
\mathcal{U}_{EM}
&=\dfrac{1}{2}\left(\epsilon_0E^2+\dfrac{1}{\mu_0}B^2\right)\\
&=\dfrac{1}{2}\left(\epsilon_0E_0^2\cos^2\left(k(x-ct)\right)+\dfrac{1}{\mu_0}\dfrac{E_0^2}{c^2}\cos^2(k(x-ct))\right)\\
&=\dfrac{E_0^2}{2}\left(\epsilon_0+\dfrac{1}{\mu_0}\dfrac{1}{c^2}\right)\cos^2(k(x-ct))\\
&=\dfrac{E_0^2}{2\mu_0}\left(\mu_0\epsilon_0+\dfrac{1}{c^2}\right)\cos^2(k(x-ct))\\
&=\dfrac{E_0^2}{2\mu_0}\dfrac{2}{c^2}\cos^2(k(x-ct))\\
\Aboxed{\mathcal{U}_{EM}&=\dfrac{E_0^2}{\mu_0c^2}\cos^2(k(x-ct))}
\end{align}$$
It looks to me that they satisfy the relationship $\mathcal{U}_{EM}=\dfrac{|\vec{S}|}{c}$
#### 4.C.II
Describe in words what this $\vec{E}$ and $\vec{B}$ field look like.
Can you "interpret" them physically? What does the constant "k" tell you?

Both $\vec{E}$ and $\vec{B}$ are components of a plane wave, where the direction of propagation is normal to the plane spanned by these 2 vectors.
1-Dimensional waves that are orthogonal.

The constant $k$ refers to the spatial frequency, an so relate to the wavelength of the electromagnetic wave.

---
## Question 5
Two points on a string are observed as a traveling sinusoidal wave passes by. The points are at $x_1=0$ and $x_2=1$. The two points are known to be less than one wavelength apart. The transverse motions of the two points are observed to be:
$$\begin{align}
y_1&=0.2\cos(3\pi t) & y_2&=0.2\cos\left(3\pi t-\tfrac{\pi}{8}\right)
\end{align}$$
### 5.A
What is the frequency of this wave in hertz? What is the wavelength? What is the wave speed? Can you tell if this wave is moving to the right or to the left? If so, which way is it moving?

From observation, we can write the total wave as:
$$\begin{align}
\psi(x,t)=0.2\cos\left(\dfrac{\pi}{8}x-3\pi t\right)
\end{align}$$
Therefore, it has the characteristics of:
$$\begin{align}
\omega&=3\pi\tfrac{\text{rad}}{\text{s}}\\
\Aboxed{f&=1.5\text{ Hz}}\\
k&=\dfrac{\pi}{8}=\dfrac{2\pi}{16}\\
\Aboxed{\lambda&= 16\text{ m}}\\
c&=\lambda f\\
\Aboxed{c&=24\text{ m/s}}
\end{align}$$
The wave must be moving to the left, since the equation takes the form of $kx-\omega t$, and so the frequency of the wave drives the wave to the right.
### 5.B
In general, for any complex plane wave $\vec{E}=\vec{E}_0\exp\left(i\left(\vec{k}\cdot\vec{r}-\omega t\right)\right)$ (where $\vec{E}_0$ is a constant, independent of position and time, and $\vec{k}$ is also a given constant wave vector), prove that $\vec\nabla\times\vec{E}=i\vec{k}\times\vec{E}$.
$$\begin{align}
\vec{E}&=\vec{E}_0\exp\left(i\left(k_xx+k_yy+k_zz-\omega t\right)\right)\\
\vec\nabla\times\vec{E}&=\left|\begin{array}{}\hat{x}&\hat{y}&\hat{z}\\\partial_x&\partial_y&\partial_z\\E_x&E_y&E_z\end{array}\right|\\
&=\left(\dfrac{\partial E_z}{\partial y}-\dfrac{\partial E_y}{\partial z}\right)\hat{x}-\left(\dfrac{\partial E_z}{\partial x}-\dfrac{\partial E_x}{\partial z}\right)\hat{y}+\left(\dfrac{\partial E_y}{\partial x}-\dfrac{\partial E_x}{\partial y}\right)\hat{z}\\
&=\left(ik_yE_{z}-ik_zE_{y}\right)\hat{x}-\left(ik_xE_z-ik_zE_x\right)\hat{y}+\left(ik_xE_y-ik_yE_x\right)\hat{z}\\
&=i\left|\begin{array}{}\hat{x}&\hat{y}&\hat{z}\\k_x&k_y&k_z\\E_x&E_y&E_z\end{array}\right|\\
\Aboxed{\vec\nabla\times\vec{E}&=i\vec{k}\times\vec{E}}
\end{align}$$
Each $n$ differential results in a factor of $ik_n$, and so could have been done by inspection.
I believe that $\vec\nabla\cdot\vec{E}=i\vec{k}\cdot\vec{E}$ by similar means as above.

---
## Question 6
Use Griffiths formulas for the stress tensor in section 8.2.2 and write out the full 3x3 stress tensor for the traveling wave of problem 4. It’s surprisingly simple! Can you interpret the result physically? (Read the portion of Griffiths where he talks about “flow of momentum” as related to the stress tensor.)

$$\begin{align}
T_{xx}&=\dfrac{1}{2}\epsilon_0\left(E_x^2-E_y^2-E_z^2\right)+\dfrac{1}{2\mu_0}\left(B_x^2-B_y^2-B_z^2\right)\\
T_{xy}&=\epsilon_0\left(E_xE_y\right)+\dfrac{1}{\mu_0}\left(B_xB_y\right)\\
\end{align}$$
From question 4, we can see that:
$$\begin{align}
\vec{E}(x,y,z,t)&=E_0\cos\left(k(x-ct)\right)\hat{y}\\
\vec{B}(x,y,z,t)&=\dfrac{E_0}{c}\cos(k(x-ct))\hat{z}\\
\end{align}$$
So we have the following:
$$\begin{align}
E_x&=0& E_y&=E_0\cos\left(k(x-ct)\right) & E_z&=0\\
B_x&=0& B_y&=0 &B_z&=\dfrac{E_0}{c}\cos(k(x-ct))\\
\end{align}$$
And so:
$$\begin{align}
T_{xx}&=\dfrac{1}{2}\epsilon_0\left(E_x^2-E_y^2-E_z^2\right)+\dfrac{1}{2\mu_0}\left(B_x^2-B_y^2-B_z^2\right)\\
&=-\dfrac{1}{2}\epsilon_0E_0^2\cos^2\left(k(x-ct)\right)-\dfrac{1}
{2\mu_0}\dfrac{E_0^2}{c^2}\cos^2(k(x-ct))\\
T_{xx}&=-\epsilon_0E_0^2\cos^2\left(k(x-ct)\right)\\
T_{yy}&=\dfrac{1}{2}\epsilon_0\left(E_y^2-E_x^2-E_z^2\right)+\dfrac{1}{2\mu_0}\left(B_y^2-B_x^2-B_z^2\right)\\
&=\dfrac{1}{2}\epsilon_0E_0^2\cos^2\left(k(x-ct)\right)-\dfrac{1}{2\mu_0}\dfrac{E_0^2}{c^2}\cos^2(k(x-ct))\\
T_{yy}&=0\\
T_{zz}&=\dfrac{1}{2}\epsilon_0\left(E_z^2-E_x^2-E_y^2\right)+\dfrac{1}{2\mu_0}\left(B_z^2-B_x^2-B_y^2\right)\\
&=-\dfrac{1}{2}\epsilon_0E_0^2\cos^2\left(k(x-ct)\right)+\dfrac{1}{2\mu_0}\dfrac{E_0^2}{c^2}\cos^2(k(x-ct))\\
T_{zz}&=0\\
\end{align}$$
$$\begin{align}
T_{xy}&=\epsilon_0\left(E_xE_y\right)+\dfrac{1}{\mu_0}\left(B_xB_y\right)\\
T_{xy}&=T_{yx}=0\\
T_{yz}&=\epsilon_0\left(E_yE_z\right)+\dfrac{1}{\mu_0}\left(B_yB_z\right)\\
T_{yz}&=T_{zy}=0\\
T_{zx}&=\epsilon_0\left(E_zE_x\right)+\dfrac{1}{\mu_0}\left(B_zB_x\right)\\
T_{zx}&=T_{xz}=0\\
\end{align}$$
The matrix is a bunch of zeros, except for $T_{xx}=-\epsilon_0E_0^2\cos^2\left(k(x-ct)\right)$.



