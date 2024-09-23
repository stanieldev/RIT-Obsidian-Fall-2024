**Name:** Stanley Goodwin
**Date:** 9/04/2024
**Collaborators:** None
**Time Taken:** N/A


## Question 1
Consider a solid, neutral, conducting metal sphere (radius $a$), centered at the origin, as shown.
It has a small spherical cavity inside it (an off-center hole) with radius $b$, centered on the $+x$-axis, centered at the point $(b, 0, 0)$. A positive point charge $+Q$ sits at the exact center of the cavity.

#### Part A
Describe how charge is distributed on the metallic shell. Be specific: where does the charge reside and how is it distributed? Explicitly calculate any charge densities that are nonzero and discuss what kind of symmetry they have (if any).

The inner spherical cavity has a uniform surface charge density *only* because the $+Q$ charge is centered on the inner cavity. $$\sigma_\text{inside} = -\dfrac{Q}{4\pi b^2}$$
The outer surface will also have a uniform surface charge density. This is because the inner surface of the conductor screens the position of the $+Q$, but not the charge itself (because of charge conservation). $$\sigma_\text{outside} = \dfrac{Q}{4\pi a^2}$$
#### Part B
Determine the electric field $\vec E(x)$ everywhere along the x-axis.
$$\vec{E}(x)=\begin{cases} 
-\dfrac{kQ}{x^2}\hat{x} & x\leq -a \\
0 & -a<x<0 \\
-\dfrac{kQ}{(x-b)^2}\hat{x} & 0\leq x<b \\
\dfrac{kQ}{(x-b)^2}\hat{x} & b<x\leq 2b \\
0 & 2b<x<a \\
\dfrac{kQ}{x^2}\hat{x} & x\geq a
\end{cases}
$$
For $x\le-a$ and $x\ge a$, the sphere acts like a point charge.
For $-a<x\le0$ and $2b\le x<a$, there is no E-field because the sphere is a conductor.
For $0<x<2b$, the E-field looks like a point charge centered at $x=b$.

Graphed on Desmos: https://www.desmos.com/calculator/zxm5strdxm 
Note: I had to scale the internal $\vec{E}$ by 1/1000 so that the shape could be easier seen.
![[HW2_Q1.png]]

#### Part C
Determine the electric potential $V(x)$ everywhere along the x-axis.
$$\vec{E}(x)=\begin{cases} 
\dfrac{kQ}{|x|} & x\leq -a \\
\dfrac{kQ}{a} & -a<x<0 \\
\dfrac{kQ}{|x-b|}-\dfrac{kQ}{b}+\dfrac{kQ}{a} & 0\leq x\leq2b \\
\dfrac{kQ}{a} & 2b<x<a \\
\dfrac{kQ}{|x|} & x\geq a
\end{cases}
$$
For $x\le-a$ and $x\ge a$, the sphere acts like a point charge voltage.
For $-a<x\le0$ and $2b\le x<a$, there is a constant voltage because the sphere is a conductor.
For $0<x<2b$, the voltage looks like a point charge centered at $x=b$.

Desmos: https://www.desmos.com/calculator/utfamoncw9
![[HW2_Q1C.png]]


## Question 2
Suppose an electric field in a region of space is given by
$$\vec{E}=\dfrac{B_0}{2\tau}\left(-y\hat{x}+x\hat{y}\right)$$
#### Part A
The units of $B_0$ are $\dfrac{\mathrm{N}\cdot\mathrm{s}}{\mathrm{C}\cdot\mathrm{m}}=\dfrac{\mathrm{kg}}{\mathrm{C}\cdot\mathrm{s}}$.
