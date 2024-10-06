**Name:** Stanley Goodwin
**Date:** 10/05/2024
**Collaborators:** Hasan
**Time Taken:** XXX Hours

---
## Question 1
Consider a standard coaxial cable consisting of an "infinite" length wire of radius $a$ surrounded by a thin conducting cylinder, coaxial with the wire, with inner radius $b$ and outer radius $c$.
Assume it’s a "thin wire and thin shell", i.e. $a\ll b$ and $c-b\ll b$ as show in the figure. We will be neglecting fields **inside** the solid metal regions, just focusing on the "coax region" $a<s<b\approx c$. A current $I(t)=I_0\cos(\omega t)$ flows down the central wire and a corresponding current $-I(t)$ returns in the opposite direction on the outer cylinder.
### 1.a
*Find the magnetic field $\vec B(s,t)$ in the "coax region" $a<s<b$, where $s$ is the usual radial coordinate and the current in the wire is $I_0$ in the $+z$ direction at $t=0$.*

Assuming that $\omega$ is small enough, we can calculate this field as a quasi-static magnetic field.
$$\begin{align}
\oint\vec{B}\cdot d\vec{l}&=\mu_0\int\vec{J}\cdot d\vec{A}\\
\int_{0}^{2\pi}\left(B\hat\phi\right)\cdot \left(sd\phi\ \hat\phi\right)&=\mu_0I_\text{enc}\\
B\cdot\int_{0}^{2\pi} sd\phi&=\mu_0I_0\cos(\omega t)\\
B\cdot 2\pi s&=\mu_0I_0\cos(\omega t)\\
\Aboxed{\vec{B}(s,t)=\dfrac{\mu_0I_0}{2\pi s}\cos(\omega t)\hat\phi}
\end{align}$$
### 1.b
*Find the induced electric field $\vec E(s,t)$ in the "coax region" $a<s<b$.*
$$\begin{align}
\oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A}\\
\oint E\cdot sd\phi&=-\dfrac{d}{dt}\iint B\cdot sdsd\phi\\
E\cdot 2\pi s&=-2\pi\dfrac{d}{dt}\int \dfrac{\mu_0I_0}{2\pi s}\cos(\omega t)\cdot sds\\
E\cdot 2\pi s&=-2\pi\dfrac{d}{dt}\left(\dfrac{\mu_0I_0}{2\pi}\cos(\omega t)\cdot s\right)\\
E &=-\dfrac{\mu_0I_0}{2\pi}\dfrac{d}{dt}\cos(\omega t)\\
E&=\dfrac{\mu_0I_0\omega}{2\pi}\sin(\omega t)\\
\Aboxed{\vec E&=\dfrac{\mu_0I_0\omega}{2\pi}\sin(\omega t)\hat\phi}
\end{align}$$
Outside of the coax region, we find that the total enclosed current is 0, and so the net electric field would also be 0, because the outside radius grows by $s$ but the B-field falls as $1/s$, and so the electric field on the top arc would be equal and opposite to the bottom arc, and so there would be 0 net electric field.

---
## Question 2
Consider the circuit shown to the right, with the power supply providing an EMF of $V(t)=V_0\cos(\omega t)$. Assume that all of the transients have died away long before $t=0$.
### 2.a
*Find the current through the power supply for $t\ge0$.*
Solving the differential equation, $L\dfrac{dI(t)}{dt}+I(t)R=V(t)$, we can find that:
$$\begin{align}
L\dfrac{dI_\mathrm{H}(t)}{dt}+I_\mathrm{H}(t)R&=0\implies I_\mathrm{H}(t)=Ae^{-\tfrac{R}{L}t}
\end{align}$$
$$\begin{align}
V_0\cos(\omega t)&=L\dfrac{dI_\mathrm{P}(t)}{dt}+I_\mathrm{P}(t)R\\
I_\mathrm{p}(t)&=\dfrac{V_0}{L^2\omega^2+R^2}\left(L\omega\sin(\omega t)+R\cos(\omega t)\right)
\end{align}$$
The question tells us that the transience has died off, removing the homogenous solution.
$$\begin{align}
\Aboxed{I(t)&=\dfrac{V_0}{L^2\omega^2+R^2}\left(L\omega\sin(\omega t)+R\cos(\omega t)\right)}
\end{align}$$
### 2.b
*How does your answer behave in the limits $\omega\rightarrow0$ and $\omega\rightarrow\infty$? Briefly discuss how these limits are consistent with the expected behavior of inductors.*
$$\begin{align}
\lim_{\omega\rightarrow0}I(t)&=\lim_{\omega\rightarrow0}\dfrac{V_0}{L^2\omega^2+R^2}\left(L\omega\sin(\omega t)+R\cos(\omega t)\right)\\
&=\dfrac{V_0}{L^20^2+R^2}\left(L0\sin(0 t)+R\cos(0t)\right)\\
&=\dfrac{V_0}{R^2}\cdot R\\
\Aboxed{\lim_{\omega\rightarrow0}I(t)&=\dfrac{V_0}{R}}
\end{align}$$
This answer as $\omega\rightarrow0$ is expected, since this as if a DC voltage has been applied to the circuit for a long time, and so acts like a singular battery and resistor.
$$\begin{align}
\lim_{\omega\rightarrow\infty}I(t)&=\lim_{\omega\rightarrow\infty}\dfrac{V_0}{L^2\omega^2+R^2}\left(L\omega\sin(\omega t)+R\cos(\omega t)\right)\\
&=\dfrac{V_0}{L^2}\lim_{\omega\rightarrow\infty}\left(\dfrac{L\omega\sin(\omega t)}{\omega^2}+\dfrac{R\cos(\omega t)}{\omega^2}\right)\\
&=\dfrac{V_0}{L^2}\left(L\lim_{\omega\rightarrow\infty}\dfrac{\sin(\omega t)}{\omega}+R\lim_{\omega\rightarrow\infty}\dfrac{\cos(\omega t)}{\omega^2}\right)\\
&=\dfrac{V_0}{L^2}\left(0+0\right)\\
\Aboxed{\lim_{\omega\rightarrow\infty}I(t)&=0}
\end{align}$$
This answer as $\omega\rightarrow\infty$ is expected, since the infinitely fast switching current would generated a potential that would oppose the incoming source voltage, and so no current will move throughout the circuit.

---
## Question 3
Now consider another (series) LR circuit, driven by the AC voltage source $V_\text{in}(t)=V_0\cos(\omega t)=\Re\left(\tilde V_\text{in}(t)\right)$. A circuit like this serves to change $V_\text{in}$ into $V_\text{out}$. It's a form of "filter" that responds better to some driving frequency than others.
### 3.a
*Use the method of phasors to find the "true" current in the circuit.*
$$\begin{align}
\tilde V_\text{in}(t)&=V_0e^{i\omega t}\\
Z_\text{total}&=R+i\omega L\\
\tilde I(t)&=\dfrac{\tilde V_\text{in}(t)}{Z_\text{total}}\\
&=\dfrac{V_0}{R+i\omega L}e^{i\omega t}\\
&=\dfrac{V_0}{\sqrt{L^2\omega^2+R^2}e^{i\tan\left(\tfrac{L\omega}{R}\right)}}e^{i\omega t}\\
&=\dfrac{V_0}{\sqrt{L^2\omega^2+R^2}}e^{i\omega t}e^{-i\tan^{-1}\left(\tfrac{L\omega}{R}\right)}\\
\tilde I(t)&=\dfrac{V_0}{\sqrt{L^2\omega^2+R^2}}e^{i\left(\omega t-\tan^{-1}\left(\tfrac{L\omega}{R}\right)\right)}\\
\Aboxed{I(t)&=\dfrac{V_0}{\sqrt{L^2\omega^2+R^2}}\cos{\left(\omega t-\tan^{-1}\left(\tfrac{L}{R}\omega\right)\right)}\\}
\end{align}$$
### 3.b
*Find and solve for the complex ratio (magnitude and phase) $\tilde V_\text{out}(t)/V_\text{in}(t)$ as a function of the driving frequency $\omega$.*
$$\begin{align}
&&\tilde V_\text{out}(t)&=V_\text{in}(t)\cdot\dfrac{Z_R}{Z_\text{total}}\\
\implies&&\dfrac{\tilde V_\text{out}(t)}{V_\text{in}(t)}&=\dfrac{Z_R}{Z_\text{total}}\\
&&&=\dfrac{R}{\sqrt{L^2\omega^2+R^2}e^{i\tan^{-1}\left(\tfrac{L\omega}{R}\right)}}\\
&&\Aboxed{\dfrac{\tilde V_\text{out}(t)}{V_\text{in}(t)}&=\dfrac{R}{\sqrt{L^2\omega^2+R^2}}e^{-i\tan^{-1}\left(\tfrac{L\omega}{R}\right)}}\\
&&\Aboxed{\left|\dfrac{\tilde V_\text{out}(t)}{V_\text{in}(t)}\right|&=\dfrac{R}{\sqrt{L^2\omega^2+R^2}}}\\
&&\Aboxed{\mathrm{arg}\left(\dfrac{\tilde V_\text{out}(t)}{V_\text{in}(t)}\right)&=-\tan^{-1}\left(\tfrac{L\omega}{R}\right)}\\
\end{align}$$
#### 3.b.I
*Sketch a plot of the magnitude of $\tilde V_\text{out}(t)/V_\text{in}(t)$ versus $\omega$.*
**TODO**
#### 3.b.II
*Check that your solution makes sense in the limits $\omega\rightarrow0$ and $\omega\rightarrow\infty$.*
$$\begin{align}
\lim_{\omega\rightarrow0}\dfrac{\tilde V_\text{out}(t)}{V_\text{in}(t)}&=
\lim_{\omega\rightarrow0}\dfrac{R}{\sqrt{L^2\omega^2+R^2}}e^{-i\tan^{-1}\left(\tfrac{L\omega}{R}\right)}\\
&=
\dfrac{R}{\sqrt{L^20^2+R^2}}e^{-i\tan^{-1}\left(\tfrac{L}{R}0\right)}\\
&=
\dfrac{R}{\sqrt{R^2}}\\
\Aboxed{\lim_{\omega\rightarrow0}\dfrac{\tilde V_\text{out}(t)}{V_\text{in}(t)}&=1}
\end{align}$$
This answer as $\omega\rightarrow0$ is expected, since this as if a DC voltage has been applied to the circuit for a long time, and so acts like a singular battery and resistor. No phase kickback is applied since the inductor is effectively inactive.
$$\begin{align}
\lim_{\omega\rightarrow\infty}\dfrac{\tilde V_\text{out}(t)}{V_\text{in}(t)}&=
\lim_{\omega\rightarrow\infty}\dfrac{R}{\sqrt{L^2\omega^2+R^2}}e^{-i\tan^{-1}\left(\tfrac{L\omega}{R}\right)}\\
&=\lim_{\omega\rightarrow\infty}\dfrac{R}{L\omega}\lim_{\omega\rightarrow\infty}e^{-i\tan^{-1}\left(\tfrac{L\omega}{R}\right)}\\
&=0\cdot e^{-i\pi/2}\\
\Aboxed{\lim_{\omega\rightarrow\infty}\dfrac{\tilde V_\text{out}(t)}{V_\text{in}(t)}&=0}
\end{align}$$
This answer as $\omega\rightarrow\infty$ is expected, since the infinitely fast switching current would generated a potential that would oppose the incoming source voltage, and so no current will move throughout the resistor. Since the inductor is fully active, there is a $-90^\circ$ phase kickback in the ratio of the input and output voltages on the resistor.
#### 3.b.III
*Briefly describe this filter. Is it a high-pass filter? Low-pass? Band-pass?*
This is exactly a **low-pass filter**, since it decreases the signal strength of high-frequency input signals and doesn't effect low-frequency input signals.

---
## Question 4
For our final circuit, consider the series RLC circuit shown to the right. Assume that the circuit is underdamped (i.e. $R$ is small), and that all transients have long since died away.
The power supply provides a driving emf $V(t)=V_0\sin(\omega t)$.
### 4.a
*What Find an equation for the true current through the power supply as a function of time.*
$$\begin{align}
...
\end{align}$$
### 4.b
*Hand sketch a rough plot of the amplitude of the true current as a function of $\omega$, showing and briefly explaining any interesting features (such as the limits and anything else that stands out to you.*
$$\begin{align}
...
\end{align}$$
### 4.c
Now let’s use some realistic values appropriate to an inexpensive oscillator, say a 1 ohm resistor, a 30 pF (picofarad) capacitor, and a 100 nH (nanohenry) inductor).
#### 4.c.I
*What is the natural resonance frequency (in hertz) of this circuit? Does this value give you any hints as to what a circuit like this might be useful for?*
$$\begin{align}
...
\end{align}$$
#### 4.c.II
*Use the software of your choice to plot the amplitude of the true current as a function of frequency. Be careful to set the scale of your frequency axis to run past the resonance. Does the graph match the expectations of your “sketch” in the previous part? Briefly comment.*
$$\begin{align}
...
\end{align}$$
---
## Question 5
Let’s return one last time to the coaxial cable we started with in Problem #1. You already found the induced electric field. Now let’s think about things in terms of displacement current.
### 5.a
*What is the displacement current density $\vec J_d$ in the coax region $(a < s < b)$?*
$$\begin{align}
...
\end{align}$$
### 5.b
*Use integration by parts to find the total displacement current in the coax region, $I_d$, then demonstrate that the units work out as a check on your integration.*
$$\begin{align}
...
\end{align}$$
### 5.c
*Using physically reasonable numbers for a real coax (say $a=1\ \mathrm{mm}$ and $b=1\ \mathrm{cm}$), determine the angular frequency needed for $I_d$ to equal 1% of $I_0$.*
$$\begin{align}
...
\end{align}$$
### 5.d
*Briefly comment on your result, expressing the frequency in hertz. Does the displacement current become a bigger issue as we move to frequencies greater than or less than this value? How do you feel about our “quasi-static” approximation in light of this result?*
$$\begin{align}
...
\end{align}$$
