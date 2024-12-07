**Name:** Stanley Goodwin
**Date:** 12/09/2024
**Collaborators:** None
**Time Taken:** X Hours

---
### Question 1
In class, it was stated, without proof, that $L^2=L_\pm L_\mp+L_z^2\mp\hbar L_z$. Prove this relation.
**Note:** $L_\pm=L_x\pm iL_y$
$$\begin{align}
L^2&=L_\pm L_\mp+L_z^2\mp\hbar L_z\\
&=(L_x\pm iL_y)(L_x\mp iL_y)+L_z^2\mp\hbar L_z\\
&=(L_x^2\mp iL_xL_y\pm iL_yL_x+L_y^2)+L_z^2\mp\hbar L_z\\
&=L_x^2\mp[L_x,L_y]+L_y^2+L_z^2\mp\hbar L_z\\
&=L_x^2+L_y^2+L_z^2\mp\hbar L_z\pm\hbar L_z\\
\Aboxed{L^2&=L_x^2+L_y^2+L_z^2}\\
\end{align}$$
### Question 2
$$\begin{align}
[L_z,x]\ket{lm}
&=(L_zx-xL_z)\ket{lm}\\
&=L_zx\ket{lm}-xL_z\ket{lm}\\
&=L_zx\ket{lm}-xm\hbar\ket{lm}
\end{align}$$


### Question 3
Show, using the generalized Ehrenfest theorem, that for any spherically-symmetric quantum problem that angular momentum is conserved, on average, in quantum mechanics.
$$\begin{align}
\dfrac{d}{dt}\langle L\rangle=\dfrac{\langle[L,\hat{H}]\rangle}{i\hbar}+\left\langle\dfrac{dL}{dt}\right\rangle
\end{align}$$
