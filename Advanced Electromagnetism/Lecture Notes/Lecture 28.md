**Name:** Stanley Goodwin
**Date:** 12/5/2024

---
### Objective
 - Write down the electromagnetic tensor that contains our electric and magnetic fields.
 - Discuss how $\vec{E}$ and $\vec{B}$ transform under Lorentz transformations.
 - Write Maxwell's equations in terms of that electromagnetic tensor.
### 4-Vectors
$$\begin{align}
X^\mu=\left[\begin{array}{c}ct\\x\\y\\z\end{array}\right]
\end{align}$$
If we boost by speed $v$ along the $+x$-axis, our 4-position undergoes a Lorentz transformation.
$$\begin{align}
\left[\begin{array}{c}ct'\\x'\\y'\\z'\end{array}\right]&=\left[\begin{array}{c}\gamma&-\beta\gamma&0&0\\-\beta\gamma&\gamma&0&0\\0&0&1&0\\0&0&0&1\end{array}\right]\left[\begin{array}{c}ct\\x\\y\\z\end{array}\right]\\
\left(X'\right)^\mu&=\Lambda_\nu^\mu X^\nu
\end{align}$$
Any column $A^\mu$ that transforms as $\left(A'\right)^\mu=\Lambda_\nu^\mu A^\nu$ is a 4-vector.
#### 4-Velocity
$$\begin{align}
U^\mu&\equiv\dfrac{dX^\mu}{d\tau}
\end{align}$$
Where $\tau$ is proper time, measured by the body's rest frame.
Vector $U$ is the 4-velocity. Note that $d/dt$ is not a 4-vector, since it is frame-dependent.
Components of $U^\mu$:
$$\begin{align}
U^0&\equiv c\dfrac{dt}{d\tau}=c\gamma\\
U^{1,2,3}&\equiv\dfrac{dx_{1,2,3}}{d\tau}=\gamma\vec{v}\\
\end{align}$$
For any 4-vector, the square (norm) is invariant.
$$\begin{align}
U_\mu U^\mu&=\dfrac{-c^2+v^2}{1-v^2/c^2}=-c^2\dfrac{1-v^2/c^2}{1-v^2/c^2}=-c^2
\end{align}$$
#### 4-Momentum
$$\begin{align}
P^\mu=\left[\begin{array}{c}E/c\\p_x\\p_y\\p_z\end{array}\right]=m\dfrac{dX^\mu}{d\tau}=mU^\mu
\end{align}$$
#### 4-Force (Minkowski Force)
$$\begin{align}
K^\mu&=\dfrac{dp^\mu}{d\tau}=\dfrac{dp^\mu}{dt}\dfrac{dt}{d\tau}\\
\vec{K}&=\dfrac{d\vec{p}}{d\tau}=\dfrac{d\vec{p}}{dt}\dfrac{dt}{d\tau}=\gamma\vec{F}\\
K^0&=\dfrac{dE}{d\tau}=\vec{F}\cdot\vec{v}/c\\
\end{align}$$
### Electromagnetic Fields in Special Relativity
$$\begin{align}
K^\mu&=\dfrac{dp^\mu}{d\tau}=\left[\begin{array}{c}\gamma\vec{F}\cdot\vec{v}/c\\\gamma\vec{F}\end{array}\right]\\
\vec{F}&=q(\vec{E}+\vec{v}\times\vec{B})
\end{align}$$
Force $K^\mu$ is a 4-vector and know how it transforms under a boost.
We can use this to show how $\vec{E}$ and $\vec{B}$ transform as well.
$$\begin{align}
K^\mu&=\dfrac{dp^\mu}{d\tau}=\left[\begin{array}{c}\gamma\vec{F}\cdot\vec{v}/c\\\gamma\vec{F}\end{array}\right]\\
\Aboxed{K^\mu&=qU_\nu F^{\mu\nu}}
\end{align}$$
This is the Lorentz force law if:
$$\begin{align}
F^{\mu\nu}&=\left[\begin{array}{}0&E_x/c&E_y/c&E_z/c\\-E_x/c&0&B_z&-B_y\\-E_y/c&-B_z&0&B_x\\-E_z/c&B_y&-B_x&0\end{array}\right]
\end{align}$$
Electromagnetic field tensor $F^{\mu\nu}$ is a rank-2 tensor object that transforms as:
$$\bar{F}^{\mu\nu}=\Lambda_\alpha^\mu F^{\alpha\beta}\Lambda_\beta^\nu$$
It's not as simple as a Lorentz transformation, but not much more complicated:
$$\begin{align}
K^0&=qU_\nu F^{0\nu}
\end{align}$$

Explicitly, we can see that:
$$\begin{align}
\left[\begin{array}{}0&E_x'/c&E_y'/c&E_z'/c\\-E_x'/c&0&B_z'&-B_y'\\-E_y'/c&-B_z'&0&B_x'\\-E_z'/c&B_y'&-B_x'&0\end{array}\right]&=\left[\begin{array}{c}\gamma&-\beta\gamma&0&0\\-\beta\gamma&\gamma&0&0\\0&0&1&0\\0&0&0&1\end{array}\right]\left[\begin{array}{}0&E_x/c&E_y/c&E_z/c\\-E_x/c&0&B_z&-B_y\\-E_y/c&-B_z&0&B_x\\-E_z/c&B_y&-B_x&0\end{array}\right]\left[\begin{array}{c}\gamma&-\beta\gamma&0&0\\-\beta\gamma&\gamma&0&0\\0&0&1&0\\0&0&0&1\end{array}\right]
\end{align}$$
**Resulting in:**
$$\begin{align}
\vec{E}'=\left[\begin{array}{}E_x\\\gamma\left(E_y-vB_z\right)\\\gamma\left(E_z+vB_y\right)\end{array}\right]\\
\vec{B}'=\left[\begin{array}{}B_x\\\gamma\left(B_y+vE_z/c^2\right)\\\gamma\left(B_z-vE_y/c^2\right)\end{array}\right]
\end{align}$$
Random Idea: Eigen-Fields that uniquely define a basis for Electromagnetism.


### Maxwell's Equations in Tensor Notation
Where $J^\mu=(c\rho,\vec{J})$ is the 4-current and $F^{\mu\nu}$ is the electromagnetic field tensor.
One more tensor to look at is $G^{\mu\nu}$:
$$\begin{align}
G^{\mu\nu}&=\left[\begin{array}{}0&B_x&B_y&B_z\\-B_x&0&-E_z/c&E_y/c\\-B_y&E_z/c&0&-E_x/c\\-B_z&-E_y/c&E_x/c&0\end{array}\right]
\end{align}$$
With these, we can rewrite electromagnetism as the following equations:
$$\begin{align}
\partial_\nu F^{\mu\nu}&=\mu_0J^\mu&
\text{(Divergence Equations)}\\
\partial_\nu G^{\mu\nu}&=0&
\text{(Curl Equations)}\\
\partial_\mu J^\mu&=0&
\text{(Continuity)}\\
\end{align}$$
With the Lorentz force law $K^\mu=qU_\nu F^{\mu\nu}$ contains all of Electromagnetism and, necessarily, respecting Lorentz transformations and special relativity.