**Name:** Stanley Goodwin
**Date:** 9/28/2024
**Collaborators:** Hasan
**Time Taken:** 3 Hours

---
## Question 1
Consider an infinitely tall solenoid (radius $R$, $n$ coils per unit length), wrapped around it is a single loop of wire (radius $r$, centered at the left edge of the solenoid, shown).
### 1.a
*What Calculate the mutual inductance $M$ between the loop and the solenoid. Would this value be bigger, smaller, or the same if $r$ were twice as big?*

Since we're calculating mutual induction, it is easier to consider the situation where the infinite solenoid has the current flowing through it instead, so we can swap the magnetic field and loop area as the following (simpler) expression:
$$\begin{align}
&&\vec{B}_\text{solenoid}&=\mu_0nI\\
&&\vec{A}_\text{loop}&=\pi r^2\\
\implies&&\Phi_\text{sl}&=\vec{B}_\text{solenoid}\cdot\vec{A}_\text{loop}\\
&&&=\mu_0nI\pi r^2\\
\implies&&M_\text{sl}&=\dfrac{\mu_0nI\pi r^2}{I}\\
&&\Aboxed{M_\text{sl}&=\mu_0n\pi r^2}
\end{align}$$
If the value of $r$ was 2x, the mutual induction would increase by 4x ($M_\text{sl}\propto r^2$).

### 1.b
*Suppose now that the loop is doubled up (but still with the same radius) so that it wraps around the solenoid twice. Again, calculate the mutual inductance of the loop-solenoid system.*

The effective area of the loop is doubled in this part, so we can write the following:
$$\begin{align}
&&\vec{B}_\text{solenoid}&=\mu_0nI\\
&&\vec{A}_\text{loop}&=2\pi r^2\\
\implies&&\Phi_\text{sl}&=\vec{B}_\text{solenoid}\cdot\vec{A}_\text{loop}\\
&&&=2\mu_0nI\pi r^2\\
\implies&&M_\text{sl}&=\dfrac{2\mu_0nI\pi r^2}{I}\\
&&\Aboxed{M_\text{sl}&=2\mu_0n\pi r^2}
\end{align}$$
### 1.c
*If the solenoid were of finite length instead, would the mutual inductance between the loop and the solenoid be larger, smaller, or the same size as in part a? Briefly explain your answer.*
**Note:** You don’t need to calculate $M$ here; a qualitative argument will be sufficient.

The mutual induction **would be lesser**, since the net magnetic field on the area would be less.
With an infinite solenoid, no magnetic field escapes the coil.
A finite coil, however, would have a very tiny (but existent) magnetic field in the opposite direction of the solenoid's interior on the outside of the solenoid, reducing net flux.

### 1.d
*Calculate the self-inductance per unit length of the infinite solenoid, all by itself, then*
*explicitly check that the units of your answer work out correctly.*
$$\begin{align}
&&\vec{B}_\text{solenoid}&=\mu_0nI\\
&&\vec{A}_\text{solenoid}&=\pi R^2\\
\implies&&\Phi_\text{solenoid}&=\vec{B}_\text{solenoid}\cdot\vec{A}_\text{solenoid}\\
&&&=\mu_0nI\pi R^2\\
\implies&&M_\text{self}&=\dfrac{nl}{I}\mu_0nI\pi R^2\\
&&\Aboxed{L&=\mu_0n^2\pi R^2l}
\end{align}$$
---
## Question 2
Two circular loops of wire are arranged so that they lie in the same plane and are concentric. One loop, of radius $a$, is TINY, much smaller than the other, which has radius $b$, i.e. $a\ll b$.  *If the small loop is driven with a time varying current $I_a(t)$, derive an approximate formula for the induced emf in the large loop (and please state the approximations or assumptions you make in your derivation).*

The assumption is that we're supposing the change in current is relatively slow compare to time, so we can approximate the EMF with just the Ampere's law (Pseudo-Static).
We can also assume that the B field inside is effectively constant since $a\ll b$.
$$\begin{align}
\vec{B}_\text{inner}(t)&=\dfrac{\mu_0 I_a(t)}{2a}\\
\vec{A}_\text{outer}(t)&=\pi b^2\\
\Phi_\text{io}(t)&=\dfrac{\mu_0 I_a(t)}{2a}\cdot\pi b^2\\
M_\text{io}&=\dfrac{\mu_0\pi b^2}{2a}\\
\mathrm{EMF}&=-M_\text{io}\dfrac{\partial I_a(t)}{\partial t}\\
\Aboxed{\mathrm{EMF}&=-\dfrac{\mu_0\pi b^2}{2a}\dfrac{\partial I_a(t)}{\partial t}}
\end{align}$$
---
## Question 3
Consider a coaxial cable consisting of an (infinitely) long wire of radius $a$, with given current flowing uniformly up it (so that $\vec J(t)=I(t)/(\pi a^2)\hat{k}$ goes uniformly through the wire). At the outside edge ($s=a$), there is an infinitesimally thin insulator, and just outside that, an infinitesimally thin sheath that returns ALL the current, basically a surface current going down the opposite direction carrying a total $-I(t)$ back down the length of the wire.
### 3.a
*Find the magnetic field vector (magnitude and direction) everywhere in space.*
**Note:** Assume that $I(t)$ varies slowly enough that quasi-static methods are appropriate.
$$\begin{align}
\oint\vec{B}\cdot d\vec{l}=\int \vec{J}\cdot d\vec{A}=I_\text{enc}
\end{align}$$
For the interior, $0\le s\lt a$, we find that:
$$\begin{align}
\oint\vec{B}\cdot d\vec{l}&=\mu_0\int \vec{J}\cdot d\vec{A}\\
\oint \left(B\hat{\phi}\right)\cdot\left(2\pi dr\hat{\phi}\right)&=\mu_0\int\left(\dfrac{I(t)}{\pi a^2}\hat{z}\right)\cdot\left(2\pi rdr\hat{z}\right)\\
B\cdot2\pi\int_0^s dr&=\dfrac{2\mu_0I(t)}{a^2}\int_0^s rdr\\
B\cdot2\pi s&=\dfrac{2\mu_0I(t)}{a^2}\dfrac{s^2}{2}\\
\Aboxed{\vec{B}(s,t)&=\dfrac{\mu_0I(t)s}{2\pi a^2}\hat\phi}
\end{align}$$
For the exterior, $s \ge a$, there is $0$ net enclosed current, and so $\vec{B}(t)=0$.
To be clear, this solution is only because it is quasi-static, so it can be written as:
$$\vec{B}(s,t)=\begin{cases}
\dfrac{\mu_0I(t)s}{2\pi a^2}\hat\phi,&0\le s\lt a\\
0,&s\ge a
\end{cases}$$
### 3.b
*Find the self-inductance per unit length of this cable.*

**Hint:** You might start from $\Phi_B=IL$, but this turns out to be tricky here, since the
current is not confined to a single path. It’s easier to instead think about the total
magnetic energy, $W$, stored by the magnetic field, and use our usual relation between
energy and current: $W=\tfrac{1}{2}LI^2$

**Something else to think about:** You found $L$ per unit length of a solenoid in question 1.
You now know that the wire making up the solenoid also has its own contribution to the
inductance. Which contribution will dominate when considering a real solenoid made up
of real wire?
$$\begin{align}
\dfrac{dL}{dl}&=\dfrac{d}{dl}\left(\dfrac{2W}{I^2}\right)\\
&=\dfrac{2}{I^2}\dfrac{dW}{dl}\\
&=\dfrac{2}{I^2}IlB\\
&=\dfrac{2l}{I}\dfrac{\mu_0I(t)s}{2\pi a^2}\\
\Aboxed{L&=\dfrac{\mu_0s}{\pi a^2}l}
\end{align}$$
---
## Question 4
Consider the electrical circuit shown to the right. There is an infinitely long solenoid in the center of the wires (shaded, shown end-on in the figure). The current in that solenoid circulates clockwise and increases linearly with time, producing a flux (into the page) that is likewise linear in time: $\Phi_B=\alpha t$. Surrounding that solenoid are some ideal wires and two resistors, as shown, with ideal voltmeters (that means they have very high internal resistance, and thus negligible current flows through them) connected as shown (the probes of voltmeter $V_1$ are directly across resistor $R_1$, and those of $V_2$ are across $R_2$).
### 4.a
*What do the two voltmeters read? Make sure to include the signs. If the two readings are different, how can that be? Is it the case that points $a$ and $b$ should have a unique voltage drop between them, and if not, why not?*

The 2 different points must have a difference of voltage, since the same amount of current is driven through both resistors.

Resistor 1 has a voltage change of $V_1=IR_1$ and Resistor 2 has $V_2=IR_2$.
Since the current goes around counterclockwise:
$$\begin{align}
\Sigma V&=V_2-V_1\\
\Aboxed{\Sigma V&=I(R_2-R_1)}
\end{align}$$
Supposing that $R_2 > R_1$, that would mean that there needs to be more voltage on the bottom to allow for the same amount of current relative to the top, leading to a potential difference.

### 4.b
Now consider two of those circuits connected as shown in the figure below. The solenoids are identical, both with the same cross-sectional area ($=0.2\ \mathrm{m}^2$), and the magnitude of the magnetic field inside both is equal and increasing at the same constant rate ($0.02\ \mathrm{T/s}$), though note the direction of the current is opposite in the two solenoids, so the B-fields are in fact increasing in opposite directions. The resistors have the values shown.
*Determine the current (magnitude and direction) passing through each resistor.*
$$\begin{align}
\mathrm{EMF}&=\dfrac{d}{dt}\left(\vec{B}\cdot\vec{A}\right)\\
&=\vec{A}\cdot\dfrac{d\vec{B}}{dt}\\
&=\left(0.2\ \mathrm{m}^2\right)\cdot\left(0.02\ \mathrm{T/s}\right)\\
&=-0.004\ \mathrm{T\ m^2/s}\\
\mathrm{EMF}&=4\ \mathrm{mV}\\
\end{align}$$
Right & Left Resistors $(1\ \Omega)$:
$$\begin{align}
I&=I_1+I_2\\
I&=\dfrac{4\ \mathrm{mV}}{1\ \Omega}+\dfrac{4\ \mathrm{mV}}{1\ \Omega}\\
\Aboxed{I&=8\ \mathrm{mA} \text{  (Upwards)}}
\end{align}$$
Center Resistor $(0.5\ \Omega)$:
$$\begin{align}
I&=I_1+I_2\\
&=\dfrac{4\ \mathrm{mV}}{0.5\ \Omega}+\dfrac{4\ \mathrm{mV}}{0.5\ \Omega}\\
\Aboxed{I&=16\ \mathrm{mA} \text{  (Downwards)}}
\end{align}$$
**Note:** This is to be expected, since the sum of the currents is $0$, I.e. Current Conservation.