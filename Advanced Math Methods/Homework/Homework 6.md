**Name:** Stanley Goodwin
**Date:** 10/13/2024
**Collaborators:** None

In this assignment, we consider the function $f(z)=\ln(z-(3+i))\tfrac{1}{z^2}$, where $\ln$ refers to the principal branch of the logarithm function. The goal is to explore the singularities of this function, its series expansions, and to compute contour integrals.

---
## Exercise 1
*Describe all singularities of $f(z)$ and classify each as either a pole, branch point, or other type of singularity. Additionally, provide a clear sketch indicating the location of each singularity in the complex plane.*

Given the function $f(z)=\ln(z-(3+i))\tfrac{1}{z^2}$, we can see the following:
 - Branch cut singularity at $z=x+i, x\lt3$.
 - Branch point at $z=3+i$.
 - Order 2 singular at $z=0+0i$

I originally did my plot in Desmos, but it looked quite boring.
I used a complex field grapher instead, and so I have the following result:
![[HW6_Q1.png]]
Exactly the same things I predicted in my mathematics.
It makes it much clearer where the branch cut is, as well as the branch point.

---
## Exercise 2
Consider $z_0=2$. Determine whether it is possible to express $f(z)$ as a Taylor series of the form:
$$f(z)=\sum_{n=0}^\infty a_n(z-z_0)^n$$
*If such a series exists, determine the radius of convergence.*
Since the terms never explode to infinity, there should be a series representation between the 2 closest singularities nearby.
Since there is a singularity at $z=0+0i$ and $z=3+i$, and $z=2+0i$ falls within the circle who's diameter is spanned between the singularities:
$$\begin{align}
2r&=|(3+i)-(0+0i)|\\
&=|(3+i)|\\
&=\sqrt{3^2+1^2}\\
&=\sqrt{10}\\
\Aboxed{r&=\dfrac{\sqrt{10}}{2}}
\end{align}$$
For this series, there's a radius of convergence who's radius is $\dfrac{\sqrt{10}}{2}$ centered at the point $z=\dfrac{3}{2}+\dfrac{1}{2}i$.

---
## Exercise 3
Consider $z_0=0$. Determine whether it is possible to express $f(z)$ as a Laurent series (bilateral series) of the form:
$$f(z)=\sum_{n=-\infty}^\infty b_n(z-z_0)^n$$
*If such a series exists, determine the radius of convergence.*
$$\begin{align}
b_0&=\ln(0-(3+i))\tfrac{1}{(0)^2}\\
&=\ln(-(3+i))\cdot\infty\\
&=\infty\\
\end{align}$$
There does not exist a series that centers at $z_0=0+0i$ that represents $f(z)$.

---
## Exercise 4
Consider $z_0=3+i$. Determine whether it is possible to express $f(z)$ as a Laurent series (bilateral series) of the form:
$$f(z)=\sum_{n=-\infty}^\infty c_n(z-z_0)^n$$
*If such a series exists, determine the radius of convergence.*
$$\begin{align}
c_0&=\ln((3+i)-(3+i))\tfrac{1}{(3+i)^2}\\
&=\ln(0)\tfrac{1}{(3+i)^2}\\
&=-\infty\\
\end{align}$$
There does not exist a series that centers at $z_0=3+i$ that represents $f(z)$.


---
## Exercise 5
Consider a closed counter-clockwise curve $\gamma_1$ around the point $1−i$ with radius $1$. Compute the contour integral:
$$I_1=\oint_{\gamma_1}f(z)\ dz$$
This contour is centered on the branch cut mentioned earlier.
The branch cut is traversed twice, but in opposite directions.
$$I_1=\oint_{\gamma_1}f(z)\ dz=2\pi i-2\pi i=0$$
This results in a total integral of 0, since the effects of the branch cut are reversed before the end of the contour.

---
## Exercise 6
Consider a closed counter-clockwise curve $\gamma_2$ around the origin with radius $1$. Compute the contour integral:
$$I_2=\oint_{\gamma_2}f(z)\ dz$$
This contour is centered on the order-2 pole, as well as touches the branch cut at $z=i$.
Unfortunately, that makes this calculation a good bit more difficult.
$$\begin{align}
I_2&=\oint_{\gamma_2}f(z)\ dz\\
&=\lim_{r\rightarrow1}\int_0^{2\pi}\dfrac{\ln(re^{i\phi}-(3+i))}{(re^{i\phi})^2}\ 1\cdot d\phi\\
&=\lim_{r\rightarrow1}\dfrac{1}{r^2}\int_0^{2\pi}e^{-2i\phi}\ln(re^{i\phi}-(3+i))\ d\phi\\
&=-i\lim_{r\rightarrow1}\int_{\ln(r-(3+i))}^{\ln(r-(3+i))}\dfrac{u\cdot e^u}{\left(e^u+(3+i)\right)^3}\ du\\
&=-i\int_{\ln(-3-i)}^{\ln(-3-i)}\dfrac{u\cdot e^u}{\left(e^u+(3+i)\right)^3}\ du\\
&=0\\
\end{align}$$
We can justify this with the 2 following limits.
If we look at radius slightly larger than 1, then like problem #5, the contour passes through the branch cut twice in opposing directions, and so they cancel out to 0.
If we look at radius slightly smaller than 1, there is no singularity encompassed other than the order-2 pole in the center, and that singularity doesn't contribute to the closed contour integral. Therefore, the value 0 is very much reasonable in both limits.
