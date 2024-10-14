**Name:** Stanley Goodwin
**Date:** 8/29/2024

---
### Fundamental Theorem of Calculus
$$\begin{align}
\int_a^b\dfrac{d}{dx}f(x)\ dx &= f(b) - f(a)\\
\int\left(\vec\nabla\times\vec{F}(\vec{x})\right)\cdot d\vec{A} &= \oint\vec{F}(\vec{x})\cdot d\vec{l}\\
\int\left(\vec\nabla\cdot\vec{F}(\vec{x})\right)\ d\tau &= \oint\vec{F}(\vec{x})\cdot d\vec{A}
\end{align}$$
### Lorentz Force Law
Tells us what is happening to a charge we are looking at.
$$\vec{F} = q\left(\vec{E}+\vec{v}\times\vec{B}\right)$$
Fields $\vec E$ and $\vec B$ act on a charge and are sourced by the rest of the universe.

### Calculating a (static) Electric Field $(\vec E)$
For a charge sitting at the origin, the field generated takes the form:
$$\vec E = \dfrac{1}{4\pi\epsilon_0}\dfrac{q}{r^2}\hat{r}$$
Since vector field $\vec E$ adds via superposition, a system of charges takes the form:
$$\begin{align}
\vec E_\mathrm{net} &= \displaystyle\sum_i\dfrac{1}{4\pi\epsilon_0}\dfrac{q_i}{r_i^2}\hat{r}_i & \text{(Discrete Charges)}\\
&= \dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho}{r^2}\hat{r}\ d\tau & \text{(Continuum Charges)}
\end{align}$$

### Calculating a (static) Electric Potential $(V)$
If Coulomb or Gauss aren't doing it, can try to attack $\vec E$ via $V$ instead.
There are lots of ways to find $V$, often easier than getting $E$ directly.

Find $V$, then $\vec E = -\vec\nabla V$.
For example, if we know $\rho(\vec{r})$, and the charge doesn't extend to infinity, then $V=\dfrac{1}{4\pi\epsilon_0}\displaystyle\int\dfrac{\rho}{r}d\tau$.

### Boundary Conditions
Chapter 3 of Griffiths gave us all kinds of neat tricks for finding $V$.
All we needed were *boundary conditions*.
#### Surface Electric Fields
For the component of $\vec E$ pointing $\perp$ to the boundary surface: $E^\perp_\mathrm{above}-E^\perp_\mathrm{below} = \dfrac{\sigma}{\epsilon_0}$.
For the component of $\vec E$ pointing $\parallel$ to the boundary surface: $\vec E^\parallel_\mathrm{above}-\vec E^\parallel_\mathrm{below} = 0$.
$\vec E^\parallel$ is continuous across the boundary, because of Stokes Theorem.
$$\oint\vec{E}\cdot d\vec{l} = \int\left(\vec\nabla\times\vec{E}\right)\cdot d\vec{A} = 0 \mathrm{\ as\ } h\rightarrow 0$$
#### Surface Electric Potentials
For $V$: $D_\hat{n}V_\mathrm{above}-D_\hat{n}V_\mathrm{below} = -\dfrac{\sigma}{\epsilon_0}$, coming from $\vec E = -\vec\nabla V$.
For $V$: $V_\mathrm{above}-V_\mathrm{below} = 0$, because $\vec E$ would be infinite if it wasn't $0$.

#### Constraint of Condition
We were able to define $V$ in statics because $\vec\nabla\times\vec{E} = 0$ in statics, which meant $\vec E$ could be thought as the gradient scalar function. In dynamics, $\vec\nabla\times\vec{E} = -\dfrac{d\vec{B}}{dt}$, the idea is more complicated. Need's both $V$ and $\vec{A}$ to find $\vec E$.
