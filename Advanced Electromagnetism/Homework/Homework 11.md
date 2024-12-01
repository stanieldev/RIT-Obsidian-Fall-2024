**Name:** Stanley Goodwin
**Date:** 12/02/2024
**Collaborators:** None
**Time Taken:** XXX Hours

As always, your work will be graded for clarity of explanation as much as for the “correctness” of your final answer. And as always, please include the names of those you collaborated with, as well as the total number of hours spent on this assignment.

---
## Question 1 (Finished)
In this problem, we’ll practice with the vector potential $\vec{A}$ by using it to calculate something we already know: The $\vec{B}$-field of a long straight wire carrying a steady current $I$. But, if we try to compute the vector potential of an *infinitely* long straight wire, we run into a problem: The integral diverges, much the same way our integral for $V$ fails when the charge extends out to infinity). Fortunately, there’s a nice trick for dodging the infinity in such cases:
### 1.A
Compute the vector potential $\vec{A}(s)$ at a distance $s$ from the axis of a long (but finite) straight wire, with limits of integration $-L$ to $L$ (where $L\gg s$) instead of $-\infty$ to $\infty$.
$$\begin{align}
\vec{A}(s)&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}}{r}\ d\tau\\
&=\dfrac{\mu_0}{4\pi}\int_{-L}^{L}\dfrac{I\hat{z}}{\sqrt{s^2+z^2}}\ dz\\
&=\dfrac{\mu_0I}{2\pi}\hat{z}\int_0^{L}\dfrac{1}{\sqrt{s^2+z^2}}\ dz\\
&=\dfrac{\mu_0I}{2\pi}\hat{z}\ln\left(\dfrac{\sqrt{s^2+L^2}+L}{s}\right)\\
\Aboxed{\vec{A}(s)&\approx\dfrac{\mu_0I}{2\pi}\ln\left(\dfrac{2L}{s}\right)\hat{z}}
\end{align}$$
### 1.B
Compute $\vec{B}$ by taking the curl of $\vec{A}$ you found in part a, and then (at the end) taking the limit as $L\rightarrow\infty$. (When computing the curl, be careful about your choice of coordinates. Should you be using the Cartesian form, the cylindrical form, or the spherical form?).
$$\begin{align}
\vec\nabla\times\vec{A}&=-\dfrac{\partial A_z}{\partial s}\hat{\phi}\\
&=-\dfrac{\partial}{\partial s}\left(\dfrac{\mu_0I}{2\pi}\ln\left(\dfrac{2L}{s}\right)\right)\hat{\phi}\\
&=-\dfrac{\mu_0I}{2\pi}\hat{\phi}\cdot\dfrac{1}{\tfrac{2L}{s}}\cdot\dfrac{-2L}{s^2}\\
\Aboxed{\vec{B}&=\dfrac{\mu_0I}{2\pi}\dfrac{1}{s}\hat{\phi}}
\end{align}$$
I used cylindrical coordinates since the wire is nicely expressible as a cylinder.
The $L$ pieces cancel out, and so as $L\rightarrow\infty$ the $\vec{B}$-field converges to the above.

---
## Question 2 (Finished)
At the start of Chapter 10, Griffiths walks us through the reasoning behind Equations
10.2 and 10.3, which are the key formulas relating $\vec{E}$ and $\vec{B}$ to $V$ and $\vec{A}$.
$$\begin{align}
\vec{B}&=\vec\nabla\times\vec{A} & \text{(10.2)}\\
-\vec{E}&=\vec\nabla V+\dfrac{\partial}{\partial t}\vec{A} & \text{(10.3)}\\
\end{align}$$
### 2.A
Substitute these relations into Maxwell’s equations and show that the general equations for the potentials $V(\vec{r},t)$ and $\vec{A}(\vec{r},t)$ (without using any particular gauge condition) are:
$$\begin{align}
\vec\nabla^2V+\dfrac{\partial}{\partial t}\left(\vec\nabla\cdot\vec{A}\right)&=-\dfrac{\rho}{\epsilon_0}\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(\vec\nabla\cdot\vec{A}+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)&=-\mu_0\vec{J}
\end{align}$$
#### Gauss's Law
$$\begin{align}
-\vec\nabla\cdot\vec{E}
&=\vec\nabla\cdot\left(\vec\nabla V+\dfrac{\partial}{\partial t}\vec{A}\right)\\
\Aboxed{-\dfrac{\rho}{\epsilon_0}&=\vec\nabla^2 V+\dfrac{\partial}{\partial t}\left(\vec\nabla\cdot\vec{A}\right)\\}
\end{align}$$
#### Ampere's Law
$$\begin{align}
\vec\nabla\times\vec{B}
&=\vec\nabla\times\left(\vec\nabla\times\vec{A}\right)\\
\mu_0\vec{J}-\dfrac{1}{c^2}\dfrac{\partial}{\partial t}\left(\vec\nabla V+\dfrac{\partial}{\partial t}\vec{A}\right)&=\vec\nabla\left(\vec\nabla\cdot\vec{A}\right)-\vec\nabla^2\vec{A}\\
\mu_0\vec{J}-\dfrac{1}{c^2}\dfrac{\partial}{\partial t}\vec\nabla V-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}&=\vec\nabla\left(\vec\nabla\cdot\vec{A}\right)-\vec\nabla^2\vec{A}\\
\vec\nabla^2\vec{A}-\vec\nabla\left(\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(\vec\nabla\cdot\vec{A}\right)&=-\mu_0\vec{J}\\
\Aboxed{\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(\vec\nabla\cdot\vec{A}+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)&=-\mu_0\vec{J}}
\end{align}$$
### 2.B
The equations in a particular gauge can be obtained from these general equations by substituting in the gauge condition. Derive the differential equations for $V$ and $\vec{A}$ in the Coulomb $\left(\text{i.e. }\vec\nabla\cdot\vec{A}=0\right)$ and Lorenz $\left(\text{i.e. }\vec\nabla\cdot\vec{A}=-\dfrac{1}{c^2}\dfrac{\partial V}{\partial t}\right)$ gauges.
#### Coulomb Gauge
$$\begin{align}
\vec\nabla^2V+\dfrac{\partial}{\partial t}\left(\vec\nabla\cdot\vec{A}\right)&=-\dfrac{\rho}{\epsilon_0}\\
\vec\nabla^2V+\dfrac{\partial}{\partial t}\left(0\right)&=-\dfrac{\rho}{\epsilon_0}\\
\Aboxed{\vec\nabla^2V&=-\dfrac{\rho}{\epsilon_0}}\\
\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(\vec\nabla\cdot\vec{A}+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)&=-\mu_0\vec{J}\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)&=-\mu_0\vec{J}\\
\Aboxed{\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\dfrac{1}{c^2}\dfrac{\partial}{\partial t}\left(\vec\nabla V\right)&=-\mu_0\vec{J}}
\end{align}$$
#### Lorenz Gauge
$$\begin{align}
\vec\nabla^2V+\dfrac{\partial}{\partial t}\left(\vec\nabla\cdot\vec{A}\right)&=-\dfrac{\rho}{\epsilon_0}\\
\vec\nabla^2V+\dfrac{\partial}{\partial t}\left(-\dfrac{1}{c^2}\dfrac{\partial V}{\partial t}\right)&=-\dfrac{\rho}{\epsilon_0}\\
\Aboxed{\dfrac{1}{c^2}\dfrac{\partial^2 V}{\partial t^2}-\vec\nabla^2V&=\dfrac{\rho}{\epsilon_0}}\\
\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(\vec\nabla\cdot\vec{A}+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)&=-\mu_0\vec{J}\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(-\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)&=-\mu_0\vec{J}\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}&=-\mu_0\vec{J}\\
\Aboxed{\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla^2\vec{A}&=\mu_0\vec{J}}
\end{align}$$
### 2.C
Consider a point charge at rest at the origin. As far back as UP2, you learned that $V(\vec{r},t)=\dfrac{q}{4\pi\epsilon_0 r}$, while in 411, the lack of current in this system would seem to suggest that $\vec{A}(\vec{r},t)=0$. Explicitly check to see if we are in the Coulomb gauge, the Lorentz gauge, or perhaps, both, or maybe neither.
#### Coulomb Gauge
$$\begin{align}
\dfrac{\rho}{\epsilon_0}&=-\vec\nabla^2V\\
&=-\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial V}{\partial r}\right)\\
&=-\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(-r^2\dfrac{q}{4\pi\epsilon_0 r^2}\right)\\
\Aboxed{\dfrac{\rho}{\epsilon_0}&=0}
\end{align}$$
It cannot be the Coulomb Gauge since it would imply there is no charge density even though there must be given the problem's details.
#### Lorenz Gauge
$$\begin{align}
\dfrac{\rho}{\epsilon_0}&=\dfrac{1}{c^2}\dfrac{\partial^2 V}{\partial t^2}-\vec\nabla^2V\\
&=0-0\\
\Aboxed{\dfrac{\rho}{\epsilon_0}&=0}
\end{align}$$
It cannot be the Lorenz Gauge as well since it would imply there is no charge density even though there must be given the problem's details.

Therefore, the problem must **not** be in either of the two gauges.
### 2.D
Now, introduce a gauge transformation $\vec{A}_\text{new}=\vec{A}+\vec\nabla\lambda$, $V_\text{new}=V-\partial_t\lambda$, using the
particular choice $\lambda(\vec{r},t)=\dfrac{qt}{4\pi\epsilon_0 r}$. Find the new $V$ and $\vec{A}$. Briefly discuss your results: are the potentials “static” or time dependent? Does this represent the same physical situation, or is something different here? Are we in the Coulomb gauge, or the Lorentz gauge now? (Do we have to be in one of those?) What has changed, what is the same?
$$\begin{align}
V_\text{new}&=V-\partial_t\lambda\\
&=V-\dfrac{\partial}{\partial t}\left(\dfrac{qt}{4\pi\epsilon_0 r}\right)\\
\Aboxed{V_\text{new}&=V-\dfrac{q}{4\pi\epsilon_0 r}}\\
\\
\vec{A}_\text{new}&=\vec{A}+\vec\nabla\lambda\\
&=\vec{A}+\vec\nabla\left(\dfrac{qt}{4\pi\epsilon_0 r}\right)\\
&=\vec{A}+\dfrac{\partial}{\partial r}\left(\dfrac{qt}{4\pi\epsilon_0 r}\right)\hat{r}\\
\Aboxed{\vec{A}_\text{new}&=\vec{A}-\dfrac{qt}{4\pi\epsilon_0 r^2}\hat{r}}
\end{align}$$
The scalar potential is static with time, however the vector potential does have a time-dependence.
We are in neither of the listed gauges, and instead look to be in a monopole gauge of sorts.
Because of the nature of a gauge, there would be no physical difference in the fields of the system, but how we define potentials do change between the gauges.

### 2.E
Look at Griffiths Example 10.1. Explicitly check to see if he is in the Coulomb gauge, the Lorenz gauge, or perhaps, both, or maybe neither.
$$\begin{align}
V&=0 & \vec{A}&=\dfrac{\mu_0k}{4c}(ct-|x|)^2\hat{z},\ \ \ |x|<ct
\end{align}$$
Using the idea that $V=V_0-\partial_t\lambda$, $\vec{A}=\vec{A}_0+\vec\nabla\lambda$, then:
$$\begin{align}
V&=V_0-\partial_t\lambda &\implies&& \lambda(x,t)&=V_0t+\lambda(x)\\
\vec{A}&=\vec{A}_0+\vec\nabla\lambda &\implies&& \lambda(x,t)&=\int\vec{A}_0\ dx+\lambda(t)\\
\end{align}$$
Solving directly, we get that:
$$\begin{align}
\lambda(x,t)&=V_0t+\dfrac{\mu_0k}{12c}\left[(ct)^3+3(ct)^2x-3(ct)x^2\mathrm{sgn}(x)+x^3\right]\\
\end{align}$$
This example is in an entirely different gauge from Coulomb or Lorenz.

---
## Question 3 (Finished)
Say the potentials throughout space and time are $V(\vec{r},t)=0$ and $\vec{A}(\vec{r},t)=A_0\sin\left(k(z-ct)\right)\hat{x}$, where $A_0$ and $k$ are given constants.
$$\begin{align}
\vec{B}&=\vec\nabla\times\vec{A} & \text{(10.2)}\\
-\vec{E}&=\vec\nabla V+\dfrac{\partial}{\partial t}\vec{A} & \text{(10.3)}\\
\end{align}$$
### 3.A
Find the $\vec{E}$ and $\vec{B}$ fields everywhere in space and time, and comment on the physics here.
What is happening in this system?
$$\begin{align}
\vec{E}(\vec{r},t)&=-\vec\nabla V-\dfrac{\partial}{\partial t}\vec{A}\\
&=0-\dfrac{\partial}{\partial t}\left(A_0\sin\left(k(z-ct)\right)\right)\hat{x}\\
\Aboxed{\vec{E}(\vec{r},t)&=ckA_0\cos\left(k(z-ct)\right)\ \hat{x}}\\
\\
\vec{B}(\vec{r},t)&=\vec\nabla\times\vec{A}\\
&=\dfrac{\partial}{\partial z}\left(\ A_0\sin\left(k(z-ct)\right)\ \right)\hat{y}\\
\Aboxed{\vec{B}(\vec{r},t)&=A_0k\cos\left(k(z-ct)\right)\ \hat{y}}\\
\end{align}$$
It looks to be a plane-wave with $\vec{E}$ fields in the $\hat{x}$ direction and $\vec{B}$ fields in the $\hat{y}$ direction.
The direction of propagation would be the $\hat{z}$ direction.
### 3.B
Are we in the Coulomb gauge, the Lorentz gauge, both, or neither?
$$\begin{align}
\vec\nabla\cdot\vec{A}=0
\end{align}$$
With the constraint that $V=0$, **we are both** in the Coulomb and Lorenz gauges.
### 3.C
Use the formulae from Question #2 to find $\rho$ and $\vec{J}$ here. Does the answer agree with your intuition about the physics of this question?
$$\begin{align}
\dfrac{\rho}{\epsilon_0}&=-\vec\nabla^2V\\
\Aboxed{\rho&=0}
\\
\mu_0\vec{J}&=-\vec\nabla^2\vec{A}+\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}\left(\vec\nabla V\right)\\
\mu_0\vec{J}&=0-\dfrac{(kc)^2}{c^2}\vec{A}\\
\Aboxed{\vec{J}&=-\dfrac{A_0}{\mu_0}k^2\sin\left(k(z-ct)\right)\hat{x}}
\end{align}$$
### 3.D
Is it possible, in principle, to find a different gauge for this problem in which $\vec{A}(\vec{r},t)=0$?
(If so, find the gauge transformation. If not, why not?)

If we enforce that $\vec{A}(\vec{r},t)=0$ (implying a lot of other things are 0), we find:
$$\begin{align}
\dfrac{\rho}{\epsilon_0}
&=-\vec\nabla^2V-\dfrac{\partial}{\partial t}\left(\vec\nabla\cdot\vec{A}\right)\\
\Aboxed{\dfrac{\rho}{\epsilon_0}&=-\vec\nabla^2V}\\
\\
\mu_0\vec{J}&=
-\vec\nabla^2\vec{A}+\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}+\vec\nabla\left(\vec\nabla\cdot\vec{A}+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)\\
\Aboxed{\mu_0\vec{J}&=\dfrac{1}{c^2}\dfrac{\partial}{\partial t}(\vec\nabla V)}
\end{align}$$
I do not think this can be written as a gauge. These constrains can be found in terms of their Laplacians and gradients, but I do not think these lead to unique solutions. Unsure.

---
## Question 4
Consider a problem similar in spirit to Griffiths Example 10.2 (which will be very helpful to consult as you work on this one), but instead of an infinite straight wire, we have an infinite SHEET which lies is the 𝑥𝑦-plane. The surface current $K(t)$ for $t\le0$, but at $t=0$, suddenly the surface current turns on, so it is a uniform, constant $K_0$ in the $+x$-direction, instantly, and everywhere in this plane. There is no charge density anywhere in the problem.





## Question 5
## Question 6

## Question 7
In a classical model, an electron in a hydrogen atom would circulate in a nice simple orbit, with radius would be given by Newton’s Second Law, $F=ma$ (so, the attractive Coulomb force from the nucleon on the electron = $\tfrac{mv^2}{r}$). The electron’s total energy is the sum of kinetic and Coulomb potential energy. Use the Newtonian force equation you just wrote down to eliminate “𝑣” from the kinetic energy term, so you have a simple formula for 𝐸(𝑟) for the electron. Now you can take into account radiation, using the Larmor formula (Griffiths Eq 11.70). By conservation of energy, the Larmor formula tells you the rate of loss of energy of the electron. Thus, you can set up an ordinary differential equation for 𝑟(𝑡). Solve it, and then find the time at which the electron would hit the nucleus. Comment on this remarkable result!
#### Energy of the Electron
$$\begin{align}
\dfrac{mv^2}{r}&=\dfrac{1}{4\pi\epsilon_0}\dfrac{q^2}{r}\\
\Aboxed{\dfrac{1}{2}mv^2&=\dfrac{q^2}{8\pi\epsilon_0}}
\end{align}$$$$\begin{align}
E&=\dfrac{1}{2}mv^2-\dfrac{1}{4\pi\epsilon_0}\dfrac{q^2}{r}\\
&=\dfrac{q^2}{8\pi\epsilon_0}-\dfrac{1}{4\pi\epsilon_0}\dfrac{q^2}{r}\\
\Aboxed{E&=\dfrac{q^2}{8\pi\epsilon_0}\left(1-\dfrac{2}{r}\right)}
\end{align}$$
#### Radiative Loss
$$\begin{align}
\dfrac{\partial}{\partial t}E
&=\dfrac{q^2}{8\pi\epsilon_0}\dfrac{\partial}{\partial t}\left(1-\dfrac{2}{r}\right)\\
\dfrac{\mu_0q^2a^2}{6\pi c}&=\dfrac{q^2}{4\pi\epsilon_0}\dfrac{1}{r^2}\dfrac{\partial r}{\partial t}\\
\dfrac{\partial r}{\partial t}&=\dfrac{2\epsilon_0\mu_0a^2}{3c}r^2\\
\dfrac{\partial r}{\partial t}&=\dfrac{2a^2}{3c^3}r^2\\
r(t)&=\left(C-\dfrac{2a^2}{3c^3}t\right)^{-1}\\
r(0)&=1/C\\
\end{align}$$




