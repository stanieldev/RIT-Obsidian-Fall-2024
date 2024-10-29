## General Tricks
### 2nd Order Linear ODEs
$$\begin{align}
ay''+by'+cy&=0 &\implies&& y(x)&=Ae^{rx}+Be^{-rx}, r=\dfrac{-b}{2a}\pm\sqrt{\left(\dfrac{b}{2a}\right)^2-\dfrac{c}{a}}\\
\end{align}$$
### Classifying PDEs
$$\begin{align}
0&=au_{xx}+bu_{xy}+cu_{yy}\\
\text{ID}&=\begin{cases}
b^2-4ac<0, & \text{Elliptic}\\
b^2-4ac=0, & \text{Parabolic}\\
b^2-4ac>0, & \text{Hyperbolic}\\
\end{cases}
\end{align}$$
### Fourier Series
$$\begin{align}
c_{n}&=\dfrac{2}{L}\int_0^Lf(x,0)\cdot\sin\left(\dfrac{n\pi}{L}x\right)\ dx\\
c_{nm}&=\dfrac{2}{L}\dfrac{2}{H}\int_0^L\int_0^Hf(x,y,0)\cdot\sin\left(\dfrac{n\pi}{L}x\right)\cdot\sin\left(\dfrac{m\pi}{L}y\right)\ dy\ dx\\
\end{align}$$

## Heat Equation
### 1D | Homogenous
#### Dirichlet Conditions
$$\begin{align}
k\cdot\dfrac{\partial^2u}{\partial x^2}&=\dfrac{\partial u}{\partial t}\\
u(0,t)=0,&\ u(L,t)=0
\end{align}$$
$$\begin{align}
u(x,t)&=\sum_{n=1}^\infty c_n\sin\left(\tfrac{n\pi}{L}x\right)e^{-\left(\tfrac{n\pi}{L}\right)^2kt}\\
c_n&=\dfrac{2}{L}\int_0^Lu(x,0)\cdot\sin\left(\tfrac{n\pi}{L}x\right)\ dx
\end{align}$$
#### Neumann Conditions (1)
$$\begin{align}
k\cdot\dfrac{\partial^2u}{\partial x^2}&=\dfrac{\partial u}{\partial t}\\
u(0,t)=0,&\ u'(L,t)=0
\end{align}$$
$$\begin{align}
X''/X=-\lambda, T''=-k\lambda T\\
X(x)&=A\sin(\sqrt{\lambda}x)+B\cos(\sqrt{\lambda}x)\\
X'(x)&=A\sqrt{\lambda}\cos(\sqrt{\lambda}x)-B\sqrt{\lambda}\sin(\sqrt{\lambda}x)\\
B=0\\
X'(L)=A\sqrt{\lambda}\cos(\sqrt{\lambda}L)-B\sqrt{\lambda}\sin(\sqrt{\lambda}L)\\
\end{align}$$
#### Neumann Conditions (2)
$$\begin{align}
k\cdot\dfrac{\partial^2u}{\partial x^2}&=\dfrac{\partial u}{\partial t}\\
u'(0,t)=0,&\ u(L,t)=0
\end{align}$$
#### Robin Conditions
$$\begin{align}
k\cdot\dfrac{\partial^2u}{\partial x^2}&=\dfrac{\partial u}{\partial t}\\
u'(0,t)=0,&\ u'(L,t)=0
\end{align}$$
### 1D | Non-Homogenous
#### Dirichlet Conditions
#### Neumann Conditions
#### Robin Conditions
### 2D | Homogenous
#### Dirichlet Conditions
#### Neumann Conditions
#### Robin Conditions
## Wave Equation
### 1D | Homogenous
#### Dirichlet Conditions
#### Neumann Conditions
#### Robin Conditions
### 1D | Non-Homogenous
#### Dirichlet Conditions
#### Neumann Conditions
#### Robin Conditions
### 2D | Homogenous
#### Dirichlet Conditions
#### Neumann Conditions
#### Robin Conditions

## Telegraph Equation 
### 1D | Homogenous
#### Dirichlet Conditions
#### Neumann Conditions
#### Robin Conditions
### 1D | Non-Homogenous
#### Dirichlet Conditions
#### Neumann Conditions
#### Robin Conditions
### 2D | Homogenous
#### Dirichlet Conditions
#### Neumann Conditions
#### Robin Conditions

## ELSE






### Heat Equation 1D (Non-Homogenous)
$$\begin{align}
k\dfrac{\partial^2u}{\partial x^2}+h(x)&=\dfrac{\partial u}{\partial t}\\
u(0,t)=a,\ u(&L,t)=b
\end{align}$$
$$\begin{align}
u(x,t)&=V(x)+\sum_{n=1}^\infty c_n\sin\left(\tfrac{n\pi}{L}x\right)e^{-\left(\tfrac{n\pi}{L}\right)^2kt}\\
V(x)&=-\dfrac{1}{k}\iint h(x)\ dx^2\\
c_n&=\dfrac{2}{L}\int_0^L\left(u(x,0)-V(x)\right)\cdot\sin\left(\tfrac{n\pi}{L}x\right)\ dx
\end{align}$$
### Heat Equation N-D (Homogenous Rectanguloid)
$$\begin{align}
k\cdot\vec\nabla^2u&=\dfrac{\partial u}{\partial t}\\
\text{Boundary}&: 0\text{ Everywhere}
\end{align}$$
$$\begin{align}
u(\vec{x},t)&=\sum_{n_1=1}^\infty\sum_{n_1=1}^\infty\dots\sum_{n_N=1}^\infty c_{n_1n_2\dots n_N}\left(\prod_{\alpha=1}^{N}\sin\left(\tfrac{n_\alpha\pi}{L_\alpha}x_\alpha\right)\right)e^{-k\pi^2\left(\sum_{\beta=1}^N\tfrac{n_\beta^2}{L_\beta^2}\right)t}\\
\\
c_{n_1n_2\dots n_N}&=\int_0^{L_N}\int_0^{L_{N-1}}\dots \int_0^{L_1}u(\vec{x},0)\cdot\prod_{\alpha=1}^{N}\dfrac{2}{L_\alpha}\sin\left(\tfrac{n_\alpha\pi}{L_\alpha}x_\alpha\right)\ dx_\alpha
\end{align}$$
### Wave Equation 1D (Homogenous)
$$\begin{align}
c^2\dfrac{\partial^2\psi}{\partial x^2}&=\dfrac{\partial^2\psi}{\partial t^2}\\
\psi(x,t)&=Ae^{i(kx-\omega t)}+Be^{-i(kx+\omega t)}\\
\end{align}$$
### Wave Equation N-D (Homogenous)
$$\begin{align}
c^2\vec\nabla^2\psi&=\dfrac{\partial^2\psi}{\partial t^2}\\
\psi(\vec{x},t)&=Ae^{i\left(\vec{k}\cdot\vec{x}-\omega t\right)}+Be^{-i\left(\vec{k}\cdot\vec{x}+\omega t\right)}\\
\end{align}$$


