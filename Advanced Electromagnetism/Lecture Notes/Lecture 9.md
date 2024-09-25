**Name:** Stanley Goodwin
**Date:** 8/24/2024

---
### Solving RLC circuits
Last time: LR Circuit driven by an AC generator.
$$I(t)=I_P(t)+I_H(t)=A\cos(\omega t+\phi)+I_He^{-\tfrac{R}{L}t}$$
The value of $I_H$ is determined by our initial conditions.
Lets consider a very high $\omega$ and $I(0)=0$,
$$I(t)=\dfrac{V_0}{R}\cos(0)+I_He^{-\tfrac{R}{L}t}$$
To make $I(0) = 0$, we need $I_H=-\tfrac{V_0}{R}$.
$$I(t)=\dfrac{V_0}{R}\left(1-e^{-\tfrac{R}{L}t}\right)$$
This is the DC solution of our ODE.
Using Euler's Identity, instead of sines and cosines:
$$e^{i\omega t}=\cos(\omega t)+i\sin(\omega t)$$
The functions $\cos(\omega t)$ and $\sin(\omega t)$ are linearly independent.
Contrast, $e^{i\omega t}$ and $\tfrac{d}{dt}e^{i\omega t}$ are scale factors of each other.
We can build $e^{i\omega t}$'s time derivatives from a linear combination of $e^{i\omega t}$.

Solving the ODE is a simple matter of algebra, but the drawback is that the solution looks complex.
In the end, you'll have to take the $\Re{}\left(V(t)\right)$.

Lets solve our current again:
$$L\dfrac{dI}{dt}+IR=V(t)$$
Let $V(t)=\tilde{V}e^{i\omega t}$, and guess $I(t)=\tilde{I}e^{i\omega t}$.
$$\begin{align}
L\dfrac{dI}{dt}+IR&=V(t)\\
\dfrac{dI}{dt}+\dfrac{R}{L}I&=\dfrac{1}{L}V(t)\\
i\omega\tilde{I}e^{i\omega t}+\dfrac{R}{L}\tilde{I}e^{i\omega t}&=\dfrac{\tilde{V}}{L}e^{i\omega t}\\
\tilde{I}\left(i\omega+\dfrac{R}{L}\right)&=\dfrac{\tilde{V}}{L}\\
\tilde{I}&=\dfrac{\tilde{V}}{R+i\omega L}\\
\end{align}$$
Taking the real part, we find:
$$\begin{align}
V(t)&=L\dfrac{dI}{dt}+IR\\
I(t)&=\dfrac{\tilde{V}}{R+i\omega L}e^{i\omega t}\\
&=\dfrac{\tilde{V}}{Z}e^{i\omega t}\\
\Aboxed{\Re(I(t))&=\left|\dfrac{\tilde{V}}{Z}\right|\cos(\omega t)}
\end{align}$$

