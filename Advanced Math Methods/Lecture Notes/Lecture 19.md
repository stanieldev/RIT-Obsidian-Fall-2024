**Name:** Stanley Goodwin
**Date:** 10/31/2024

---
### Analytic Continuation
Given $f(z)$ is a holomorphic function on $\Omega\subset\mathbb{C}$ and $z_0\in\Omega$, we say that $z_0$ is a zero of order $m$ if:
$$f(z)=(z-z_0)^mg(z)$$
Where $g(z)$ is a holomorphic function on $\Omega$ and that $g(z_0)\ne0$.

**Theorem 1** 
1) If $f(z)$ is holomorphic on $\Omega\subset\mathbb{C}$,
2) $\Omega$ is *path-connected* and *open*, 
3) $f^{(n)}(z_0)=0 \ \forall n\in\mathbb{Z}^+_0$ for $z_0\in\Omega$.
$\implies f(z)=0\ \forall z\in\Omega$.

**Theorem 2**
1) If $f(z)$ is holomorphic on $\Omega\subset\mathbb{C}$,
2) $\Omega$ is *path-connected* and *open*, 
3) $f^{(n)}(z_0)=0 \ \forall n\in\mathbb{Z}^+_0$ for $z_0\in\Omega$.
$\implies$All zeros are isolated singularities, unless $f(z)=0\ \forall z\in\Omega$ (the zero function).

**Theorem 3**
1) If $f(z)$ and $g(z)$ are a holomorphic functions on $\Omega\subset\mathbb{C}$
2) $f(z)=g(z)$ on a continuous interval of $l_z\subset\Omega$
$\implies f(z)=g(z)\ \forall z\in\Omega$.

### Example 1
Let's take the example of the sum of the geometric series:
$$\begin{align}
f(z)&=\sum_{n=0}^\infty z^n=\dfrac{1}{1-z}, \ \ \ z\in\Omega\\
\Omega&=\left\{\ z\ |\ |z|\le1\right\}-\{1+0i\}
\end{align}$$
For a domain that is outside the given set above, they must have the same function outside the domain as inside the domain, given Theorem 3, excluding the poles.
$$\begin{align}
f(z)&=\dfrac{1}{1-z}, \ \ \ z\in\Omega_\text{AC}\\
\Omega_\text{AC}&=\left\{\ z\ |\ |z|>1\right\}-\{1+0i\}
\end{align}$$
Therefore, the function $f(z)$ extends the summation to the entire complex plane par $z=1+0i$.
$$\begin{align}
\sum_{n=0}^\infty z^n&=\dfrac{1}{1-z}, \ \ \ z\in\mathbb{C}\backslash\{1+0i\}\\
\end{align}$$
This doesn't mean that the summation is *equal* to the function outside of its original domain, but it follows that this is the *only* extension that is holomorphic.

### Example 2
Let's take the new example of the (real) *gamma function*:
$$\begin{align}
\Gamma(z)&=\int_0^\infty t^{z-1}e^{-t}\ dt, \ \ \ z\in\Omega\\
\Omega&=\left\{\ x+0i\ |\ 0<x<\infty\right\}
\end{align}$$
For a domain that extends outside the real axis, the function outside must be *equal* in the entire complex plane bar singularities, since another holomorphic function $g(z)$ is equal to $f(z)$ on the entire positive real axis, and so:
$$\begin{align}
\Gamma(z)&=\int_0^\infty t^{z-1}e^{-t}\ dt, \ \ \ z\in\Omega_\text{AC}\\
\Omega_\text{AC}&=\left\{\ x+iy\ |\ x\in\mathbb{R}-\mathbb{Z}^-_0\ \&\ y\ne0\right\}
\end{align}$$
Therefore, the function $f(z)$ extends the gamma function to the entire complex plane bar negative integers and 0.
$$\begin{align}
\Gamma(z)&=\int_0^\infty t^{z-1}e^{-t}\ dt, \ \ \ z\in\mathbb{C}-\mathbb{Z}^-_0
\end{align}$$
Since there is no typically defined way to represent the gamma function on the complex plane, we define the complex gamma function as the above.
