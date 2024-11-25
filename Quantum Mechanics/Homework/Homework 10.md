

### Question 1 (Verified)
$$\begin{align}
L_q&=e^x\dfrac{d^q}{dx^q}\left(e^{-x}x^q\right)
\end{align}$$
#### 1.1
$$\begin{align}
L_2(x)&=e^x\dfrac{d^2}{dx^2}\left(e^{-x}x^2\right)\\
&=e^x\dfrac{d}{dx}\left(2xe^{-x}-x^2e^{-x}\right)\\
&=e^x\left(2e^{-x}-4xe^{-x}+x^2e^{-x}\right)\\
\Aboxed{L_2(x)&=x^2-4x+2}\\
\end{align}$$
#### 1.2
$$\begin{align}
L_3&=e^x\dfrac{d^3}{dx^3}\left(e^{-x}x^3\right)\\
&=e^x\dfrac{d^2}{dx^2}\left(-x^3e^{-x}+3x^2e^{-x}\right)\\
&=e^x\dfrac{d}{dx}\left(x^3e^{-x}-6x^2e^{-x}+6xe^{-x}\right)\\
&=e^x\left(-x^3e^{-x}+3x^2e^{-x}-12xe^{-x}+6x^2e^{-x}+6e^{-x}-6xe^{-x}\right)\\
\Aboxed{L_3&=-x^3+9x^2-18x+6}
\end{align}$$
### Question 2 (Verified)
$$\begin{align}
L_{q-p}^p&=(-1)^p\dfrac{d^p}{dx^p}L_q
\end{align}$$
#### 2.1
$$\begin{align}
L_{3-1}^1&=-\dfrac{d}{dx}L_3\\
&=-\dfrac{d}{dx}\left(-x^3+9x^2-18x+6\right)\\
\Aboxed{L_{2}^1&=3x^2-18x+18}
\end{align}$$
#### 2.2
$$\begin{align}
L_{3-2}^2&=(-1)^2\dfrac{d^2}{dx^2}L_3\\
&=\dfrac{d^2}{dx^2}\left(-x^3+9x^2-18x+6\right)\\
\Aboxed{L_{1}^2&=-6x+18}
\end{align}$$
---

### Question 3
$$\begin{align}
\psi_{100}(r,\theta,\phi)&=\dfrac{1}{\sqrt{\pi}a_0^{3/2}}e^{-r/a_0}
\end{align}$$
#### 3.1
$$\begin{align}
\langle x\rangle
&=\int\psi_{100}^\dagger(r,\theta,\phi)\ \hat{x}\ \psi_{100}(r,\theta,\phi)\ d\tau\\
&=\int_{0}^{2\pi}\int_{0}^\pi\int_0^\infty\dfrac{1}{\pi a_0^3}e^{-2r/a_0}r\sin\theta\cos\phi\ r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\dfrac{1}{\pi a_0^3}\int_{0}^{2\pi}\cos\phi\ d\phi\int_{0}^\pi\sin^2\theta\ d\theta\int_0^\infty r^3e^{-2r/a_0}\ dr\ \\
\Aboxed{\langle x\rangle&=0}
\end{align}$$
#### 3.2
$$\begin{align}
\langle x^2\rangle
&=\int\psi_{100}^\dagger(r,\theta,\phi)\ \hat{x}^2 \psi_{100}(r,\theta,\phi)\ d\tau\\
&=\int_{0}^{2\pi}\int_{0}^\pi\int_0^\infty\dfrac{1}{\pi a_0^3}e^{-2r/a_0}r^2\sin^2\theta\cos^2\phi\ r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\dfrac{1}{\pi a_0^3}\int_{0}^{2\pi}\cos^2\phi\ d\phi\int_{0}^\pi\sin^3\theta\ d\theta\int_0^\infty r^4e^{-2r/a_0}\ dr\ \\
&=\dfrac{1}{\pi a_0^3}\cdot\pi\cdot\dfrac{4}{3}\dfrac{a_0^5}{2^5}\int_0^\infty w^4e^{-w}\ dw\ \\
&=a_0^2\dfrac{4!}{24}\\
\Aboxed{\langle x^2\rangle&=a_0^2}
\end{align}$$










### TMP
$$\begin{align}
...
\end{align}$$


