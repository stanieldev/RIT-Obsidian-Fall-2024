**Name:** Stanley Goodwin
**Date:** 11/03/2024
**Collaborators:** Hasan, Chris
**Time Taken:** 7 Hours

---
## Question 1
In class (and/or Griffiths section 9.3.2) we worked out the case of normally incident light, and claimed that reflected and transmitted waves have the same *polarization* as the incident wave (on the $x$-axis). Prove this must be true by starting with fully general reflected and transmitted polarization directions $\hat{n}_R=n_{Rx}\hat{x}+n_{Ry}\hat{y}$ and $\hat{n}_T=n_{Tx}\hat{x}+n_{Ty}\hat{y}$ and showing that our boundary conditions require that $n_{Ry}=n_{Ty}=0$.
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel &
\epsilon_1\vec{E}_1^\perp&=\epsilon_2\vec{E}_2^\perp\\
\vec{B}_1^\perp&=\vec{B}_2^\perp &
\dfrac{1}{\mu_1}\vec{B}_1^\parallel&=\dfrac{1}{\mu_2}\vec{B}_2^\parallel\\
\end{align}$$
We only have to consider the electric field parallel since $\mu_1\approx\mu_2\approx\mu_0$.
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel\\
\tilde{E}_I\hat{x}+\tilde{E}_R(n_{Rx}\hat{x}+n_{Ry}\hat{y})&=\tilde{E}_T(n_{Tx}\hat{x}+n_{Ty}\hat{y})\\\\
\tilde{E}_I\hat{x}+\tilde{E}_Rn_{Rx}\hat{x}&=\tilde{E}_Tn_{Tx}\hat{x}\\
\tilde{E}_Rn_{Ry}&=\tilde{E}_Tn_{Ty}\\
\end{align}$$
Since the $y$-component has no relation to the incident wave, it wouldn't make sense for the wave to spontaneously change polarization, and so:
$$n_{Ry}=n_{Ty}=0$$
It also violates the B-field being perpendicular at every point by a similar argument above, and so they must not change polarization on reflection nor transmission.

---
## Question 2
Electromagnetic Waves in Matter.
### 2.A
Starting with Maxwell’s Equations in Matter (in terms of the $\vec{D}$ and $\vec{H}$ fields), show that, for a linear, homogenous dielectric (i.e. $\vec{D}=\epsilon\vec{E}$ and $\vec{B}=\mu\vec{H}$, where $\epsilon$ and $\mu$ are uniform, constant scalars) with no free charges or currents ($\rho_\text{free}=0$ and $\vec{J}_\text{free}=0$), both the $\vec{E}$ and the $\vec{B}$ fields obey a wave equation with wave speed given by $v=\dfrac{1}{\sqrt{\mu\epsilon}}$.
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
\Aboxed{\mu\epsilon\dfrac{\partial^2\vec{D}}{\partial t^2}&=\vec\nabla^2\vec{D}}\\\\
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
Equation 1:
$$\begin{align}
\oint\vec{D}\cdot d\vec{A}&=0\\
\vec{D}_\text{above}\cdot A\hat{n}-\vec{D}_\text{below}\cdot A\hat{n}&=0\\
D^\perp_\text{above}&=D^\perp_\text{below}\\
\Aboxed{\epsilon_\text{above}E^\perp_\text{above}&=\epsilon_\text{below}E^\perp_\text{below}}
\end{align}$$
This shows that the perpendicular component of the $D$ field is continuous over an interface.

Equation 2:
$$\begin{align}
\oint\vec{H}\cdot d\vec{A}&=0\\
\vec{H}_\text{above}\cdot A\hat{n}-\vec{H}_\text{below}\cdot A\hat{n}&=0\\
\Aboxed{H^\perp_\text{above}&=H^\perp_\text{above}}\\
\Aboxed{B^\perp_\text{above}&=B^\perp_\text{above}}
\end{align}$$
This shows that the perpendicular component of the $H$ field is continuous over an interface.

Equation 3:
$$\begin{align}
\oint\vec{D}\cdot d\vec{l}&=-\mu\epsilon\dfrac{d}{dt}\int\vec{H}\cdot d\vec{A}\\
\vec{D}_\text{above}\cdot\vec{l}-\vec{D}_\text{below}\cdot\vec{l}&=0\\
\Aboxed{D^\parallel_\text{above}&=D^\parallel_\text{below}}\\
\Aboxed{E^\parallel_\text{above}&=E^\parallel_\text{below}}
\end{align}$$
This shows that the tangential component of the $D$ field is continuous over an interface.

Equation 4:
$$\begin{align}
\oint\vec{H}\cdot d\vec{l}&=\dfrac{d}{dt}\int\vec{D}\cdot d\vec{A}\\
\vec{H}_\text{above}\cdot\vec{l}-\vec{H}_\text{below}\cdot\vec{l}&=0\\
H^\parallel_\text{above}&=H^\parallel_\text{below}\\
\Aboxed{\dfrac{B^\parallel_\text{above}}{\mu_\text{above}}&=\dfrac{B^\parallel_\text{below}}{\mu_\text{below}}}
\end{align}$$
This shows that the tangential component of the $D$ field is continuous over an interface.

I omitted the sketches since they're just boxes that loop around the interface, where the width of the box approaches 0 so that the time-component vanishes.

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
We only really need the parallel components, since the perpendicular is trivial (normal).
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel\\
\Aboxed{\tilde{E}_I+\tilde{E}_R&=\tilde{E}_T}\\\\
\dfrac{1}{\mu_1}\vec{B}_1^\parallel&=\dfrac{1}{\mu_2}\vec{B}_2^\parallel\\
\dfrac{1}{\mu_1}\tilde{B}_I-\dfrac{1}{\mu_1}\tilde{B}_R&=\dfrac{1}{\mu_2}\tilde{B}_T\\
\dfrac{1}{\mu_1c_1}\left(\tilde{E}_I-\tilde{E}_R\right)&=\dfrac{1}{\mu_2c_2}\tilde{E}_T\\
\Aboxed{\tilde{E}_I-\tilde{E}_R&=\dfrac{\mu_1c_1}{\mu_2c_2}\tilde{E}_T}
\end{align}$$
From there, we can find that:
$$\begin{align}
2\tilde{E}_I+0\tilde{E}_R&=\tilde{E}_T+\dfrac{\mu_1c_1}{\mu_2c_2}\tilde{E}_T\\
2\tilde{E}_I&=\left(1+\dfrac{\mu_1c_1}{\mu_2c_2}\right)\tilde{E}_T\\
\Aboxed{\tilde{E}_T&=\left(\dfrac{2}{1+\tfrac{\mu_1c_1}{\mu_2c_2}}\right)\tilde{E}_I}\\\\
0\tilde{E}_I+2\tilde{E}_R&=\tilde{E}_T-\dfrac{\mu_1c_1}{\mu_2c_2}\tilde{E}_T\\
2\tilde{E}_R&=\left(1-\dfrac{\mu_1c_1}{\mu_2c_2}\right)\tilde{E}_T\\
2\tilde{E}_R&=\left(1-\dfrac{\mu_1c_1}{\mu_2c_2}\right)\left(\dfrac{2}{1+\tfrac{\mu_1c_1}{\mu_2c_2}}\right)\tilde{E}_I\\
\Aboxed{\tilde{E}_R&=\left(\dfrac{1-\tfrac{\mu_1c_1}{\mu_2c_2}}{1+\tfrac{\mu_1c_1}{\mu_2c_2}}\right)\tilde{E}_I}\\
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
$$\begin{align}
\beta&=\dfrac{\mu_1c_1}{\mu_2c_2}\\
&=\dfrac{\epsilon_2\epsilon_1}{\epsilon_1\epsilon_2}\dfrac{\mu_1c_1}{\mu_2c_2}\\
&=\dfrac{\epsilon_2}{\epsilon_1}\dfrac{\epsilon_1\mu_1}{\epsilon_2\mu_2}\dfrac{c_1}{c_2}\\
&=\dfrac{\epsilon_2}{\epsilon_1}\dfrac{c_2^2}{c_1^2}\dfrac{c_1}{c_2}\\
\Aboxed{\beta&=\dfrac{\epsilon_2c_2}{\epsilon_1c_1}}\\
\end{align}$$
To make sure I did everything correct, let's see if $T+R=1$:
$$\begin{align}
T+R&=\dfrac{4\beta}{(1+\beta)^2}+\dfrac{(1-\beta)^2}{(1+\beta)^2}\\
&=\dfrac{(1-\beta)^2+4\beta}{(1+\beta)^2}\\
&=\dfrac{\beta^2-2\beta+4\beta+1}{(1+\beta)^2}\\
&=\dfrac{(1+\beta)^2}{(1+\beta)^2}\\
\Aboxed{T+R&=1}
\end{align}$$

---
## Question 4
In class (and in Griffiths 9.3.3), we worked out the case of reflection and transmission at any angle. However, we were specifically considering the case in which the incident electric field is polarized in the plane of incidence. You will now repeat that process for the different case where the electric field is polarized perpendicular to the plane of incidence. You may once again assume $\mu_1=\mu_2=\mu_0$.
$$\begin{align}
\vec{E}_I&=\tilde{E}_Ie^{i(k_I\cdot\vec{x}-\omega t)}\hat{y} &
\vec{B}_I&=\dfrac{\tilde{E}_I}{c_1}e^{i(k_I\cdot\vec{x}-\omega t)}\left(\hat{x}\cos\theta_I+\hat{z}\sin\theta_I\right)\\
\vec{E}_R&=\tilde{E}_Re^{i(k_R\cdot\vec{x}-\omega t)}\hat{y} &
\vec{B}_R&=\dfrac{\tilde{E}_R}{c_1}e^{i(k_R\cdot\vec{x}-\omega t)}\left(\hat{x}\cos\theta_R+\hat{z}\sin\theta_R\right)\\
\vec{E}_T&=\tilde{E}_Te^{i(k_T\cdot\vec{x}-\omega t)}\hat{y} &
\vec{B}_T&=\dfrac{\tilde{E}_T}{c_2}e^{i(k_T\cdot\vec{x}-\omega t)}\left(\hat{x}\cos\theta_T+\hat{z}\sin\theta_T\right)\\
\end{align}$$
### 4.A
Make a clear sketch (modeled on Griffiths Figure 9.15) of the geometry and angles for this case, then write out what the four boundary conditions become in this case (i.e. modify Griffiths Equations 9.101 through 9.104 for the new situation.
![[HW9_4A.png]]
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel\\
\vec{B}_1^\perp&=\vec{B}_2^\perp\\
\epsilon_1\vec{E}_1^\perp&=\epsilon_2\vec{E}_2^\perp\\
\dfrac{1}{\mu_1}\vec{B}_1^\parallel&=\dfrac{1}{\mu_2}\vec{B}_2^\parallel\\
\end{align}$$
### 4.B
Find the new "Fresnel Equations" (i.e. a version of Equation 9.109, but for this polarization case). Explicitly check that your Fresnel Equations reduce to the proper results at normal incidence!
$$\begin{align}
\vec{E}_1^\parallel&=\vec{E}_2^\parallel\\
\Aboxed{\tilde{E}_I+\tilde{E}_R&=\tilde{E}_T}\\\\
\dfrac{1}{\mu_1}\vec{B}_1^\parallel&=\dfrac{1}{\mu_2}\vec{B}_2^\parallel\\
\dfrac{1}{\mu_1}\tilde{B}_I\cos\theta_I-\dfrac{1}{\mu_1}\tilde{B}_R\cos\theta_R&=\dfrac{1}{\mu_2}\tilde{B}_T\cos\theta_T\\
\dfrac{\cos\theta_I}{\mu_1c_1}\left(\tilde{E}_I-\tilde{E}_R\right)&=\dfrac{\cos\theta_T}{\mu_2c_2}\tilde{E}_T\\
\Aboxed{\tilde{E}_I-\tilde{E}_R&=\dfrac{\mu_1c_1}{\mu_2c_2}\dfrac{\cos\theta_T}{\cos\theta_I}\tilde{E}_T}
\end{align}$$
Like before, let $\beta=\dfrac{\mu_1c_1}{\mu_2c_2}$ and $\alpha=\dfrac{\cos\theta_T}{\cos\theta_I}$, so:
$$\begin{align}
\tilde{E}_I+\tilde{E}_R&=\tilde{E}_T\\
\tilde{E}_I-\tilde{E}_R&=\alpha\beta\tilde{E}_T
\end{align}$$
Which then can be turned into:
$$\begin{align}
\tilde{E}_T+\alpha\beta\tilde{E}_T&=\tilde{E}_I+\tilde{E}_R+\tilde{E}_I-\tilde{E}_R\\
(1+\alpha\beta)\tilde{E}_T&=2\tilde{E}_I\\
\Aboxed{\tilde{E}_T&=\dfrac{2}{(1+\alpha\beta)}\tilde{E}_I}\\\\
\tilde{E}_T-\alpha\beta\tilde{E}_T&=\tilde{E}_I+\tilde{E}_R-\tilde{E}_I+\tilde{E}_R\\
(1-\alpha\beta)\tilde{E}_T&=2\tilde{E}_R\\
\tilde{E}_R&=\dfrac{(1-\alpha\beta)}{2}\tilde{E}_T\\
\Aboxed{\tilde{E}_R&=\dfrac{(1-\alpha\beta)}{(1+\alpha\beta)}\tilde{E}_I}
\end{align}$$
Checking that this isn't nonsense, at $\theta_I=0$:
$$\begin{align}
\Aboxed{\tilde{E}_T&=\dfrac{2}{1+\beta}\tilde{E}_I}\\
\Aboxed{\tilde{E}_R&=\dfrac{1-\beta}{1+\beta}\tilde{E}_I}
\end{align}$$
Which is exactly what we expected.

### 4.C
Replicate Griffiths Figure 9.16 for this polarization case by using the plotting software of your choice. Assume $n_2/n_1=2$. Briefly, discuss what is similar and what is different about this case compared to the case of polarization in the plane of incidence. Is there a "Brewster’s Angle" for this polarization case (i.e. a non-trivial angle where the reflected light vanishes)?
![[HW9_4C.png]]
https://www.desmos.com/calculator/bkzelp1rax

They do look quite similar to the parallel polarized light, however both curves arc downward, indicating that the reflected light picked up an extra negative sign.

There does exist a Brewster's angle at the following:
$$\begin{align}
\theta_\text{B}&=\cos^{-1}\left(\dfrac{n_2}{n_1}\cos\theta_T\right)\\
\end{align}$$
### 4.D
Replicate Griffiths Figure 9.17 for this polarization case by using the plotting software of your choice, again taking $n_2/n_1=2$. Show that $R+T=1$ for this situation, no matter the angle, and briefly comment on the physics.
![[HW9_4D.png]]
https://www.desmos.com/calculator/hlpkl6cyrq
$$\begin{align}
\Aboxed{T&=\dfrac{4\alpha\beta}{(1+\beta)^2}}\\
\Aboxed{R&=\left(\dfrac{1-\alpha\beta}{1+\alpha\beta}\right)^2}
\end{align}$$
They do look quite similar to the parallel polarized light. Since both components are squared, they appear almost identical to the parallel polarized light.

There does exist a Brewster's angle at the following:
$$\begin{align}
\theta_\text{B}&=\cos^{-1}\left(\dfrac{n_2}{n_1}\cos\theta_T\right)\\
\end{align}$$
---
## Question 5
The figure to the right shows three layers of dielectric. The index of refraction of air is $n_0=1$, the middle layer has dielectric constant $n_1$, and behind that is a third layer with dielectric constant $n_2$. I claim that one can show that the transmission coefficient for light of angular frequency $\omega$ entering this setup from the left is given by the equation:
$$T=4n_0n_2\left[(n_0+n_2)^2+\dfrac{(n_0^2-n_1^2)(n_2^2-n_1^2)}{n_1^2}\sin^2\left(\dfrac{n_1\omega d}{c}\right)\right]^{-1}$$
where $d$ is the thickness of the middle dielectric layer (deriving this equation is not required— that’s this week’s extra credit).
### 5.A
If you are standing outside of a fish tank and shine a flashlight at the fish ($n_\text{glass}=1.7, n_\text{water}=1.3$), what is the maximum fraction of the light intensity that will reflect from the tank? And what is the minimum?
$$\begin{align}
R&=1-4n_0n_2\left[(n_0+n_2)^2+\dfrac{(n_0^2-n_1^2)(n_2^2-n_1^2)}{n_1^2}\sin^2\left(\dfrac{n_1\omega d}{c}\right)\right]^{-1}\\
&=1-4\cdot1.3\left[(1+1.3)^2+\dfrac{(1-1.7^2)(1.3^2-1.7^2)}{1.7^2}\sin^2\left(\dfrac{1.7\omega d}{c}\right)\right]^{-1}\\
\Aboxed{R&=1-\dfrac{5.2}{5.29+0.784775\sin^2\left(\dfrac{1.7\omega d}{c}\right)}}
\end{align}$$
Lets look at 2 values: $\sin^2\theta=0$ and $\sin^2\theta=1$.
$$\begin{align}
R_\text{min}&=0.017=1.7\%\\
R_\text{max}&=0.144=14.4\%\\
\end{align}$$
### 5.B
*Does the fish see you any better or worse than you see it? (Neglect any complications from the differences between fish and human eyes.) Explain.*

Since the transmission coefficient is symmetric under swapping $n_0$ and $n_2$, the fish would see the human as well as the human sees the fish. 

### 5.C
Suppose you had a monochromatic light source and wanted to see the fish better. Further, suppose that the thickness $d$ were "tuned" so that the $\sin^2$ factor was equal to $1$. *Would you be better off choosing a glass whose $n_1$ is larger, smaller than, or the same as $n_2$? You don’t need to compute the formula for the optimal $n_1$; I just want a qualitative answer.*
$$\begin{align}
T&=4n_0n_2\left[(n_0+n_2)^2+\dfrac{(n_0^2-n_1^2)(n_2^2-n_1^2)}{n_1^2}\sin^2\left(\dfrac{n_1\omega d}{c}\right)\right]^{-1}\\
&=4n_0n_2\left[(n_0+n_2)^2+\left(\dfrac{n_0^2}{n_1^2}-1\right)\left(\dfrac{n_2^2}{n_1^2}-1\right)\right]^{-1}\\
\end{align}$$
![[HW9_5C.png]]
After plotting $T(n_1)$ and finding its peak, it is before the index of refraction of water.
This means we should get a glass who's $n_1$ is smaller than $n_\text{water}$.

---
## Question 6
**Extra Credit:** Prove the equation in Problem 5.

Let's start with normally-incident light, assuming that $\mu_0=\mu_1=\mu_2$ (ignoring magnetic interaction):
$$\begin{align}
T_{13}&=T_{12}+R_{12}\cdot T_{23}
\end{align}$$
I tried the algebra and it was... terrible so I left it at this.
