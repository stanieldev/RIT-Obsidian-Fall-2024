**Name:** Stanley Goodwin
**Date:** 11/19/2024

---
### Jefimenko's Equations
In the Lorenz Gauge, our general solutions to $V(\vec{r},t)$ and $\vec{A}(\vec{r},t)$ are:
$$\begin{align}
V(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho(\vec{r}', t_R)}{|\vec{r}-\vec{r}'|}\ d\tau'\\
\vec{A}(\vec{r},t)&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}(\vec{r}', t_R)}{|\vec{r}-\vec{r}'|}\ d\tau'\\
\end{align}$$
Where $t_R=t-\dfrac{|\vec{r}-\vec{r}'|}{c}$, called the *retarded time*.
From there, we can get $\vec{E}(\vec{r},t)$ and $\vec{B}(\vec{r},t)$:
$$\begin{align}
\vec{E}(\vec{r},t)&=-\dfrac{\partial}{\partial t}\vec{A}(\vec{r},t)\\
\vec{B}(\vec{r},t)&=\vec\nabla\times\vec{A}(\vec{r},t)\\
\end{align}$$
And using the above, we see that:
$$\begin{align}
\vec{E}(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\left[\dfrac{\rho(\vec{r}', t_R)}{|\mathscr{r}|^2}\hat{r}+\dfrac{\dot\rho(\vec{r}', t_R)}{c|\mathscr{r}|}\hat{r}-\dfrac{\vec{J}(\vec{r},t_R)}{c^2|\mathscr{r}|}\right]d\tau'\\
\vec{B}(\vec{r},t)&=\dfrac{\mu_0}{4\pi}\int\left[\dfrac{\vec{J}(\vec{r},t_R)}{|\mathscr{r}|^2}+\dfrac{\dot{\vec{J}}(\vec{r},t_R)}{c|\mathscr{r}|}\right]\times\hat{\mathscr{r}}\ d\tau'
\end{align}$$
Where $\vec{\mathscr{r}}=\vec{r}-\vec{r}'$ (displacement vector).

### Single Point Charge
If we look at Griffiths Section 10.3, we can see that a single point charge has the potentials:
$$\begin{align}
V(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\dfrac{qc}{\mathscr{r}c-\vec{\mathscr{r}}\cdot\vec{v}}\\
\vec{A}(\vec{r},t)&=\dfrac{\vec{v}}{c^2}V(\vec{r},t)\\
\end{align}$$

