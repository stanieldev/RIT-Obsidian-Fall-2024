**Name:** Stanley Goodwin
**Date:** 12/02/2024
**Collaborators:** Ethan
**Time Taken:** 5 Hours

---
## Question 1
Use the following to answer the next two parts:
$$\begin{align}
L_q&=e^x\dfrac{d^q}{dx^q}\left(e^{-x}x^q\right)
\end{align}$$
### 1.1
Derive an expression for $L_2$.
$$\begin{align}
L_2(x)&=e^x\dfrac{d^2}{dx^2}\left(e^{-x}x^2\right)\\
&=e^x\dfrac{d}{dx}\left(2xe^{-x}-x^2e^{-x}\right)\\
&=e^x\left(2e^{-x}-4xe^{-x}+x^2e^{-x}\right)\\
\Aboxed{L_2(x)&=x^2-4x+2}\\
\end{align}$$
### 1.2
Derive an expression for $L_3$.
$$\begin{align}
L_3&=e^x\dfrac{d^3}{dx^3}\left(e^{-x}x^3\right)\\
&=e^x\dfrac{d^2}{dx^2}\left(-x^3e^{-x}+3x^2e^{-x}\right)\\
&=e^x\dfrac{d}{dx}\left(x^3e^{-x}-6x^2e^{-x}+6xe^{-x}\right)\\
&=e^x\left(-x^3e^{-x}+3x^2e^{-x}-12xe^{-x}+6x^2e^{-x}+6e^{-x}-6xe^{-x}\right)\\
\Aboxed{L_3&=-x^3+9x^2-18x+6}
\end{align}$$
---
## Question 2
Use the following to answer the next two parts:
$$\begin{align}
L_{q-p}^p&=(-1)^p\dfrac{d^p}{dx^p}L_q
\end{align}$$
### 2.1
Derive an expression for $L_2^1$.
$$\begin{align}
L_{3-1}^1&=-\dfrac{d}{dx}L_3\\
&=-\dfrac{d}{dx}\left(-x^3+9x^2-18x+6\right)\\
\Aboxed{L_{2}^1&=3x^2-18x+18}
\end{align}$$
### 2.2
Derive an expression for $L_1^2$.
$$\begin{align}
L_{3-2}^2&=(-1)^2\dfrac{d^2}{dx^2}L_3\\
&=\dfrac{d^2}{dx^2}\left(-x^3+9x^2-18x+6\right)\\
\Aboxed{L_{1}^2&=-6x+18}
\end{align}$$
---
## Question 3
Given the wavefunction of the ground state of hydrogen:
$$\begin{align}
\psi_{100}(r,\theta,\phi)&=\dfrac{1}{\sqrt{\pi}a_0^{3/2}}e^{-r/a_0}
\end{align}$$
### 3.1
Find the expected value of position for the hydrogen atom in the ground state.
$$\begin{align}
\langle x\rangle
&=\int\psi_{100}^\dagger(r,\theta,\phi)\ \hat{x}\ \psi_{100}(r,\theta,\phi)\ d\tau\\
&=\int_{0}^{2\pi}\int_{0}^\pi\int_0^\infty\dfrac{1}{\pi a_0^3}e^{-2r/a_0}r\sin\theta\cos\phi\ r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\dfrac{1}{\pi a_0^3}\int_{0}^{2\pi}\cos\phi\ d\phi\int_{0}^\pi\sin^2\theta\ d\theta\int_0^\infty r^3e^{-2r/a_0}\ dr\ \\
\Aboxed{\langle x\rangle&=0}
\end{align}$$
### 3.2
Find the expected value of the square of position for the hydrogen atom in the ground state.
$$\begin{align}
\langle x^2\rangle
&=\int\psi_{100}^\dagger(r,\theta,\phi)\ \hat{x}^2 \psi_{100}(r,\theta,\phi)\ d\tau\\
&=\int_{0}^{2\pi}\int_{0}^\pi\int_0^\infty\dfrac{1}{\pi a_0^3}e^{-2r/a_0}r^2\sin^2\theta\cos^2\phi\ r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\dfrac{1}{\pi a_0^3}\int_{0}^{2\pi}\cos^2\phi\ d\phi\int_{0}^\pi\sin^3\theta\ d\theta\int_0^\infty r^4e^{-2r/a_0}\ dr\ \\
&=\dfrac{1}{\pi a_0^3}\cdot\pi\cdot\dfrac{4}{3}\dfrac{a_0^5}{2^5}\int_0^\infty w^4e^{-w}\ dw\ \\
&=a_0^2\dfrac{4!}{24}\\
\Aboxed{\langle x^2\rangle&=a_0^2}
\end{align}$$
### 3.3
Find the expected value of the kinetic energy for the Hydrogen atom.
$$\begin{align}
\langle T\rangle
&=\int\psi_{100}^\dagger(r,\theta,\phi)\hat{T}\psi_{100}(r,\theta,\phi)\ d\tau\\
&=\int\dfrac{1}{\sqrt{\pi}a_0^{3/2}}e^{-r/a_0}\left(-\dfrac{\hbar^2}{2m}\vec\nabla^2\right)\dfrac{1}{\sqrt{\pi}a_0^{3/2}}e^{-r/a_0}\ d\tau\\
&=-\dfrac{\hbar^2}{2m}\dfrac{1}{\pi a_0^3}\int_0^\infty4\pi r^2e^{-r/a_0}\vec\nabla^2e^{-r/a_0}\ dr\\
&=-\dfrac{2\hbar^2}{ma_0^3}\int_0^\infty r^2e^{-r/a_0}\vec\nabla^2e^{-r/a_0}\ dr\\
\end{align}$$
Calculating the Laplacian, we can see that:
$$\begin{align}
\vec\nabla^2 e^{-r/a_0}
&=\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2 \dfrac{\partial}{\partial r}e^{-r/a_0}\right)\\
&=-\dfrac{1}{a_0}\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2e^{-r/a_0}\right)\\
\Aboxed{\vec\nabla^2 e^{-r/a_0}&=-\dfrac{1}{a_0}\dfrac{1}{r^2}\left(2re^{-r/a_0}-\dfrac{1}{a_0}r^2e^{-r/a_0}\right)}
\end{align}$$
Continuing, we find that:
$$\begin{align}
\langle T\rangle
&=-\dfrac{2\hbar^2}{ma_0^3}\int_0^\infty r^2e^{-r/a_0}\vec\nabla^2e^{-r/a_0}\ dr\\
&=-\dfrac{2\hbar^2}{ma_0^3}\int_0^\infty -r^2\dfrac{1}{a_0}\dfrac{1}{r^2}\left(2re^{-r/a_0}-\dfrac{1}{a_0}r^2e^{-r/a_0}\right)e^{-r/a_0}\ dr\\
&=\dfrac{2\hbar^2}{ma_0^3}\int_0^\infty\dfrac{1}{a_0}\left(2r-\dfrac{1}{a_0}r^2\right)e^{-2r/a_0}\ dr\\
&=\dfrac{\hbar^2}{ma_0^2}\int_0^\infty\left(\dfrac{2r}{a_0}-\dfrac{1}{4}\left(\dfrac{2r}{a_0^2}\right)^2\right)e^{-2r/a_0}\ \dfrac{2dr}{a_0}\\
&=\dfrac{\hbar^2}{ma_0^2}\int_0^\infty\left(w-\dfrac{1}{4}w^2\right)e^{-w}\ dw, \ \ \ w=2r/a_0\\
&=\dfrac{\hbar^2}{ma_0^2}\int_0^\infty we^{-w}\ dw-\dfrac{\hbar^2}{4ma_0^2}\int_0^\infty w^2e^{-w}\ dw\\
&=\dfrac{\hbar^2}{ma_0^2}\cdot1-\dfrac{\hbar^2}{4ma_0^2}\cdot2\\
&=\dfrac{2\hbar^2}{2ma_0^2}-\dfrac{\hbar^2}{2ma_0^2}\\
\Aboxed{\langle T\rangle&=\dfrac{\hbar^2}{2ma_0^2}}
\end{align}$$
### 3.4
Find $\langle x^2\rangle$ for $n=2,l=1,m=+1$.
$$\begin{align}
R(r)&=\dfrac{1}{2\sqrt{6}a_0^{3/2}}\dfrac{r}{a_0}e^{-r/2a_0}\\
\Theta(\theta)&=\dfrac{\sqrt{3}}{2}\sin\theta\\
\Phi(\phi)&=\dfrac{1}{\sqrt{2\pi}}e^{i\phi}
\end{align}$$
Source: http://hyperphysics.phy-astr.gsu.edu/hbase/quantum/hydwf.html

Using the above, we can get a wavefunction:
$$\begin{align}
\psi_{211}(r,\theta,\phi)&=\dfrac{1}{8\sqrt{\pi}a_0^{5/2}}\cdot re^{-r/2a_0}e^{i\phi}\sin\theta\\
\psi_{211}^\dagger(r,\theta,\phi)&=\dfrac{1}{8\sqrt{\pi}a_0^{5/2}}\cdot re^{-r/2a_0}e^{-i\phi}\sin\theta
\end{align}$$
We can then find $\langle x^2\rangle$ similar to the previous problem:
$$\begin{align}
\langle x^2\rangle
&=\int\psi_{211}^\dagger(r,\theta,\phi)\hat{x}^2 \psi_{211}(r,\theta,\phi)\ d\tau\\
&=\int\left(\dfrac{1}{8\sqrt{\pi}a_0^{5/2}}\cdot re^{-r/2a_0}e^{-i\phi}\sin\theta\right)\left(r\sin\theta\cos\phi\right)^2\left(\dfrac{1}{8\sqrt{\pi}a_0^{5/2}}\cdot re^{-r/2a_0}e^{i\phi}\sin\theta\right)\ d\tau\\
&=\dfrac{1}{64\pi a_0^{5}}\int_{0}^{2\pi}\int_{0}^\pi\int_0^\infty\left(r^4e^{-r/a_0}\sin^4\theta\cos^2\phi\right)r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\dfrac{1}{64\pi a_0^{5}}\int_{0}^{2\pi}\cos^2\phi\ d\phi\int_{0}^\pi\sin^5\theta\ d\theta\int_0^\infty r^6e^{-r/a_0}\ dr\ \\
&=\dfrac{1}{64\pi a_0^{5}}\cdot\pi\cdot\dfrac{16}{15}\cdot a_0^7\int_0^\infty \dfrac{r^6}{a_0^6}e^{-r/a_0}\ \dfrac{dr}{a_0}, \ \ \ w=r/a_0\\
&=\dfrac{a_0^2}{60}\int_0^\infty w^6e^{-w}\ dw\\
&=\dfrac{a_0^2}{60}\cdot 6!\\
&=\dfrac{a_0^2}{60}\cdot 6!\\
\Aboxed{\langle x^2\rangle&=12a_0^2}
\end{align}$$
---
## Question 4
A hydrogen atom starts out with the initial wavefunction:
$$\begin{align}
\psi(\vec{r},0)=\dfrac{\psi_{2,1,1}+\psi_{2,1,-1}}{\sqrt{2}}
\end{align}$$
### 4.1
Construct $\psi(\vec{r},t)$. Simplify as much as possible.
$$\begin{align}
\psi(\vec{r},t)&=\int e^{-i\vec{k}\cdot\vec{r}}\phi(\vec{k},0)e^{-iE_nt/\hbar}\ d^3\vec{k}\\
\phi(\vec{k},0)&=\int e^{i\vec{k}\cdot\vec{r}}\psi(\vec{r},0)\ d^3\vec{r}\\
\end{align}$$
#### Finding $\psi(\vec{r},0)$
Using a table online at this [link](https://chem.libretexts.org/Courses/University_of_California_Davis/Chem_107B%3A_Physical_Chemistry_for_Life_Scientists/Chapters/4%3A_Quantum_Theory/4.10%3A_The_Schr%C3%B6dinger_Wave_Equation_for_the_Hydrogen_Atom), we can write the position-space wavefunction as:
$$\begin{align}
\psi_{2,1,\pm1}(\vec{r},0)&=\dfrac{1}{\sqrt{64\pi}a_0^{5/2}}re^{-r/2a_0}\sin\theta\ e^{\pm i\phi}
\end{align}$$
So we can find the superposition as the following:
$$\begin{align}
\psi(\vec{r},0)
&=\dfrac{1}{\sqrt{2}}\dfrac{1}{\sqrt{64\pi}a_0^{5/2}}re^{-r/2a_0}\sin\theta\left(e^{i\phi}+e^{-i\phi}\right)\\
&=\dfrac{2}{\sqrt{2}}\dfrac{1}{\sqrt{64\pi}a_0^{5/2}}re^{-r/2a_0}\sin\theta\cos\phi\\
\Aboxed{\psi(\vec{r},0)&=\dfrac{1}{\sqrt{32\pi}a_0^{5/2}}re^{-r/2a_0}\sin\theta\cos\phi}
\end{align}$$
We can then write the total wavefunction as:
$$\begin{align}
\Aboxed{\psi(\vec{r},0)&=\dfrac{1}{\sqrt{32\pi}a_0^{5/2}}re^{-r/2a_0}\sin\theta\cos\phi e^{-iE_2t/\hbar}, \ \ \ E_2=-\dfrac{\hbar^2}{8ma_0^2}}
\end{align}$$
### 4.2
Find a formula for the expected value of potential energy $\langle V\rangle$.
$$\begin{align}
\langle V\rangle
&=\int\psi^\dagger(\vec{r},0)\hat{V}\psi(\vec{r},0)\ d^3\vec{r}\\
&=\dfrac{1}{32\pi a_0^{5}}\int\left(-\dfrac{1}{4\pi\epsilon_0}\dfrac{e^2}{r}\right)r^2e^{-r/a_0}\sin^2\theta\cos^2\phi\ \cdot r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=-\dfrac{e^2}{4\pi\epsilon_0}\dfrac{1}{32\pi a_0^{5}}\int_0^{2\pi}\int_0^\pi \int_0^\infty r^3e^{-r/a_0}\sin^3\theta\cos^2\phi\ dr\ d\theta\ d\phi\\
&=-\dfrac{e^2}{4\pi\epsilon_0}\dfrac{1}{32\pi a_0^{5}}\int_0^{2\pi}\cos^2\phi\ d\phi\int_0^\pi\sin^3\theta\ d\theta\int_0^\infty r^3e^{-r/a_0}\ dr\\
&=-\dfrac{e^2}{4\pi\epsilon_0}\dfrac{1}{32\pi a_0}\pi\dfrac{4}{3}\int_0^\infty \dfrac{r^3}{a_0^3}e^{-r/a_0}\ \dfrac{dr}{a_0}\\
&=-\dfrac{e^2}{96\pi\epsilon_0a_0}\int_0^\infty w^3e^{-w}\ dw\\
&=-\dfrac{e^2}{16\pi\epsilon_0a_0}\\
&=-\dfrac{e^2}{16\pi\epsilon_0}\dfrac{me^2}{4\pi\epsilon_0\hbar^2}\\
\Aboxed{\langle V\rangle&=-\dfrac{me^4}{64\pi^2\epsilon_0^2\hbar^2}}
\end{align}$$
### 4.3
$$\begin{align}
\langle V\rangle
&=-\dfrac{me^4}{64\pi^2\epsilon_0^2\hbar^2}\\
&=-\dfrac{(9.11\cdot10^{-31}\text{kg})(1.60\cdot10^{-19}\text{C})^4}{64\pi^2(8.85\cdot10^{-12}\text{ F/m})^2(1.05\cdot10^{-34}\text{J}\cdot\text{s})^2}\\
&=-1.095\cdot10^{-18}\text{ J}\\
\Aboxed{\langle V\rangle&=-6.832\text{ eV}}
\end{align}$$
### 4.4
The potential is independent of time since the expected distance of the electron stays at a uniform distance from the nucleus, and so the central potential is static in time. If the electron were to change the average distance from the nucleus, there would be a response of the potential with time, but this situation isn't one of those cases.