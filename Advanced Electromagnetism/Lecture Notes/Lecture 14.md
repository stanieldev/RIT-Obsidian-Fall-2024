**Name:** Stanley Goodwin
**Date:** 10/10/2024

---

Exam day!

### Types of Current
**Line Current (Unphysical)**
$$\begin{align}
\vec{I}(s,\phi,z)&=I(s,\phi,z)\cdot\delta(s-s_0)\cdot\delta(\phi-\phi_0)\cdot\delta(z-z_0)\\
\end{align}$$
**Surface Current**
$$\begin{align}
K_s(s,\phi,z)&=I(s,\phi,z)\cdot\delta(\phi-\phi_0)\cdot\delta(z-z_0)\hat{s}\\
K_\phi(s,\phi,z)&=I(s,\phi,z)\cdot\delta(s-s_0)\cdot\delta(z-z_0)\hat{\phi}\\
K_z(s,\phi,z)&=I(s,\phi,z)\cdot\delta(s-s_0)\cdot\delta(\phi-\phi_0)\hat{z}\\
\end{align}$$
**Volume Current**
$$\begin{align}
J_{\phi,z}(s,\phi,z)&=I(s,\phi,z)\cdot\delta(s-s_0)(\hat{\phi}\times\hat{z})\\
J_{s,z}(s,\phi,z)&=I(s,\phi,z)\cdot\delta(\phi-\phi_0)(\hat{s}\times\hat{z})\\
J_{\phi,s}(s,\phi,z)&=I(s,\phi,z)\cdot\delta(z-z_0)(\hat{s}\times\hat{\phi})\\
\end{align}$$
### Magnetic Fields of Current

**Surface Current**
$$\begin{align}
\vec{B}_s&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{K_s}\times\hat{r}}{r^2}\ d\tau=0\\
\vec{B}_\phi&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{K_\phi}\times\hat{r}}{r^2}\ d\tau\\
&=-\dfrac{\mu_0}{4\pi}\hat{z}\int\dfrac{I(s,\phi,z)\cdot\delta(s-s_0)\cdot\delta(z-z_0)}{s^2}\ d\tau\\
&=-\dfrac{\mu_0}{4\pi}\dfrac{I(s_0,\phi,z_0)}{s_0}\hat{z}\int\ d\phi\\
&=-\dfrac{\mu_0I(s_0,\phi,z_0)}{2s_0}\\
\vec{B}_z&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{K_z}\times\hat{r}}{r^2}\ d\tau\\
&=\dfrac{\mu_0}{4\pi}\hat{\phi}\int\dfrac{I(s,\phi,z)\cdot\delta(s-s_0)\cdot\delta(\phi-\phi_0)}{s^2}\ d\tau\\
&=\dfrac{\mu_0}{4\pi}\hat{\phi}\int\dfrac{I(s_0,\phi_0,z)}{s_0}\ dz\\
&=\dfrac{\mu_0}{4\pi s_0}\hat{\phi}\int I(s_0,\phi_0,z)\ dz\\
&=\dfrac{\mu_0I}{4\pi s_0}z
\end{align}$$
**Volume Current**
$$\begin{align}
\vec{B}&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}\times\hat{r}}{r^2}\ d\tau
\end{align}$$










Let $\vec{J}=K_0\hat{\phi}\cdot\delta(r-R)\cdot\delta(z)$
$$\begin{align}
\vec{B}&=\dfrac{\mu_0}{4\pi}\displaystyle\int\dfrac{\vec{J}\times\hat{r}}{r^2}\ d\tau\\
&=\dfrac{\mu_0K_0}{4\pi}\displaystyle\int\dfrac{\hat{\phi}\times\hat{r}}{r^2}\delta(r-R)\delta(z)\ d\tau\\
&=\dfrac{\mu_0K_0}{4\pi}\hat{z}\displaystyle\int\dfrac{\delta(r-R)\delta(z)\cdot r\ dr\ d\phi\ dz}{r^2}\\
&=\dfrac{\mu_0K_0}{4\pi}\hat{z}\displaystyle\int\dfrac{\delta(r-R)\delta(z)\ dr\ d\phi\ dz}{r}\\
&=\dfrac{\mu_0K_0}{4\pi}\hat{z}\int_0^\infty\dfrac{\delta(r-R)}{r}\ dr\cdot\int_0^{2\pi} d\phi\cdot\int_{-\infty}^\infty\delta(z)\ dz\\
&=\dfrac{\mu_0K_0}{4\pi}\hat{z}\cdot\dfrac{1}{R}\cdot2\pi\cdot1\\
\vec{B}&=\dfrac{\mu_0K_0}{2R}\hat{z}\\
\end{align}$$
However, from boundary conditions, we know that:
$$\begin{align}
\vec{B}_\text{outside}^\parallel-\vec{B}_\text{inside}^\parallel&=\mu_0\left(\vec{K}\times\hat{n}\right)\\
0-\vec{B}_\text{inside}^\parallel&=-\mu_0\left(K_0\hat\phi\times\hat{r}\right)\\
\Aboxed{\vec{B}_\text{inside}^\parallel&=\mu_0K_0\hat{z}}
\end{align}$$
This directly conflicts with the previous evaluation.




Start over, using a new idea:
$$\begin{align}
\vec{B}&=\dfrac{\mu_0}{4\pi}\int\dfrac{Id\vec{l}\times\hat{r}}{r^2}\\
\vec{B}&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{K}dA\times\hat{r}}{r^2}\\
&=\dfrac{\mu_0}{4\pi}\int\dfrac{\tfrac{dI}{dl_\perp}d\vec{l}_\perp d\vec{l}_\parallel\times\hat{r}}{r^2}\\
\vec{B}&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}d\tau\times\hat{r}}{r^2}\\
&=\dfrac{\mu_0}{4\pi}\int\dfrac{\tfrac{dI}{dA_\perp}dA_\perp d\vec{l}_\parallel\times\hat{r}}{r^2}\\
\end{align}$$





$$\begin{align}
\vec{B}&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{K}dA\times\hat{r}}{r^2}\\
&=\dfrac{\mu_0}{4\pi}\int\dfrac{\tfrac{dI}{d\vec{l}_\perp}d\vec{l}_\perp d\vec{l}_\parallel\times\hat{r}}{r^2}\\
\vec{B}&=\dfrac{\mu_0}{4\pi}\int\dfrac{dI}{d\vec{l}_\perp}d\vec{l}_\perp\cdot\int\dfrac{d\vec{l}_\parallel\times\hat{r}}{r^2}\\
\end{align}$$






