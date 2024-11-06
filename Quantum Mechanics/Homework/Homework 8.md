**Name:** Stanley Goodwin
**Date:** 11/01/2024
**Collaborators:** None

---

$$\Psi(x,0)=\begin{cases}\dfrac{1}{\sqrt{2\lambda}}e^{i\tfrac{2\pi x}{\lambda}},&-\lambda<x<\lambda\\0,&\text{Elsewhere}\end{cases}$$
1.1)
$$|\Psi(x,0)|^2=\begin{cases}\dfrac{1}{2\lambda},&-\lambda<x<\lambda\\0,&\text{Elsewhere}\end{cases}$$
1.2)
$$\begin{align}
\Psi(p,0)&=\dfrac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^{\infty}e^{ipx/\hbar}\Psi(x,0) \ dx\\
&=\dfrac{1}{\sqrt{2\pi\hbar}}\int_{-\lambda}^{\lambda}e^{ipx/\hbar}\dfrac{1}{\sqrt{2\lambda}}e^{i\tfrac{2\pi x}{\lambda}} \ dx\\
&=\dfrac{1}{\sqrt{2\pi\hbar}}\dfrac{1}{\sqrt{2\lambda}}\int_{-\lambda}^{\lambda}e^{ipx/\hbar}e^{i\tfrac{2\pi x}{\lambda}} \ dx\\
&=\dfrac{1}{\sqrt{2\pi\hbar}}\dfrac{1}{\sqrt{2\lambda}}\int_{-\lambda}^{\lambda}e^{i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)x}\ dx\\
&=\dfrac{1}{\sqrt{2\pi\hbar}}\dfrac{1}{\sqrt{2\lambda}}\dfrac{1}{i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)}e^{i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)x}\left.\right|_{-\lambda}^\lambda\\
&=\dfrac{1}{\sqrt{2\pi\hbar}}\dfrac{1}{\sqrt{2\lambda}}\dfrac{1}{i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)}\left(e^{i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\lambda}-e^{-i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\lambda}\right)\\
&=\dfrac{1}{2i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\sqrt{\pi\lambda\hbar}}\left(e^{i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\lambda}-e^{-i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\lambda}\right)\\
&=\dfrac{2i}{2i\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\sqrt{\pi\lambda\hbar}}\sin\left(\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\lambda\right)\\
\Aboxed{\Psi(p,0)&=\dfrac{1}{\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\sqrt{\pi\lambda\hbar}}\sin\left(\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\lambda\right)}
\end{align}$$
1.3)
$$\begin{align}
|\Psi(p,0)|^2&=\dfrac{1}{\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)^2(\pi\lambda\hbar)}\sin^2\left(\left(p/\hbar+\tfrac{2\pi}{\lambda}\right)\lambda\right)
\end{align}$$



We define $Q^\dagger=-Q$:
2.1)
$$\begin{align}
\langle Q^\dagger\rangle&=\int_{-\infty}^\infty\psi^*(x)Q^\dagger\psi(x)\ dx\\
&=-\int_{-\infty}^\infty\psi^*(x)Q\psi(x)\ dx\\
\langle Q^\dagger\rangle&=-\langle Q\rangle\\
\end{align}$$


$$\begin{align}
-Q&=-\Re(Q)-\Im(Q)\\
Q^\dagger&=\Re(Q)-\Im(Q)\\
Q^\dagger-Q&=-2\Im(Q)
\end{align}$$





2.2)
$$\begin{align}
[A,B]^\dagger&=(AB-BA)^\dagger\\
&=(AB)^\dagger-(BA)^\dagger\\
&=B^\dagger A^\dagger-A^\dagger B^\dagger\\
&=-(A^\dagger B^\dagger-B^\dagger A^\dagger)\\
&=-(AB-BA)\\
[A,B]^\dagger&=-[A,B]
\end{align}$$


### 3
$$\sigma_A^2\sigma_B^2\ge\left(\dfrac{\langle[A,B]\rangle}{2i}\right)^2$$
$$\sigma_A\sigma_B\ge\dfrac{\langle[A,B]\rangle}{2i}$$


3.1)
$$\begin{align}
\sigma_x\sigma_p&\ge\dfrac{\langle[\hat{x},\hat{p}]\rangle}{2i}\\
\sigma_x\sigma_p&\ge\dfrac{i\hbar}{2i}\\
\Aboxed{\sigma_x\sigma_p&\ge\dfrac{\hbar}{2}}
\end{align}$$
3.2)
$$\begin{align}
\sigma_x\sigma_T&\ge\dfrac{\langle[\hat{x},\hat{T}]\rangle}{2i}\\
&=\dfrac{\langle\hat{x}\hat{T}-\hat{T}\hat{x}\rangle}{2i}\\
&=\dfrac{1}{4mi}\langle\hat{x}\hat{p}^2-\hat{p}^2\hat{x}\rangle\\
\end{align}$$
3.3)
$$\begin{align}
\sigma_U\sigma_p&\ge\dfrac{\langle[\hat{U},\hat{p}]\rangle}{2i}\\
&=\dfrac{\langle\hat{U}\hat{p}-\hat{p}\hat{U}\rangle}{2i}\\
&=\dfrac{k}{4i}\langle\hat{x}^2\hat{p}-\hat{p}\hat{x}^2\rangle\\
\end{align}$$

### 4
$$U=\dfrac{1}{\sqrt2}\begin{bmatrix}1&1\\i&-i\end{bmatrix}$$
4.1)
$$\begin{align}
U^\dagger&=\dfrac{1}{\sqrt2}\begin{bmatrix}1&1\\i&-i\end{bmatrix}^\dagger\\
&=\dfrac{1}{\sqrt2}\begin{bmatrix}1&-i\\1&i\end{bmatrix}\\
\end{align}$$
4.2)

