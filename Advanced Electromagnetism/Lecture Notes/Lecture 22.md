**Name:** Stanley Goodwin
**Date:** 11/12/2024

---
### Gauge Invariance
In last Thursday's worksheet, we had show that $\vec{A}\rightarrow\vec{A}+\vec\nabla\lambda$ doesn't effect the $\vec{B}$ field.
We had also shown that:
$$\oint\vec{E}\cdot d\vec{l}=-\dfrac{d}{dt}\oint\vec{A}\cdot d\vec{l}$$
Which is equivalent to the statement that
$$\vec\nabla\times\left(\vec{E}+\partial_t\vec{A}\right)=0$$
This means we can write $\vec{E}+\partial_t\vec{A}$ as the gradient of a scalar function.
$$\vec{E}+\dfrac{d}{dt}\vec{A}=-\vec\nabla\phi\implies\boxed{\vec{E}=-\vec\nabla\phi-\partial_t\vec{A}}$$
In statics, $\partial_t\vec{A}=0$, and so we recover $\vec{E}=-\vec\nabla\phi$.

Now, given the fact that $\vec{E}=-\vec\nabla\phi-\partial_t\vec{A}$, and that $\vec{A}\rightarrow\vec{A}+\vec\nabla\lambda$, we know that $\vec{E}=\vec{E}'$, a gauge transformation cannot effect the field.
$$\begin{align}
-\vec\nabla\phi-\partial_t\vec{A}&=-\vec\nabla\phi'-\partial_t\vec{A}-\partial_t\vec\nabla\lambda\\
-\vec\nabla\phi&=-\vec\nabla\phi'-\partial_t\vec\nabla\lambda\\
\partial_t\vec\nabla\lambda&=-\vec\nabla(\phi'-\phi)\\
\vec\nabla\partial_t\lambda&=-\vec\nabla(\phi'-\phi)\\
\partial_t\lambda&=-(\phi'-\phi)\\
-\partial_t\lambda&=\phi'-\phi\\
\Aboxed{\phi'&=\phi-\partial_t\lambda}\\
\Aboxed{\vec{A}'&=\vec{A}+\vec\nabla\lambda}
\end{align}$$
This Gauge Transformation doesn't change any physically-measurable quantities, like the $\vec{E}$ and $\vec{B}$ fields, but allows us to change what the divergence of $\vec{A}$ is equal to, which makes it easier to solve Maxwell's Equations.

In total, we can write a potential and get our Electromagnetic Fields:
$$\begin{align}
\phi'&=\phi-\partial_t\lambda&\vec{E}&=-\vec\nabla\phi+\partial_t\vec{A}\\
\vec{A}'&=\vec{A}+\vec\nabla\lambda&\vec{B}&=\vec\nabla\times\vec{A}
\end{align}$$
### Maxwell's Equations with Gauge Invariance

**Gauss's Law**
$$\begin{align}
\vec\nabla\cdot\vec{E}&=\dfrac{\rho}{\epsilon_0}\\
\vec\nabla\cdot\left(-\vec\nabla\phi+\partial_t\vec{A}\right)&=\\
\Aboxed{-\vec\nabla^2\phi+\partial_t\left(\vec\nabla\cdot\vec{A}\right)&=\dfrac{\rho}{\epsilon_0}}
\end{align}$$
**Ampere's Law**
$$\begin{align}
\vec\nabla\times\vec{B}&=\mu_0\vec{J}+\mu_0\epsilon_0\partial_t\vec{E}\\
\vec\nabla\left(\vec\nabla\cdot\vec{A}\right)-\vec\nabla^2\vec{A}&=\mu_0\vec{J}-\dfrac{1}{c^2}\partial_t\vec\nabla\phi+\dfrac{1}{c^2}\partial_t^2\vec{A}
\end{align}$$
### Coulomb Gauge
Condition: $\vec\nabla\cdot\vec{A}=0$.

**Gauss's Law**
$$\begin{align}
-\vec\nabla^2\phi-\partial_t\left(\vec\nabla\cdot\vec{A}\right)&=\dfrac{\rho}{\epsilon_0}
\end{align}$$
**Ampere's Law**
$$\begin{align}
\vec\nabla\left(\vec\nabla\cdot\vec{A}\right)-\vec\nabla^2\vec{A}&=\mu_0\vec{J}-\dfrac{1}{c^2}\partial_t\vec\nabla\phi-\dfrac{1}{c^2}\partial_t^2\vec{A}
\end{align}$$


### Lorenz Gauge
Condition: $\vec\nabla\cdot\vec{A}=\dfrac{1}{c^2}\partial_t\phi$.

**Gauss's Law**
$$\begin{align}
-\vec\nabla^2\phi+\partial_t\left(\vec\nabla\cdot\vec{A}\right)&=\dfrac{\rho}{\epsilon_0}\\
-\vec\nabla^2\phi+\partial_t\left(\dfrac{1}{c^2}\partial_t\phi\right)&=\dfrac{\rho}{\epsilon_0}\\
-\vec\nabla^2\phi+\dfrac{1}{c^2}\partial_t^2\phi&=\dfrac{\rho}{\epsilon_0}\\
\end{align}$$
**Ampere's Law**
$$\begin{align}
...
\end{align}$$

### Maxwell's Equations in Terms of Potentials (Lorenz Gauge)
$$\begin{align}
-\vec\nabla^2\phi+\dfrac{1}{c^2}\partial_t^2\phi&=\dfrac{\rho}{\epsilon_0}\\
-\vec\nabla^2\vec{A}+\dfrac{1}{c^2}\partial_t^2\vec{A}&=\mu_0\vec{J}\\
\end{align}$$
Besides the fact that we have wave equations, this gauge puts $\phi$ and $\vec{A}$ on equal footing.

For solutions to the wave equations, we get:
$$\begin{align}
\phi(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho(\vec{r},t_R)}{|\vec{r}-\vec{r}'|}\ d\tau\\
\vec{A}(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\vec{J}(\vec{r},t_R)}{|\vec{r}-\vec{r}'|}\ d\tau\\
\end{align}$$
The time is no longer the time at the observer, but instead the retarded time.
Effectively, the time of where it *was* $|r|/c$ time ago. It's a latency in the field information.



(Update for Sign Corrections)
https://mycourses.rit.edu/d2l/le/content/1101235/viewContent/10444180/View
