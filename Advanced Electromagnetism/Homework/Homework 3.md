**Name:** Stanley Goodwin
**Date:** 9/11/2024
**Collaborators:** None
**Time Taken:** 8 Hours over 2 days

---

**Notes:** 
 - I didn't really know how to do Q2D, but I know it has to relate to the drift velocities and $\rho$ at the interface making sure that enough current is flowing in both wires.
 - I didn't graph any of these by hand, but they were Gaussian-Adjacent, so I don't think it mattered too much.

*As always, your work will be graded for clarity of explanation as much as for the “correctness” of your final answer. And as always, please include the names of those you collaborated with, as well as the total number of hours spent on this assignment.*

### Question 1
*Suppose the magnetic vector potential in a region of space is given by:*
$$\vec{A}=A_0e^{-\tfrac{x^2+y^2}{a^2}}\hat{z}$$

**a.1)** *What are the units of the given constants $a$ and $A_0$* ?
$$\begin{align}
[a]&= \mathrm{m}\\
[A_0]&=\mathrm{T}\cdot\mathrm{m}
\end{align}$$
The units of $a$ are length (meters) and $A_0$ is in terms of Tesla Meters, since $dA = B$.

**a.2)** *Determine the magnetic field $\vec{B}$ from this vector potential.*
For the sake of the following, I rewrote $\vec{A}$ in cylindrical coordinates.
$$\vec{A}=A_0e^{-\tfrac{x^2+y^2}{a^2}}\hat{z} \implies \vec{A}=A_0e^{-\tfrac{s^2}{a^2}}\hat{z}$$
$$\begin{align}
\vec{B}&=\vec\nabla\times\vec{A}\\
&=\left(\dfrac{1}{s}\dfrac{\partial A_z}{\partial\phi}-\dfrac{\partial A_\phi}{\partial z}\right)\hat{s} + \left(\dfrac{\partial A_s}{\partial z}-\dfrac{\partial A_z}{\partial s}\right)\hat{\phi} + \dfrac{1}{s}\left(\dfrac{\partial (sA_\phi)}{\partial s}-\dfrac{\partial A_s}{\partial \phi}\right)\hat{z}\\
&= -\left(\dfrac{\partial A_z}{\partial s}\right)\hat{\phi}\\
&= -\dfrac{\partial}{\partial s}\left(A_0e^{-\tfrac{s^2}{a^2}}\right)\hat{\phi}\\
&= -A_0e^{-\tfrac{s^2}{a^2}}\dfrac{\partial}{\partial s}\left(-\dfrac{s^2}{a^2}\right)\hat{\phi}\\
&= -A_0e^{-\tfrac{s^2}{a^2}}\left(-\dfrac{2s}{a^2}\right)\hat{\phi}\\
\Aboxed{\vec{B} &= \dfrac{2A_0s}{a^2}e^{-\tfrac{s^2}{a^2}}\hat{\phi}}
\end{align}$$
The magnetic field loops around in the $\hat\phi$ direction.

**a.3)** *Determine the current density $\vec{J}$ by use of the appropriate Maxwell Equation.*
For current density, I used the static form of Maxwell's equations for the curl of $\vec B$.
$$\begin{align}
\vec\nabla\times\vec{B}&=\left(\dfrac{1}{s}\dfrac{\partial A_z}{\partial\phi}-\dfrac{\partial A_\phi}{\partial z}\right)\hat{s} + \left(\dfrac{\partial A_s}{\partial z}-\dfrac{\partial A_z}{\partial s}\right)\hat{\phi} + \dfrac{1}{s}\left(\dfrac{\partial (sA_\phi)}{\partial s}-\dfrac{\partial A_s}{\partial \phi}\right)\hat{z}=\left(\dfrac{1}{s}\dfrac{\partial (sA_\phi)}{\partial s}\right)\hat{z}\\
&=\left(\dfrac{1}{s}\dfrac{\partial\left(\tfrac{2A_0s^2}{a^2}e^{-\tfrac{s^2}{a^2}}\right)}{\partial s}\right)\hat{z}=\left(\dfrac{1}{s}\dfrac{2A_0}{a^2}\dfrac{\partial\left(s^2e^{-\tfrac{s^2}{a^2}}\right)}{\partial s}\right)\hat{z}\\
&=\dfrac{2A_0}{sa^2}\left(2se^{-\tfrac{s^2}{a^2}}-\dfrac{2s^3}{a^2}e^{-\tfrac{s^2}{a^2}}\right)\\
\mu_0\vec{J}&=\left(\dfrac{4A_0}{a^2}-\dfrac{4A_0s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\\
\Aboxed{\vec{J}&=\dfrac{4A_0}{\mu_0}\left(\dfrac{1}{a^2}-\dfrac{s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\hat{z}\\}
\end{align}$$

**b)** *Separately sketch $\vec A$, $\vec B$, and $\vec J$ fields. Describe what they look like in English.*

**Vector Potential Field** (Magnitude) ![[HW3_Q1B_1.png]]
The distribution looks to be a bell curve, which is quite interesting.
The vector field points directly up $(+\hat{z})$ and tapers off as the field moves away from the $z$-axis.

**Magnetic Field** (Magnitude) ![[HW3_Q1B_2.png]]
This distribution follows the slope of the bell curve along the path.
The vector field curls in the $+\hat\phi$ direction, with the strongest field found where $|\vec{A}|$ was changing most rapidly.

**Current Density** (Magnitude) ![[HW3_Q1B_3.png]]
This distribution looks to be the concavity of a bell curve.
The vector field points in the $\hat z$ direction, with the current density being dependent on the change of magnetic field magnitude over space.


**c)** *Integrate the current density to show that the total current flowing through any infinite plane parallel to the 𝑥𝑦-plane is zero. Then, give a simple argument (without doing any formal integral) why you might have known before calculating that this must be the case.*
$$\begin{align}\vec{J}&=\dfrac{4A_0}{\mu_0}\left(\dfrac{1}{a^2}-\dfrac{s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\hat{z}& 
\gamma&:\lim_{r\rightarrow\infty}\left\{ \begin{array}.x=r\cos(\theta)\\y=r\sin(\theta)\end{array} \right.,\theta\in[0,2\pi)\end{align}$$
$$\begin{align}
\int_\gamma\vec{J}\cdot d\vec{A}&=\int\dfrac{4A_0}{\mu_0}\left(\dfrac{1}{a^2}-\dfrac{s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\hat{z}\cdot\hat{z}(s\ d\phi\ ds)\\
&=\dfrac{4A_0}{\mu_0a^4}\int_0^\infty\int_0^{2\pi}\left(a^2-s^2\right)e^{-\tfrac{s^2}{a^2}}\cdot (s\ d\phi\ ds)\\
&=\dfrac{4A_0}{\mu_0a^4}\int_0^\infty s\left(a^2-s^2\right)e^{-\tfrac{s^2}{a^2}}\ ds\\
&=\dfrac{2A_0}{\mu_0a^4}\left(a^2s^2e^{-\tfrac{s^2}{a^2}}\right|_0^\infty\\
&=\dfrac{2A_0}{\mu_0a^4}\left(0-0\right)\\
\Aboxed{\int_\gamma\vec{J}\cdot d\vec{A}&=0}
\end{align}$$
We could have made this judgement without the calculation since the integral is radially symmetric without a z-component, and so the current through a plane parallel to the xy plane would have to be 0. There is also a symmetry argument to make that, if it was not 0, then it would not be rotationally symmetric.

**d.1)** Calculate the divergence of the current density $\vec J$. 
$$\begin{align}\vec{J}&=\dfrac{4A_0}{\mu_0}\left(\dfrac{1}{a^2}-\dfrac{s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\hat{z}\end{align}$$
$$\begin{align}
\vec\nabla\cdot\vec{J}&=\vec\nabla\cdot\left(\dfrac{4A_0}{\mu_0}\left(\dfrac{1}{a^2}-\dfrac{s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\hat{z}\right)\\
&=\dfrac{\partial}{\partial z}\left(\dfrac{4A_0}{\mu_0}\left(\dfrac{1}{a^2}-\dfrac{s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\right)\\
\Aboxed{\vec\nabla\cdot\vec{J}&=0}
\end{align}$$

**d.2)** What does the value of the divergence imply, in terms of Griffiths’s Equation 5.29?
$$\left(\vec\nabla\cdot\vec{J}=-\dfrac{\partial\rho}{\partial t}\right)\wedge\left(\vec\nabla\cdot\vec{J}=0\right)\implies
\boxed{\dfrac{\partial\rho}{\partial t}=0}$$
This shows that there is no net flow of charge from anywhere in the domain since the divergence of the current density is zero.


### Question 2

**a)** *We frequently use the relation for current density $\vec J = nq\vec{v}$, where $n$ is the number density (number per volume) of charge carriers, $q$ is the charge of each carrier, and $\vec v$ is the average velocity of the charge carriers (the “drift” velocity). This is not, strictly speaking, the definition of $\vec J$, but rather a derived expression. Briefly but clearly summarize in your own words the chain of arguments in its derivation. A little sketch may be helpful. You might also review Griffiths Section 5.1.3.*

The way I had interpreted the derivation is to be the following:
$$\begin{align}
\vec{J}&=\dfrac{dI}{dA_\perp}\\
&=\dfrac{d}{dA_\perp}\dfrac{dQ}{dt}\\
&=\dfrac{d^2Q}{dA_\perp}\dfrac{1}{dt}\cdot\dfrac{dx_\parallel}{dx_\parallel}\\
&=\dfrac{d^2Q}{dA_\perp dx_\parallel}\dfrac{dx_\parallel}{dt}\\
&=\dfrac{d(Nq)}{dV}\dfrac{dx_\parallel}{dt}\\
\Aboxed{\vec{J}&=nq\vec{v}}
\end{align}$$
I had a hard time putting my ideas into words, but this is the mathematical expressions in my head that I was processing.


**b)** *In most metals, there is roughly one conduction electron per atom. Consider a copper wire (1 mm diameter) carrying a current of 10 A (these numbers are typical of home wiring). Compute the drift velocity of electrons in this wire. Is it surprising? Comment, briefly.*

$$\begin{align}
A&=\pi(0.5\ \mathrm{mm})^2= 7.854\cdot10^{-7}\mathrm{m}^2\\
I&=10\mathrm{A}\\
J&=\dfrac{I}{A}=\dfrac{10\mathrm{A}}{7.854\cdot10^{-7}\mathrm{m}^2}=1.273\cdot10^{7}\dfrac{\mathrm{A}}{\mathrm{m}^2}\\
n&=\dfrac{8960\ \mathrm{kg}}{1\ \mathrm{m}^3}\cdot\dfrac{1\ \mathrm{mol}\ e^-}{0.063546\ \mathrm{kg}} = \dfrac{1.41\cdot10^5\ \mathrm{mol}\ e^-}{1\ \mathrm{m}^3} = 8.491\cdot10^{28}\ \dfrac{e^-}{\mathrm{m}^3}
\end{align}$$
$$J=nqv\implies v=\dfrac{J}{nq}=\dfrac{1.273\cdot10^{7}\dfrac{\mathrm{A}}{\mathrm{m}^2}}{\left(8.491\cdot10^{28}\ \dfrac{e^-}{\mathrm{m}^3}\right)\left(1.602\cdot10^{-19}\ \dfrac{\mathrm{C}}{e^-}\right)}$$
$$\boxed{v_\text{drift}=9.359\cdot10^{-4}\dfrac{\mathrm{m}}{\mathrm{s}}}$$
I'm not surprised that they move slowly, since I've seen this demonstration before.
However, when I saw it for the first time, I was amazed at how slow they are.
Electromagnetism deals with speeds near the speed of light, so seeing electrons barely move was definitely a shock.


**c)** *If I stretch a given piece of copper wire, making it 0.1% longer, how much would this (roughly) change the resistance from end to end? What assumptions are you making?*

Assuming that this copper is ohmic, then we can say that $R=\rho\dfrac{l}{A}$.
$$R_{k\cdot l}-R_l=\rho\dfrac{kl}{A}-\rho\dfrac{l}{A}=\rho\dfrac{l}{A}(k-1)=R_0(k-1)$$
$$\Delta R=R_0(k-1)=R_0(1+0.1\%-1) = (0.1\%)R_0$$
The resistance of the wire would change by about $1/1000$ of the original resistance.


**d)** *Suppose I connect two 1-mm diameter wires end to end, made of different materials, copper to gold. When 10 A flows through the system, a thin layer of charge appears at the boundary. Estimate the total charge that has accumulated at the boundary. (I took a guess that it will come out + in the figure. Did I get it right? What determines this sign? Note: Griffiths Table 7.1 may be helpful here, and of course our usual boundary conditions, back in Griffiths Chapter 2.3.5.)*

I was confused on what I needed to do and all I needed was Hasan saying "Boundary Conditions" and I was like "oh duh, obviously."

$$\begin{align}
E_\text{above}^\perp-E_\text{below}^\perp&=\dfrac{\sigma}{\epsilon_0}\\
\dfrac{J^\perp}{\sigma_\text{cu}}-\dfrac{J^\perp}{\sigma_\text{au}}&=\dfrac{\sigma}{\epsilon_0}\\
\epsilon_0J^\perp\left(\dfrac{1}{\sigma_\text{cu}}-\dfrac{1}{\sigma_\text{au}}\right)&=\sigma\\
\end{align}$$
---
$$\begin{align}
\sigma&=\epsilon_0J^\perp\left(\dfrac{1}{\sigma_\text{cu}}-\dfrac{1}{\sigma_\text{au}}\right)\\
&=\left(8.854\cdot10^{-12}\dfrac{\mathrm{F}}{\mathrm{m}}\right)\left(1.273\cdot10^{7}\dfrac{\mathrm{A}}{\mathrm{m}^2}\right)\left(\dfrac{1}{5.96\cdot10^7\dfrac{\mathrm{S}}{\mathrm{m}}}-\dfrac{1}{4.11\cdot10^7\dfrac{\mathrm{S}}{\mathrm{m}}}\right)\\
\Aboxed{\sigma&=-8.5124\cdot10^{-13}\dfrac{\mathrm{C}}{\mathrm{m^2}}}
\end{align}$$

### Question 3
*The region between two concentric metal spherical shells (radius $a$ and $b$, respectively) is filled with a weakly conducting material of conductivity $\sigma$. Assume the outer shell is electrically grounded, and a battery maintains a potential difference of $|V|=V_0$ between the two shells. (In this problem, be careful not to confuse conductivity, $\sigma$, with surface charge density. Also, ignore any dielectric properties of the weakly conducting material.)*

**a.1)** *What total current, $I$, flows between the shells?*
$$\begin{align}
\Delta V&=\int I(r)dR(r)\\
&=\int_a^b I(r)\cdot \dfrac{dr}{4\pi r^2\sigma}\\
&=\dfrac{1}{4\pi\sigma}\int_a^b \left(I(r)\cdot \dfrac{1}{ r^2}\right)dr\\
\dfrac{1}{4\pi\sigma}\dfrac{d}{dr}\int_a^b \left(I(r)\cdot \dfrac{1}{ r^2}\right)dr&=\left(I(r)\cdot \dfrac{1}{ r^2}\right|_a^b=0\\
&=\dfrac{I(b)}{b^2}=\dfrac{I(a)}{a^2}
\end{align}$$
Current Density must be constant. This gives us a hint for:
$$\begin{align}
I&=\int\vec{J}\cdot d\vec{A}\\
&=\int J\hat{r}\cdot \hat{r}\ dA\\
\Aboxed{I&=4\pi J\left(b^2-a^2\right)}
\end{align}$$
$$\begin{align}
\Delta V&=IR\\
V_0 &= \dfrac{4\pi}{4\pi\sigma}J\left(b^2-a^2\right)\left(\dfrac{1}{a}-\dfrac{1}{b}\right)\\
\sigma V_0 &= J\left(b^2-a^2\right)\left(\dfrac{b-a}{ab}\right)\\
\Aboxed{J &= \dfrac{\sigma (ab)}{\left(b^2-a^2\right)\left(b-a\right)} V_0}\\
\Aboxed{I &= \dfrac{4\pi\sigma}{\left(\dfrac{1}{a}-\dfrac{1}{b}\right)} V_0}\\
\end{align}$$

**a.2)** *What is the total resistance, $R$, of the weakly conducting material between the shells?*
$$\begin{align}
R&=\int dR(r)\\
&=\int_a^b \dfrac{dr}{A(r)\sigma}\\
&=\int_a^b \dfrac{dr}{4\pi r^2\sigma}\\
&=\dfrac{1}{4\pi\sigma}\int_a^b \dfrac{dr}{r^2}\\
\Aboxed{R &=\dfrac{1}{4\pi\sigma}\left(\dfrac{1}{a}-\dfrac{1}{b}\right)}
\end{align}$$

**b.1)** *Revisit Griffiths section 2.5.4, and re-express your final answers (for $I$ and $R$) in part a, in terms of the total capacitance, $C$, for this same arrangement of two concentric shells.*

$$\begin{align}
I &= \dfrac{4\pi\sigma}{\left(\dfrac{1}{a}-\dfrac{1}{b}\right)} V_0\\
&=\dfrac{\sigma}{\epsilon}\dfrac{4\pi\epsilon}{\left(\dfrac{1}{a}-\dfrac{1}{b}\right)} V_0\\
\Aboxed{I&=\dfrac{\sigma}{\epsilon}C V_0}\\
R &=\dfrac{1}{4\pi\sigma}\left(\dfrac{1}{a}-\dfrac{1}{b}\right)\\
&=\dfrac{\epsilon}{\sigma}\dfrac{1}{4\pi\epsilon}\left(\dfrac{1}{a}-\dfrac{1}{b}\right)\\
\Aboxed{R&=\dfrac{\epsilon}{\sigma C}}\\
V&=IR=\left(\dfrac{\sigma}{\epsilon}C V_0\right)\left(\dfrac{\epsilon}{\sigma C}\right)\\
&=\left(C V_0\right)\left(\dfrac{1}{ C}\right)\\
V &= V_0
\end{align}$$

**b.2)** *Now, suppose the battery maintaining $|V|=V_0$ between the concentric spheres is suddenly disconnected at $t = 0$. At $t = 0$, $\Delta V$ between the inner and outer spheres is thus $V_0$, but there is no battery to maintain this. Describe qualitatively what you expect happens over time.*

Between the 2 spheres, there'll be a current in the medium in-between that will slow equalize the voltages on both surfaces, and this will be an exponential decay.


**b.3)** *Then, calculate the voltage, and the current that flows, between the two shells as a function of time, i.e., find $V(t)$ and $I(t)$. Does your calculation agree with your qualitative prediction?*
$$Q(t)=CV(t), I(t)=V(t)/R \implies CV'(t)=V(t)/R$$
$$V'(t)=\dfrac{1}{RC}\cdot V'(t) \implies V(t)=Ae^{-\tfrac{t}{RC}}$$
$$V'(0)=A=V_0$$
$$\begin{align}
\Aboxed{V(t)&=V_0e^{-\tfrac{t}{\tau}}, \ \ \ \tau=RC}\\
\Aboxed{I(t)&=\dfrac{V_0}{R}e^{-\tfrac{t}{\tau}}, \ \ \ \tau=RC}
\end{align}$$
These agree with my conjecture that this would look like an RC circuit with an exponential decay discharging.


c) *For the situation of part b, calculate the original total energy stored in the spherical capacitor (use Griffiths Eq. 2.55). By time-integrating Power (that is, $V\cdot I$), explicitly confirm that the heat delivered to the resistance is equal to the energy lost.*

$$\begin{align}
\int_0^t P(t)dt &= -\int_0^t V(t)\cdot I(t)\ dt\\
&= -\int_0^t \left(V_0e^{-\tfrac{t}{\tau}}\right)\cdot\left(\dfrac{V_0}{R}e^{-\tfrac{t}{\tau}}\right)\ dt\\
&= -\dfrac{V_0^2}{R}\int_0^t e^{-\tfrac{2t}{\tau}}\ dt\\
&= \dfrac{\tau}{2}\dfrac{V_0^2}{R}\left(e^{-\tfrac{2t}{\tau}}\right|_0^t\\
&= \dfrac{RC}{2}\dfrac{V_0^2}{R}\left(e^{-\tfrac{2t}{\tau}}-1\right)\\
\Aboxed{E_\text{losted}&= -\dfrac{1}{2}CV_0^2\left(1-e^{-\tfrac{2t}{\tau}}\right)}
\end{align}$$
$$\begin{align}
\int_0^t P(t)dt &= \int_0^t V(t)\cdot I(t)\ dt\\
&= \int_0^t I(t)R\cdot I(t)\ dt\\
&= R\int_0^t I(t)^2\ dt\\
&= R\int_0^t \left(\dfrac{V_0}{R}e^{-\tfrac{t}{\tau}}\right)^2\ dt\\
&= \dfrac{RV_0^2}{R^2}\int_0^t \left(e^{-\tfrac{t}{\tau}}\right)^2\ dt\\
&= \dfrac{\tau}{2}\dfrac{V_0^2}{R}\left(1-e^{-\tfrac{2t}{\tau}}\right)\\
&= \dfrac{RC}{2}\dfrac{V_0^2}{R}\left(1-e^{-\tfrac{2t}{\tau}}\right)\\
\Aboxed{E_\text{heat}&= \dfrac{1}{2}CV_0^2\left(1-e^{-\tfrac{2t}{\tau}}\right)}\\
\end{align}$$
$$\implies \boxed{E_\text{lost}=-E_\text{heat}}$$


**d.1)** *Extra Credit: Adapt your equation for the resistance of the system to a situation where a single conducting sphere of radius $a$ is embedded in a VERY large uniform volume with conductivity $\sigma$ out to infinity (with the conducting sphere held at a potential of $V_0$ with respect to infinity).*

$$\begin{align}
I &= \dfrac{4\pi\sigma}{\left(\dfrac{1}{a}-\dfrac{1}{b}\right)} V_0
&\implies&&I &= 4\pi\sigma a V_0\\
R &= \dfrac{1}{4\pi\sigma}\left(\dfrac{1}{a}-\dfrac{1}{b}\right)
&\implies&& R &= \dfrac{1}{4\pi a\sigma}\\
C &= \dfrac{4\pi\epsilon}{\left(\dfrac{1}{a}-\dfrac{1}{b}\right)}
&\implies&&C &= 4\pi\epsilon a
\end{align}$$

**d.2)** *Extra Credit: What is the resistance for this system (for current from the conductor out to infinity)?*
$$R=\dfrac{1}{(4\pi\sigma) a}$$

**d.3)** *Extra Credit: Now use the above in the following real-world application: take a single spherical conductor of radius $a_1$, and lower it by a conducting wire into a large, deep, body of water. Do the same with a second conducting sphere of radius $a_2$, located a significant distance away. (Carefully consider: What does "significant" mean here?) Then set up a fixed potential difference of $|V|=V_0$ between the two spheres with a car battery.*

$$\begin{align}
&\text{Sphere A} & &\text{Sphere B}\\
I &= 4\pi\sigma a_1 V_0 & I &= 4\pi\sigma a_2 V_0\\
R &= \dfrac{1}{4\pi a_1\sigma} & R&=\dfrac{1}{4\pi a_2\sigma}\\
C &= 4\pi\epsilon a_1 & C &= 4\pi\epsilon a_2
\end{align}$$

**d.4)**  Describe what electrical quantity (or quantities) you would measure to determine the resistivity $\rho$ of the water medium in which these two spheres are immersed. Include a formula telling how you would deduce $\rho$ from what you measured. Putting in plausible numbers, do you think this experiment could work in practice (e.g. to measure the resistivity of sea-water)?

$$I = 4\pi\sigma a V_0 \implies \sigma=\dfrac{I}{4\pi a V_0} \implies \rho=\dfrac{4\pi a V_0}{I}$$
$$\Delta I = 4\pi\sigma a V_0 \implies \sigma=\dfrac{\Delta I}{4\pi (\Delta a) V_0} \implies \boxed{\rho=4\pi V_0\dfrac{\Delta a}{\Delta I}}$$

### Question 4
Consider a parallel-plate capacitor attached to a battery of constant voltage $V_0$ as shown in the diagram on the right. The plates are separated by a distance $d$. The plates are square with area $L^2$, where $L\gg d$, so that the edge effects are negligible (the diagram exaggerates the dimension $d$). The space between the plates is filled with a weakly conducting material that has a *non-constant* conductivity, a conductivity that depends on position $x$ between the plates as $\sigma(x)=\sigma_0+\sigma'x$, where $\sigma_0>0$ and $\sigma'>0$. Ignore dielectric properties.

**a)** Consider the following quantities: current $I$, current density $\vec J$, electric field $\vec E$, and voltage $V$. Which of these quantities is uniform (i.e. independent of position) in the space between the plates? Explain.

**Note: This assumes that $\sigma'(x)\ne 0$**

 - Both current $I$ and current density $\vec J$ would be independent of space if the conductivity $\sigma(x)$ was constant. Since $\sigma(x)$ scales linearly with distance, the current $I$ and current density $\vec J$ are **not independent** of distance.

 - The electric field $\vec E$ is not constant since the spacing of voltage potential lines are non-uniform, and so the electric field $\vec{E}$ is **not independent** of distance.

 - As the distance increases, the current encounters more resistance, and so the field lines of Voltage would not be uniform. Therefore $V$ is **not independent** of distance.

**b.1)** *Make a qualitative sketch of magnitude of field vs position $x$.*
I actually did Question 4D before 4B, so that's where I got my resistance values.
$$\begin{align}
R&=\dfrac{1}{\sigma'L^2}\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right) &\implies V(x)&=\dfrac{I_0}{\sigma'L^2}\ln\left(1+\dfrac{\sigma'}{\sigma_0}x\right)\\
&&\implies I_0&=\dfrac{V_0\sigma'L^2}{\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}
\end{align}$$
$$\begin{align}
\vec\nabla\ V(x) &= \vec\nabla\left(V_0\cdot\dfrac{\ln\left(1+\dfrac{\sigma'}{\sigma_0}x\right)}{\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\right)\\
&=\dfrac{V_0}{\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\dfrac{\partial}{\partial x}\left(\ln\left(1+\dfrac{\sigma'}{\sigma_0}x\right)\right)\hat{x}\\
&=\dfrac{V_0}{\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\left(\dfrac{\dfrac{\sigma'}{\sigma_0}}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)}\right)\hat{x}\\
\vec{E}&=-\dfrac{V_0\sigma'}{\sigma_0\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\left(\dfrac{1}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)}\right)\hat{x}
\end{align}$$
![[HW3_Q4B.png]]
The graph follows a $1/(1+x)$ distribution, which makes sense since the further the plates get apart the more resistance is added along the way non-linearly.


**b.2)** Show that your expression makes sense by considering the limit where $\sigma'\rightarrow 0$.
$$\begin{align}
\lim_{\sigma'\rightarrow\ 0}\vec{E}(x)&=\lim_{\sigma'\rightarrow\ 0}-\dfrac{V_0\sigma'}{\sigma_0\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\left(\dfrac{1}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)}\right)\hat{x}\\
&=-\dfrac{V_0}{\sigma_0}\hat{x}\lim_{\sigma'\rightarrow\ 0}\dfrac{\sigma'}{\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\dfrac{1}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)}\\
&=-\dfrac{V_0}{\sigma_0}\hat{x}\left(\dfrac{\sigma_0}{d}\right)\\
\Aboxed{\lim_{\sigma'\rightarrow\ 0}\vec{E}(x)&=-\dfrac{V_0}{d}\hat{x}}
\end{align}$$
As $\sigma'\rightarrow 0$, the Electric Field becomes uniform.


**c)** *Perhaps slightly surprising (but related conceptually to the last part of question 2d from earlier in the assignment), I claim the steady-state charge density in the region between the plates is non-zero! Show this, by deriving an expression for the charge density $\rho$ (watch out: $\rho$ here is now charge density, NOT resistivity!) between the plates in terms of the known quantities in the problem, and check that your answer makes sense by considering the limit where $\sigma'\rightarrow 0$, i.e. the limit of uniform conductivity. Also explain your results briefly (being sure to include a physical justification for the sign of the charge density)*


$$\begin{align}
\rho(x)&=\epsilon_0\vec\nabla\cdot\vec{E}\\
&=\epsilon_0\vec\nabla\cdot\left(-\dfrac{V_0\sigma'}{\sigma_0\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\left(\dfrac{1}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)}\right)\hat{x}\right)\\
&=-\dfrac{V_0\epsilon_0\sigma'}{\sigma_0\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\dfrac{\partial}{\partial x}\left(\dfrac{1}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)}\right)\hat{x}\\
&=-\dfrac{V_0\epsilon_0\sigma'}{\sigma_0\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}\left(\dfrac{-\left(\dfrac{\sigma'}{\sigma_0}\right)}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)^2}\right)\\
&=\dfrac{V_0\epsilon_0(\sigma')^2}{\sigma_0^2\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}  \dfrac{1}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)^2}\\
\Aboxed{\rho(x)&=\dfrac{V_0\epsilon_0(\sigma')^2}{\sigma_0^2\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}  \dfrac{1}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)^2}}
\end{align}$$
$$\begin{align}
\lim_{\sigma'\rightarrow\ 0}\rho(x)&=\lim_{\sigma'\rightarrow\ 0}\dfrac{V_0\epsilon_0(\sigma')^2}{\sigma_0^2\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)}  \dfrac{1}{\left(1+\dfrac{\sigma'}{\sigma_0}x\right)^2}\\
&=\dfrac{V_0\epsilon_0}{\sigma_0^2}\lim_{\sigma'\rightarrow\ 0}\dfrac{(\sigma')^2}{\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)\left(1+\dfrac{\sigma'}{\sigma_0}x\right)^2}\\
\Aboxed{\lim_{\sigma'\rightarrow\ 0}\rho(x)&=0}
\end{align}$$
What we can see here is that there is a charge density within the material when its conductance has a linear dependence on distance, and when that term approaches zero there is no longer any charge density!


**d.1)** *Derive an expression for the total resistance $R$ of the material between the plates.*
$$\sigma(x)=\sigma_0+\sigma'x \implies \rho(x)=\dfrac{1}{\sigma_0+\sigma'x}$$
$$\begin{align}
R&=\int_0^d dR(x)\\
R&=\int_0^d \rho(x)\dfrac{dx}{L^2}\\
R&=\dfrac{1}{L^2}\int_0^d \dfrac{1}{\sigma_0+\sigma'x}dx\\
R&=\dfrac{1}{L^2}\left.\dfrac{\ln\left(\sigma_0+\sigma'x\right)}{\sigma'}\right|_0^d\\
R&=\dfrac{1}{\sigma'L^2}\left(\ln\left(\sigma_0+\sigma'd\right){}-\ln\sigma_0\right)\\
R&=\dfrac{1}{\sigma'L^2}\ln\left(\dfrac{\sigma_0+\sigma'd}{\sigma_0}\right){}\\
R&=\dfrac{1}{\sigma'L^2}\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)\\
\end{align}$$

**d.2)** Show that your expression makes sense by considering the limit where $\sigma'\rightarrow 0$.
$$\begin{align}
\lim_{\sigma'\rightarrow\ 0}R&=\lim_{\sigma'\rightarrow\ 0}\dfrac{1}{\sigma'L^2}\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)\\
&=\dfrac{1}{L^2}\lim_{\sigma'\rightarrow\ 0}\dfrac{1}{\sigma'}\ln\left(1+\dfrac{\sigma'}{\sigma_0}d\right)\\
&=\dfrac{1}{L^2}\lim_{\sigma'\rightarrow\ 0}\dfrac{1}{\sigma'}\left(\dfrac{\sigma'}{\sigma_0}d+\dfrac{(\sigma')^2d^2}{2\sigma_0^2}+\dots\right)\\
&=\dfrac{1}{L^2}\lim_{\sigma'\rightarrow\ 0}\dfrac{1}{\sigma'}\left(\dfrac{\sigma'}{\sigma_0}d\right)+\dfrac{1}{L^2}\lim_{\sigma'\rightarrow\ 0}\dfrac{1}{\sigma'}\left(\dfrac{(\sigma')^2d^2}{2\sigma_0^2}+\dots\right)\\
\Aboxed{\lim_{\sigma'\rightarrow\ 0}R&=\dfrac{d}{\sigma_0L^2}}
\end{align}$$
As $\sigma'\rightarrow0$, we return to a resistance that's linear in distance!