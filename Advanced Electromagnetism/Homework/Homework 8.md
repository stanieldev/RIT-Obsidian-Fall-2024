**Name:** Stanley Goodwin
**Date:** 10/26/2024
**Collaborators:** Hasan, Chris
**Time Taken:** 4 Hours

---
## Question 1
Consider a 3D electromagnetic plane wave in vacuum, described in complex form by $\vec{E}(\vec{r},t)=\vec{E}_0e^{i\left(\vec{k}\cdot\vec{r}-\omega t\right)}$, where $\vec{E_0}=E_0\hat{y}$, with $\vec{E_0}=|E_0|e^{i\pi/2}$. $\vec{k}$ is the wave vector $k\hat{x}$ and $\omega$ is the angular frequency. As usual, the true field is $\vec{E}_r=\Re\left(\vec{E}\right)$.
### 1.A
*Which direction is the wave moving in, and in what direction does the electric field point?*
$$\begin{align}
\text{Wave Propagation} : \hat{x}\\
\text{Electric Field} : \hat{y}\\
\text{Magnetic Field} : \hat{z}\\
\end{align}$$
*What is the speed, wavelength, and period of the wave?*
$$\begin{align}
v&=\dfrac{\omega}{k}\\
\lambda&=\dfrac{2\pi}{k}\\
T&=\dfrac{2\pi}{\omega}
\end{align}$$
*What does the phase of $\pi/2$ in $\vec{E_0}$ do?*
 - The phase of $\pi/2$ moves the electric wave back by a quarter of a wavelength, shown as a phase offset.

Sketch the true field $\vec{E}_r(x,0,0,0)$ (a 2D plot with x on the horizontal axis) and $\vec{E}_r(0,0,0,t)$ (a 2d plot with t on the horizontal axis). Clearly indicate the direction of the field and the scale of both your axes. *How is the field at $(0,a,0)$ different from the field at $y=0$*?

![[HW8_1AIV_1.png]]
**Figure 1:** Plot of $\vec{E}_r(x,0,0,0)$, scaled by $1/k$ on the $x$-axis, and scaled by $1/|E_0|$ on the $y$-axis.
![[HW8_1AIV_2.png]]
**Figure 2:** Plot of $\vec{E}_r(0,0,0,t)$, scaled by $1/\omega$ on the $x$-axis, and scaled by $1/|E_0|$ on the $y$-axis.

The field at $(0,a,0)$ is identical to the field at $y=0$, since there is no $y$-component.
### 1.B
*Describe in words what this mathematical expression represents physically. Why is this called a plane wave (where is/are the planes)?*
 - The plane wave is a 2D cross-section of space whose normal is in the direction of propagation and the plane spanned by the cross product of $\vec{E}$ and $\vec{B}$. 
 - Alternatively, the "plane" of the plane wave is the plane of the direction that the Electric field is independent of, and so the $y$ and $z$ axes.

*Sketch or represent this in 3d. Describe how the direction of the electric field changes in time. If $\vec{E}$ always points along the same axis, the wave is said to be linearly polarized. Is this wave linearly polarized?*
![[HW8_2.png]]
**Figure 3:** Plot of the plane wave, the span of $\vec{E}$, scaled by $1/k$ on the $x$-axis.

 - The wave is linearly polarized since the plane wave never changes direction. 
 - It always travels in the $x$ direction found in the $\vec{k}$.
### 1.C
Find the associated magnetic field $\vec{B}(\vec{r},t)$ for this plane wave.
Sketch the magnetic fields $\vec{B}(x,0,0,0)$ and $\vec{B}(0,0,0,t)$ (as above, be clear about your axes.
*Describe in words how $B$ compares/contrasts with $E$.*

![[HW8_1C_1.png]]
**Figure 4:** Plot of $\vec{B}_r(x,0,0,0)$, scaled by $1/k$ on the $x$-axis, and scaled by $1/|B_0|$ on the $y$-axis.

![[HW8_1C_2.png]]
**Figure 5:** Plot of $\vec{B}_r(0,0,0,t)$, scaled by $1/\omega$ on the $x$-axis, and scaled by $1/|B_0|$ on the $y$-axis.
 - The time-dependence is identical, since they are in-phase orthogonal waves.
 - The only difference between the fields is the scaling between the two.
### 1.D
Calculate the energy density $\mathcal{U}_\text{EM}$, the Poynting Vector $\vec{S}$, and the momentum density for these fields. Interpret the answers physically—make sense of their units, signs, and directions.
**Note:** The correct way to do this is to take the real parts of E and B first, and then use the usual formulas to find the desired quantities.
$$\begin{align}
\mathcal{U}_\text{EM}&=\epsilon_0 E^2\\
&=\epsilon_0 |\vec{E}_0|^2\cos^2\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)\\
\Aboxed{\mathcal{U}_\text{EM}&=\epsilon_0 E_0^2\cos^2\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)}\\
\Aboxed{\langle\mathcal{U}_\text{EM}\rangle&=\dfrac{1}{2}\epsilon_0 E_0^2}
\end{align}$$
$$\begin{align}
\vec{S}&=\dfrac{\vec{E}\times\vec{B}}{\mu_0}\\
&=\dfrac{\vec{E}\cdot\vec{E}/c}{\mu_0}\hat{k}\\
&=\dfrac{E^2}{c\mu_0}\hat{x}\\
&=c\epsilon_0|\vec{E}_0|^2\cos^2\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)\hat{x}\\
\Aboxed{\vec{S}&=c\epsilon_0E_0^2\cos^2\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)\hat{x}}\\
\Aboxed{\langle\vec{S}\rangle&=c\epsilon_0E_0^2\hat{x}}
\end{align}$$
$$\begin{align}
\vec{\mathbb{P}}&=\dfrac{1}{c^2}\vec{S}\\
&=\dfrac{\epsilon_0E_0^2}{c}\cos^2\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)\hat{x}\\
\Aboxed{\vec{\mathbb{P}}&=\dfrac{\epsilon_0E_0^2}{c}\cos^2\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)\hat{x}}\\
\Aboxed{\vec{\langle\mathbb{P}\rangle}&=\dfrac{\epsilon_0E_0^2}{2c}\hat{x}}
\end{align}$$
---
## Question 2
Write down the real $\vec{E}$ and $\vec{B}$ fields for a monochromatic plane wave of amplitude $E_0$, frequency $f$ (given in Hz), and phase angle $\pi/2$ that is traveling in the direction from the origin to the point $(1,1,0)$ with polarization in the $xy$-plane. Please give the explicit Cartesian components of $\vec{k}$ and also of the $\vec{E}$ and $\vec{B}$ fields. Your final answer might involve new symbols, but they should all be clearly defined in terms of just the two givens ($E_0$ and $f$) and fundamental constants.
$$\begin{align}
\Aboxed{\vec{k}&=\hat{x}+\hat{y}} \implies \hat{k}=\dfrac{1}{\sqrt{2}}\hat{x}+\dfrac{1}{\sqrt{2}}\hat{y}\\
\Aboxed{\vec{E}(x,y,z,t)&=E_0\cos\left(x+y-\omega t+\pi/2\right)\hat{z}}\\
\Aboxed{\vec{B}(x,y,z,t)&=\dfrac{E_0}{c}\cos\left(x+y-\omega t+\pi/2\right)\left(\dfrac{-\hat{x}+\hat{y}}{\sqrt{2}}\right)}
\end{align}$$
---
## Question 3
Let’s superpose two plane waves, $\vec{E}_1$ and $\vec{E}_2$, to find the net electric field. Suppose $\vec{E}_1$ and $\vec{E}_2$ are out of phase and polarized in different directions. In particular,
$$\vec{E}(\vec{r},t)=\vec{E}_1\cos\left(\vec{k}\cdot\vec{r}-\omega t\right)+\vec{E}_2\cos\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)$$
where $\vec{E}_1=E_0\hat{z}$, $\vec{E}_2=E_0\hat{y}$, and $\vec{k}=k\hat{x}$ ($E_0$ and $k$ are given constants).
### 3.A
Simplify $\vec{E}$ to the extent that you can (there’s not much simplifying you can do). 
*Which direction does this wave travel in? How fast is it propagating?*
$$\begin{align}
\vec{E}(\vec{r},t)&=\vec{E}_1\cos\left(\vec{k}\cdot\vec{r}-\omega t\right)+\vec{E}_2\cos\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)\\
&=E_0\left(\hat{z}\cos\left(\vec{k}\cdot\vec{r}-\omega t\right)-\hat{y}\sin\left(\vec{k}\cdot\vec{r}-\omega t\right)\right)\\
&=E_0\left(\hat{z}\cos\left(-\vec{k}\cdot\vec{r}+\omega t\right)+\hat{y}\sin\left(-\vec{k}\cdot\vec{r}+\omega t\right)\right)\\
\end{align}$$
The wave travels in the $\hat{x}$-direction with a speed is $v=\dfrac{\omega}{k}$.
### 3.B
To visualize how this wave varies in time, we’ll consider some fixed spot(s) and picture the wave there as time goes by. Let’s consider all points in space where $\vec{k}\cdot\vec{r}=0$. 

*Describe this set of points in words, then describe in words and sketches what your electric field looks like there (magnitude and direction) as time proceeds.*
$$\begin{align}
\vec{E}(\vec{r},t)&=E_0\left(\hat{z}\cos\left(\omega t\right)+\hat{y}\sin\left(\omega t\right)\right)\\
\end{align}$$
 - The electric field is rotating in a circle of constant radius $E_0$, cycling at $\omega$ radians per sec.
 - I chose not to use a diagram since I think that a video would be better for representation.

 *How would you describe the polarization state? If you look down the axis with the wave approaching you, how would you describe what’s happening to the direction of $\vec{E}$ in time?*
 - It is circularly polarized light, and seems to be right-chiral, but I could be incorrect.
 - When looking head-on, perpendicular to the $yz$-plane, it would appear to cycle counterclockwise around the chosen point.

---
## Question 4
We’ll wrap up this week by considering radiation pressure. On earth, the time-averaged flux of electromagnetic energy $(\langle\vec{S}\rangle)$ from the sun is $0.14\text{ W/cm}^2$.
### 4.A
Consider steady sunlight hitting $1\mathrm{m}^2$ of earth. Picture an imaginary box (containing streaming sunshine) striking this area, with a "box height" of 1 light-second. There is a certain amount of momentum stored in that box, and in one second, ALL of that momentum will strike the $1\mathrm{m}^2$ area. Assuming the EM wave is absorbed (not reflected), what force does that work out to? How does the radiation pressure from this light compare to atmospheric air pressure? And if the earth reflected the sunlight instead, how would that affect the radiation pressure?
$$\begin{align}
I&=\dfrac{\langle P\rangle}{A}=\langle|\vec{S}|\rangle\\
\langle\Delta\vec{\mathbb{P}}\rangle&=\dfrac{\langle|\vec{S}|\rangle}{c^2}=\dfrac{I}{c^2}\\
&=\dfrac{1400\text{ W/}\text{m}^2}{\left(3\cdot10^8\text{ m/s}\right)^2}\\
&\approx1.556\cdot10^{-14}\dfrac{\text{ W/}\text{m}^2}{\text{m}^2\text{/s}^2}\\
\Aboxed{\langle\Delta\vec{\mathbb{P}}\rangle&=1.556\cdot10^{-14}\dfrac{\text{ N}\cdot\text{s}}{\text{m}^3}}
\end{align}$$
Here's where it gets tricky. I assumed that since the above is "per unit volume", I just multiplied by the volume of the box.
$$\begin{align}
|\Delta\vec{p}|&=\langle\Delta\vec{\mathbb{P}}\rangle\cdot V\\
&=\left(1.556\cdot10^{-14}\dfrac{\text{ N}\cdot\text{s}}{\text{m}^3}\right)\cdot\left(1\text{m}
\cdot1\text{m}\cdot3\cdot10^8\text{m}\right)\\
&=\left(1.556\cdot10^{-14}\dfrac{\text{ N}\cdot\text{s}}{\text{m}^3}\right)\cdot\left(1\text{m}
\cdot1\text{m}\cdot3\cdot10^8\text{m}\right)\\
\Aboxed{|\Delta\vec{p}|&\approx4.667\cdot10^{-6}\text{ N}\cdot\text{s}}
\end{align}$$
It was mentioned that the momentum change over 1 second is done all at once, and so:
$$\begin{align}
\vec{F}&=\dfrac{|\Delta\vec{p}|}{\Delta t}\\
&=\dfrac{4.667\cdot10^{-6}\text{ N}\cdot\text{s}}{1\text{ s}}\\
\Aboxed{\vec{F}&=4.667\cdot10^{-6}\text{ N}}\\
\end{align}$$
This was a bit hacky but I think it's reasonable. The pressure is much much much smaller than atmospheric pressure, which is $101\text{ kN}$ per square meter, this would be almost negligible.

Supposing earth reflected the light, the change in momentum would be doubled, and so the force would be doubled, but that would still be a very small force.
### 4.B
These days, it’s (relatively) inexpensive to launch tiny satellites ("CubeSats" one liter in volume with mass of around 1.3 kg) into near-earth orbit. Efforts have also been made to steer and boost these satellites by means of reflective “solar sails.” For this problem, we’ll investigate a very basic model of sailing to the moon. We won’t worry about the complicated orbital mechanics here. Just give me a UP1-level estimate of how long it would take for a satellite to sail from near Earth to the moon by using a reflective solar sail with surface area of $32\text{ m}^2$ (this was the size of LightSail’s sails), accelerated by the constant light pressure alone. What are some advantages and disadvantages you can think of for this propulsion method compared to conventional rocket boosters?

Let's assume that the light pressure would be uniform over the trip and that it has the same characteristics of intensity as 4.A.
$$\begin{align}
|\vec{P}|&=2\cdot4.667\cdot10^{-6}\text{ N}/\text{m}^2\\
|\vec{F}|&=|\vec{P}|\cdot A\\
m\cdot|\vec{a}|&=|\vec{P}|\cdot A\\
|\vec{a}|&=\dfrac{|\vec{P}|\cdot A}{m}\\
&=\dfrac{9.334\cdot10^{-6}\text{ N}/\text{m}^2\cdot 32\text{ m}^2}{1.3\text{ kg}}\\
|\vec{a}|&=2.2974\cdot10^{-4}\text{ m}/\text{s}^2
\end{align}$$
Using the distance to the moon $\Delta x=384,400\mathrm{ km}$ and no initial velocity (assuming it was place into orbit and doesn't need to escape earth):
$$\begin{align}
\Delta x&=\dfrac{1}{2}a(\Delta t)^2\\
\Delta t&=\sqrt{\dfrac{2\Delta x}{a}}\\
&=\sqrt{\dfrac{2\left(384.4\cdot10^6\text{ m}\right)}{2.2974\cdot10^{-4}\text{ m}/\text{s}^2}}\\
&=1,829,314.5\text{ s}\\
\Aboxed{\Delta t&\approx 21\text{ days}, 4\text{ hours}}
\end{align}$$
The advantage to these kinds of objects is that they don't require hauling fuel that is used for their acceleration, and so they can get very small masses.

However, they won't be able to slow down, nor really control how much acceleration it gets. Even if it does have some method of blocking reflected lights, it would require another light source at the location it wants to slow down at. It is also a very tiny force that is good for the vacuum of space, but not necessarily getting it into orbit.
### 4.C
Fine particles of dust in interplanetary space are pushed out of the solar system by radiation pressure from the Sun, too. That’s why the night sky is nice and dark and transparent. Derive an expression for the size (the radius) of a particle (located 1 AU from the sun, so the solar flux is the same as in part A) that is at the critical size where the outward radiation pressure balances the inward pull of gravity. Insert reasonable numbers in your expression and estimate this critical size. Would the answer you get be different if you were closer, or farther, from the sun?

I used an estimated density of space rock of $3\text{ g/}\text{cm}^3=3000\text{ kg/}\text{m}^3$
$$\begin{align}
|\vec{P}|&=4.667\cdot10^{-6}\text{ N}/\text{m}^2\\
|\vec{P}|\cdot \pi r^2&=\dfrac{GMm}{d^2}\\
|\vec{P}|\cdot \pi r^2&=\dfrac{GM\rho\cdot\tfrac{4}{3}\pi r^3}{d^2}\\
r&=\dfrac{|\vec{P}|\cdot \pi d^2}{GM\rho\cdot\tfrac{4}{3}\pi}\\
&=\dfrac{3}{4}\dfrac{|\vec{P}|}{\rho}\dfrac{d^2}{GM}\\
&=\dfrac{3}{4}\dfrac{4.667\cdot10^{-6}\text{ N}/\text{m}^2}{3000\text{ kg/}\text{m}^3}\dfrac{\left(1.496\cdot10^{11}\text{m}\right)^2}{\left(6.674\cdot10^{-11}\text{ N}\cdot\text{m}^2/\text{kg}^2\right)\left(1.989\cdot10^{30}\text{ kg}\right
)}\\
\Aboxed{r&\approx1.967\cdot10^{-7}\text{ m}=196.7\text{ nm}}
\end{align}$$
If I were closer to the sun, the radius would have to be smaller since the intensity of light would be larger when its closer to the sun. Supposing I was further from the sun, the radius can be larger since the amount of light intensity drops off as you get further away.

---
## Question 5
Look back at question 1 part D. You might note that another way you might consider doing part D might could be to use the usual formulas, but plugging in your general (complex) fields, and then only AT THE VERY END taking the real part. Try this for $\mathcal{U}_\text{EM}$ and convince yourself (and me) that this gives a different answer. So beware! Complex notation is great, but when dealing with quadratic quantities like energy density or Poynting vector, you must work with the (real) physical fields)

Supposing we don't know about calculating the modulus:
$$\begin{align}
\mathcal{U}_\text{EM}&=\epsilon_0 E^2\\
&=\epsilon_0\vec{E}_0^2e^{2i\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)}\\
\Aboxed{\mathcal{U}_\text{EM}&=\epsilon_0\vec{E}_0^2e^{2i\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)}}
\end{align}$$
If we know about the modulus:
$$\begin{align}
\mathcal{U}_\text{EM}&=\epsilon_0 E^2\\
&=\epsilon_0E^*_0E_0e^{i\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)}e^{-i\left(\vec{k}\cdot\vec{r}-\omega t+\pi/2\right)}\\
\Aboxed{\mathcal{U}_\text{EM}&=\epsilon_0E^*_0E_0}
\end{align}$$
So both answers give us general nonsense, even if the value does end up being real.
It makes sense, then, why we look at the real part before calculating values using the field.