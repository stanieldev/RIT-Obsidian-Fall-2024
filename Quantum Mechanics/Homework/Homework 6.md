**Name:** Stanley Goodwin
**Date:** 10/18/2024
**Collaborators:** None

---
## Question 1
Evaluate the following:
### 1.1
$$\begin{align}
\int_{-3}^1\left(x^3-3x^2+2x-1\right)\cdot\delta(x+2)\ dx
&=\left((-2)^3-3(-2)^2+2(-2)-1\right)\\
&=-8-12-2-1\\
\Aboxed{\int_{-3}^1\left(x^3-3x^2+2x-1\right)\cdot\delta(x+2)\ dx&=-23}
\end{align}$$
### 1.2
$$\begin{align}
\int_0^\infty\left(\cos(3x)+2\right)\cdot\delta(x-\pi)\ dx&=\cos(3(\pi))+2\\
&=-1+2\\
\Aboxed{\int_0^\infty\left(\cos(3x)+2\right)\cdot\delta(x-\pi)\ dx&=1}
\end{align}$$
---
## Question 2
Show the following:
### 2.1
$$\begin{align}
\delta(cx)=\dfrac{\delta(x)}{c}
\end{align}$$
### 2.2
$$\begin{align}
\delta(-x)=\delta(x)
\end{align}$$
---
## Question 3
Consider the bound state of the attractive delta function well $V(x)=-\alpha\delta(x)$, for which we know $\psi(x)=\dfrac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^2}$.
### 3.1
$$\begin{align}
\left\langle{x}\right\rangle&=\int_{-\infty}^\infty \psi^*(x)\hat{x}\psi(x)\ dx\\
&=\int_{-\infty}^\infty \left(\dfrac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^2}\right)x\left(\dfrac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^2}\right)\ dx\\
&=\dfrac{m\alpha}{\hbar^2}\int_{-\infty}^\infty x\cdot e^{-2m\alpha|x|/\hbar^2}\ dx\\
\Aboxed{\left\langle{x}\right\rangle&=0}
\end{align}$$
### 3.2
$$\begin{align}
\left\langle{x^2}\right\rangle&=\int_{-\infty}^\infty \psi^*(x)\hat{x}^2\psi(x)\ dx\\
&=\int_{-\infty}^\infty \left(\dfrac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^2}\right)x^2\left(\dfrac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^2}\right)\ dx\\
&=\dfrac{m\alpha}{\hbar^2}\int_{-\infty}^\infty x^2\cdot e^{-2m\alpha|x|/\hbar^2}\ dx\\
&=\dfrac{2m\alpha}{\hbar^2}\int_{0}^\infty x^2\cdot e^{-2m\alpha x/\hbar^2}\ dx\\
&=\dfrac{2m\alpha}{\hbar^2}\left(\dfrac{x^2}{-2m\alpha /\hbar^2}+\dfrac{2x}{(-2m\alpha /\hbar^2)^2}+\dfrac{2}{(-2m\alpha /\hbar^2)^3}\right)\left.e^{-2m\alpha x/\hbar^2}\right|_0^\infty\\
&=\dfrac{2m\alpha}{\hbar^2}\left(0+0+0-0-0-\dfrac{2}{(-2m\alpha /\hbar^2)^3}\right)\\
&=\dfrac{2m\alpha}{\hbar^2}\dfrac{2\hbar^6}{(2m\alpha)^3}\\
\Aboxed{\left\langle{x^2}\right\rangle&=\dfrac{\hbar^4}{2m^2\alpha^2}}\\
\Aboxed{\sigma_x^2&=\dfrac{\sqrt{2}}{2}\dfrac{\hbar^2}{m\alpha}}
\end{align}$$
---
## Question 4
Consider the double delta-function potential $V(x)=-\alpha\left(\delta(x+a)+\delta(x-a)\right)$, where $\alpha, a$ are positive constants.
### 4.1
TODO: Sketch Potential Well
### 4.2
Assume $\psi(x)=\begin{cases}Ae^{-kx},&x>a\\B\left(e^{kx}+e^{-kx}\right),&-a<x<a\\Ae^{kx},&x<-a\\\end{cases}$, where $k=\dfrac{\sqrt{-2mE}}{\hbar}$.
$$\begin{align}
\lim_{x\rightarrow a^+}\psi(x)&=Ae^{-ka}\\
\lim_{x\rightarrow a^-}\psi(x)&=B\left(e^{ka}+e^{-ka}\right)\\
Ae^{-ka}&=B\left(e^{ka}+e^{-ka}\right)\\
\Aboxed{A&=B\left(e^{2ka}+1\right)}\\
\lim_{x\rightarrow -a^-}\psi(x)&=Ae^{-ka}\\
\lim_{x\rightarrow -a^+}\psi(x)&=B\left(e^{ka}+e^{-ka}\right)\\
Ae^{-ka}&=B\left(e^{ka}+e^{-ka}\right)\\
\Aboxed{A&=B\left(e^{2ka}+1\right)}
\end{align}$$
### 4.3
Let $\psi'(x)=\begin{cases}-kAe^{-kx},&x>a\\kB\left(e^{kx}-e^{-kx}\right),&-a<x<a\\kAe^{kx},&x<-a\\\end{cases}$, where $k=\dfrac{\sqrt{-2mE}}{\hbar}$.
$$\begin{align}
\lim_{x\rightarrow a^+}\psi'(x)&=-kAe^{-ka}\\
\lim_{x\rightarrow a^-}\psi'(x)&=kB\left(e^{ka}-e^{-ka}\right)\\
-kAe^{-ka}&=kB\left(e^{ka}-e^{-ka}\right)\\
A&=-B\left(e^{2ka}-1\right)\\
\Aboxed{A&=-B\left(e^{2ka}-1\right)}
\end{align}$$
### 4.4
$$\begin{align}
&&-Ae^{-ka}&=B\left(e^{ka}-e^{-ka}\right)\\
&&Ae^{-ka}&=B\left(e^{ka}+e^{-ka}\right)\\
\div&&-1&=\tanh(ka)\\
&&\Aboxed{k&=\dfrac{1}{a}\tanh^{-1}(-1)}
\end{align}$$
---
## Question 5
Assume a particle incident from the left described by the wave function: $$\psi(x)=\begin{cases}
Ae^{ikx}+Be^{-ikx},&x>a\\
Ce^{ikx}+De^{-ikx},&-a<x<a\\
Fe^{ikx},&x<-a\\
\end{cases}$$
$$\psi'(x)=\begin{cases}
ikAe^{ikx}-ikBe^{-ikx},&x>a\\
ikCe^{ikx}-ikDe^{-ikx},&-a<x<a\\
ikFe^{ikx},&x<-a\\
\end{cases}$$
### 5.1
Continuity constraints:
$$\begin{align}
\lim_{x\rightarrow a^+}\psi(x)&=Ae^{ika}+Be^{-ika}\\
\lim_{x\rightarrow a^-}\psi(x)&=Ce^{ika}+De^{-ika}\\
Ae^{ika}+Be^{-ika}&=Ce^{ika}+De^{-ika}\\
(A-C)e^{ika}&=(D-B)e^{-ika}\\
\Aboxed{A=C \ \ &, \ \ B = D}\\
\lim_{x\rightarrow -a^-}\psi(x)&=Fe^{ika}\\
\lim_{x\rightarrow -a^+}\psi(x)&=Ce^{ika}+De^{-ika}\\
Fe^{ika}&=Ce^{ika}+De^{-ika}\\
\Aboxed{F=De^{-2ika}&+C}
\end{align}$$
Differential constraints:
$$\begin{align}
\lim_{x\rightarrow -a^-}\psi'(x)&=ikFe^{ika}\\
\lim_{x\rightarrow -a^+}\psi'(x)&=ikCe^{ika}-ikDe^{-ika}\\
ikFe^{ika}&=ikCe^{ika}-ikDe^{-ika}\\
Fe^{ika}&=Ae^{ika}-Be^{-ika}\\
\end{align}$$
### 5.2
$$\begin{align}
...
\end{align}$$
