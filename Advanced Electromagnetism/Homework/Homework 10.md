**Name:** Stanley Goodwin
**Date:** 11/10/2024
**Collaborators:** Chris
**Time Taken:** 7 Hours

---
## Question 1
In class, we derived equations for EM waves in conductors, assuming a “good conductor”. Interestingly, it turns out that the formulas we got can be pushed a good deal further than you might expect, into regimes where e.g. $\sigma$ is not so large (“poor conductors”). In this case, you will need to use Griffiths more careful results (9.126) for the real and imaginary parts of the $k$ vector and work with those.
$$\begin{align}
\tilde{k}&=k+i\kappa\\
k&=\omega\sqrt{\dfrac{\epsilon\mu}{2}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}+1\right]^{1/2}\\
\kappa&=\omega\sqrt{\dfrac{\epsilon\mu}{2}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}-1\right]^{1/2}\\
\end{align}$$
### 1.A
Based on the above comments, *show that the skin depth for a “poor conductor” (that is,*
*with $\sigma\ll\epsilon\omega$) is $d\approx??\sqrt{\epsilon/\mu}$, independent of frequency or wavelength.* Work out what the “??” is in this equation and *explicitly check the units of your answer*.
$$\begin{align}
d&=\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}-1\right]^{-1/2}\\
&\approx\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left[\left(1+\dfrac{1}{2}\left(\dfrac{\sigma}{\epsilon\omega}\right)^2\right)-1\right]^{-1/2}\\
&\approx\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left[\dfrac{1}{2}\left(\dfrac{\sigma}{\epsilon\omega}\right)^2\right]^{-1/2}\\
&\approx\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\sqrt2\left(\dfrac{\epsilon\omega}{\sigma}\right)\\
\Aboxed{d&\approx\dfrac{2}{\sigma}\sqrt{\dfrac{\epsilon}{\mu}}}
\end{align}$$
Checking units:
$$\begin{align}
[d]&=\dfrac{[2]}{[\sigma]}\sqrt{\dfrac{[\epsilon]}{[\mu]}}=\Omega\cdot\mathrm{m}\cdot\sqrt{\dfrac{\text{F/m}}{\text{H/m}}}=\Omega\cdot\mathrm{m}\cdot\sqrt{\dfrac{\text{F}}{\text{s}^2/\text{F}}}\\
&=\Omega\cdot\mathrm{m}\cdot\dfrac{\text{F}}{\text{s}}=\dfrac{\text{V}}{\text{A}}\cdot\mathrm{m}\cdot\dfrac{\text{C}}{\text{V}\cdot\text{s}}=\dfrac{\text{V}}{\text{A}}\cdot\mathrm{m}\cdot\dfrac{\text{A}}{\text{V}}\\
\Aboxed{[d]&=\mathrm{m}}
\end{align}$$
The units of $d$ are in terms of a length, which is what we expect from distances.

### 1.B
*Show that the skin depth for a “good conductor” (i.e., $\sigma\gg\epsilon\omega$) is $d\approx\lambda/??$, where $\lambda$ is the wavelength in the conductor and ?? is something you’ll have to work out. Find the skin depth for microwaves ($f=2.5\text{ GHz}$) in copper. Briefly, how do you interpret that answer physically?*
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
d&=\dfrac{1}{\kappa}\\
d&\approx\dfrac{1}{k}\\
d&\approx\dfrac{1}{2\pi}\dfrac{2\pi}{k}\\
d&\approx\dfrac{1}{2\pi}\lambda\\
\Aboxed{d&\approx\dfrac{\lambda}{2\pi}}
\end{align}$$
For copper, we can rewrite the equation as:
$$\begin{align}
d&\approx\dfrac{c}{2\pi f}
\end{align}$$
So using $f=2.5\text{ GHz}$, we see that:
$$\begin{align}
\Aboxed{d&\approx19.10\text{ mm}}
\end{align}$$
At a distance of 19.10mm, only 37% of the light still remains as it goes into the metal.

### 1.C
About how thick should aluminum foil be to be optically opaque? Briefly comment.

The largest wavelength we can see is about $700\mathrm{\ nm}$, and so:
$$\begin{align}
d&\approx\dfrac{\lambda}{2\pi}=\dfrac{700\mathrm{\ nm}}{2\pi}\approx111.41\mathrm{\ nm}\\
\Aboxed{d&\approx0.111\ \mu\text{m}}
\end{align}$$
It looks as if about a tenth of a micron is large enough for aluminum to be effectively opaque (31% transmitted). Supposing we look at $5\tau$ like in circuits, that would mean that:
$$\begin{align}
\Aboxed{d_\text{opaque}&\approx0.555\ \mu\text{m}}
\end{align}$$
Or put another way, just over half a micron of thickness.

### 1.D
For biological tissues (like skin), $\epsilon$ and $\sigma$ depend on frequency, so we can’t use their free space values ($\mu$ on the other hand is close to its free space value). At microwave frequencies (say, about $2.5\text{ GHz}$), their values are $\epsilon=47\epsilon_0$, and $\sigma=2.2\ \Omega^{-1}\text{m}^{-1}$. Is this the “good conductor” or “poor conductor” case, or neither? Evaluate the skin depth for microwaves hitting your body.

Whether or not human skin is a good conductor comes down to the equations used before.
$$\begin{align}
\dfrac{\sigma}{\epsilon\omega}&\approx\dfrac{2.2}{47\cdot(8.85\cdot10^{-12})\cdot2\pi(2.5\cdot10^9)}\\
\Aboxed{\dfrac{\sigma}{\epsilon\omega}&\approx0.3367}
\end{align}$$
Is it not much smaller than 1, nor much larger than 1, so it's realistically neither a good nor bad conductor. Very interesting...
$$\begin{align}
d&=\dfrac{1}{\omega}\sqrt{\dfrac{2}{\epsilon\mu}}\left[\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}-1\right]^{-1/2}\\
\Aboxed{d&\approx1.533\text{ cm}}
\end{align}$$
### 1.E
If the EM wave from part D (e.g. from a radar station) hits your body, what fraction of the incident power do you absorb? (Hint: think about $R$ first, then you can get $T$ easily.)
$$\begin{align}
\dfrac{|E|}{|B|}=\left(\epsilon\mu\sqrt{1+\left(\dfrac{\sigma}{\epsilon\omega}\right)^2}\right)^{-1/2}\\
\end{align}$$
I don't think we covered this in class. I assume this has something to do with *impedance matching* from Electronic Measurements, but it wasn't shown in the textbook.

Supposing my hunch is correct, then:
$$R=\left(\dfrac{Z_\text{skin}-Z_\text{air}}{Z_\text{skin}+Z_\text{air}}\right)^2$$
If that's correct, then the transmission is basically the same as absorption since $1.5$ cm times multiple times is still small enough compared to the human body, and so:
$$\text{Absorption}=1-R=1-\left(\dfrac{Z_\text{skin}-Z_\text{air}}{Z_\text{skin}+Z_\text{air}}\right)^2=\boxed{\dfrac{4\cdot Z_\text{skin}Z_\text{air}}{(Z_\text{skin}+Z_\text{air})^2}}$$
### 1.F
Let’s think about contacting submarines by radio. For low frequency radio waves (say, $f=3\text{ kHz}$) estimate the skin depth in the sea, and comment on the feasibility/issues of such radio communication.
$$\begin{align}
d&=\sqrt{\dfrac{2\rho}{\mu\omega}}\\
&=\sqrt{\dfrac{\rho}{\pi\mu_0 f}}\\
&=\sqrt{\dfrac{0.2}{\pi(4\pi\cdot10^{-7})(3\cdot10^3)}}\\
d&=4.11\text{ m}
\end{align}$$
At $5d$ it's only about $21\text{ m}$, so this is entirely infeasible to communicating with submarines any further down than approximately $10\text{ m}$ below water.

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

![[HW10_Q2B.png]]
**Figure:** A graph of $A(k)$ against $k$, with the FWHM plotted, as well as the area of the FWHM.

This function of $A(k)$ is effectively the momentum-space wavefunction. The calculation for finding $f(x,t)$ is pretty much identical to an inverse Fourier transform. The offset of $k_0$ is the expected value of momentum this wave.

For the area under the curve, I used the Full Width, Half Maximum that I learned in Vibes & Waves and Quantum Mechanics. This accounts for $76\%$ of the area under the curve.
$$\boxed{\Delta k=\dfrac{2}{\sigma}\sqrt{2\ln2}}$$
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

For the area under the curve, I used the Full Width, Half Maximum that I learned in Vibes & Waves and Quantum Mechanics. This accounts for $76\%$ of the area under the curve.
$$\boxed{\Delta x=2\sigma\sqrt{2\ln2}}$$
The function $f(x,t)$ is a gaussian distribution in its magnitude, as well as having an oscillatory pattern due to the plane wave component. It would look like a wiggly gaussian distribution, effectively. It's best seen in part 2.E.

The standard deviation seem to be inversely proportional, where $\sigma_k\sim1/\sigma_x$. 
In quantum mechanics, this is pretty much the Heisenberg Uncertainty Principle.
$$\Delta x\Delta k=2\sigma\sqrt{2\ln2}\cdot2\dfrac{1}{\sigma}\sqrt{2\ln2}=8\ln2$$
### 2.E
Pick a visible wavelength and sketch or plot (with the software of your choice) a Gaussian pulse that lasts one femtosecond (when I say sketch, I’m thinking of $\Re(f(x,t=0))$, and then thinking about what happens as time goes by). Try to get as many details reasonably correct as you can. (Laser physicists can indeed create pulses of visible light that last only a few femtoseconds or less.)

![[HW10_2E.png]]
https://www.desmos.com/calculator/rxixasedzr

As time passes, the wave propagates to the right at the speed $c$, which for photons is the speed of light. The amount of wiggles in the packet has to do with the wavelength, and for clarity I purposely chose a lower frequency even though it mentions visible light. As the frequency gets larger, it looks effectively like a gaussian that is mirrored along the $x$-axis, making this funny bulb shape.

---
## Question 3
I mentioned in class that later in the term we will consider electromagnetic radiation from a point-like antenna, and will get what are called spherical waves, rather than plane waves. Here is a *simplified* mathematical formula for such a spherical wave (simplified in the sense that it is accurate for large distances from the origin):
$$\vec{E}(\vec{r})=A\dfrac{\sin\theta}{r}\cos\left(\vec{k}\cdot\vec{r}-\omega t\right)\hat\phi$$
### 3.A
Why would we call this a “spherical wave”? Describe it in words or pictures as best you can. Far from the origin, how is it similar to/different from a polarized traveling plane wave?

The way I thought about is that it's like a plane wave that's been wrapped around a spherical geometry. The wave propagation is radially inward/outward.

### 3.B
Show that this wave satisfies Gauss’ Law in free space. Then use Faraday’s Law to find the formula for the corresponding magnetic field. Since we are assuming we are far from the origin, you can (and should!) toss terms that appear which drop off FASTER than $1/r$.

For the sake of not having as much mathematics, we can observe that $\vec{k}$ must only be in the radial direction, and so $\vec{k}=k_r\hat{r}$ and that $k_\theta=k_\phi=0$.
$$\vec{E}(\vec{r})=A\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)\hat\phi$$

**Gauss's Law**
$$\begin{align}
\vec\nabla\cdot\vec{E}(\vec{r})&=\vec\nabla\cdot\left(A\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)\hat\phi\right)\\
&=\dfrac{1}{r\sin\theta}\dfrac{\partial}{\partial\phi}\left(A\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)\right)\\
&=\dfrac{1}{r\sin\theta}\dfrac{A\sin\theta}{r}\dfrac{\partial}{\partial\phi}\cos\left(kr-\omega t\right)\\
&=\dfrac{A}{r^2}\cdot 0\\
\Aboxed{\vec\nabla\cdot\vec{E}(\vec{r})&=0}
\end{align}$$
**Faraday's Law**
$$\begin{align}
\vec\nabla\times\vec{E}&=\dfrac{1}{r\sin\theta}\dfrac{\partial}{\partial\theta}\left(E_\phi\sin\theta\right)\hat{r}-\dfrac{1}{r}\dfrac{\partial}{\partial r}\left(rE_\phi\right)\hat\theta\\
\end{align}$$
Lets evaluate each differential separately:
$$\begin{align}
\dfrac{\partial}{\partial\theta}\left(E_\phi\sin\theta\right)
&=\sin\theta\dfrac{\partial}{\partial\theta}\left(E_\phi\right)+E_\phi\dfrac{\partial}{\partial\theta}\left(\sin\theta\right)\\
&=\sin\theta\left(E_\phi\cdot\dfrac{\cos\theta}{\sin\theta}\right)+E_\phi\cos\theta\\
\Aboxed{\dfrac{\partial}{\partial\theta}\left(E_\phi\sin\theta\right)
&=2E_\phi\cos\theta}
\end{align}$$
$$\begin{align}
\dfrac{\partial}{\partial r}\left(rE_\phi\right)
&=E_\phi\dfrac{\partial}{\partial r}\left(r\right)+r\dfrac{\partial}{\partial r}\left(E_\phi\right)\\
&=E_\phi+rA\sin\theta\left(\cos\left(kr-\omega t\right)\dfrac{\partial}{\partial r}\dfrac{1}{r}+\dfrac{1}{r}\dfrac{\partial}{\partial r}\cos\left(kr-\omega t\right)\right)\\
&=E_\phi+rA\sin\theta\left(-\cos\left(kr-\omega t\right)\dfrac{1}{r^2}-\dfrac{k}{r}\sin\left(kr-\omega t\right)\right)\\
&=E_\phi-A\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)-rkA\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)\dfrac{\sin\left(kr-\omega t\right)}{\cos\left(kr-\omega t\right)}\\
&=E_\phi-E_\phi-rk\dfrac{\sin\left(kr-\omega t\right)}{\cos\left(kr-\omega t\right)}E_\phi\\
\Aboxed{\dfrac{\partial}{\partial r}\left(rE_\phi\right)&=-rkE_\phi\tan\left(kr-\omega t\right)\\}
\end{align}$$
We can then write Faraday's law as:
$$\begin{align}
-\dfrac{\partial\vec{B}}{\partial t}&=\vec\nabla\times\vec{E}\\
&=\dfrac{1}{r\sin\theta}\dfrac{\partial}{\partial\theta}\left(E_\phi\sin\theta\right)\hat{r}-\dfrac{1}{r}\dfrac{\partial}{\partial r}\left(rE_\phi\right)\hat\theta\\
&=\dfrac{2E_\phi}{r}\dfrac{\cos\theta}{\sin\theta}\hat{r}+\dfrac{1}{r}rkE_\phi\tan\left(kr-\omega t\right)\hat\theta\\
&=\dfrac{2E_\phi}{r}\cot\theta\ \hat{r}+kE_\phi\tan\left(kr-\omega t\right)\hat\theta\\
\vec{B}(\vec{r},t)-\vec{B}(\vec{r},0)
&=-\int_0^t\dfrac{2E_\phi}{r}\cot\theta\ \hat{r}+kE_\phi\tan\left(kr-\omega t\right)\hat\theta\ dt\\
&=-A\dfrac{\sin\theta}{r}\int_0^t\dfrac{2}{r}\cot\theta\cos\left(kr-\omega t\right)\ \hat{r}+kE_\phi\sin\left(kr-\omega t\right)\hat\theta\ dt\\
&=-A\dfrac{\sin\theta}{r}\int_0^t\dfrac{2}{r}\cot\theta\cos\left(kr-\omega t\right)\ \hat{r}\ dt-Ak\dfrac{\sin\theta}{r}\int_0^t\sin\left(kr-\omega t\right)\hat\theta\ dt\\
&=-Ak\dfrac{\sin\theta}{r}\int_0^t\sin\left(kr-\omega t\right)\hat\theta\ dt\\
&=-Ak\dfrac{\sin\theta}{r\omega}\left.\cos\left(kr-\omega t\right)\hat\theta\right|_0^t\\
&=-Ak\dfrac{\sin\theta}{r\omega}\left(\cos\left(kr-\omega t\right)-1\right)\hat\theta\\
\Aboxed{\vec{B}(\vec{r},t)&=-Ak\dfrac{\sin\theta}{r\omega}\cos\left(kr-\omega t\right)\hat\theta}
\end{align}$$
### 3.C
Discuss the physics of this $B$ field. Does it agree with everything you already know from plane waves about how $\vec{E}$ and $\vec{B}$ are supposed to be related to each other (and to the direction of propagation)? Discuss both magnitudes and directions.

The electric field $\vec{E}$ points in the $\hat\phi$ direction, and magnetic field $\vec{B}$ points in the $\hat\theta$ direction.
The 2 field are perpendicular, which is what we expect from EM waves. This also implies that the wavevector must point outward radially in order to be normal to both $\vec{E}$ and $\vec{B}$.

From the equation above, we can also see that the magnitude of the $\vec{B}$ field is exactly the same as the magnitude of the $\vec{E}$ field with a division by $\omega/k_r$, which is just the speed of the wave in the medium, resembling $B_0=E_0/c$. This is also to be expected.

### 3.D
Verify that the formulas you just got (for $\vec{E}$ and $\vec{B}$) satisfy the remaining two Maxwell equations in free space (remember that you are ignoring any terms that drop faster than 1/r).

**No monopoles**
$$\begin{align}
\vec\nabla\cdot\vec{B}(\vec{r},t)&=\vec\nabla\cdot\left(-\dfrac{A}{c}\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)\hat\theta\right)\\
&=\dfrac{1}{r\sin\theta}\dfrac{\partial}{\partial\theta}\left(-\dfrac{A}{c}\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)\sin\theta\right)\\
&=-\dfrac{A}{rc}\dfrac{1}{r\sin\theta}\cos\left(kr-\omega t\right)\dfrac{\partial}{\partial\theta}\left(\sin^2\theta\right)\\
&=-\dfrac{A}{rc}\dfrac{1}{r\sin\theta}\cos\left(kr-\omega t\right)2\sin\theta\cos\theta\\
&=-\dfrac{1}{r^2}\dfrac{2A}{c}\cos\left(kr-\omega t\right)\cos\theta\\
\Aboxed{\vec\nabla\cdot\vec{B}(\vec{r},t)&=0}
\end{align}$$

**Ampere's Law**
$$\begin{align}
\vec\nabla\times\vec{B}&=-\dfrac{1}{r\sin\theta}\dfrac{\partial}{\partial\phi}\left(B_\theta\right)\hat{r}+\dfrac{1}{r}\dfrac{\partial}{\partial r}\left(rB_\theta\right)\hat\phi\\
\end{align}$$
Lets evaluate each differential separately:
$$\begin{align}
\dfrac{\partial}{\partial\phi}\left(B_\theta\right)
&=\dfrac{\partial}{\partial\phi}\left(Ak\dfrac{\sin\theta}{r\omega}\cos\left(kr-\omega t\right)\right)\\
\Aboxed{\dfrac{\partial}{\partial\phi}\left(B_\theta\right)
&=0}
\end{align}$$
$$\begin{align}
\dfrac{\partial}{\partial r}\left(rB_\theta\right)
&=B_\theta\dfrac{\partial}{\partial r}\left(r\right)-r\dfrac{\partial}{\partial r}\left(B_\theta\right)\\
&=B_\theta-r\dfrac{\partial}{\partial r}\left(Ak\dfrac{\sin\theta}{r\omega}\cos\left(kr-\omega t\right)\right)\\
&=B_\theta-rAk\dfrac{\sin\theta}{\omega}\dfrac{\partial}{\partial r}\left(\dfrac{1}{r}\cos\left(kr-\omega t\right)\right)\\
&=B_\theta-rAk\dfrac{\sin\theta}{\omega}\left(-\dfrac{1}{r^2}\cos\left(kr-\omega t\right)-\dfrac{k}{r}\sin\left(kr-\omega t\right)\right)\\
\Aboxed{\dfrac{\partial}{\partial r}\left(rB_\theta\right)&=Ak^2\dfrac{\sin\theta}{\omega}\sin\left(kr-\omega t\right)}
\end{align}$$
We can then write Ampere's law as:
$$\begin{align}
\dfrac{\partial\vec{E}}{\partial t}&=c^2\vec\nabla\times\vec{B}\\
&=c^2\left(-\dfrac{1}{r\sin\theta}\dfrac{\partial}{\partial\phi}\left(B_\theta\right)\hat{r}+\dfrac{1}{r}\dfrac{\partial}{\partial r}\left(rB_\theta\right)\hat\phi\right)\\
&=-c^2\dfrac{1}{r}\hat\phi\dfrac{\partial}{\partial r}\left(rB_\theta\right)\\
&=c^2\dfrac{1}{r}Ak^2\dfrac{\sin\theta}{\omega}\sin\left(kr-\omega t\right)\hat\phi\\
\dfrac{\partial\vec{E}}{\partial t}&=c^2\dfrac{Ak^2\sin\theta}{r\omega}\sin\left(kr-\omega t\right)\hat\phi\\
\vec{E}(\vec{r},t)&=c^2\dfrac{Ak^2\sin\theta}{r\omega}\int\sin\left(kr-\omega t\right)\hat\phi\ dt\\
&=c^2\dfrac{A\sin\theta}{r}\dfrac{k^2}{\omega^2}\cos\left(kr-\omega t\right)\hat\phi\\
&=\dfrac{c^2}{c^2}\dfrac{A\sin\theta}{r}\cos\left(kr-\omega t\right)\hat\phi\\
\Aboxed{\vec{E}(\vec{r},t)&=\dfrac{A\sin\theta}{r}\cos\left(kr-\omega t\right)\hat\phi}
\end{align}$$
### 3.E
What is the direction of the Poynting vector? Does that make physical sense? Find the mathematical fall-off with distance from the origin, and argue that your result makes physical sense, given simple arguments about energy conservation/flow from a point source.
$$\begin{align}
\vec{E}(\vec{r},t)&=A\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)\hat\phi\\
\vec{B}(\vec{r},t)&=-\dfrac{A}{c}\dfrac{\sin\theta}{r}\cos\left(kr-\omega t\right)\hat\theta\\
\vec{S}(\vec{r},t)&=\dfrac{1}{\mu_0}\vec{E}(\vec{r},t)\times\vec{B}(\vec{r},t)\\
&=-\dfrac{1}{\mu_0}\dfrac{A^2}{c}\dfrac{\sin^2\theta}{r^2}\cos^2\left(\vec{k}\cdot\vec{r}-\omega t\right)\left(\hat\phi\times\hat\theta\right)\\
\Aboxed{\vec{S}(\vec{r},t)&=\dfrac{A^2}{\mu_0c}\dfrac{\sin^2\theta}{r^2}\cos^2\left(\vec{k}\cdot\vec{r}-\omega t\right)\hat{r}}
\end{align}$$
As the energy flows out from a point source, it is spread out over a surface area that increases as $r^2$, and since energy must be conserved, then intensity must drop as $1/r^2$ to conserve energy/power. Effectively: $\vec{S}\cdot\vec{A}=C$ where $C$ is a constant (power).