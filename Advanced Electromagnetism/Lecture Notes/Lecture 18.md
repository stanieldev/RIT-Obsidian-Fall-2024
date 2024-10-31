**Name:** Stanley Goodwin
**Date:** 10/29/2024

---
### Reflection & Transmission
$$\begin{align}
\tilde{E}_{0\text{T}}&=\dfrac{2}{1+\beta}\tilde{E}_{0\text{I}} & \tilde{E}_{0\text{R}}&=\dfrac{1-\beta}{1+\beta}\tilde{E}_{0\text{I}}\\
T&=\dfrac{\epsilon_2v_2}{\epsilon_1v_1}\dfrac{E^2_{0\text{T}}}{E^2_{0\text{I}}} &
R&=\dfrac{E^2_{0\text{R}}}{E^2_{0\text{I}}}\\
\beta&=\dfrac{n_2}{n_1}=\dfrac{v_1}{v_2}
\end{align}$$
Writing it in terms of the indices of refraction:
$$\begin{align}
\Aboxed{T&=\dfrac{4n_1n_2}{(n_1+n_2)^2}}\\
\Aboxed{R&=\dfrac{(n_1-n_2)^2}{(n_1+n_2)^2}}\\
T+R&=\dfrac{4n_1n_2}{(n_1+n_2)^2}+\dfrac{(n_1-n_2)^2}{(n_1+n_2)^2}\\
&=\dfrac{(n_1-n_2)^2+4n_1n_2}{(n_1+n_2)^2}\\
&=\dfrac{n_1^2-2n_1n_2+n_2^2+4n_1n_2}{(n_1+n_2)^2}\\
&=\dfrac{n_1^2+2n_1n_2+n_2^2}{(n_1+n_2)^2}\\
&=\dfrac{(n_1+n_2)^2}{(n_1+n_2)^2}\\
\Aboxed{T+R&=1}
\end{align}$$
We can use the above to find the following relationships:
$$\begin{align}
n_1\sin(\theta_I)&=n_2\sin(\theta_T) & &\text{(Snell's Law)}\\
\theta_I&=\theta_R & &\text{(Law of Reflection)}\\
\end{align}$$
Next, use the Boundary Conditions from Maxwell's Equations to find $T$ and $R$.
$$\begin{align}
T&=\dfrac{n_2}{n_1}\dfrac{E_{0\text{T}}^2}{E_{0\text{I}}^2}=\dfrac{4n_1n_2}{(n_1+n_2)^2}\\
R&=\dfrac{E_{0\text{T}}^2}{E_{0\text{I}}^2}=\dfrac{(n_1-n_2)^2}{(n_1+n_2)^2}\\
\end{align}$$
For $n_1\gg n_2$: $T=0, R=1$.
For $n_1\approx n_2$: $T=1, R=0$.
For $n_1\ll n_2$: $T=0, R=1$.

**But what about the amplitudes:**
For $n_1\gg n_2$: $\beta=0, E_{0\text{T}}=2E_{0\text{I}}, E_{0\text{R}}=E_{0\text{I}}$.
 - This is okay since intensity depends on both $E$ and $c$, and so they adjust to conserve energy.
For $n_1\approx n_2$: 
 - 
For $n_1\ll n_2$: $\beta=0, E_{0\text{T}}=2E_{0\text{I}}, E_{0\text{R}}=E_{0\text{I}}$.
 - This is okay since intensity depends on both $E$ and $c$, and so they adjust to conserve energy.




### Reflection and Transmission for Oblique Incidence
$$\begin{align}
n_1\sin(\theta_I)&=n_2\sin(\theta_T) & &\text{(Snell's Law)}\\
\theta_I&=\theta_R & &\text{(Law of Reflection)}\\
\end{align}$$
Next, use the Boundary Conditions from Maxwell's Equations to find $T$ and $R$.
We already argued that $\vec{k}\cdot\vec{r}$ and $\omega$ must be the same at an interface.
$$\begin{align}
\vec{E}_I&=\vec{E}_{0I}e^{i\left(\vec{k}_I\cdot\vec{r}-\omega t\right)} &
\vec{B}_I&=\dfrac{\hat{k}_I\times\vec{E_I}}{c_1}\\
\vec{E}_R&=\vec{E}_{0R}e^{i\left(\vec{k}_R\cdot\vec{r}-\omega t\right)} &
\vec{B}_R&=\dfrac{\hat{k}_R\times\vec{E_R}}{c_1}\\
\vec{E}_T&=\vec{E}_{0T}e^{i\left(\vec{k}_T\cdot\vec{r}-\omega t\right)} &
\vec{B}_T&=\dfrac{\hat{k}_T\times\vec{E_T}}{c_2}\\
\end{align}$$
We are going to take the wave to be polarized in the plane of incidence.
$$\begin{align}
\hat{E}&=E_0\left(\hat{x}\cos(\phi)+\hat{z}\sin(\phi)\right) & \hat{B}&=B_0\hat{y}
\end{align}$$
Boundary conditions:
$$\begin{align}
\left.\left(\vec{D}_\text{above}^\perp-\vec{D}_\text{below}^\perp\right)\right|_\text{surface}&=0\\
\left.\left(\vec{B}_\text{above}^\perp-\vec{B}_\text{below}^\perp\right)\right|_\text{surface}&=0\\
\left.\left(\vec{E}_\text{above}^\parallel-\vec{E}_\text{below}^\parallel\right)\right|_\text{surface} &=0\\
\left.\left(\vec{H}_\text{above}^\parallel-\vec{H}_\text{below}^\parallel\right)\right|_\text{surface}&=0
\end{align}$$
If we take $\mu_1=\mu_2$: $\left.\left(\vec{B}_\text{above}^\parallel-\vec{B}_\text{below}^\parallel\right)\right|_\text{surface}=0$
From the first boundary condition:
$$\begin{align}
\vec{D}_\text{above}^\perp&=\vec{D}_\text{below}^\perp\\
\epsilon_1\vec{E}_\text{above}^\perp&=\epsilon_2\vec{E}_\text{below}^\perp\\
-\epsilon_1\vec{E}_{0I}\sin\theta_I+\epsilon_1\vec{E}_{0R}\sin\theta_R&=-\epsilon_2\vec{E}_{0R}\sin\theta_T\\
-\epsilon_1\vec{E}_{0I}\sin\theta_I+\epsilon_1\vec{E}_{0R}\sin\theta_I&=-\epsilon_2\vec{E}_{0R}\dfrac{n_1}{n_2}\sin\theta_I\\
\epsilon_1\left(\vec{E}_{0I}-\vec{E}_{0R}\right)&=\dfrac{n_1}{n_2}\epsilon_2\vec{E}_{0R}\\
\end{align}$$
Using our 3rd boundary condition:
$$\begin{align}
\vec{E}_\text{above}^\parallel&=\vec{E}_\text{below}^\parallel\\
\epsilon_1\vec{E}_{0I}\cos\theta_I+\epsilon_1\vec{E}_{0R}\cos\theta_R&=\epsilon_2\vec{E}_{0R}\cos\theta_T\\
\epsilon_1\left(\vec{E}_{0I}+\vec{E}_{0R}\right)\cos\theta_I&=\epsilon_2\vec{E}_{0R}\cos\theta_T\\
\end{align}$$
We can combine them as:
$$\begin{align}
\vec{E}_{0I}-\vec{E}_{0R}&=\dfrac{n_1}{n_2}\dfrac{\epsilon_2}{\epsilon_1}\vec{E}_{0R}\\
\vec{E}_{0I}+\vec{E}_{0R}&=\dfrac{\epsilon_2}{\epsilon_1}\dfrac{\cos\theta_T}{\cos\theta_I}\vec{E}_{0R}\\
2\vec{E}_{0I}&=\dfrac{\epsilon_2}{\epsilon_1}\left(\dfrac{n_1}{n_2}+\dfrac{\cos\theta_T}{\cos\theta_I}\right)\vec{E}_{0R}\\
\end{align}$$
Woot!
