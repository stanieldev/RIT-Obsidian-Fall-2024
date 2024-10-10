**Name:** Stanley Goodwin
**Date:** 9/22/2024 (Previously 9/18/2024)
**Collaborators:** None
**Time Taken:** 9 Hours over 2 days

---
## Question 1
### 1.A
*A homopolar generator: What Michael Faraday came up with a relatively simple DC generator called a homopolar generator; a conducting wheel of diameter $D$ rotates with angular velocity $\omega$ in a uniform B-field oriented along the wheel axis. Sliding contacts make an electrical connection between the center of the wheel and the edge, as shown, and an EMF is induced across a load resistance $R$.*
#### 1.A.1
*Show that the power dissipated in the resistor is $P=c\dfrac{\omega^2B^2D^4}{R}$, where $c$ is an unknown numerical constant you’ll have to uncover for yourself.*
$$\begin{align}
\mathrm{EMF}&=-\int_0^{D/2} \vec{E}\cdot d\vec{r}\\
&=-\int_0^{D/2} \dfrac{d\vec{F}}{dq}\cdot d\vec{r}\\
&=-\int_0^{D/2} \left((r\vec\omega)\times \vec{B}\right)\cdot d\vec{r}\\
&=-B\omega\int_0^{D/2} r\ dr\\
&=-B\omega\dfrac{(D/2)^2}{2}\\
\Aboxed{\mathrm{EMF}&=-\dfrac{1}{8}B\omega D^2}
\end{align}$$
$$\begin{align}
P&=VI &&\text{(Definition)}\\
&=\mathrm{EMF}\cdot\dfrac{\mathrm{EMF}}{R} &&\text{(Ohmic Material)}\\
&=\dfrac{\left(\dfrac{1}{8}B\omega D^2\right)^2}{R} &&\text{(Substitution)}\\
\Aboxed{P&=\dfrac{1}{64}\dfrac{B^2\omega^2 D^4}{R}} &&\text{(Q.E.D.)}
\end{align}$$
#### 1.A.2
*How fast (in Hz) would a 1m diameter generator in a 0.2 tesla magnetic field have*
*to rotate to produce an EMF of 120V?*
$$\begin{align}
|\mathrm{EMF}|&=\dfrac{1}{8}B\omega D^2\\
120\mathrm{V}&=\dfrac{1}{8}(0.2\mathrm{T})(2\pi f)(1\mathrm{m})^2\\
2\pi f&=\dfrac{8\cdot120\mathrm{V}}{0.2\mathrm{T}\cdot1\mathrm{m}^2}\\
\Aboxed{f&=763.94\ \mathrm{Hz}}
\end{align}$$
### 1.B
*An AC generator: A square loop with side $a$ is mounted on a horizontal axis and rotates with a steady frequency $f$ (rotations/sec). A uniform magnetic field $\vec B$ points left to right between the two pole faces. The figure shows the configuration at time $t=0$ (note that there is no flux at this instant).*
#### 1.B.1
*If the output is connected to a load resistance $R$, calculate the instantaneous and average power dissipated in the resistor.*
$$\begin{align}
\mathrm{EMF}&=N\dfrac{d}{dt}\left(\vec{B}\cdot\vec{A}\right)\\
&=NBA\cdot\dfrac{d}{dt}\left(\sin\theta\right)\\
&=NBA\cos\theta\cdot\dfrac{d\theta}{dt}\\
\Aboxed{\mathrm{EMF}&=NBA\omega\cos\theta}
\end{align}$$
$$\begin{align}
P&=VI &&\text{(Definition)}\\
&=\mathrm{EMF}\cdot\dfrac{\mathrm{EMF}}{R} &&\text{(Ohmic Material)}\\
&=\dfrac{\left(NBA\omega\cos\theta\right)^2}{R} &&\text{(Substitution)}\\
\Aboxed{P(\theta)&=\dfrac{(NBA\omega)^2}{R}\cos^2\theta} &&\text{(Power)}\\
\bar{P}&=\dfrac{1}{2\pi}\int_0^{2\pi}P(\theta)\ d\theta &&\text{(RMS Definition)}\\
&=\dfrac{1}{2\pi}\int_0^{2\pi}\dfrac{(NBA\omega)^2}{R}\cos^2\theta\ d\theta &&\text{(Substitution)}\\
&=\dfrac{1}{2\pi}\dfrac{(NBA\omega)^2}{R}\int_0^{2\pi}\cos^2\theta\ d\theta &&\text{(Extraction)}\\
&=\dfrac{1}{2\pi}\dfrac{(NBA\omega)^2}{R}\pi &&\text{(Evaluation)}\\
\Aboxed{\bar{P}&=\dfrac{(NBA\omega)^2}{2R}} &&\text{(Q.E.D.)}
\end{align}$$
#### 1.B.2
*Compare your results to the mechanical power needed to turn the loop.*
$$\begin{align}
\bar{P}&=\dfrac{1}{2\pi}\int\vec{\tau}\cdot \vec{\omega}\ d\theta\\
&=\dfrac{1}{2\pi}\int\left(\dfrac{a}{2}\hat{r}\times\vec{F}\right)\cdot \omega\hat{\omega}\ d\theta\\
&=\dfrac{\omega a}{4\pi}\int\left(\hat{r}\times\vec{F}\right)\cdot \hat{\omega}\ d\theta\\
&=\dfrac{\omega a}{4\pi}\int\left|\vec{F}\right|\cos\theta\ d\theta\\
&=\dfrac{\omega a}{4\pi}\int\left(N\cdot\dfrac{\mathrm{EMF}}{R}\cdot(2a)\cdot B\right)\cos\theta\ d\theta\\
&=\dfrac{\omega a}{4\pi}\dfrac{2aBN}{R}\int\mathrm{EMF}\cos\theta\ d\theta\\
&=\dfrac{\omega BNa^2}{2R\pi}\int\left(NBA\omega\cos\theta\right)\cos\theta\ d\theta\\
&=\dfrac{\omega BNa^2}{2R\pi}NBA\omega\int\cos\theta\cos\theta\ d\theta\\
&=\dfrac{\omega^2 B^2N^2a^2A}{2R}\\
\Aboxed{\bar{P}&=\dfrac{(NBA\omega)^2}{2R}}\\
\end{align}$$
This mechanical power is identical to the electrical power generated.
This makes sense, since power should be conserved.
#### 1.B.3
*If the rotation rate is 60Hz the loop has area 0.02$\mathrm{m}^2$, and the magnetic field has a magnitude of 0.2T, about how many turns of wire would you need to produce a standard 120V (RMS) output?*
$$\begin{align}
\dfrac{V_\mathrm{rms}^2}{R}&=\dfrac{(NBA\omega)^2}{2R}\\
2V_\mathrm{rms}^2&=N^2B^2A^2\omega^2\\
N^2&=\dfrac{2V_\mathrm{rms}^2}{B^2A^2\omega^2}\\
\Aboxed{N&=\dfrac{\sqrt2V_\mathrm{rms}}{BA\omega}}\\
N&=\dfrac{\sqrt2(120\mathrm{V})}{(0.2\mathrm{T})(0.02\mathrm{m}^2)(2\pi\cdot60\ \mathrm{Hz})}\\
\Aboxed{N&\approx 112.5\text{ Loops}}
\end{align}$$
### 1.C
*Eddy-current break: An electromagnetic "eddy-current brake" consists of a solid spinning wheel of conductivity $\sigma$ and thickness $d$. A uniform field of magnitude $B_0$ is applied perpendicular to the surface of the wheel over a small area $A$ located a distance $s$ from the axis.*
#### 1.C.1
**i)** *Show that the torque on this disk is given (very approximately) by $\tau = \sigma\omega B^2s^2Ad$.*

$$\begin{align}
\tau&=\vec{s}\times\vec{F_\mathrm{B}}\\
&=(s\hat{s})\times(F_\mathrm{B}\hat\phi)\\
&=s\cdot \left|q\vec{v}\times \vec{B}\right|\\
&=s\cdot \left(qs\omega B_0\right)\\
&=qs^2B_0\omega\\
&=\left(\sigma Ad B_0\right)\omega B_0s^2\\
\Aboxed{\tau&=\sigma\omega B_0^2s^2Ad}
\end{align}$$

I wasn't 100% sure about how to find a "charge," but I assumed it had to be linear to conductivity, linear to volume, and linear to the strength of the field.
There's a proper way to calculate an effective charge, but I ran out of time to do so.
#### 1.C.2 : Extra Credit
*Perform an order of magnitude estimate for how strong $B_0$ should be for this kind of brake to be functional as a car break, given a magnet size of 20$\mathrm{cm}^2$per break. Do you foresee any problems as the car slows down?*

$$\vec\tau=\vec{r}\times\vec{F}\implies \vec{F}=\vec\tau\times\dfrac{\vec{r}}{r^2}$$
$$\begin{align}
\left|\vec{F}\right|&=\left|\vec\tau\times\dfrac{\vec{s}}{s^2}\right|\\
&=\left|\dfrac{\tau}{s}\right|\\
&=\left|\dfrac{\sigma\omega B_0^2s^2Ad}{s}\right|\\
\Aboxed{\left|\vec{F}\right|&=\sigma\omega B_0^2sAd}
\end{align}$$
$$\begin{align}
ma&=4\sigma\omega B_0^2sAd\\
m\dfrac{d^2x}{dt^2}&=(4\sigma B_0^2Ad)\dfrac{dx}{dt}\\
\dfrac{d^2x}{dt^2}&=\left(\dfrac{4\sigma B_0^2Ad}{m}\right)\dfrac{dx}{dt}\\
\Delta x(t)&=v_0e^{\left(\tfrac{4\sigma B_0^2Ad}{m}\right)t}
\end{align}$$
As the wheels get slower, they produce less braking force and it's an exponential decay of velocity breaking.
Something else that may affect it is that $\sigma$ decreases as temperature increases.

---
## Question 2
A rectangular loop of metal wire, of width $w$, moving with constant speed $v$, is entering a region of uniform B-field. The B-field is out of the page and is increasing at a constant rate $B=B_0+\alpha t$, where $B_0$ and $\alpha$ are positive constants. At $t=0$, the right edge of the loop is a distance $x_0$ into the field, as shown. Note that the EMF around the loop has two different causes: the motion of the loop and the changing of the B-field.
### 2.A
*Derive an expression for the magnitude of the EMF around the loop as a function of time, while the loop is entering the field.*

$$\begin{align}
\mathrm{EMF}(t)&=\dfrac{d\Phi_\mathrm{B}}{dt}\\
&=\dfrac{d(B(t)\cdot A(t))}{dt}\\
&=B(t)\cdot\dfrac{dA(t))}{dt}+\dfrac{d(B(t))}{dt}\cdot A(t)\\
&=\left(B_0+\alpha t\right)\cdot(wv)+(\alpha)\cdot (w(x_0+vt))\\
&=wvB_0+\alpha twv+\alpha wx_0+\alpha wvt\\
\Aboxed{\mathrm{EMF}(t)&=v(wB_0)+2\alpha v(wt)+\alpha (wx_0)}
\end{align}$$
### 2.B
*Is the induced current in the loop clockwise, counterclockwise (or impossible to determine without knowing the values of $v$ and $\alpha$?) Explain. Also, explicitly check that your answer to part a) makes sense by checking units and considering the two cases $v=0$ and $\alpha=0$. Explain how these limits give answers you might expect.*

For the system where there's no velocity and there's just an increasing field, the flux in the area increases, meaning the current opposes the new flux by decreasing flux. By the right hand rule, the current must flow clockwise.
$$\mathrm{EMF}(t)=\alpha (wx_0)=\alpha A_0 \ge 0$$
For the system where there's no increasing field, but the loop of wire moves, the flux in the area increases, meaning the current opposes the new flux by decreasing flux. By the right hand rule, the current must flow clockwise.
$$\mathrm{EMF}(t)=(wB_0)v=B_0A(t) \ge 0$$
Taking a look at the original EMF equation, we can see:
$$\mathrm{EMF}(t)=v(wB_0)+2\alpha v(wt)+\alpha (wx_0) \ge0$$
While the 2 different methods do have a coupling term between them, that coupling is also always positive, the current would *still* go clockwise.

Since all 3 methods of EMF production cause currents going around clockwise, there would be no canceling action where the direction of the currents change.
**Current always goes clockwise in this example.**

---
## Question 3
*A square metal loop is released from rest and falls straight down. The loop is between the poles of a magnet with uniform B-field, and initially, the top of the loop is inside the field and the bottom of the loop is outside the field. The metal has mass density $\rho_\mathrm{m}$ and electrical resistivity $\rho_\mathrm{res}$. The loop has edge length $L$, and is made of a rectangular wire with very small transverse dimensions $w$ and $l$.*
### 3.A
#### 3.A.1
*What is the EMF around the loop in terms of the downward speed $v$ of the loop?*
$$\begin{align}
\mathrm{EMF}(t)&=\dfrac{d\Phi_\mathrm{B}}{dt}\\
&=\dfrac{d(B\cdot A(t))}{dt}\\
&=B\cdot\dfrac{d(L\cdot y(t))}{dt}\\
\Aboxed{\mathrm{EMF}(t)&=BLv}\\
\end{align}$$
#### 3.A.2
*Assume the loop reaches terminal velocity before it passes entirely outside the field, and derive an expression for the terminal speed of the loop.*

Electrical Power (Lost to heat):
$$\begin{align}
P_\mathrm{E} &= \dfrac{\mathrm{EMF}^2}{R}=\dfrac{\mathrm{EMF}^2}{\rho_\mathrm{res}(s/A)}=\dfrac{(BLv)^2}{\rho_\mathrm{res}}\dfrac{wl}{4L}\\
\end{align}$$
Gravitational Power (Gained from losing height):
$$\begin{align}
P_\mathrm{G} &= F_g\cdot v \approx \rho_\mathrm{m}(4wlL)gv\\
\end{align}$$
Since energy cannot be created or destroyed:
$$\begin{align}
P_\mathrm{E} &= P_\mathrm{G}\\
\dfrac{(BLv)^2}{\rho_\mathrm{res}}\dfrac{wl}{4L}&=\rho_\mathrm{m}(4wlL)gv\\
(BL)^2v&=(4L)^2\rho_\mathrm{res}\rho_\mathrm{m}g\\
\Aboxed{v_\mathrm{terminal}&=\dfrac{16g}{B^2}\rho_\mathrm{res}\rho_\mathrm{m}}
\end{align}$$
#### 3.A.3
*Do some qualitative sensemaking/sanity checks: Units? Does the functional dependence on the various variables seem reasonable? (Nothing quantitative, just e.g. arguing that the terminal velocity should be bigger if $g$ is bigger, since it’s pulled harder by gravity.)*

$$\begin{align}
[v_\mathrm{terminal}]&=\dfrac{[16][g]}{[B^2]}[\rho_\mathrm{res}][\rho_\mathrm{m}]\\
&=\dfrac{\mathrm{m/s^2}}{\left(\tfrac{\mathrm{N/C}}{\mathrm{m/s}}\right)^2}\left(\dfrac{\mathrm{V}}{\mathrm{A}}\cdot\mathrm{m}\right)(\mathrm{kg/m^3})\\
&=\dfrac{\mathrm{m^3/s^4}}{\left(\mathrm{N/C}\right)^2}\left(\dfrac{\mathrm{N/C\cdot\mathrm{m}}}{\mathrm{A}}\cdot\mathrm{m}\right)(\mathrm{kg/m^3})\\
&=\dfrac{\mathrm{m^3}}{\left(\mathrm{N/A\cdot s^3}\right)}\dfrac{\mathrm{m^2}}{\mathrm{A}}\dfrac{\mathrm{kg}}{\mathrm{m^3}}\\
&=\dfrac{\mathrm{kg\cdot m^2}}{\mathrm{N\cdot s^3}}\\
&=\dfrac{\mathrm{N}\cdot\mathrm{m}}{\mathrm{N\cdot s}}\\
\Aboxed{[v_\mathrm{terminal}]&=\dfrac{\mathrm{m}}{\mathrm{s}}}
\end{align}$$
### 3.B
*Show that, when the loop is traveling at terminal velocity, the rate at which thermal energy is generated by resistive heating is equal to the rate at which gravity does work on the loop (you are comparing power here). Briefly, why must the two be equal?*

Electrical Power (Lost to heat):
$$\begin{align}
P_\mathrm{E} &= \dfrac{\mathrm{EMF}^2}{R}=\dfrac{\mathrm{EMF}^2}{\rho_\mathrm{res}(s/A)}=\dfrac{(BLv)^2}{\rho_\mathrm{res}}\dfrac{wl}{4L}\\
\end{align}$$
Gravitational Power (Gained from losing height):
$$\begin{align}
P_\mathrm{G} &= F_g\cdot v \approx \rho_\mathrm{m}(4wlL)gv\\
\end{align}$$
They are equal because of the conservation of energy over time.
I also used this in my formulation since I know the conservation of energy.
### 3.C
*At $t=0$, the loop starts at rest. Use $F=ma$ to write down a differential equation for the speed $v$ of the loop. Then, solve for the speed $v$ as a function of time. You should find that the speed approaches the terminal speed exponentially. Sketch $v(t)$. What the time constant for this exponential motion? If the metal is aluminum, and $B$ is, say, 0.2T, what is the numerical value of the time constant? (Hint: I claim the values of $L$, $w$, and $t$ don’t matter. Show us why not.)*
$$\begin{align}
\vec{F}&=-\rho_\mathrm{m}(4wlL)g+\dfrac{(B_0L)^2}{\rho_\mathrm{res}}\dfrac{wl}{4L}v\\
-g&=\dfrac{dv}{dt}-\left(\dfrac{B_0^2}{16\rho_\mathrm{res}\rho_\mathrm{m}}\right)v\\
\end{align}$$
Using the substitution $v=v_0e^{\left(\tfrac{B_0^2}{16\rho_\mathrm{res}\rho_\mathrm{m}}\right)t}+c$
$$\begin{align}
-g&=\dfrac{dv}{dt}-\left(\dfrac{B_0^2}{16\rho_\mathrm{res}\rho_\mathrm{m}}\right)v\\
g&=\left(\dfrac{B_0^2}{16\rho_\mathrm{res}\rho_\mathrm{m}}\right)c\\
\end{align}$$
So, therefore:
$$\begin{align}
v(t)&=v_0e^{\left(\tfrac{B_0^2}{16\rho_\mathrm{res}\rho_\mathrm{m}}\right)t}+\dfrac{16g}{B_0^2}\rho_\mathrm{res}\rho_\mathrm{m}\\
0&=v_0+\dfrac{16g}{B_0^2}\rho_\mathrm{res}\rho_\mathrm{m}\\
v(t)&=\left(\dfrac{16g}{B_0^2}\rho_\mathrm{res}\rho_\mathrm{m}\right)\left(1-e^{\tfrac{B_0^2}{16\rho_\mathrm{res}\rho_\mathrm{m}}t}\right)\\
\Aboxed{v(t)&=v_\text{terminal}\cdot\left(1-e^{\tfrac{g}{v_\text{terminal}}t}\right)}
\end{align}$$
This is the expression we'd expect, since it's an exponential decay to $v_\text{terminal}$.

---
## Question 4
A conducting disk with radius $a$, height $h\gg a$, and conductivity $\sigma$ is immersed in a time-varying, but spatially uniform, magnetic field parallel to its axis, $\vec B=B_0\sin(\omega t)\hat{z}$.
### 4.A
*Ignoring the effects of any induced magnetic fields find the induced electric field $\vec{E}(\vec{r},t)$ and current density $\vec{J}(\vec{r},t)$ in the disk, and sketch the current distribution.*
$$\begin{align}
\int\vec{E}\cdot d\vec{l}&=-\omega \pi r^2B_0\cos(\omega t)\hat{z}\\
\vec{E}\cdot2\pi r&=-\omega \pi r^2B_0\cos(\omega t)\hat{z}\\
\Aboxed{\vec{E}(\vec{r},t) &=-\dfrac{B_0\omega|\vec{r}|}{2}\cos(\omega t)\hat{z}}\\
\Aboxed{\vec{J}(\vec{r},t)&=-\dfrac{\sigma B_0\omega|\vec{r}|}{2}\cos(\omega t)\hat{z}}\\
\end{align}$$
#### Current Distribution (of a slice) over Time
![[HW4_Q4A.png]]
I normalized $J$ so that we can see the cosine component more thoroughly.
It grows radially outward linearly for $0\le r\le a$.
### 4.B
Compare $\vec{E}(\vec{r},t)$ to the electric field in presented in problem #2 on problem set #2 in the limit 𝜔𝑡 ≪ 1.
$$\begin{align}
\lim_{\omega t\ll1}\vec{E}(\vec{r},t)&=\dfrac{B_0|\vec{r}|}{2t}\hat{z}\cdot\lim_{\omega t\ll1}-\omega t\cos(\omega t)\\
&=\dfrac{B_0|\vec{r}|}{2t}\hat{z}\cdot\lim_{\omega t\ll1}-\omega t\left(1\right)\\
\Aboxed{\lim_{\omega t\ll1}\vec{E}(\vec{r},t)&=-\dfrac{B_0\omega|\vec{r}|}{2}\hat{z}}\\
\end{align}$$
$$\begin{align}
\vec{E}(\vec{r},t)&=\dfrac{B_0}{2\tau}\left(-y\hat{x}+x\hat{y}\right)\\
&=-\dfrac{B_0y}{2\tau}\hat{x}+\dfrac{B_0x}{2\tau}\hat{y}
\end{align}$$
It looks like to me that $\tau$ and $\omega$ is inversely proportional to each other.
### 4.C : Induction Stoves!
#### 4.C.1
If the power dissipated in a resistor is $P=IV$, show that the power dissipated per
unit volume is $\vec{J}\cdot\vec{E}$ . Calculate the total instantaneous power dissipated in the disk at
time $t$, and the average power dissipated per cycle of the field.
$$\begin{align}
\dfrac{dP}{d\tau}&=\dfrac{d}{d\tau}\left(IV\right)\\
&=\dfrac{dI}{d\tau}V+I\dfrac{dV}{d\tau}\\
&=\dfrac{dJ}{dh}V+I\dfrac{\vec{E}}{\pi a^2}\\
&=0+\vec{J}\cdot\vec{E}\\
\Aboxed{\mathcal{P}&=\vec{J}\cdot\vec{E}}
\end{align}$$
$$\begin{align}
\mathcal{P}&=\vec{J}\cdot\vec{E}=\sigma\vec{E}^2\\
&=\sigma\left(-\dfrac{B_0\omega|\vec{r}|}{2}\cos(\omega t)\right)^2\\
&=\dfrac{\sigma B_0^2\omega^2 r^2}{4}\cos^2(\omega t)\\
\int\mathcal{P}&=\int_0^a\dfrac{\sigma B_0^2\omega^2 r^2}{4}\cos^2(\omega t)\cdot2\pi rh\ dr\\
&=\dfrac{\pi\sigma B_0^2\omega^2h}{2}\cos^2(\omega t)\int_0^ar^3\ dr\\
\Aboxed{P(t)&=\dfrac{\pi\sigma B_0^2\omega^2a^4h}{8}\cos^2(\omega t)}\\
\end{align}$$
$$\begin{align}
\bar P&=\dfrac{\pi\sigma B_0^2\omega^2a^4h}{8}\dfrac{\omega}{2\pi}\int_0^{2\pi/\omega}\cos^2(\omega t)\ dt\\
\Aboxed{\bar P&=\dfrac{\pi\sigma B_0^2\omega^2a^4h}{16}}
\end{align}$$
#### 4.C.2
*If this disk was roughly the size of the solid base of a typical frying pan, and the frequency was $20\ \mathrm{kHz}$, use the above result for power per unit volume to find what approximate scale for $B_0$ you would need to rapidly and significantly heat up the pan (say, 1000 watts of power). Does this seem feasible?*

For the sake of argument, lets use a 10" frying pan with a thickness of 5mm.
It is also made of stainless steel, and so $\sigma=1.45\cdot10^6\ \mathrm{S/m}$ at $T=20\mathrm{^{\circ}C}$.

We can then rearrange for $B_0$:
$$\begin{align}
\bar{P}&=\dfrac{\pi\sigma B_0^2\omega^2a^4h}{16}\\
B_0^2&=\dfrac{16\bar{P}}{\pi\sigma \omega^2a^4h}\\
\Aboxed{B_0&=\dfrac{2}{\pi f a^2}\sqrt{\dfrac{\bar{P}}{\pi\sigma h}}}\\
&=\dfrac{2}{\pi (2\cdot10^4\ \mathrm{Hz})(0.127\mathrm{m})^2}\sqrt{\dfrac{10^3\ \mathrm{W}}{\pi(1.45\cdot10^6\ \mathrm{S/m}) (5\cdot10^{-3}\mathrm{m})}}\\
&=4.135\cdot10^{-4}\ \mathrm{T}\\
\end{align}$$
It seems pretty reasonable that we could do this form of induction cooktop, since the magnitude of $B_0$ is around the order of less than $1.0\text{ mT}$.
#### 4.C.3
Didn't have enough time!

