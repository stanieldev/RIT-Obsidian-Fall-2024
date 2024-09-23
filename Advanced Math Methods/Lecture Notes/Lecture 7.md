**Name:** Stanley Goodwin
**Date:** 9/17/2024

---
### Function $\log(w)$ 
The function $e^z=w$ does not have a unique solution $z$.
The solution is $z=\log(w)=\ln(r)+i\left(\theta+2\pi n\right)$.
The common restriction is using the principle branch $(n=0)$
$$\implies \log(w)=\ln(r)+i\theta, \ \theta\in(-\pi,\pi)$$
### Function $\sqrt{w}=w^{1/2}$
The function $z^2=w$ does not have a unique solution $z$.
The solution is $z=\sqrt{w}=\sqrt{r}e^{i\left(\tfrac{\theta+2\pi n}{2}\right)}$.
We will restrict the domain is using the principle branch $(n=0)$
$$\implies \sqrt{w}=\sqrt{r}e^{i\tfrac{\theta}{2}}, \ \theta\in\left(-\pi,\pi\right)$$
### Functions of the form $w^{1/k}$
The function $z^k=w$ does not have a unique solution $z$.
The solution is $z=w^{1/k}=r^{1/k}e^{i\left(\tfrac{\theta+2\pi n}{k}\right)}$.
We will restrict the domain is using the principle branch $(n=0)$
$$\implies w^{1/k}=r^{1/k}e^{i\tfrac{\theta}{k}},\ \theta\in\left(-\pi,\pi\right)$$
These form the roots of unity, rotated by $\theta$.

### Complex Integration
Let $\omega$ be a 1-form on $\mathbb{C}$.
$$\omega=f(z)dz=f(z)dx + if(z)dy$$
$$\int_\gamma \omega=\int_\gamma f(z)dz=\int_{t_0}^tf(z)\dfrac{\partial z}{\partial t}dt$$
On a close contour on $\omega$, we can find that:
$$\oint_\gamma \omega=2\pi i\sum_{z\in\omega}\mathrm{res}(z)$$

#### Example
Let $f(z)=(z-z_0)^k$, where $k\in\mathbb{Z}$, and $\gamma$ is some contour including $z=z_0$.
$$\begin{align}
\oint_\gamma f(z)dz&=\oint_\gamma (z-z_0)^k\ dz\\
&=\begin{cases}\left.\dfrac{(z-z_0)^{k+1}}{k+1}\right|_\gamma,& k\ne-1\\
\ln|z-z_0|_\gamma,&k=-1\end{cases}\\
\oint_\gamma f(z)dz&=\begin{cases}0,& k\ne-1\\
2\pi i,&k=-1\end{cases}
\end{align}$$
Using a Laurent Series $f(z)=\displaystyle\sum_{k=1}^\infty c_n(z-z_0)^{-k}$, then:
$$\begin{align}
\oint_\gamma f(z)dz&=\oint_\gamma \sum_{k=1}^\infty c_k(z-z_0)^{-k}\ dz\\
&=\sum_{k=1}^\infty c_k\oint_\gamma (z-z_0)^{-k}\ dz\\
\Aboxed{\oint_\gamma f(z)dz&=2\pi i c_1}
\end{align}$$

### Triangle Inequality
This is effectively a continuation of the triangle inequality.
$$\left|\int g(r)\ dr\right|\le\int |g(r)|\ dr$$

### Parboux Theorem
This is an extensions of the triangle inequality for complex functions.
$$\left|\int_\gamma f(z)\ dz\right|\le\int |f(z)|\cdot|dz|\le M\cdot L_\gamma$$
Where $M$ is the maximum value of $f(z)$ on $\gamma$, and $L_\gamma$ is the path length of $\gamma$.
