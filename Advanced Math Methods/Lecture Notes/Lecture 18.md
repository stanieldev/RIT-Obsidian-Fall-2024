**Name:** Stanley Goodwin
**Date:** 10/29/2024

---
### Example from Last Time
$$\begin{align}
\text{Given }\Omega&=\left[-R,R\right]\backslash\left[-\epsilon,\epsilon\right]\\
I&=\lim_{R\rightarrow\infty}\int_{-R}^R\dfrac{\sin(x)}{x}\ dx\\
&=\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\int_{{\Omega_{\epsilon,R}}}\dfrac{\sin(x)}{x}\ dx\\
\Aboxed{I&=\dfrac{1}{2i}\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\left(\int_{\Omega_{\epsilon,R}}\dfrac{e^{ix}}{x}\ dx-\int_{\Omega_{\epsilon,R}}\dfrac{e^{-ix}}{x}\ dx\right)}
\end{align}$$
### Continuation of Example
$$\begin{align}
\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\int_{\Omega_{\epsilon,R}}\dfrac{e^{ix}}{x}\ dx
+i\lim_{\epsilon\rightarrow0}\int_\pi^0e^{i(\epsilon e^{i\phi})}\ d\phi
+i\lim_{R\rightarrow\infty}\int_0^\pi e^{i(Re^{i\phi})}\ d\phi&=0\\
\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\int_{\Omega_{\epsilon,R}}\left(\dfrac{e^{ix}}{x}\right)\ dx-\pi i+0&=0\\
\Aboxed{\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\int_{\Omega_{\epsilon,R}}\dfrac{e^{ix}}{x}\ dx&=i\pi}
\end{align}$$
$$\begin{align}
\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\int_{\Omega_{\epsilon,R}}\dfrac{e^{-ix}}{x}\ dx
+i\lim_{\epsilon\rightarrow0}\int_\pi^0e^{i(\epsilon e^{i\phi})}\ d\phi
+i\lim_{R\rightarrow\infty}\int_0^\pi e^{i(Re^{i\phi})}\ d\phi&=0\\
\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\int_{\Omega_{\epsilon,R}}\left(\dfrac{e^{-ix}}{x}\right)\ dx+\pi i+0&=0\\
\Aboxed{\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\int_{\Omega_{\epsilon,R}}\dfrac{e^{-ix}}{x}\ dx&=-i\pi}
\end{align}$$
$$\begin{align}
\int_{-\infty}^\infty\dfrac{\sin(x)}{x}\ dx&=\dfrac{1}{2i}\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}\left(\int_{\Omega_{\epsilon,R}}\dfrac{e^{ix}}{x}\ dx-\int_{\Omega_{\epsilon,R}}\dfrac{e^{-ix}}{x}\ dx\right)\\
&=\dfrac{1}{2i}\left(i\pi-(-i\pi)\right)\\
&=\dfrac{2i\pi}{2i}\\
\Aboxed{\int_{-\infty}^\infty\dfrac{\sin(x)}{x}\ dx&=\pi}
\end{align}$$

### Another Example
Fourier Transform:
$$\begin{align}
\tilde{f}(t)&=\lim_{\Omega\rightarrow\infty}\int_{-\Omega}^\Omega e^{i\omega t}f(t)\ dt\\
f(t)&=\lim_{\Omega\rightarrow\infty}\int_{-\Omega}^\Omega e^{-i\omega t}\tilde{f}(\omega)\dfrac{d\omega}{2\pi}\\
\end{align}$$
Given the function $\tilde{f}(\omega)$:
$$\begin{align}
\tilde{f}(\omega)&=\dfrac{2}{T}\dfrac{\sin\left(\tfrac{\omega T}{2}\right)}{\omega}\\
f(t)&=\lim_{\Omega\rightarrow\infty}\int_{-\Omega}^\Omega e^{-i\omega t}\tilde{f}(\omega)\dfrac{d\omega}{2\pi}\\
&=\dfrac{1}{2i}\dfrac{1}{2\pi}\dfrac{2}{T}
\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}
\left(\int_{\Omega_{\epsilon,R}}e^{-i\omega t}\dfrac{e^{i\left(\tfrac{\omega T}{2}\right)}}{\omega}\ d\omega-\int_{\Omega_{\epsilon,R}}e^{-i\omega t}\dfrac{e^{-i\left(\tfrac{\omega T}{2}\right)}}{\omega}\ d\omega\right)\\
&=\dfrac{1}{2\pi i T}
\lim_{R\rightarrow\infty}\lim_{\epsilon\rightarrow0}
\left(\int_{\Omega_{\epsilon,R}}\dfrac{e^{i\omega \left(\tfrac{T}{2}-t\right)}}{\omega}\ d\omega-\int_{\Omega_{\epsilon,R}}\dfrac{e^{-i\omega\left(\tfrac{T}{2}+t\right)}}{\omega}\ d\omega\right)\\
&=\dfrac{1}{2\pi i T}\left(
\begin{cases}
+\pi i,& t<\tfrac{T}{2}\\
-\pi i,& t>\tfrac{T}{2}\\
\end{cases}-
\begin{cases}
-\pi i,& t>-\tfrac{T}{2}\\
+\pi i,& t<-\tfrac{T}{2}\\
\end{cases}
\right)\\
&=\dfrac{1}{2\pi i T}
\begin{cases}
0,& -\infty<t<-\tfrac{T}{2}\\
2\pi i,& -\tfrac{T}{2}<t<+\tfrac{T}{2}\\
0,& +\tfrac{T}{2}<t<+\infty\\
\end{cases}\\
f(t)&=\begin{cases}\tfrac{1}{T},& -\tfrac{T}{2}<t<+\tfrac{T}{2}\\0&\text{Elsewhere}\end{cases}\\
\Aboxed{f(t)&=\dfrac{1}{T}\chi{\left[-\tfrac{T}{2},\tfrac{T}{2}\right]}}
\end{align}$$
Where $\chi(a,b)$ is the step function of 1 on the interval $[a,b]$ and 0 elsewhere.


### Analytic Continuation
Given $f(z)$ is a holomorphic function on $\Omega\subset\mathbb{C}$ and $z_0\in\Omega$, we say that $z_0$ is a zero of order $m$ if:
$$f(z)=(z-z_0)^mg(z)$$
Where $g(z)$ is a holomorphic function on $\Omega$ and that $g(z)\ne0$.

**Theorem:** 
1) If $f(z)$ is holomorphic on $\Omega\subset\mathbb{C}$,
2) $\Omega$ is *path-connected* and *open*, 
3) $f^{(n)}(z_0)=0 \ \forall n\in\mathbb{Z}^+_0$ for $z_0\in\Omega$.
$\implies f(z)=0\ \forall z\in\Omega$.

