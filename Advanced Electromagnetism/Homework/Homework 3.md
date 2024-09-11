**Stanley Goodwin | 9/11/2024**

*As always, your work will be graded for clarity of explanation as much as for the “correctness” of your final answer. And as always, please include the names of those you collaborated with, as well as the total number of hours spent on this assignment.*


### Question 1
*Suppose the magnetic vector potential in a region of space is given by*
$$\vec{A}=A_0e^{-\tfrac{x^2+y^2}{a^2}}\hat{z}$$

a) *What are the units of the given constants $a$ and $A_0$* ?
$$\begin{align}
[a]&= \mathrm{m}\\
[A_0]&=\mathrm{T}\cdot\mathrm{m}
\end{align}$$
The units of $a$ are length (meters) and $A_0$ is in terms of B-Field Meters, since $dA = B$.
$$\vec{A}=A_0e^{-\tfrac{x^2+y^2}{a^2}}\hat{z} \implies \vec{A}=A_0e^{-\tfrac{s^2}{a^2}}\hat{z}$$
For the sake of the following, I rewrote $\vec{A}$ in cylindrical coordinates.
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
For current density, I used the static form of Maxwell's equations for the curl of $\vec B$.
$$\begin{align}
\vec\nabla\times\vec{B}&=\left(\dfrac{1}{s}\dfrac{\partial A_z}{\partial\phi}-\dfrac{\partial A_\phi}{\partial z}\right)\hat{s} + \left(\dfrac{\partial A_s}{\partial z}-\dfrac{\partial A_z}{\partial s}\right)\hat{\phi} + \dfrac{1}{s}\left(\dfrac{\partial (sA_\phi)}{\partial s}-\dfrac{\partial A_s}{\partial \phi}\right)\hat{z}=\left(\dfrac{1}{s}\dfrac{\partial (sA_\phi)}{\partial s}\right)\hat{z}\\
&=\left(\dfrac{1}{s}\dfrac{\partial\left(\tfrac{2A_0s^2}{a^2}e^{-\tfrac{s^2}{a^2}}\right)}{\partial s}\right)\hat{z}=\left(\dfrac{1}{s}\dfrac{2A_0}{a^2}\dfrac{\partial\left(s^2e^{-\tfrac{s^2}{a^2}}\right)}{\partial s}\right)\hat{z}\\
&=\dfrac{2A_0}{sa^2}\left(2se^{-\tfrac{s^2}{a^2}}-\dfrac{2s^3}{a^2}e^{-\tfrac{s^2}{a^2}}\right)\\
\mu_0\vec{J}&=\left(\dfrac{4A_0}{a^2}-\dfrac{4A_0s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\\
\Aboxed{\vec{J}&=\dfrac{4A_0}{\mu_0}\left(\dfrac{1}{a^2}-\dfrac{s^2}{a^4}\right)e^{-\tfrac{s^2}{a^2}}\\}
\end{align}$$

b) *Separately sketch $\vec A$, $\vec B$, and $\vec J$ fields. Describe what they look like in English.*


c) *Integrate the current density to show that the total current flowing through any infinite plane parallel to the 𝑥𝑦-plane is zero. Then, give a simple argument (without doing any formal integral) why you might have known before calculating that this must be the case.*


d) *Calculate the divergence of the current density $\vec J$. 
   What does the value of the divergence imply, in terms of Griffiths’s Equation 5.29?*


### Question 2
a) *We frequently use the relation for current density 𝚥⃑ = 𝑛𝑞𝑣⃑, where 𝑛 is the number density (number per volume) of charge carriers, 𝑞 is the charge of each carrier, and 𝑣⃑ is the average velocity of the charge carriers (the “drift” velocity). This is not, strictly speaking, the definition of 𝚥⃑, but rather a derived expression. Briefly but clearly summarize in your own words the chain of arguments in its derivation. A little sketch may be helpful. You might also review Griffiths Section 5.1.3.*

b) *In most metals, there is roughly one conduction electron per atom. Consider a copper wire (1 mm diameter) carrying a current of 10 A (these numbers are typical of home wiring). Compute the drift velocity of electrons in this wire. Is it surprising? Comment, briefly.*

c) *If I stretch a given piece of copper wire, making it 0.1% longer, how much would this (roughly) change the resistance from end to end? What assumptions are you making?*

d) *Suppose I connect two 1-mm diameter wires end to end, made of different materials, copper to gold. When 10 A flows through the system, a thin layer of charge appears at the boundary. Estimate the total charge that has accumulated at the boundary. (I took a guess that it will come out + in the figure. Did I get it right? What determines this sign? Note: Griffiths Table 7.1 may be helpful here, and of course our usual boundary conditions, back in Griffiths Chapter 2.3.5.)*


### Question 3
*The region between two concentric metal spherical shells (radius 𝑎 and 𝑏, respectively) is filled with a weakly conducting material of conductivity 𝜎. Assume the outer shell is electrically grounded, and a battery maintains a potential difference of |𝑉| = 𝑉଴ between the two shells. (In this problem, be careful not to confuse conductivity, 𝜎, with surface charge density. Also, ignore any dielectric properties of the weakly conducting material.)*

a) *What total current, 𝐼, flows between the shells? Also, what is the total resistance, 𝑅, of the weakly conducting material between the shells?*

b) *Revisit Griffiths section 2.5.4, and re-express your final answers (for 𝐼 and 𝑅) in part a, in terms of the total capacitance, 𝐶, for this same arrangement of two concentric shells. Now, suppose the battery maintaining |𝑉| = 𝑉଴ between the concentric spheres is suddenly disconnected at 𝑡 = 0. At 𝑡 = 0, ∆𝑉 between the inner and outer spheres is thus𝑉଴, but there is no battery to maintain this. Describe qualitatively what you expect happens over time. Then, calculate the voltage, and the current that flows, between the two shells as a function of time, i.e., find 𝑉(𝑡) and 𝐼(𝑡). Does your calculation agree with your qualitative prediction?*

c) *For the situation of part b, calculate the original total energy stored in the spherical capacitor (use Griffiths Eq. 2.55). By time-integrating Power (that is, 𝑉 ∗ 𝐼), explicitly confirm that the heat delivered to the resistance is equal to the energy lost*

d) *Extra Credit: Adapt your equation for the resistance of the system to a situation where a single conducting sphere of radius 𝑎 is embedded in a VERY large uniform volume with conductivity 𝜎 out to infinity (with the conducting sphere held at a potential of 𝑉଴ with respect to infinity). What is the resistance for this system (for current from the conductor out to infinity)? Now use the above in the following real-world application: take a single spherical conductor of radius 𝑎ଵ, and lower it by a conducting wire into a large, deep, body of water. Do the same with a second conducting sphere of radius 𝑎ଶ, located a significant distance away. (Carefully consider: What does "significant" mean here?) Then set up a fixed potential difference of |𝑉| = 𝑉଴ between the two spheres with a car battery. Describe what electrical quantity (or quantities) you would measure to determine the resistivity 𝜌 of the water medium in which these two spheres are immersed. Include a formula telling how you would deduce ρ from what you measured. Putting in plausible numbers, do you think this experiment could work in practice (e.g. to measure the resistivity of sea-water)?*


### Question 4
