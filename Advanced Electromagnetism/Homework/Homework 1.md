**Name:** Stanley Goodwin
**Date:** 8/31/2024
**Collaborators:** None
**Time Taken:** ~2 Hours

---

**Q1.** *Make a quick sketch, in the x-y plane, of the following (two-dimensional) vector function.*
Plot enough different vectors to give a feeling for what this field looks like in the x-y plane.

$$\begin{align}
f(x,y)&=\dfrac{x}{\left(x^2+y^2\right)^\tfrac{3}{2}}\hat{x}+\dfrac{y}{\left(x^2+y^2\right)^\tfrac{3}{2}}\hat{y}\\
&= \dfrac{r\left(\cos\theta\ \hat{x}+\sin\theta\ \hat{y}\right)}{r^3}\\
\Aboxed{f(r,\theta) &= \dfrac{\hat r}{r^2}}
\end{align}$$

I used my Vector Field grapher that I made during Chaos Theory (PHYS-360).
![[HW1_Q1.png]]

Given both the equation reduction to polar coordinates, as well as the graphical example, it looks to be a field that follows $1/r^2$, so some physical examples could be Universal Gravitation or a Point-Electric Field.


**Q1.** Extra Credit Example

$$\begin{align}
f(r,\theta)&=\dfrac{2\cos\theta}{r^3}\hat{r}+\dfrac{\sin\theta}{r^3}\hat{\theta}\\
f(x,y)&=\dfrac{2\cos\theta}{r^3}\left(\hat{x}\cos\theta+\hat{y}\sin\theta\right)+\dfrac{\sin\theta}{r^3}\left(-\hat{x}\sin\theta+\hat{y}\cos\theta\right)\\
&=\dfrac{2\cos^2\theta}{r^3}\hat{x}+\dfrac{2\sin\theta\cos\theta}{r^3}\hat{y}-\dfrac{\sin^2\theta}{r^3}\hat{x}+\dfrac{\sin\theta\cos\theta}{r^3}\hat{y}\\
&=\left(\dfrac{2\cos^2\theta}{r^3}-\dfrac{\sin^2\theta}{r^3}\right)\hat{x}+\left(\dfrac{2\sin\theta\cos\theta}{r^3}+\dfrac{\sin\theta\cos\theta}{r^3}\right)\hat{y}\\
&=\left(\dfrac{2\cos^2\theta-\sin^2\theta}{r^3}\right)\hat{x}+\left(\dfrac{3\sin\theta\cos\theta}{r^3}\right)\hat{y}\\
\Aboxed{f(x,y)&=\left(\dfrac{2x^2-y^2}{\left(x^2+y^2\right)^\tfrac{5}{2}}\right)\hat{x}+\left(\dfrac{3xy}{\left(x^2+y^2\right)^\tfrac{5}{2}}\right)\hat{y}}
\end{align}$$

![[HW1_Q1E.png]]

The field looks to be like a *dipole* at a far distance, since the distribution drops off as $1/r^3$.


**Q2.** *Given the graphs, A-E, answer the following:*

Which of the following have non-zero *divergence* somewhere?
$\vec\nabla\cdot A = 0$, $\vec\nabla\cdot B = 0$, $\vec\nabla\cdot C > 0$, $\vec\nabla\cdot D > 0$, $\vec\nabla\cdot E > 0$.
**So $C$, $D$, and $E$ have divergences.**

Which of the following have non-zero *curl* somewhere?
$\vec\nabla\times A > 0$, $\vec\nabla\times B > 0$, $\vec\nabla\times C = 0$, $\vec\nabla\times D = 0$, $\vec\nabla\times E = 0$.
**So $A$ and $B$ are have curls.**


**Q3.A** Compute the divergence and curl of the following vector field:
$$\vec F(x,y)=(x+y)\hat x+(y+z)\hat y + (x-2z)\hat z$$
**Divergence:**
$$\begin{align}
\vec\nabla\cdot\vec{F}&=\dfrac{\partial}{\partial x}(x+y)+\dfrac{\partial}{\partial y}(y+z) + \dfrac{\partial}{\partial z}(x-2z)\\
&= 1+1-2\\
\Aboxed{\vec\nabla\cdot\vec{F}&=0}
\end{align}$$
**Curl:**
$$\begin{align}
\vec\nabla\times\vec{F}&=\left(\dfrac{\partial}{\partial y}(x-2z)-\dfrac{\partial}{\partial z}(y+z)\right)\hat{x}-\left(\dfrac{\partial}{\partial x}(x-2z)-\dfrac{\partial}{\partial z}(x+y)\right)\hat{y}+\left(\dfrac{\partial}{\partial x}(y+z)-\dfrac{\partial}{\partial y}(x+y)\right)\hat{z}\\
&=\left(0-1\right)\hat{x}-\left(1-0\right)\hat{y}+\left(0-1\right)\hat{z}\\
\Aboxed{\vec\nabla\times\vec{F}&=-\hat{x}-\hat{y}-\hat{z}}
\end{align}$$
I do not believe it's possible that a physical electrostatic system would exist here, since there is no divergence, as well as the curl being independent of position.


**Q3.B** Given $\rho$, describe the charge distribution in words.
Draw a sketch of where the charges are as well.
$$\rho(\vec{r})=a\delta^3\left(\vec{r}-\vec{R}\right)+b\delta\left(|\vec{r}|-|\vec{R}|\right)$$
This distribution looks to be the sum of:
a) A point charge at $\vec r = (2\mathrm{m}, 0, 0)$.
b) A surface of charge, centered at $(0,0,0)$, with radius $2\mathrm{m}$.

The units for our 2 parameters are:
a) Coulombs $\left(C\right)$.
b) Coulombs per Square Meter $\left(C\ m^{-2}\right)$.

The total charge would be the sum of the charges over their point/surface:
$$\begin{align}
Q &= Q_a+Q_b = a + \left(4\pi(2\mathrm{m})^2\right)\cdot b\\
&= \boxed{a + 16\pi b\ \mathrm{m^2}}
\end{align}$$

**Q4.** Explaining the Electric Field!

a) *What exactly is $\vec E$ ? Define it; how do you think it, both mathematically and in words.*

Electric field is a characterization of a Force on a unit of some importance, which in this case is electric charge. Given a charge of known magnitude at point $P$, there exists a field such that
$$\vec{E}(P)=\dfrac{\vec{F}_\text{Q on q}}{q}$$
Supposing our unit charge to be non-zero, the electric field defines a vector field in all points in space that describes how much force would be applied on a particle, proportional to its charge, over all space.


b) *Given Gauss's Law, and a cube with a uniform electric charge density, can you use Gauss's law to simply compute the value of the electric field for points outside the cube.*

Due to the nature of the electric field pointing radially from the center of charge, and that cubes do not contain surfaces always parallel or normal to the surface, using Gauss's law wouldn't likely be the best usage of it. While Gauss's law is 100% correct, it doesn't help simplify our example much at all.

However, given perhaps that the Gaussian Cube around the charged cube were to be sufficient size, such that $|\vec{r}| \gg L$, the cube would approximate a point charge, so then a Gaussian Cube would be approximated as a Gaussian Sphere.


**Q5.** *Given the electric field $\vec{E}(\vec{x})=(cy)\hat{y}$  :*

a.1) *What are the SI units of $c$?*
Parameter $c$ is in units of $\dfrac{\text{N}}{\text{m}\cdot\text{C}}$.

a.2) *What can you say about $\rho(\vec{x})$ throughout this region?*
We can see the charge distribution looking at the divergence of the E-field.
$$\begin{align}
\vec\nabla\cdot \vec{E} &= c\dfrac{\partial}{\partial y}(y)\\
\dfrac{\rho(\vec{x})}{\epsilon_0}&= c\\
\Aboxed{\rho(\vec{x})&=c\epsilon_0}
\end{align}$$

b) *What is the voltage associated with this E-field?*
Since the field is without curl, it is conservative, and so should be able to be written as a scalar field.
$$V(\vec{x})=-\dfrac{cy^2}{2}+V_0$$
This was found by seeing that $V$ is independent of $x$ and $z$, and so only $y$ has to be figured out.


**Q6.** Ampere's Law Review
*You have an infinitely tall, infinitesimally thin, cylindrical sheet of surface current running around the z-axis $\left(\vec{K}=K_0\hat\phi\right)$ as $s=R$.*

a) *What are the SI units of $K_0$ ?*
Given that a surface current is in units of $\dfrac{\text{A}}{\text{m}}$, $K_0$ should also follow since $\hat\phi$ is unitless.

b) *Sketch the magnitude of the resulting $B$ field as a function of radial distance, $s$.*
I'm not sure what the equation for surface current density is, but I will guess using:
$$\vec{B}=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{J}\times\hat{r}}{r^2}\ d\tau$$
I would expect it to take something like the following form:
$$\vec{B}=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{K}\times\hat{s}}{s^2}\ dA$$
Using this, we can see that, for the outside, it takes the form:
$$\begin{align}
\vec{B}&=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{K}\times\hat{s}}{s^2}\ dA\\
&= \dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{K_0\hat\phi\times\hat{s}}{s^2}\ R\ d\phi\cdot dz\\
\dfrac{d\vec{B}}{dz}&= \dfrac{\mu_0 RK_0}{4\pi}\hat{z}\int_0^{2\pi}\dfrac{1}{s^2}d\phi\\
\Aboxed{\dfrac{d\vec{B}}{dz}&= \dfrac{\mu_0 (2\pi RK_0)}{4\pi s^2}\hat{z}}
\end{align}$$
On the outside of the surface, it looks to have a $1/s^2$ drop-off.
As for the inside, it should be a constant, since this is effectively a solenoid.
$$\dfrac{d\vec{B}}{dz}=\dfrac{\mu_0K_0}{2R}\hat{z}$$
Therefore, it should be like the following ([Link](https://www.desmos.com/calculator/gmpc8i06lq)):
![[HW1_Q6.png]]
I'm not 100% sure about this one, since it's been a long time since I've done magnetostatics.