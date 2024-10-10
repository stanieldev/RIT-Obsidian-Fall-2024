**Name:** Stanley Goodwin
**Date:** 8/29/2024

---

### Example 1
$$\omega=-\dfrac{y}{x^2+y^2}\mathrm{d}x+\dfrac{x}{x^2+y^2}\mathrm{d}y$$
1: Is $\omega$ closed?
$$\begin{align}
\mathrm{d}\omega&=\left[\dfrac{d}{dx}\left(\dfrac{x}{x^2+y^2}\right)-\dfrac{d}{dy}\left(-\dfrac{y}{x^2+y^2}\right)\right]\mathrm{d}x\ \mathrm{d}y\\
\Aboxed{\mathrm{d}\omega&=0}
\end{align}$$
Yes, $\omega$ is closed.

2: Is $\omega$ an exact form? (Take $\gamma$ to be a circle of radius 1)
$$\begin{align}
\oint_\gamma\omega&=\oint_\gamma\left(-\dfrac{y}{x^2+y^2}\mathrm{d}x+\dfrac{x}{x^2+y^2}\mathrm{d}y\right)\\
&=\int_0^{2\pi}\left(\dfrac{r^2\sin^2\theta}{r^2}+\dfrac{r^2\cos^2\theta}{r^2}\right)\mathrm{d}\theta\\
&=\int_0^{2\pi}\mathrm{d}\theta\\
\Aboxed{\oint_\gamma\omega&=2\pi\ne 0}
\end{align}$$
No, $\omega$ is not an exact form.

### Example 2
$$\omega=x\mathrm{d}x-y\mathrm{d}y$$
1: Is $\omega$ closed?
$$\begin{align}
\mathrm{d}\omega&=\left[\dfrac{d}{dx}\left(y\right)-\dfrac{d}{dy}\left(x\right)\right]\mathrm{d}x\ \mathrm{d}y\\
\Aboxed{\mathrm{d}\omega&=0}
\end{align}$$
Yes, $\omega$ is closed.

2: Is $\omega$ an exact form? (Take $\gamma$ to be a circle of radius 1)
Let $\phi=\dfrac{1}{2}\left(x^2-y^2\right)$, then 
$$\begin{align}
\mathrm{d}\phi&=\dfrac{d\phi}{dx}\mathrm{d}x+\dfrac{d\phi}{dy}\mathrm{d}y\\
&=x\ \mathrm{d}x-y\ \mathrm{d}y\\
\end{align}$$
Yes, $\omega$ is an exact form.

### Example 3
$$\omega=z^2\ \mathrm{d}z=\left(x^2-y^2+2ixy\right)\mathrm{d}x+\left(ix^2-iy^2-2xy\right)\mathrm{d}y$$
1: Is $\omega$ closed?
$$\begin{align}
\mathrm{d}\omega&=\left[\dfrac{d}{dx}\left(ix^2-iy^2-2xy\right)-\dfrac{d}{dy}\left(x^2-y^2+2ixy\right)\right]\mathrm{d}x\ \mathrm{d}y\\
&=\left[\left(2ix-2y\right)-\left(-2y+2ix\right)\right]\mathrm{d}x\ \mathrm{d}y\\
&=2\left[0\right]\mathrm{d}x\ \mathrm{d}y\\
\Aboxed{\mathrm{d}\omega&=0}
\end{align}$$
Yes, $\omega$ is closed.

2: Is $\omega$ an exact form? (Take $\gamma$ to be a circle of radius r)
$$\begin{align}
\oint_\gamma\omega&=\oint_\gamma\left(\left(x^2-y^2+2ixy\right)\mathrm{d}x+\left(ix^2-iy^2-2xy\right)\mathrm{d}y\right)\\
&=r^3\int_0^{2\pi}\left(-\left(\cos^2\theta-\sin^2\theta+2i\sin\theta\cos\theta\right)\sin\theta+\left(i\cos^2\theta-i\sin^2\theta-2\sin\theta\cos\theta\right)\cos\theta\right)\mathrm{d}\theta\\
&=r^3\int_0^{2\pi}\left(-\cos^2\theta\sin\theta+\sin^3\theta-2i\sin^2\theta\cos\theta+i\cos^3\theta-i\sin^2\theta\cos\theta-2\sin\theta\cos^2\theta\right)\mathrm{d}\theta\\
&=ir^3\int_0^{2\pi}\left(i\sin\theta\cos^2\theta+i^3\sin^3\theta+3i^2\sin^2\theta\cos\theta+\cos^3\theta\right)\mathrm{d}\theta\\
&=ir^3\int_0^{2\pi}\left(\cos\theta+i\sin\theta\right)^3\mathrm{d}\theta\\
&=ir^3\int_0^{2\pi}e^{3i\theta}\mathrm{d}\theta\\
&=\dfrac{r^3i}{3i}\left.e^{3i\theta}\right|_0^{2\pi}\\
&=\dfrac{r^3i}{3i}\left(e^{6\pi i}-e^0\right)\\
&=\dfrac{r^3i}{3i}\left(1-1\right)\\
\Aboxed{\oint_\gamma\omega&=0}
\end{align}$$
Yes, $\omega$ is an exact form.
