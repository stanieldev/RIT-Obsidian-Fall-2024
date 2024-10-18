**Name:** Stanley Goodwin
**Date:** 10/17/2024
**Collaborators:** None
**Status:** Revision 2

In this assignment, we consider the function $f(z)=\dfrac{\ln(z-(2-i))}{z(z-i)^2}$, where $\ln$ refers to the principal branch of the logarithm function. The goal is to explore the singularities of this function, its series expansions, and to compute contour integrals.

---
## Exercise 1
*Describe all singularities of $f(z)$ and classify each as either a pole, branch point, or other type of singularity. Additionally, provide a clear sketch indicating the location of each singularity in the complex plane.*

Given the function $f(z)=\dfrac{\ln(z-(2-i))}{z(z-i)^2}$, we can see the following:
 - $z=0$ (Order-1 pole)
 - $z=i$ (Order-2 pole)
 - $z\in\left\{x-i\ |\ x\le2\right\}$ (Interval branch-cut)
### Graph of $f(z)$
![[HW6_Q1.png]]

---
## Exercise 2
Consider $z_a=0$. Determine whether it is possible to express $f(z)$ as a Laurent series (bilateral series) of the form:
$$f(z)=\sum_{n=-\infty}^\infty a_n(z-z_a)^n$$
*If such a series exists, determine the annulus of convergence, (i.e. the radius of its internal boundary $\rho_1$ and the radius of its external boundary $\rho_2$). Also, state explicitly if the series involves negative powers and what is the smallest value of $n$ such that $a_n\ne0$.*

About the point $z_b=0$, the closest singularity (that is not the center) is the point $z=\pm i$ on the branch cut of the natural log and the order-2 singularity.
$$\begin{align}
\Aboxed{\rho_1=0, &\rho_2=1}\\
\Aboxed{|z-z_a|&\in\left(0,1\right)}
\end{align}$$
The inner singularity has a radius of 0, since it's centered at a singularity, but the outer one is able to go out to a radius of 1 before encountering a singularity.

Since this series expansion does enclose a pole at the origin, the Laurent series is necessary to express this function about the point $z=0$.
Therefore, the smallest $a_n\ne0$ is $n=-1$, with the term $\dfrac{a_{-1}}{z}$.

I'm not sure why the order-2 singularity at radius 1 wouldn't contribute to the Laurent series, but based on lecture material the above is the correct statement.

---
## Exercise 3
Consider $z_b=2$. Determine whether it is possible to express $f(z)$ as a Laurent series (bilateral series) of the form:
$$f(z)=\sum_{n=-\infty}^\infty b_n(z-z_b)^n$$
*If such a series exists, determine the annulus of convergence, (i.e. the radius of its internal boundary $\rho_1$ and the radius of its external boundary $\rho_2$). Also, state explicitly if the series involves negative powers and what is the smallest value of $n$ such that $b_n\ne0$.*

About the point $z_b=2$, the closest singularity is the point $z=2-i$ on the branch cut of the natural log. The radius between the center rand this point is 1, written as:
$$\begin{align}
\Aboxed{\rho_1=0, &\rho_2=1}\\
\Aboxed{|z-z_a|&\in\left[0,1\right)}
\end{align}$$
Since it doesn't enclose any poles, the Laurent series is equal to a Taylor series.
Put differently, the smallest $b_n\ne0$ is $n=0$.

---
## Exercise 4
Consider $z_c=-1-2i$. Determine whether it is possible to express $f(z)$ as a Laurent series (bilateral series) of the form:
$$f(z)=\sum_{n=-\infty}^\infty c_n(z-z_c)^n$$
*If such a series exists, determine the annulus of convergence, (i.e. the radius of its internal boundary $\rho_1$ and the radius of its external boundary $\rho_2$). Also, state explicitly if the series involves negative powers and what is the smallest value of $n$ such that $c_n\ne0$.*

About the point $z_c=-1-2i$, the closest singularity is the point $z=-1-i$ on the branch cut of the natural log. The radius between the center rand this point is 1, written as:
$$\begin{align}
\Aboxed{\rho_1=0, &\rho_2=1}\\
\Aboxed{|z-z_a|&\in\left[0,1\right)}
\end{align}$$
Since it doesn't enclose any poles, the Laurent series is equal to a Taylor series.
Put differently, the smallest $c_n\ne0$ is $n=0$.

---
## Exercise 5
Consider a closed counter-clockwise curve $\gamma$ around the point $z=i$ with radius $1/2$.
*Compute the contour integral:*
$$I=\oint_{\gamma}f(z)\ dz$$
About the point $z_0=i$, there is only 1 enclosed singularity within a circle of radius 1/2, which is a pole of order 2 at $z=i$. Therefore, we can write:
$$\begin{align}
\mathrm{Res}(f,i)&=\dfrac{1}{(2-1)!}\lim_{z\rightarrow i}\dfrac{d^1}{dz^1}\left((z-i)^2f(z)\right)\\
&=\lim_{z\rightarrow i}\dfrac{d}{dz}\left(\dfrac{\ln(z-(2-i))}{z}\right)\\
&=\lim_{z\rightarrow i}\dfrac{1}{z^2}\left(\dfrac{z}{z-2+i}-\ln(z-2+i)\right)\\
&=\dfrac{i}{2-2i}+\ln(-2+2i)\\
&=\dfrac{i}{2-2i}\dfrac{2+2i}{2+2i}+\ln\left(\sqrt{8}e^{i\tfrac{3\pi}{4}}\right)\\
&=\dfrac{(i)(2+2i)}{4+4}+\ln\left(\sqrt{8}e^{i\tfrac{3\pi}{4}}\right)\\
&=\dfrac{-1+i}{4}+\dfrac{3}{2}\ln(2)+i\dfrac{3\pi}{4}\\
\mathrm{Res}(f,i)&=\dfrac{6\ln(2)-1}{4}+\dfrac{3\pi-1}{4}i\\
\end{align}$$
Then, to find the integral, we can use the residue theorem to write:
$$\begin{align}
I&=\oint_{\gamma}f(z)\ dz\\
&=2\pi i\cdot \mathrm{Res}(f,i)\\
&=2\pi i\cdot \left(\dfrac{6\ln(2)-1}{4}+\dfrac{3\pi-1}{4}i\right)\\
&=\dfrac{2\pi(6\ln(2)-1)}{4}i+\dfrac{2\pi(3\pi-1)}{4}i^2\\
\Aboxed{I&=-\dfrac{2\pi(3\pi-1)}{4}+\dfrac{2\pi(6\ln(2)-1)}{4}i}
\end{align}$$
