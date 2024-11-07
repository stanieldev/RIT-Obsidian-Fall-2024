**Name:** Stanley Goodwin
**Date:** 11/7/2024

---
### Heuristic of Linear Response Theory
Physical systems like $\vec{E}(t)\rightarrow\vec{P}(t)$ or $V(t)\rightarrow I(t)$.
These systems have the following properties.
#### Linearity
This integral is effectively a continuous version of a matrix multiplication.
$$\vec{P}(t)=\int G(t,\tau)\vec{E}(\tau)\ d\tau$$
#### Time Translational Invariance
Doing an experiment at another time should preserve physics relative to a reference time.
$$\vec{P}'(t)=\vec{P}(t-T)\implies \vec{E}'(t)=\vec{E}(t-T)$$
Which is identical to saying:
$$\vec{P}(t-T)=\int G(t,\tau)\vec{E}(\tau-T)\ d\tau=\int G(t,\tau)\vec{E}'(\tau)\ d\tau$$
Where $G(t,\tau)$ is a "property of nature" where it would be invariant over time.
This function will be "the same today as it will be tomorrow."
#### Special Case of $\vec{E}$ (Green's Function Definition)
In the case where $\vec{E}(\tau)=\delta(t'-\tau)$, we can say that:
$$G(t+T,t'+T)=G(t,t')$$
It also means we can express it as a single-variable function:
$$G(t,t')=G(t-t')$$
#### Causality
Events in the future cannot influence the past.
$$\vec{P}(t)=\int_{-\infty}^t G(t-\tau)\vec{E}(\tau)\ d\tau=\int_0^\infty G(\tau')\vec{E}(t-\tau')\ d\tau'$$
So that we can include the whole domain, we can write the following:
$$\vec{P}(t)=\int_{-\infty}^\infty G_\theta(\tau)\vec{E}(t-\tau)\ d\tau, \ \ \ G_\theta(\tau)=\theta(\tau)\cdot G(\tau)$$
### Application in a Physical Model (RL Circuit)
We can write the EOM of an RL circuit as the following: 
$$\left[\dfrac{d}{dt}+\alpha\right]I(t)=W(t)$$
Where $\alpha=R/L$ and $W(t)=V(t)/L$.

**Observation #1**
$$\tilde{f}(\omega)=\int e^{i\omega t}f(t)\ dt, \ \ \ f(t)=\int e^{-i\omega t}\tilde{f}(\omega)\dfrac{d\omega}{2\pi}$$
Where $f\in L^2(\mathbb{R})$.

**Observation #2**
$$\begin{align}
f(t)&=\int e^{-i\omega t}\tilde{f}(\omega)\dfrac{d\omega}{2\pi}\\
\dfrac{d}{dt}f(t)&=\dfrac{d}{dt}\int e^{-i\omega t}\tilde{f}(\omega)\dfrac{d\omega}{2\pi}\\
&=\int \dfrac{\partial}{\partial t}e^{-i\omega t}\tilde{f}(\omega)\dfrac{d\omega}{2\pi}\\
&=-i\omega\int e^{-i\omega t}\tilde{f}(\omega)\dfrac{d\omega}{2\pi}\\
\Aboxed{\dfrac{d}{dt}f(t)&=-\omega\tilde{f}(\omega)}
\end{align}$$
Where $\tilde{f}(\omega)\in L^1(\mathbb{R})$ and $-i\omega\tilde{f}(\omega)\in L^1(\mathbb{R})$.

**Observation #3**
$$\begin{align}
f(t)&=(G\star W)(t)\\
&=\int G(t-\tau)W(\tau)\ d\tau\\
\tilde{f}(\omega)&=\tilde{G}(\omega)\tilde{W}(\omega)
\end{align}$$
Where $G\in L^1(\mathbb{R})$ and $W\in L^1(\mathbb{R})$.

With these observations, we will find that:
$$\begin{align}
\left[\dfrac{d}{dt}+\alpha\right]I(t)&=W(t)\\
\int e^{-i\omega t}(-i\omega+\alpha)\tilde{I}(\omega)\dfrac{d\omega}{2\pi}&=\int e^{-i\omega t}\tilde{W}(\omega)\dfrac{d\omega}{2\pi}\\
(-i\omega+\alpha)\tilde{I}(\omega)&=\tilde{W}(\omega)\\
\dfrac{1}{-i\omega+\alpha}\tilde{W}(\omega)&=\tilde{I}(\omega)\\
\end{align}$$
From Observation 3, we can write this with the Green's Function, and so:
$$\begin{align}
\tilde{G}(\omega)&=\dfrac{1}{-i\omega+\alpha}\\
\tilde{I}(\omega)&=\tilde{G}(\omega)\tilde{W}(\omega)
\end{align}$$
Therefore, we can then write:
$$\begin{align}
I(t)&=\int e^{-i\omega t}\tilde{I}(\omega)\dfrac{d\omega}{2\pi}\\
&=\int e^{-i\omega t}\tilde{G}(\omega)\tilde{W}(\omega)\dfrac{d\omega}{2\pi}\\
&=(G\star W)(t)\\
&=\int G(t-\tau)W(\tau)\ d\tau\\
\end{align}$$
Since there is a Green's Function, it must have Linearity, Time Translation Invariance, and Causality.
$$\begin{align}
G(t)&=\int e^{-i\omega t}\tilde{G}(\omega)\dfrac{d\omega}{2\pi}\\
&=\int e^{-i\omega t}\dfrac{1}{-i\omega+\alpha}\dfrac{d\omega}{2\pi}\\
&=i\int e^{-i\omega t}\dfrac{1}{\omega+i\alpha}\dfrac{d\omega}{2\pi}\\
G(t)&=\begin{cases}0,&t<0\\-2\pi i\dfrac{i}{2\pi}e^{-\alpha t}& t>0\end{cases}\\
G(t)&=\begin{cases}0,&t<0\\e^{-\alpha t}& t>0\end{cases}
\end{align}$$
