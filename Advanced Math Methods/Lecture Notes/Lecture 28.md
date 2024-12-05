**Name:** Stanley Goodwin
**Date:** 12/5/2024

---
### Viscous Model
$$\begin{align}
\chi(t)&=\dfrac{\chi_0}{\tau}e^{-t/\tau}\theta(t)
\end{align}$$
**Convolution Integral**
$$\begin{align}
P(t)&=\int_{-\infty}^\infty\chi(t-\nu)E(\nu)\ d\nu\\
&=\int_{-\infty}^\infty\dfrac{\chi_0}{\tau}e^{-(t-\nu)/\tau}\theta(t-\nu)E(\nu)\ d\nu\\
&=\dfrac{\chi_0}{\tau}e^{-t/\tau}\int_{-\infty}^\infty e^{\nu/\tau}\theta(t-\nu)E(\nu)\ d\nu\\
\end{align}$$
For the case of $E(t)=E_0\theta(t)$, then:
$$\begin{align}
P(t)&=\dfrac{\chi_0}{\tau}e^{-t/\tau}\int_{-\infty}^\infty e^{\nu/\tau}\theta(t-\nu)E(\nu)\ d\nu\\
&=\dfrac{E_0\chi_0}{\tau}e^{-t/\tau}\int_0^t e^{\nu/\tau}\ d\nu\\
&=\dfrac{E_0\chi_0}{\tau}\tau e^{-t/\tau}\left(e^{\nu/\tau}\right|_0^t\\
&=E_0\chi_0e^{-t/\tau}\left(e^{t/\tau}-1\right)\\
\Aboxed{P(t)&=E_0\chi_0\left(1-e^{-t/\tau}\right)}
\end{align}$$
### Lanata Classic Example
$$\begin{align}
C_e\dfrac{dT_e}{dt}&=-g(T_e-T_p)-\epsilon_eT_e+P_e(t)\\
C_p\dfrac{dT_p}{dt}&=+g(T_e-T_p)-\epsilon_pT_p+P_p(t)\\
\end{align}$$
Using vectors, we can rewrite the top as the following:
$$\begin{align}
\dfrac{dT_e}{dt}&=(g/C_e)(T_p-T_e)-(\epsilon_e/C_e)T_e+(1/C_e)P_e(t)\\
\dfrac{dT_p}{dt}&=(g/C_p)(T_e-T_p)-(\epsilon_p/C_p)T_p+(1/C_p)P_p(t)\\
\dfrac{d}{dt}\left[\begin{array}{c}T_e\\T_p\end{array}\right]&=
\left[\begin{array}{c}-g/C_e-\epsilon_e/C_e&g/C_e\\g/C_p&-g/C_p-\epsilon_p/C_p\end{array}\right]\left[\begin{array}{c}T_e\\T_p\end{array}\right]-
\left[\begin{array}{c}1/C_e&0\\0&1/C_p\end{array}\right]\left[\begin{array}{c}P_e(t)\\P_p(t)\end{array}\right]\\
\Aboxed{\dfrac{d}{dt}\vec{T}(t)&=A\vec{T}(t)-B\vec{P}(t)}
\end{align}$$
We want to solve for $T(t)$ on one side, and so:
$$\begin{align}
\Aboxed{-\dfrac{d}{dt}\vec{T}(t)+A\vec{T}(t)&=B\vec{P}(t)}
\end{align}$$
Then you diagonalize the matrix. It's just a coupled versions of things we've seen before.
$$\begin{align}
(\lambda-\eta)\left(\lambda-\eta-g(1/C_e+1/C_p)\right)=0
\end{align}$$
Positive definite eigenvalues are the same idea as "no upper half singularities" from previous.
