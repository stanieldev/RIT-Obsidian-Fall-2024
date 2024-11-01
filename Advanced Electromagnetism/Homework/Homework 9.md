**Name:** Stanley Goodwin
**Date:** 11/02/2024
**Collaborators:** None
**Time Taken:** XXX Hours

---
## Question 1
In class (and/or Griffiths section 9.3.2) we worked out the case of normally incident light, and claimed that reflected and transmitted waves have the same *polarization* as the incident wave (on the $x$-axis). *Prove this must be true by starting with fully general reflected and transmitted polarization directions $\hat{n}_R=n_{Rx}\hat{x}+n_{Ry}\hat{y}$ and $\hat{n}_T=n_{Tx}\hat{x}+n_{Ty}\hat{y}$ and showing that our boundary conditions require that $n_{Ry}=n_{Ty}=0$.*
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel &
\epsilon_1\vec{E}_1^\perp&=\epsilon_2\vec{E}_2^\perp\\
\vec{B}_1^\perp&=\vec{B}_2^\perp &
\dfrac{1}{\mu_1}\vec{B}_1^\parallel&=\dfrac{1}{\mu_2}\vec{B}_2^\parallel\\
\end{align}$$
Electric Field Perpendicular:
$$\begin{align}
\epsilon_1\vec{E}_1^\perp&=\epsilon_2\vec{E}_2^\perp\\
-\epsilon_1\tilde{E}_I\sin\theta_I+\epsilon_1\tilde{E}_R\sin\theta_R&=-\epsilon_2\tilde{E}_T\sin\theta_T\\
-\epsilon_1\tilde{E}_In_{Iy}+\epsilon_1\tilde{E}_Rn_{Ry}&=-\epsilon_2\tilde{E}_Tn_{Ty}\\
\epsilon_1\tilde{E}_Rn_{Ry}&=-\epsilon_2\tilde{E}_Tn_{Ty}\\
\end{align}$$
Not sure how this would prove that $n_{Ry}=n_{Ty}=0$. 





---
## Question 2
Electromagnetic Waves in Matter.
### 2.A
Starting with Maxwell’s Equations in Matter (in terms of the $\vec{D}$ and $\vec{H}$ fields), show that,
for a linear, homogenous dielectric (i.e. $\vec{D}=\epsilon\vec{E}$ and $\vec{B}=\mu\vec{H}$, where $\epsilon$ and $\mu$ are uniform, constant scalars) with no free charges or currents ($\rho_\text{free}=0$ and $\vec{J}_\text{free}=0$), both the $\vec{E}$ and the $\vec{B}$ fields obey a wave equation with wave speed given by $v=\dfrac{1}{\sqrt{\mu\epsilon}}$.
Given Maxwell's Equations:
$$\begin{align}
\vec\nabla\cdot\vec{D}&=0\\
\vec\nabla\cdot\vec{H}&=0\\
\vec\nabla\times\vec{D}&=-\mu\epsilon\dfrac{\partial\vec{H}}{\partial t}\\
\vec\nabla\times\vec{H}&=\dfrac{\partial\vec{D}}{\partial t}
\end{align}$$
Then we can write the twice curls of each field as:
$$\begin{align}
\vec\nabla\times\left(\vec\nabla\times\vec{D}\right)&=\vec\nabla\left(\vec\nabla\cdot\vec{D}\right)-\vec\nabla^2\vec{D}\\
\vec\nabla\times\left(-\mu\epsilon\dfrac{\partial\vec{H}}{\partial t}\right)&=\vec\nabla\left(0\right)-\vec\nabla^2\vec{D}\\
\mu\epsilon\dfrac{\partial\left(\vec\nabla\times\vec{H}\right)}{\partial t}&=\vec\nabla^2\vec{D}\\
\Aboxed{\mu\epsilon\dfrac{\partial^2\vec{D}}{\partial t^2}&=\vec\nabla^2\vec{D}}\\
\vec\nabla\times\left(\vec\nabla\times\vec{H}\right)&=\vec\nabla\left(\vec\nabla\cdot\vec{H}\right)-\vec\nabla^2\vec{H}\\
\vec\nabla\times\left(\dfrac{\partial\vec{D}}{\partial t}\right)&=\vec\nabla\left(0\right)-\vec\nabla^2\vec{H}\\
\dfrac{\partial\left(\vec\nabla\times\vec{D}\right)}{\partial t}&=-\vec\nabla^2\vec{D}\\
-\mu\epsilon\dfrac{\partial^2\vec{D}}{\partial t^2}&=-\vec\nabla^2\vec{D}\\
\Aboxed{\mu\epsilon\dfrac{\partial^2\vec{D}}{\partial t^2}&=\vec\nabla^2\vec{D}}\\
\end{align}$$
In the place where $1/v^2$, we have $\mu\epsilon$, and so:
$$\boxed{v=\dfrac{1}{\sqrt{\mu\epsilon}}}$$
### 2.B
Starting from the same equations as in part A, rewrite them in integral form, then briefly sketch out the reasoning which leads to all the boundary conditions on $\vec{E}$ and $\vec{B}$ at a planar interface between two different linear materials (labeled 1 and 2), with permittivities and permeabilities $\epsilon_1, \mu_1$ and $\epsilon_2, \mu_2$, respectively (again, assume no free charges or currents are present).

Given Maxwell's Equations:
$$\begin{align}
\oint\vec{D}\cdot d\vec{A}&=0\\
\oint\vec{H}\cdot d\vec{A}&=0\\
\oint\vec{D}\cdot d\vec{l}&=-\mu\epsilon\dfrac{d}{dt}\int\vec{H}\cdot d\vec{A}\\
\oint\vec{H}\cdot d\vec{l}&=\dfrac{d}{dt}\int\vec{D}\cdot d\vec{A}
\end{align}$$
Then we can write the twice curls of each field as:
$$\begin{align}
...
\end{align}$$
---
## Question 3
In our Worksheet 15 last Thursday, we worked out the case of reflection and transmission at normal incidence and found the reflection and transmission coefficients $R$ and $T$ (you can find Griffiths’s derivation in 9.3.2). We simplified the process by assuming that $\mu_1=\mu_2=\mu_0$. *Now, drop that assumption (i.e. keep $\mu_1$ and $\mu_2$ general) and find the general formulas for $R$ and $T$.* To check, *explicitly confirm that $R+T=1$ still* (as it must be).

**Hint:** You don’t have to redo work that we (and Griffiths) already did once. Use whatever you need from Griffiths 9.3.2, just be careful not to use results where he assumed $\mu_1=\mu_2=\mu_0$. You should be able to express your final results for $R$ and $T$ as simple functions of $\beta$.

Starting with the boundary conditions:
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel\\
\vec{B}_1^\perp&=\vec{B}_2^\perp\\
\epsilon_1\vec{E}_1^\perp&=\epsilon_2\vec{E}_2^\perp\\
\dfrac{1}{\mu_1}\vec{B}_1^\parallel&=\dfrac{1}{\mu_2}\vec{B}_2^\parallel\\
\end{align}$$
We only really need the parallel components since the perpendicular is trivial (normal).
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel\\
\tilde{E}_I+\tilde{E}_R&=\tilde{E}_T\\
\end{align}$$
$$\begin{align}
\dfrac{1}{\mu_1}\vec{B}_1^\parallel&=\dfrac{1}{\mu_2}\vec{B}_2^\parallel\\
\dfrac{1}{\mu_1}\tilde{B}_I-\dfrac{1}{\mu_1}\tilde{E}_R&=\dfrac{1}{\mu_2}\tilde{B}_T\\
\dfrac{1}{\mu_1c_1}\left(\tilde{E}_I-\tilde{E}_R\right)&=\dfrac{1}{\mu_2c_2}\tilde{E}_T\\
\tilde{E}_I-\tilde{E}_R&=\dfrac{\mu_1c_1}{\mu_2c_2}\tilde{E}_T\\
\end{align}$$
From there, we can find that:
$$\begin{align}
2\tilde{E}_I+0\tilde{E}_R&=\tilde{E}_T+\dfrac{\mu_1c_1}{\mu_2c_2}\tilde{E}_T\\
2\tilde{E}_I&=\left(1+\dfrac{\mu_1c_1}{\mu_2c_2}\right)\tilde{E}_T\\
\tilde{E}_T&=\left(\dfrac{2}{1+\tfrac{\mu_1c_1}{\mu_2c_2}}\right)\tilde{E}_I\\
\end{align}$$
And
$$\begin{align}
0\tilde{E}_I+2\tilde{E}_R&=\tilde{E}_T-\dfrac{\mu_1c_1}{\mu_2c_2}\tilde{E}_T\\
2\tilde{E}_R&=\left(1-\dfrac{\mu_1c_1}{\mu_2c_2}\right)\tilde{E}_T\\
2\tilde{E}_R&=\left(1-\dfrac{\mu_1c_1}{\mu_2c_2}\right)\left(\dfrac{2}{1+\tfrac{\mu_1c_1}{\mu_2c_2}}\right)\tilde{E}_I\\
\tilde{E}_R&=\left(\dfrac{1-\tfrac{\mu_1c_1}{\mu_2c_2}}{1+\tfrac{\mu_1c_1}{\mu_2c_2}}\right)\tilde{E}_I\\
\end{align}$$
Putting it all together, we get:
$$\begin{align}
\tilde{E}_T&=\left(\dfrac{2}{1+\tfrac{\mu_1c_1}{\mu_2c_2}}\right)\tilde{E}_I=\left(\dfrac{2}{1+\beta}\right)\tilde{E}_I\\
\tilde{E}_R&=\left(\dfrac{1-\tfrac{\mu_1c_1}{\mu_2c_2}}{1+\tfrac{\mu_1c_1}{\mu_2c_2}}\right)\tilde{E}_I=\left(\dfrac{1-\beta}{1+\beta}\right)\tilde{E}_I\\
\end{align}$$
To find the transmission and reflection coefficients:
$$\begin{align}
R&=\left(\dfrac{1-\beta}{1+\beta}\right)^2\dfrac{\tilde{E}_I^2}{\tilde{E}_I^2}\\
\Aboxed{R&=\dfrac{(1-\beta)^2}{(1+\beta)^2}, \ \ \ \beta=\tfrac{\mu_1c_1}{\mu_2c_2}}
\end{align}$$
$$\begin{align}
T&=\dfrac{\epsilon_2c_2}{\epsilon_1c_1}\left(\dfrac{2}{1+\beta}\right)^2\dfrac{\tilde{E}_I^2}{\tilde{E}_I^2}\\
&=\dfrac{\epsilon_2c_2}{\epsilon_1c_1}\dfrac{4}{(1+\beta)^2}\dfrac{\tilde{E}_I^2}{\tilde{E}_I^2}\\
\Aboxed{T&=\dfrac{\epsilon_2c_2}{\epsilon_1c_1}\dfrac{4}{(1+\beta)^2}, \ \ \ \beta=\tfrac{\mu_1c_1}{\mu_2c_2}}\\
\end{align}$$
To make sure I did everything correct, let's see if $T+R=1$:
$$\begin{align}
T+R&=\dfrac{(\mu_2n_1-\mu_1n_2)^2}{(\mu_2n_1+\mu_1n_2)^2}+\dfrac{\epsilon_2n_1}{\epsilon_1n_2}\dfrac{4(\mu_2n_1)^2}{(\mu_2n_1+\mu_1n_2)^2}\\
\end{align}$$



---
## Question 4
In class (and in Griffiths 9.3.3), we worked out the case of reflection and transmission at any angle. However, we were specifically considering the case in which the incident electric field is polarized in the plane of incidence. You will now repeat that process for the different case where the electric field is polarized perpendicular to the plane of incidence. You may once again assume $\mu_1=\mu_2=\mu_0$.
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel\\
\vec{B}_1^\perp&=\vec{B}_2^\perp\\
\epsilon_1\vec{E}_1^\perp&=\epsilon_2\vec{E}_2^\perp\\
\dfrac{1}{\mu_1}\vec{B}_1^\parallel&=\dfrac{1}{\mu_2}\vec{B}_2^\parallel\\
\end{align}$$
### 4.A
Make a clear sketch (modeled on Griffiths Figure 9.15) of the geometry and angles for this case, then write out what the four boundary conditions become in this case (i.e. modify Griffiths Equations 9.101 through 9.104 for the new situation.
$$\begin{align}
...
\end{align}$$
### 4.B
Find the new "Fresnel Equations" (i.e. a version of Equation 9.109, but for this polarization case). Explicitly check that your Fresnel Equations reduce to the proper results at normal incidence!
$$\begin{align}
...
\end{align}$$
### 4.C
Replicate Griffiths Figure 9.16 for this polarization case by using the plotting software of your choice. Assume $n_2/n_1=2$. Briefly, discuss what is similar and what is different about this case compared to the case of polarization in the plane of incidence. Is there a "Brewster’s Angle" for this polarization case (i.e. a non-trivial angle where the reflected light vanishes)?
$$\begin{align}
...
\end{align}$$
### 4.D
Replicate Griffiths Figure 9.17 for this polarization case by using the plotting software of your choice, again taking $n_2/n_1=2$. Show that $R+T=1$ for this situation, no matter the angle, and briefly comment on the physics.
$$\begin{align}
...
\end{align}$$
---
## Question 5
The figure to the right shows three layers of dielectric. The index of refraction of air is $n_0=1$, the middle layer has dielectric constant $n_1$, and behind that is a third layer with dielectric constant $n_2$. I claim that one can show that the transmission coefficient for light of angular frequency $\omega$ entering this setup from the left is given by the equation:
$$T=4n_0n_2\left[(n_0+n_2)^2+\dfrac{(n_0^2-n_1^2)(n_2^2-n_1^2)}{n_1^2}\sin^2\left(\dfrac{n_1\omega d}{c}\right)\right]^{-1}$$
where $d$ is the thickness of the middle dielectric layer (deriving this equation is not required— that’s this week’s extra credit).
### 5.A
If you are standing outside of a fish tank and shine a flashlight at the fish ($n_\text{glass}=1.7, n_\text{water}=1.3$), what is the maximum fraction of the light intensity that will reflect from the tank? And what is the minimum?
$$\begin{align}
...
\end{align}$$
### 5.B
Does the fish see you any better or worse than you see it? (Neglect any complications from the differences between fish and human eyes.) Explain.
$$\begin{align}
...
\end{align}$$
### 5.C
Suppose you had a monochromatic light source and wanted to see the fish better. Further, suppose that the thickness $d$ were "tuned" so that the $\sin^2$ factor was equal to $1$. Would you be better off choosing a glass whose $n_1$ is larger, smaller than, or the same as $n_2$? You don’t need to compute the formula for the optimal $n_1$; I just want a qualitative answer.

$$\begin{align}
...
\end{align}$$
---
## Question 6
**Extra Credit:** Prove the equation in Problem 5.
