**Name:** Stanley Goodwin
**Date:** 11/09/2024
**Collaborators:** None
**Time Taken:** XXX Hours

---
## Question 1
In class, we derived equations for EM waves in conductors, assuming a “good conductor”. Interestingly, it turns out that the formulas we got can be pushed a good deal further than you might expect, into regimes where e.g. $\sigma$ is not so large (“poor conductors”). In this case, you will need to use Griffiths more careful results (9.126) for the real and imaginary parts of the $k$ vector and work with those.
$$\begin{align}
\tilde{k}&=k+i\kappa\\
k&=\omega\sqrt{\dfrac{\epsilon\mu}{2}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}+1\right]^{1/2}\\
\kappa&=\omega\sqrt{\dfrac{\epsilon\mu}{2}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}-1\right]^{1/2}\\
\end{align}$$
### 1.A
Based on the above comments, show that the skin depth for a “poor conductor” (that is,
with $\sigma\ll\epsilon\omega$) is $d\approx??\sqrt{\epsilon/\mu}$, independent of frequency or wavelength. Work out what the “??” is in this equation and explicitly check the units of your answer.
$$\begin{align}
d&=\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}-1\right]^{-1/2}\\
&\approx\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left[\left(1+\dfrac{1}{2}\left(\dfrac{\sigma}{\epsilon\omega}\right)^2\right)-1\right]^{-1/2}\\
&\approx\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left[\dfrac{1}{2}\left(\dfrac{\sigma}{\epsilon\omega}\right)^2\right]^{-1/2}\\
&\approx\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\sqrt2\left(\dfrac{\epsilon\omega}{\sigma}\right)\\
\Aboxed{d&\approx\dfrac{2}{\sigma}\sqrt{\dfrac{\epsilon}{\mu}}}
\end{align}$$
Checking units:
$$\begin{align}
[d]&=\dfrac{[2]}{[\sigma]}\sqrt{\dfrac{[\epsilon]}{[\mu]}}\\
&=\Omega\cdot\mathrm{m}\cdot\sqrt{\dfrac{\text{F/m}}{\text{H/m}}}\\
&=\Omega\cdot\mathrm{m}\cdot\sqrt{\dfrac{\text{F}}{\text{s}^2/\text{F}}}\\
&=\Omega\cdot\mathrm{m}\cdot\dfrac{\text{F}}{\text{s}}\\
&=\dfrac{\text{V}}{\text{A}}\cdot\mathrm{m}\cdot\dfrac{\text{C}}{\text{V}\cdot\text{s}}\\
&=\dfrac{\text{V}}{\text{A}}\cdot\mathrm{m}\cdot\dfrac{\text{A}}{\text{V}}\\
\Aboxed{[d]&=\mathrm{m}}
\end{align}$$
### 1.B
Show that the skin depth for a “good conductor” (i.e., $\sigma\gg\epsilon\omega$) is $d\approx\lambda/??$, where $\lambda$ is the wavelength in the conductor and ?? is something you’ll have to work out. Find the skin depth for microwaves ($f=2.5\text{ GHz}$) in copper. Briefly, how do you interpret that answer physically?
$$\begin{align}
k&=\omega\sqrt{\dfrac{\epsilon\mu}{2}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}+1\right]^{1/2}\\
&\approx\omega\sqrt{\dfrac{\epsilon\mu}{2}}\sqrt{\dfrac{\sigma}{\epsilon\omega}}\\
\Aboxed{k&\approx\omega\sqrt{\dfrac{\mu\sigma}{2\omega}}}\\
\kappa&=\omega\sqrt{\dfrac{\epsilon\mu}{2}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}-1\right]^{1/2}\\
&\approx\omega\sqrt{\dfrac{\epsilon\mu}{2}}\sqrt{\dfrac{\sigma}{\epsilon\omega}}\\
\Aboxed{\kappa&\approx\omega\sqrt{\dfrac{\mu\sigma}{2\omega}}}\\
\end{align}$$
From there, we can express:
$$\begin{align}
d&=\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}-1\right]^{-1/2}\\
&\approx\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left(\dfrac{\sigma}{\epsilon\omega}\right)^{-1/2}\\
d&\approx\sqrt{\dfrac{2}{\mu\sigma\omega}}\\
\end{align}$$
### 1.C
About how thick should aluminum foil be to be optically opaque? Briefly comment.
$$\begin{align}
...
\end{align}$$
### 1.D
For biological tissues (like skin), $\epsilon$ and $\sigma$ depend on frequency, so we can’t use their free space values (m on the other hand is close to its free space value). At microwave frequencies (say, about $2.5\text{ GHz}$), their values are $~\epsilon=47\epsilon_0$, and $\sigma=2.2\ \Omega^{-1}\text{m}^{-1}$. Is this the “good conductor” or “poor conductor” case, or neither? Evaluate the skin depth for microwaves hitting your body.
$$\begin{align}
...
\end{align}$$
### 1.E
If the EM wave from part D (e.g. from a radar station) hits your body, what fraction of the incident power do you absorb? (Hint: think about $R$ first, then you can get $T$ easily.)
$$\begin{align}
...
\end{align}$$
### 1.F
Let’s think about contacting submarines by radio. For low frequency radio waves (say, $f=3\text{ kHz}$) estimate the skin depth in the sea, and comment on the feasibility/issues of such radio communication.
$$\begin{align}
...
\end{align}$$
---
## Question 2
I’ve claimed repeatedly that we can always sum up plane waves to get real wave packets. Let’s try it now. Consider a localized wave packet that satisfies the one-dimensional wave equation from a sum of sinusoidal waves using Fourier’s integral method:
$$f(x,t)=\int_{-\infty}^\infty A(k)e^{ik(x-ct)}dk$$
### 2.A
Show that $f(x,t)$ satisfies the wave equation with wave speed $c$.
$$\begin{align}
\dfrac{\partial^2f}{\partial t^2}&=c^2\dfrac{\partial^2f}{\partial x^2}\\
\dfrac{\partial^2}{\partial t^2}\int_{-\infty}^\infty A(k)e^{ik(x-ct)}dk&=c^2\dfrac{\partial^2}{\partial x^2}\int_{-\infty}^\infty A(k)e^{ik(x-ct)}dk\\
\int_{-\infty}^\infty A(k)\dfrac{\partial^2}{\partial t^2}e^{ik(x-ct)}dk&=c^2\int_{-\infty}^\infty A(k)\dfrac{\partial^2}{\partial x^2}e^{ik(x-ct)}dk\\
\int_{-\infty}^\infty A(k)(-ikc)^2e^{ik(x-ct)}dk&=c^2\int_{-\infty}^\infty A(k)(ik)^2e^{ik(x-ct)}dk\\
-c^2\int_{-\infty}^\infty A(k)k^2e^{ik(x-ct)}dk&=-c^2\int_{-\infty}^\infty A(k)k^2e^{ik(x-ct)}dk\\
\end{align}$$
They are equal, so therefore the initial $f(x,t)$ satisfies the wave equation.
### 2.B
Assume $A(k)$ is given by a Gaussian distribution centered at some positive wavevector $k_0$:
$$A(k)=\dfrac{1}{\sqrt{2\pi\sigma^2}}e^{-\tfrac{(k-k_0)^2\sigma^2}{2}}$$
Hand-sketch this function. Roughly, what range of wavevectors $\Delta k$ contribute significantly to this wave packet?
$$\begin{align}
...
\end{align}$$
### 2.C
Calculate $f(x,t)$ from the above $A(k)$.
$$\begin{align}
f(x,t)&=\int_{-\infty}^\infty A(k)e^{ik(x-ct)}dk\\
&=\int_{-\infty}^\infty \dfrac{1}{\sqrt{2\pi\sigma^2}}e^{-\tfrac{(k-k_0)^2\sigma^2}{2}}e^{ik(x-ct)}dk\\
&=\dfrac{1}{\sqrt{2\pi\sigma^2}}\int_{-\infty}^\infty e^{-\tfrac{(k-k_0)^2\sigma^2}{2}}e^{ik(x-ct)}dk\\
&=\dfrac{1}{\sqrt{2\pi\sigma^2}}\int_{-\infty}^\infty e^{-\tfrac{k^2\sigma^2}{2}}e^{i(k+k_0)(x-ct)}dk\\
&=\dfrac{1}{\sqrt{2\pi\sigma^2}}e^{ik_0(x-ct)}\int_{-\infty}^\infty e^{-\tfrac{k^2\sigma^2}{2}}e^{ik(x-ct)}dk\\
&=\dfrac{1}{\sqrt{2\pi\sigma^2}}e^{ik_0(x-ct)}\int_{-\infty}^\infty e^{-\tfrac{\sigma^2k^2}{2}+i(x-ct)k}dk\\
&=\dfrac{1}{\sqrt{2\pi\sigma^2}}e^{ik_0(x-ct)}\sqrt{\dfrac{2\pi}{\sigma^2}}e^{-\tfrac{(x-ct)^2}{2\sigma^2}}\\
&=\sqrt{\dfrac{2\pi}{2\pi\sigma^4}}e^{ik_0(x-ct)}e^{-\tfrac{(x-ct)^2}{2\sigma^2}}\\
\Aboxed{f(x,t)&=\dfrac{1}{\sigma^2}e^{-\tfrac{(x-ct)^2}{2\sigma^2}}e^{ik_0(x-ct)}}
\end{align}$$
### 2.D
Describe $f(x,t)$ physically as best you can. How wide is the x-width $\Delta x$ of the “wave packet” compared to the k-width $\Delta k$? Does the relationship between $\Delta k$ and $\Delta x$ remind you of anything you’ve seen in a quantum context (perhaps in Modern)?

They seem to be basically inversely proportional, where $\sigma_k\sim1/\sigma_x$. In quantum mechanics, this is pretty much the Heisenberg Uncertainty Principle.
### 2.E
Pick a visible wavelength and sketch or plot (with the software of your choice) a Gaussian pulse that lasts one femtosecond (when I say sketch, I’m thinking of $\Re(f(x,t=0))$, and then thinking about what happens as time goes by). Try to get as many details reasonably correct as you can. (Laser physicists can indeed create pulses of visible light that last only a few femtoseconds or less.)
$$\begin{align}
...
\end{align}$$
---
## Question 3
I mentioned in class that later in the term we will consider electromagnetic radiation from a point-like antenna, and will get what are called spherical waves, rather than plane waves. Here is a simplified mathematical formula for such a spherical wave (simplified in the sense that it is accurate for large distances from the origin):
$$\vec{E}(\vec{r})=A\dfrac{\sin\theta}{r}\cos\left(\vec{k}\cdot\vec{r}-\omega t\right)\hat\phi$$
### 3.A
Why would we call this a “spherical wave”? Describe it in words or pictures as best you can. Far from the origin, how is it similar to/different from a polarized traveling plane wave?
$$\begin{align}
...
\end{align}$$
### 3.B
Show that this wave satisfies Gauss’ Law in free space. Then use Faraday’s Law to find the formula for the corresponding magnetic field. Since we are assuming we are far from the origin, you can (and should!) toss terms that appear which drop off FASTER than $1/r$.
$$\begin{align}
...
\end{align}$$
### 3.C
Discuss the physics of this $B$ field. Does it agree with everything you already know from plane waves about how $\vec{E}$ and $\vec{B}$ are supposed to be related to each other (and to the direction of propagation)? Discuss both magnitudes and directions.
$$\begin{align}
...
\end{align}$$
### 3.D
Verify that the formulas you just got (for $\vec{E}$ and $\vec{B}$) satisfy the remaining two Maxwell equations in free space (remember that you are ignoring any terms that drop faster than 1/r!).
$$\begin{align}
...
\end{align}$$
### 3.E
What is the direction of the Poynting vector? Does that make physical sense? Find the mathematical fall-off with distance from the origin, and argue that your result makes physical sense, given simple arguments about energy conservation/flow from a point source.
$$\begin{align}
...
\end{align}$$
