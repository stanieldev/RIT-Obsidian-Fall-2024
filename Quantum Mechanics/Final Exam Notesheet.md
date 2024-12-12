**Schrodinger's Equation**
$$\begin{align}
\hat{H}\ket{\psi}&=i\hbar\dfrac{\partial}{\partial t}\ket{\psi} & \text{(TDSE)}\\
\hat{H}\ket{\psi}&=\dfrac{\hat{p}^2}{2m}\ket{\psi}+V(\hat{x})\ket{\psi} & \text{(TISE)}
\end{align}$$
**Statistics**
$$\begin{align}
\langle\hat{A}\rangle&=\bra{\psi}\hat{A}\ket{\psi} & \text{(Expected Value)}\\
\sigma^2_A&=\langle\hat{A}^2\rangle-\langle\hat{A}\rangle^2 & \text{(Variance)}
\end{align}$$
**Operators**
$$\begin{align}
a_\pm=\dfrac{1}{\sqrt{2\hbar m\omega}}\left(m\omega\hat{x}\mp i\hat{p}\right)
\end{align}$$
**Commutators**
$$\begin{align}
[A,BC]&=[A,B]C+B[A,C]\\
[AB,C]&=A[B,C]+[A,C]B\\
\end{align}$$
**Energies**
$$\begin{align}
E_n&=\dfrac{\hbar^2\pi^2}{2ma^2}n^2 &
E_n&=\left(n+\dfrac{1}{2}\right)\hbar\omega &
E&=-\dfrac{m\alpha^2}{2\hbar^2}
\end{align}$$
**Uncertainty**
$$\begin{align}
\sigma^2_A\sigma^2_B&\ge\left(\dfrac{\langle[\hat{A},\hat{B}]\rangle}{2i}\right)^2\\
\phi(k,0)&=\dfrac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{-ikx}\psi(x,0)\ dx\\
\psi(x,t)&=\dfrac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{+ikx}\phi(x,0)e^{-iE_kt/\hbar}\ dk\\
\end{align}$$
**Waves Mechanics**
$$\begin{align}
v_p&=\dfrac{\omega}{k} & v_g&=\dfrac{\Delta\omega}{\Delta k}\\
T&=\dfrac{1}{1+\beta^2} & R&=\dfrac{\beta^2}{1+\beta^2}
\end{align}$$
**Ehrenfest Theorem**
$$\dfrac{d\langle\hat{A}\rangle}{dt}=\dfrac{\langle[A,\hat{H}]\rangle}{i\hbar}+\left\langle\dfrac{dA}{dt}\right\rangle$$
**Angular Momenta**
$$\begin{align}
[L^2,\vec{L}]&=0 & [L_i,L_j]&=i\hbar\epsilon_{ijk}L_k & L_\pm&=L_x\pm iL_y\\
[S^2,\vec{S}]&=0 & [S_i,S_j]&=i\hbar\epsilon_{ijk}S_k & S_\pm&=S_x\pm iS_y
\end{align}$$
$$\begin{align}
L^2\ket{\psi}&=l(l+1)\hbar^2\ket{\psi} & L_z\ket{\psi}&=m_l\hbar\ket{\psi}\\
S^2\ket{\psi}&=s(s+1)\hbar^2\ket{\psi} & S_z\ket{\psi}&=m_s\hbar\ket{\psi}
\end{align}$$
$$\begin{align}
L_\pm\ket{l,m_l}&=\sqrt{l(l+1)-m_l(m_l\pm1)}\hbar\ket{l,m_l\pm1}\\
S_\pm\ket{s,m_s}&=\sqrt{s(s+1)-m_s(m_s\pm1)}\hbar\ket{s,m_s\pm1}
\end{align}$$
**Polynomials**
$$\begin{align}
j_l(x)&=(-x)^l\left(\dfrac{1}{x}\dfrac{d}{dx}\right)^l\dfrac{\sin x}{x} & \text{(Bessel Function)}\\
n_l(x)&=-(-x)^l\left(\dfrac{1}{x}\dfrac{d}{dx}\right)^l\dfrac{\cos x}{x} & \text{(Neumann Function)}\\
L_q(x)&=e^x\left(\dfrac{d}{dx}\right)^q(e^{-x}x^q) & \text{(Legendre Polynomial)}\\
L_{p-q}^p(x)&=(-1)^pe^x\left(\dfrac{d}{dx}\right)^pL_q(x) & \text{(Associated Polynomial)}\\
\end{align}$$
