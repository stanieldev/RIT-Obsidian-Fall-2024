**Name:** Stanley Goodwin
**Date:** 8/26/2024

---
## Syllabus Review
 - Chapters 11-13 are being used.

## Review of Ordinary Differential Equations (ODEs)
Homogenous w/ constant coefficients : $ay''+by'+cy=0$
$$\begin{align}
y''-4y=0 &\implies \left(\dfrac{d}{dx}-2\right)\left(\dfrac{d}{dx}+2\right)y=0\\
&\implies \boxed{y=Ae^{2x}+Be^{-2x}}
\end{align}$$
$$\begin{align}
y''-6y'+9y=0 &\implies \left(\dfrac{d}{dx}-3\right)^2y=0\\
&\implies \boxed{y=(A+Bx)e^{3x}}
\end{align}$$
$$\begin{align}
y''+y=0 &\implies \left(\dfrac{d}{dx}-i\right)\left(\dfrac{d}{dx}+i\right)y=0\\
&\implies \boxed{y=Ae^{ix}+Be^{-ix}}
\end{align}$$

### Separatable Equations
Equations that can be separated into independent and dependent variables.
$$\begin{align}
&\dfrac{dy}{dx}=f(x)\cdot g(y)\\
\implies& \dfrac{dy}{g(y)} = f(x)\ dx\\
\implies& \boxed{\int\dfrac{dy}{g(y)} = \int f(x)\ dx}
\end{align}$$
$$\begin{align}
y' &= y\cdot x^2\\
\int\dfrac{dy}{y}&=\int x^2 dx\\
\ln|y|&=\dfrac{x^3}{3}+c\\
\Aboxed{y &= Ae^{\tfrac{x^3}{3}}}
\end{align}$$

## Partial Differential Equations (PDEs)
A PDE is an equation which involves partial derivatives.

Given $u(x,y)$, then $u_x=\dfrac{\partial u}{\partial x}$ and $u_y=\dfrac{\partial u}{\partial y}$.
For the systems we consider in this course, $u_{xy}=u_{yx}$.

$$2\dfrac{\partial u}{\partial x}+3\dfrac{\partial u}{\partial y} = 0$$
$$\dfrac{\partial^2 u}{\partial x^2}+u\dfrac{\partial u}{\partial y} = 1$$
$$\dfrac{\partial^3 u}{\partial x^2 \partial y}+\left(\dfrac{\partial u}{\partial x}\right)^2 = e^x$$

### PDE Equation Orders
Same as ODEs, defined as the highest order derivative.
Can be mixed between differentials.

### PDE Equation Linearity
Same as all forms of linearity.
PDE of Order 1 that generally is:
$$a(x,y)\cdot \dfrac{\partial u}{\partial x}+b(x,y)\cdot \dfrac{\partial u}{\partial y}+c(x,y)\cdot u = d(x,y)$$
