**Name:** Stanley Goodwin
**Date:** XX/XX/2024
**Collaborators:** None



## 1
$$x=x_0\left(a^\dagger+a\right), x_0=\sqrt{\dfrac{\hbar}{2m\omega}}$$
$$p=p_0\left(a^\dagger-a\right), p_0=\sqrt{\dfrac{m\hbar\omega}{2}}$$
### 1.1
$$\begin{align}
\langle x\rangle&=\int\bra{\psi_n(x)}x\ket{\psi_n(x)}\ dx\\
&=\int\bra{\psi_n(x)}x_0\left(a^\dagger+a\right)\ket{\psi_n(x)}\ dx\\
&=x_0\int\bra{\psi_n(x)}\left(a^\dagger+a\right)\ket{\psi_n(x)}\ dx\\
&=x_0\int\bra{\psi_n(x)}\left(a^\dagger\ket{\psi_n(x)}+a\ket{\psi_n(x)}\right)\ dx\\
&=x_0\int\bra{\psi_n(x)}\left(\sqrt{n+1}\ket{\psi_{n+1}(x)}+\sqrt{n}\ket{\psi_{n-1}(x)}\right)\ dx\\
&=x_0\sqrt{n+1}\int\bra{\psi_n(x)}\ket{\psi_{n+1}(x)}\ dx+x_0\sqrt{n}\int\bra{\psi_n(x)}\mathbb{}\ket{\psi_{n-1}(x)}\ dx\\
\Aboxed{\langle x\rangle&=0}
\end{align}$$

$$\begin{align}
\langle p\rangle&=\int\bra{\psi_n(x)}p\ket{\psi_n(x)}\ dx\\
&=\int\bra{\psi_n(x)}ip_0\left(a^\dagger-a\right)\ket{\psi_n(x)}\ dx\\
&=ip_0\int\bra{\psi_n(x)}\left(a^\dagger-a\right)\ket{\psi_n(x)}\ dx\\
&=ip_0\int\bra{\psi_n(x)}\left(a^\dagger\ket{\psi_n(x)}-a\ket{\psi_n(x)}\right)\ dx\\
&=ip_0\int\bra{\psi_n(x)}\left(\sqrt{n+1}\ket{\psi_{n+1}(x)}-\sqrt{n}\ket{\psi_{n-1}(x)}\right)\ dx\\
&=ip_0\sqrt{n+1}\int\bra{\psi_n(x)}\ket{\psi_{n+1}(x)}\ dx+x_0\sqrt{n}\int\bra{\psi_n(x)}\ket{\psi_{n-1}(x)}\ dx\\
\Aboxed{\langle p\rangle&=0}
\end{align}$$
$$\begin{align}
\langle x^2\rangle&=\int\bra{\psi_n(x)}x^2\ket{\psi_n(x)}\ dx\\
&=\int\bra{\psi_n(x)}x_0^2\left(a^\dagger+a\right)^2\ket{\psi_n(x)}\ dx\\
&=x_0^2\int\bra{\psi_n(x)}\left(a^\dagger a^\dagger+a a^\dagger+a^\dagger a+aa\right)\ket{\psi_n(x)}\ dx\\
&=x_0^2\int\bra{\psi_n(x)}\left(a^\dagger a^\dagger+1+aa\right)\ket{\psi_n(x)}\ dx\\
&=x_0^2\int\bra{\psi_n(x)}\left(\sqrt{n+2}\sqrt{n+1}\ket{\psi_{n+2}(x)}+\psi_{n}(x)+\sqrt{n}\sqrt{n-1}\ket{\psi_{n-2}(x)}\right)\ dx\\
&=x_0^2\int\bra{\psi_n(x)}\ket{\psi_{n}(x)}dx\\
\Aboxed{\langle x^2\rangle&=x_0^2=\dfrac{\hbar}{2m\omega}}
\end{align}$$
$$\begin{align}
\langle p^2\rangle&=\int\bra{\psi_n(x)}p^2\ket{\psi_n(x)}\ dx\\
&=\int\bra{\psi_n(x)}p_0^2\left(a^\dagger-a\right)^2\ket{\psi_n(x)}\ dx\\
&=i^2p_0^2\int\bra{\psi_n(x)}\left(a^\dagger a^\dagger-a a^\dagger-a^\dagger a+aa\right)\ket{\psi_n(x)}\ dx\\
&=-p_0^2\int\bra{\psi_n(x)}\left(a^\dagger a^\dagger-1+aa\right)\ket{\psi_n(x)}\ dx\\
&=-p_0^2\int\bra{\psi_n(x)}\left(\sqrt{n+2}\sqrt{n+1}\ket{\psi_{n+2}(x)}-\psi_{n}(x)+\sqrt{n}\sqrt{n-1}\ket{\psi_{n-2}(x)}\right)\ dx\\
&=p_0^2\int\bra{\psi_n(x)}\ket{\psi_{n}(x)}dx\\
\Aboxed{\langle p^2\rangle&=p_0^2=\dfrac{m\hbar\omega}{2}}
\end{align}$$
$$\begin{align}
\sigma_x&=\sqrt{\langle x^2\rangle-\langle x\rangle^2}\\
&=\sqrt{\dfrac{\hbar}{2m\omega}-0^2}\\
\sigma_x&=\sqrt{\dfrac{\hbar}{2m\omega}}\\
\sigma_p&=\sqrt{\langle p^2\rangle-\langle p\rangle^2}\\
&=\sqrt{\dfrac{m\hbar\omega}{2}-0^2}\\
\sigma_p&=\sqrt{\dfrac{m\hbar\omega}{2}}\\
\end{align}$$
$$\begin{align}
\sigma_x\sigma_p&=\sqrt{\dfrac{\hbar}{2m\omega}}\sqrt{\dfrac{m\hbar\omega}{2}}\\
&=\sqrt{\dfrac{\hbar}{2m\omega}\dfrac{m\hbar\omega}{2}}\\
&=\sqrt{\left(\dfrac{\hbar}{2}\right)^2}\\
\Aboxed{\sigma_x\sigma_p&=\dfrac{\hbar}{2}}
\end{align}$$

These are missing $n$. Use the wikipedia:
https://en.wikipedia.org/wiki/Quantum_harmonic_oscillator










## 2
$$\psi_0(x)=\left(\dfrac{m\omega}{\hbar\pi}\right)^{1/4}e^{-\tfrac{n\omega}{2\hbar}x^2}$$
$$\psi_1(x)=\left(\dfrac{m\omega}{\hbar\pi}\right)^{1/4}xe^{-\tfrac{n\omega}
{2\hbar}x^2}$$
$$\begin{align}
\psi_2(x)&=\dfrac{1}{\sqrt{2}}a^\dagger\psi_1(x)\\
&=\dfrac{1}{\sqrt{2}}a^\dagger\left(\dfrac{m\omega}{\hbar\pi}\right)^{1/4} xe^{-\tfrac{n\omega}
{2\hbar}x^2}\\
&=\dfrac{1}{\sqrt{2}}\left(\dfrac{m\omega}{\hbar\pi}\right)^{1/4} a^\dagger\left(xe^{-\tfrac{m\omega}
{2\hbar}x^2}\right)\\
&=\dfrac{1}{\sqrt{2}}\left(\dfrac{m\omega}{\hbar\pi}\right)^{1/4} \sqrt{\dfrac{m\omega}{2\hbar}}\left(x-\dfrac{\hbar}{m\omega}\dfrac{d}{dx}\right)\left(xe^{-\tfrac{m\omega}
{2\hbar}x^2}\right)\\
&=\dfrac{1}{\sqrt{2}}\left(\dfrac{m\omega}{\hbar\pi}\right)^{1/4} \sqrt{\dfrac{m\omega}{\hbar\pi}}\sqrt{\dfrac{\pi}{2}}\left(x^2+x-\dfrac{\hbar}{m\omega}
\right)e^{-\tfrac{m\omega}
{2\hbar}x^2}\\
&=\dfrac{\sqrt{\pi}}{2}\left(\dfrac{m\omega}{\hbar\pi}\right)^{3/4} \left(x^2+x-\dfrac{\hbar}{m\omega}
\right)e^{-\tfrac{m\omega}
{2\hbar}x^2}\\
\end{align}$$





## 3
$$\begin{align}
\sin\left(a^\dagger a\right)\psi_n(x)&=\sum_{k=0}^\infty\dfrac{(-1)^k}{(2k+1)!}\left(a^\dagger a\right)^{2k+1}\psi_n(x)\\
&=\sum_{k=0}^\infty\dfrac{(-1)^k}{(2k+1)!}n^{2k+1}\psi_n(x)\\
&=\sin(n)\cdot\psi_n(x)\\
\Aboxed{\sin\left(a^\dagger a\right)&=\sin(n)}
\end{align}$$

$$\begin{align}
e^{\left(a^\dagger a+1\right)^2}\psi_n(x)&=\sum_{k=0}^\infty\dfrac{1}{k!}\left(a^\dagger a+1\right)^{2k}\psi_n(x)\\
&=\sum_{k=0}^\infty\dfrac{1}{k!}\left(n^2\right)^{k}\psi_n(x)\\
&=e^{n^2}\psi_n(x)\\
\Aboxed{e^{\left(a^\dagger a+1\right)^2}&=e^{n^2}}
\end{align}$$


## 4
Let $\Psi(x,t)=A\left[3\psi_0(x)+2\psi_1(x)\right]e^{-\tfrac{iEt}{\hbar}}$

### 4.1
$$\begin{align}
\int\Psi^\dagger(x,0)\Psi(x,0)\ dx &= \int A^2\left[3\psi_0(x)+2\psi_1(x)\right]^2 dx\\
1&=A^2\left(9\int\psi_0^\dagger(x)\psi_0(x) dx+4\int\psi_1^\dagger(x)\psi_1(x) dx\right)\\
1&=13A^2\\
\Aboxed{A&=\dfrac{1}{\sqrt{13}}}
\end{align}$$
### 4.2
$$\begin{align}
|\Psi(x,t)|^2&=A^2\left[3\psi_0(x)+2\psi_1(x)\right]^2\left(e^{+\tfrac{iEt}{\hbar}}e^{-\tfrac{iEt}{\hbar}}\right)\\
&=A^2\left[3\psi_0(x)+2\psi_1(x)\right]^2\\
|\Psi(x,t)|^2&=\dfrac{9}{13}\psi_0(x)^2+\dfrac{12}{13}\psi_0(x)\psi_1(x)+\dfrac{4}{13}\psi_1(x)^2\\
\end{align}$$



