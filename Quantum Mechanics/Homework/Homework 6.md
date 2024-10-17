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
&=-8-12-4-1\\
\Aboxed{\int_{-3}^1\left(x^3-3x^2+2x-1\right)\cdot\delta(x+2)\ dx&=-25}
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
\int_{-\infty}^\infty f(x)\cdot\delta(cx)\ dx
&=\int_{-\infty}^\infty f\left(\dfrac{u}{c}\right)\cdot\delta(u)\ \dfrac{du}{|c|}\\
&=\dfrac{1}{|c|}\int_{-\infty}^\infty f\left(\dfrac{u}{c}\right)\cdot\delta(u)\ du\\
&=\dfrac{f(0)}{|c|}\\
\int_{-\infty}^\infty f(x)\cdot\delta(cx)\ dx&=\int_{-\infty}^\infty f\left(x\right)\cdot\dfrac{\delta(x)}{|c|}\ dx\\
\Aboxed{\delta(cx)&=\dfrac{\delta(x)}{|c|}}
\end{align}$$
### 2.2
Let $c=-1$:
$$\begin{align}
\delta(cx)&=\dfrac{\delta(x)}{|c|}\\
\delta(-x)&=\dfrac{\delta(x)}{|-1|}\\
\Aboxed{\delta(-x)&=\delta(x)}
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
\Aboxed{\sigma_x&=\dfrac{\sqrt{2}}{2}\dfrac{\hbar^2}{m\alpha}}
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
-\dfrac{\hbar^2}{2m}\left(\lim_{x\rightarrow a^+}\psi'(x)-\lim_{x\rightarrow a^-}\psi'(x)\right)&=\alpha\cdot\psi(a)\\
-\dfrac{\hbar^2}{2m}\left(-kAe^{-ka}-kB\left(e^{ka}-e^{-ka}\right)\right)&=\alpha\cdot Ae^{-ka}\\
\dfrac{\hbar^2k}{2m}\left(A+B\left(e^{2ka}-1\right)\right)&=\alpha\cdot A\\
A\left(\alpha-\dfrac{\hbar^2k}{2m}\right)&=\dfrac{\hbar^2k}{2m}\left(e^{2ka}-1\right)B\\
A&=\dfrac{\dfrac{\hbar^2k}{2m}\left(e^{2ka}-1\right)}{\alpha-\dfrac{\hbar^2k}{2m}}B\\
A&=\dfrac{\left(e^{2ka}-1\right)}{\dfrac{2m\alpha}{\hbar^2k}-1}B\\
\end{align}$$
### 4.4
$$\begin{align}
A&=\dfrac{\left(e^{2ka}-1\right)}{\dfrac{2m\alpha}{\hbar^2k}-1}B\\
A&=B\left(e^{2ka}+1\right)\\
\dfrac{A}{A}&=\dfrac{1}{\tfrac{2m\alpha}{\hbar^2k}-1}\dfrac{\left(e^{2ka}-1\right)}{\left(e^{2ka}+1\right)}\dfrac{B}{B}\\
\dfrac{2m\alpha}{\hbar^2k}-1&=\dfrac{e^{ka}-e^{-ka}}{e^{ka}+e^{-ka}}\\
\dfrac{2m\alpha}{\hbar^2k}&=\dfrac{\sinh(ka)}{\cosh(ka)}+1\\
\dfrac{2m\alpha}{\hbar^2}&=k\left(\tanh(ka)+1\right)\\
\end{align}$$
### 4.5
$$\begin{align}
\dfrac{2m\alpha}{\hbar^2}&=k\left(\tanh(ka)+1\right)\\
\dfrac{1}{4\alpha}\dfrac{8m\alpha^2}{\hbar^2}\dfrac{\hbar^2}{2m\alpha}&=k\dfrac{\hbar^2}{2m\alpha}\left(\tanh\left(k\dfrac{\hbar^2}{2m\alpha}\right)+1\right)\\
1&=k\dfrac{\hbar^2}{2m\alpha}\left(\tanh\left(k\dfrac{\hbar^2}{2m\alpha}\right)+1\right)\\
k&\approx0.63923\cdot\dfrac{2m\alpha}{\hbar^2}\\
\dfrac{\sqrt{-2mE}}{\hbar}&\approx0.63923\cdot\dfrac{2}{2a}\\
\dfrac{-2mE}{\hbar^2}&\approx0.63923^2\cdot\dfrac{1}{a^2}\\
E&\approx-0.63923^2\cdot\dfrac{\hbar^2}{2ma^2}\\
E&\approx-4\cdot0.63923^2\cdot\dfrac{\hbar^2}{8ma^2}\\
E&\approx-4\cdot0.63923^2\cdot0.1\text{ MeV}\\
\Aboxed{E&\approx-0.16345\text{ MeV}}\\
\end{align}$$
---
## Question 5
Assume a particle incident from the left described by the wave function:
$$\begin{align}
\psi(x)&=\begin{cases}
Ae^{ikx}+Be^{-ikx},&x<-a\\
Ce^{ikx}+De^{-ikx},&-a<x<a\\
Fe^{ikx},&x>a\\
\end{cases}\\
\psi'(x)&=\begin{cases}
ikAe^{ikx}-ikBe^{-ikx},&x<-a\\
ikCe^{ikx}-ikDe^{-ikx},&-a<x<a\\
ikFe^{ikx},&x>a\\
\end{cases}
\end{align}$$
### 5.1
**Continuity at $x=-a$:**
$$\begin{align}
\lim_{x\rightarrow -a^+}\psi(x)&=Ce^{-ika}+De^{ika}\\
\lim_{x\rightarrow -a^-}\psi(x)&=Ae^{-ika}+Be^{ika}\\
Ae^{-ika}+Be^{ika}&=Ce^{-ika}+De^{ika}\\
Ae^{-ika}-Ce^{-ika}&=+De^{ika}-Be^{ika}\\
(A-C)e^{-ika}&=(D-B)e^{ika}\\
\Aboxed{A&=(D-B)e^{2ika}+C}
\end{align}$$
**Continuity at $x=+a$:**
$$\begin{align}
\lim_{x\rightarrow a^+}\psi(x)&=Fe^{ika}\\
\lim_{x\rightarrow a^-}\psi(x)&=Ce^{ika}+De^{-ika}\\
Fe^{ika}&=Ce^{ika}+De^{-ika}\\
\Aboxed{F&=De^{-2ika}+C}
\end{align}$$
**Discontinuity at $x=-a$:**
$$\begin{align}
\lim_{x\rightarrow -a^+}\psi'(x)-\lim_{x\rightarrow -a^-}\psi'(x)&=-\dfrac{2m\alpha}{\hbar^2}\psi(-a)\\
ikAe^{-ika}-ikBe^{ika}-ikCe^{-ika}+ikDe^{ika}&=-\dfrac{2m\alpha}{\hbar^2}\left(Ae^{-ika}+Be^{ika}\right)\\
Ae^{-ika}-Be^{ika}-Ce^{-ika}+De^{ika}&=-\dfrac{2m\alpha}{ik\hbar^2}\left(Ae^{-ika}+Be^{ika}\right)\\
(A-C)+(D-B)e^{2ika}&=-\dfrac{2m\alpha}{ik\hbar^2}A-\dfrac{2m\alpha}{ik\hbar^2}Be^{2ika}\\
2(D-B)e^{2ika}&=-\dfrac{2m\alpha}{ik\hbar^2}A-\dfrac{2m\alpha}{ik\hbar^2}Be^{2ika}\\
\Aboxed{De^{2ika}-B\left(1+i\dfrac{m\alpha}{k\hbar^2}\right)e^{2ika}&=-\dfrac{m\alpha}{ik\hbar^2}A\\}
\end{align}$$
**Discontinuity at $x=+a$:**
$$\begin{align}
\lim_{x\rightarrow a^+}\psi'(x)-\lim_{x\rightarrow a^-}\psi'(x)&=-\dfrac{2m\alpha}{\hbar^2}\psi(a)\\
ikFe^{ika}-ikCe^{ika}+ikDe^{-ika}&=-\dfrac{2m\alpha}{\hbar^2}\left(Fe^{ika}\right)\\
Fe^{ika}-Ce^{ika}+De^{-ika}&=-\dfrac{2m\alpha}{ik\hbar^2}Fe^{ika}\\
(F-C)+De^{-2ika}&=-\dfrac{2m\alpha}{ik\hbar^2}F\\
De^{-2ika}+De^{-2ika}&=-\dfrac{2m\alpha}{ik\hbar^2}F\\
De^{-2ika}&=-\dfrac{m\alpha}{ik\hbar^2}F\\
\Aboxed{-\dfrac{ik\hbar^2}{m\alpha}De^{-2ika}&=F}\\
\end{align}$$
**Combination**
$$\begin{align}
\Aboxed{A&=(D-B)e^{2ika}+C}\\
\Aboxed{F&=De^{-2ika}+C}\\
\Aboxed{-\dfrac{m\alpha}{ik\hbar^2}A&=De^{2ika}-B\left(1+i\dfrac{m\alpha}{k\hbar^2}\right)e^{2ika}\\}\\
\Aboxed{F&=-\dfrac{ik\hbar^2}{m\alpha}De^{-2ika}}\\
\end{align}$$

Consequences
$$\begin{align}
C&=-\left(\dfrac{ik\hbar^2}{m\alpha}De^{-2ika}+1\right)\\
\end{align}$$
$$\begin{align}
A&=(D-B)e^{2ika}+\dfrac{ik\hbar^2}{m\alpha}De^{-2ika}-1\\
A&=-\dfrac{ik\hbar^2}{m\alpha}De^{2ika}+\dfrac{ik\hbar^2}{m\alpha}B\left(1+i\dfrac{m\alpha}{k\hbar^2}\right)e^{2ika}\\
\left(\dfrac{m\alpha}{ik\hbar^2}+1\right)De^{2ika}+De^{-2ika}-\dfrac{m\alpha}{ik\hbar^2}&=Be^{2ika}
\end{align}$$











