**Name:** Stanley Goodwin
**Date:** 12/09/2024
**Collaborators:** Chris Gravina, Hasanat Hasan
**Time Taken:** 2 Hours

---
### Question 1
In class, it was stated, without proof, that $L^2=L_\pm L_\mp+L_z^2\mp\hbar L_z$. Prove this relation.

**Observation 1:** $L_\pm=L_x\pm iL_y$.
$$\begin{align}
L_+L_-&=(L_x+iL_y)(L_x-iL_y)\\
&=L_x^2-iL_xL_y+iL_yL_x-i^2L_y^2\\
&=L_x^2+L_y^2-i[L_x,L_y]\\
&=L_x^2+L_y^2-i(i\hbar L_z)\\
\Aboxed{L_+L_-&=L_x^2+L_y^2+\hbar L_z}\\\\
L_-L_+&=(L_x-iL_y)(L_x+iL_y)\\
&=L_x^2+iL_xL_y-iL_yL_x-i^2L_y^2\\
&=L_x^2+L_y^2+i[L_x,L_y]\\
&=L_x^2+L_y^2+i(i\hbar L_z)\\
\Aboxed{L_-L_+&=L_x^2+L_y^2-\hbar L_z}
\end{align}$$
**Observation 2:** If we look at the magnitude of $L^2$, we find a resemblance where:
$$\begin{align}
L^2&=L_x^2+L_y^2+L_z^2\\
&=(L_+L_--\hbar L_z)+L_z^2\\
\Aboxed{L^2&=L_+L_-+L_z^2-\hbar L_z}\\\\
L^2&=L_x^2+L_y^2+L_z^2\\
&=(L_-L_++\hbar L_z)+L_z^2\\
\Aboxed{L^2&=L_-L_++L_z^2+\hbar L_z}\\
\end{align}$$
Combining the two expressions, we write our final expression as:
$$\begin{align}
\Aboxed{L^2&=L_\pm L_\mp+L_z^2\mp\hbar L_z}\\
\end{align}$$
---
### Question 2
**Note:** The $z$-component of angular momentum is $\hat{L}_z=\hat{x}\hat{p}_y-\hat{y}\hat{p}_x$.
#### 2.1
$$\begin{align}
[\hat{L}_z,\hat{x}]&=[\hat{x}\hat{p}_y-\hat{y}\hat{p}_x,\hat{x}]\\
&=[\hat{x}\hat{p}_y,\hat{x}]-[\hat{y}\hat{p}_x,\hat{x}]\\
&=\hat{x}[\hat{p}_y,\hat{x}]+[\hat{x},\hat{x}]\hat{p}_y-\hat{y}[\hat{p}_x,\hat{x}]-[\hat{y},\hat{x}]\hat{p}_x\\
&=0+0-\hat{y}(-i\hbar)-0\\
\Aboxed{[\hat{L}_z,\hat{x}]&=i\hbar\hat{y}}
\end{align}$$
#### 2.2
$$\begin{align}
[\hat{L}_z,\hat{y}]&=[\hat{x}\hat{p}_y-\hat{y}\hat{p}_x,\hat{y}]\\
&=[\hat{x}\hat{p}_y,\hat{y}]-[\hat{y}\hat{p}_x,\hat{y}]\\
&=\hat{x}[\hat{p}_y,\hat{y}]+[\hat{x},\hat{y}]\hat{p}_y-\hat{y}[\hat{p}_x,\hat{y}]-[\hat{y},\hat{y}]\hat{p}_x\\
&=\hat{x}(-i\hbar)+0-0-0\\
\Aboxed{[\hat{L}_z,\hat{y}]&=-i\hbar\hat{x}}
\end{align}$$
#### 2.3
$$\begin{align}
[\hat{L}_z,\hat{z}]&=[\hat{x}\hat{p}_y-\hat{y}\hat{p}_x,\hat{z}]\\
&=[\hat{x}\hat{p}_y,\hat{z}]-[\hat{y}\hat{p}_x,\hat{z}]\\
&=\hat{x}[\hat{p}_y,\hat{z}]+[\hat{x},\hat{z}]\hat{p}_y-\hat{y}[\hat{p}_x,\hat{z}]-[\hat{y},\hat{z}]\hat{p}_x\\
&=0+0-0-0\\
\Aboxed{[\hat{L}_z,\hat{z}]&=0}
\end{align}$$
#### 2.4
$$\begin{align}
[\hat{L}_z,\hat{p}_x]&=[\hat{x}\hat{p}_y-\hat{y}\hat{p}_x,\hat{p}_x]\\
&=[\hat{x}\hat{p}_y,\hat{p}_x]-[\hat{y}\hat{p}_x,\hat{p}_x]\\
&=\hat{x}[\hat{p}_y,\hat{p}_x]+[\hat{x},\hat{p}_x]\hat{p}_y-\hat{y}[\hat{p}_x,\hat{p}_x]-[\hat{y},\hat{p}_x]\hat{p}_x\\
&=0+i\hbar\hat{p}_y-0-0\\
\Aboxed{[\hat{L}_z,\hat{p}_x]&=i\hbar\hat{p}_y}
\end{align}$$
#### 2.5
$$\begin{align}
[\hat{L}_z,\hat{p}_y]&=[\hat{x}\hat{p}_y-\hat{y}\hat{p}_x,\hat{p}_y]\\
&=[\hat{x}\hat{p}_y,\hat{p}_y]-[\hat{y}\hat{p}_x,\hat{p}_y]\\
&=\hat{x}[\hat{p}_y,\hat{p}_y]+[\hat{x},\hat{p}_y]\hat{p}_y-\hat{y}[\hat{p}_x,\hat{p}_y]-[\hat{y},\hat{p}_y]\hat{p}_x\\
&=0+0-0-(i\hbar)\hat{p}_x\\
\Aboxed{[\hat{L}_z,\hat{p}_y]&=-i\hbar\hat{p}_x}
\end{align}$$
#### 2.6
$$\begin{align}
[\hat{L}_z,\hat{p}_z]&=[\hat{x}\hat{p}_y-\hat{y}\hat{p}_x,\hat{p}_z]\\
&=[\hat{x}\hat{p}_y,\hat{p}_z]-[\hat{y}\hat{p}_x,\hat{p}_z]\\
&=\hat{x}[\hat{p}_y,\hat{p}_z]+[\hat{x},\hat{p}_z]\hat{p}_y-\hat{y}[\hat{p}_x,\hat{p}_z]-[\hat{y},\hat{p}_z]\hat{p}_x\\
&=0+0-0-0\\
\Aboxed{[\hat{L}_z,\hat{p}_z]&=0}
\end{align}$$
#### 2.7
$$\begin{align}
[\hat{L}_z,\hat{r}^2]&=[\hat{L}_z,\hat{x}^2+\hat{y}^2+\hat{z}^2]\\
&=[\hat{L}_z,\hat{x}^2]+[\hat{L}_z,\hat{y}^2]+[\hat{L}_z,\hat{z}^2]\\
&=\hat{x}[\hat{L}_z,\hat{x}]+[\hat{L}_z,\hat{x}]\hat{x}
+\hat{y}[\hat{L}_z,\hat{y}]+[\hat{L}_z,\hat{y}]\hat{y}
+\hat{z}[\hat{L}_z,\hat{z}]+[\hat{L}_z,\hat{z}]\hat{z}\\
&=0+0+0+0+0+0\\
\Aboxed{[\hat{L}_z,\hat{r}^2]&=0}
\end{align}$$
#### 2.8
$$\begin{align}
[\hat{L}_z,\hat{p}^2]&=[\hat{L}_z,\hat{p}_x^2+\hat{p}_y^2+\hat{p}_z^2]\\
&=[\hat{L}_z,\hat{p}_x^2]+[\hat{L}_z,\hat{p}_y^2]+[\hat{L}_z,\hat{p}_z^2]\\
&=\hat{p}_x[\hat{L}_z,\hat{p}_x]+[\hat{L}_z,\hat{p}_x]\hat{p}_x
+\hat{p}_y[\hat{L}_z,\hat{p}_y]+[\hat{L}_z,\hat{p}_y]\hat{p}_y
+\hat{p}_z[\hat{L}_z,\hat{p}_z]+[\hat{L}_z,\hat{p}_z]\hat{p}_z\\
&=0+0+0+0+0+0\\
\Aboxed{[\hat{L}_z,\hat{p}^2]&=0}
\end{align}$$
#### 2.9
$$\begin{align}
[\vec{L},\hat{H}]&=\left[\vec{L},\dfrac{\vec{p}^2}{2m}+V(\hat{r})\right]\\
&=\left[\vec{L},\dfrac{\vec{p}^2}{2m}\right]+\left[\vec{L},V(\hat{r})\right]\\
&=\dfrac{1}{2m}\left[\vec{L},\vec{p}^2\right]+\left[\vec{L},V(\hat{r})\right]\\
&=\dfrac{1}{2m}\cdot0+0\\
\Aboxed{[\vec{L},\hat{H}]&=0}
\end{align}$$
Both commutators evaluate to $0$ because of question 2.7 and 2.8.

---
### Question 3
Show, using the generalized Ehrenfest theorem, that for any spherically-symmetric quantum problem that angular momentum is conserved, on average, in quantum mechanics.

With the choice of a spherically-symmetric potential, $\vec\tau=0$, and by extension $d\vec{L}/dt=0$.
Accounting for Question 2.9, where $[\vec{L},\hat{H}]=0$, we can then say:
$$\begin{align}
\dfrac{d\langle\vec{L}\rangle}{dt}
&=\dfrac{\langle[\vec{L},\hat{H}]\rangle}{i\hbar}+\left\langle\dfrac{d\vec{L}}{dt}\right\rangle\\
&=\dfrac{\langle0\rangle}{i\hbar}+\left\langle0\right\rangle\\
&=\dfrac{0}{i\hbar}+0\\
\Aboxed{\dfrac{d\langle\vec{L}\rangle}{dt}&=0}
\end{align}$$


