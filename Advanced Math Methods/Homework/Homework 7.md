**Name:** Stanley Goodwin
**Date:** 10/17/2024
**Collaborators:** None

In this assignment, we will evaluate the integral:
$$I=\int_0^\infty\dfrac{\sqrt{x}}{1+x^2}\ dx$$
**Hint:** It's a good idea to consider the complex square root with the branch cut on the positive real axis. Then, perform a contour integral around the branch cut, consisting of the following four concatenated parts.
1. Infinitesimally above the real axis, from $\epsilon$ to $R$.
2. CCW circle from the end of the segment 1, centered at the origin with radius $R$, ending infinitesimally below the real axis.
3. Going backwards toward the left from $R$ to $\epsilon$, infinitesimally below the real axis.
4. CW circle of radius $\epsilon$, centered around the origin, ending at the initial point.
Finally, take the limit as $\epsilon\rightarrow0$ and $R\rightarrow\infty$.
## Construction of the Integral
$$\int_0^\infty\dfrac{\sqrt{x}}{1+x^2}\ dx=\int_{\Gamma_1}\dfrac{\sqrt{z}}{1+z^2}\ dz+\int_{\Gamma_2}\dfrac{\sqrt{z}}{1+z^2}\ dz+\int_{\Gamma_3}\dfrac{\sqrt{z}}{1+z^2}\ dz+\int_{\Gamma_4}\dfrac{\sqrt{z}}{1+z^2}\ dz$$
$$\begin{align}
\int_{\Gamma_1}\dfrac{\sqrt{z}}{1+z^2}\ dz&=\int_{\epsilon}^{R}\dfrac{\sqrt{x+\delta}}{1+(x+\delta)^2}\ dx\\
\int_{\Gamma_2}\dfrac{\sqrt{z}}{1+z^2}\ dz&=\int_{0}^{2\pi}\dfrac{\sqrt{Re^{i\phi}}}{1+R^2e^{2i\phi}}\ iRe^{i\phi}d\phi\\
\int_{\Gamma_3}\dfrac{\sqrt{z}}{1+z^2}\ dz&=\int_{R}^{\epsilon}\dfrac{\sqrt{x-\delta}}{1+(x-\delta)^2}\ dx\\
\int_{\Gamma_4}\dfrac{\sqrt{z}}{1+z^2}\ dz&=\int_{2\pi}^{0}\dfrac{\sqrt{\epsilon e^{i\phi}}}{1+\epsilon^2e^{2i\phi}}\ i\epsilon e^{i\phi}d\phi\\
\end{align}$$


---
## Exercise 1
Prove that the contributions from pieces 2 and 4 vanish in the limit as $\epsilon\rightarrow0$ and $R\rightarrow\infty$.
$$\begin{align}
\int_{\Gamma_2}\dfrac{\sqrt{z}}{1+z^2}\ dz
&=\lim_{R\rightarrow\infty}\int_{0}^{2\pi}\dfrac{\sqrt{Re^{i\phi}}}{1+R^2e^{2i\phi}}\ iRe^{i\phi}d\phi\\
&=\lim_{R\rightarrow\infty}\int_{0}^{2\pi}\dfrac{iR^\tfrac{3}{2}\left(e^{i\phi}\right)^\tfrac{3}{2}}{1+R^2e^{2i\phi}}\ d\phi\\
&=\lim_{R\rightarrow\infty}\int_{0}^{2\pi}\dfrac{iR^\tfrac{3}{2}\left(e^{i\phi}\right)^\tfrac{3}{2}}{R^2e^{2i\phi}}\ d\phi\\
&=\lim_{R\rightarrow\infty}\int_{0}^{2\pi}\dfrac{i}{R^\tfrac{1}{2}e^{i\tfrac{1}{2}\phi}}\ d\phi\\
\Aboxed{\int_{\Gamma_2}\dfrac{\sqrt{z}}{1+z^2}\ dz&=0}
\end{align}$$
$$\begin{align}
\int_{\Gamma_4}\dfrac{\sqrt{z}}{1+z^2}\ dz
&=\lim_{\epsilon\rightarrow0}\int_{2\pi}^{0}\dfrac{\sqrt{\epsilon e^{i\phi}}}{1+\epsilon^2e^{2i\phi}}\ i\epsilon e^{i\phi}d\phi\\
&=\lim_{\epsilon\rightarrow0}\int_{2\pi}^{0}\dfrac{\sqrt{\epsilon e^{i\phi}}}{1+\epsilon^2e^{2i\phi}}\ i\epsilon e^{i\phi}d\phi\\
\end{align}$$
---
## Exercise 2
Prove that the contributions from pieces 1 and 3 sum up to $2I$.

---
## Exercise 3
Apply the residue theorem to calculate the final integral.
If everything is done correctly, the final result should be $I=\dfrac{\pi}{\sqrt{2}}$.
