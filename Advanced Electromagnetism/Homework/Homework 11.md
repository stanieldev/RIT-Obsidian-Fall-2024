**Name:** Stanley Goodwin
**Date:** 11/30/2024
**Collaborators:** None
**Time Taken:** XXX Hours

As always, your work will be graded for clarity of explanation as much as for the “correctness” of your final answer. And as always, please include the names of those you collaborated with, as well as the total number of hours spent on this assignment.

---
## Question 1
In this problem, we’ll practice with the vector potential $\vec{A}$ by using it to calculate something we already know: The $\vec{B}$-field of a long straight wire carrying a steady current $I$. But, if we try to compute the vector potential of an *infinitely* long straight wire, we run into a problem: The integral diverges, much the same way our integral for $V$ fails when the charge extends out to infinity). Fortunately, there’s a nice trick for dodging the infinity in such cases:
### 1.A
Compute the vector potential $\vec{A}(s)$ at a distance $s$ from the axis of a long (but finite) straight wire, with limits of integration $-L$ to $L$ (where $L\gg s$) instead of $-\infty$ to $\infty$.
$$\begin{align}
...
\end{align}$$
### 1.B
Compute $\vec{B}$ by taking the curl of $\vec{A}$ you found in part a, and then (at the end) taking the limit as $L\rightarrow\infty$. (When computing the curl, be careful about your choice of coordinates. Should you be using the Cartesian form, the cylindrical form, or the spherical form?).
$$\begin{align}
...
\end{align}$$
---
## Question 2
At the start of Chapter 10, Griffiths walks us through the reasoning behind Equations
10.2 and 10.3, which are the key formulas relating $\vec{E}$ and $\vec{B}$ to $V$ and $\vec{A}$.
### 2.A
Substitute these relations into Maxwell’s equations and show that the general equations for the potentials $V(\vec{r},t)$ and $\vec{A}(\vec{r},t)$ (without using any particular gauge condition) are:
$$\begin{align}
\vec\nabla^2V+\dfrac{\partial}{\partial t}\left(\vec\nabla\cdot\vec{A}\right)&=-\dfrac{\rho}{\epsilon_0}\\
\vec\nabla^2\vec{A}-\dfrac{1}{c^2}\dfrac{\partial^2}{\partial t^2}\vec{A}-\vec\nabla\left(\vec\nabla\cdot\vec{A}+\dfrac{1}{c^2}\dfrac{\partial}{\partial t}V\right)&=-\mu_0\vec{J}
\end{align}$$
**Note:** We did go through this in class, as does Griffiths. The idea here is for you to do it yourself, explain your work, and convince yourself (and me). I strongly recommend you close the book (though you’ll probably want to keep the sheet of vector calculus identities handy) and derive it on your own as much as you can.
$$\begin{align}
...
\end{align}$$
### 2.B
The equations in a particular gauge can be obtained from these general equations by substituting in the gauge condition. Derive the differential equations for $V$ and $\vec{A}$ in the Coulomb $\left(\text{i.e. }\vec\nabla\cdot\vec{A}=0\right)$ and Lorenz $\left(\text{i.e. }\vec\nabla\cdot\vec{A}=-\dfrac{1}{c^2}\dfrac{\partial V}{\partial t}\right)$ gauges.
$$\begin{align}
...
\end{align}$$
### 2.C
Consider a point charge at rest at the origin. As far back as UP2, you learned that $V(\vec{r},t)=\dfrac{q}{4\pi\epsilon_0 r}$, while in 411, the lack of current in this system would seem to suggest that $\vec{A}(\vec{r},t)=0$. Explicitly check to see if we are in the Coulomb gauge, the Lorentz gauge, or perhaps, both, or maybe neither.
$$\begin{align}
...
\end{align}$$
### 2.D
Now, introduce a gauge transformation $\vec{A}_\text{new}=\vec{A}+\vec\nabla\lambda$, $V_\text{new}=V-\partial_t\lambda$, using the
particular choice $\lambda(\vec{r},t)=\dfrac{qt}{4\pi\epsilon_0 r}$. Find the new $V$ and $\vec{A}$. Briefly discuss your results: are the potentials “static” or time dependent? Does this represent the same physical situation, or is something different here? Are we in the Coulomb gauge, or the Lorentz gauge now? (Do we have to be in one of those?) What has changed, what is the same?
$$\begin{align}
...
\end{align}$$
### 2.E
Look at Griffiths Example 10.1. Explicitly check to see if he is in the Coulomb gauge, the Lorentz gauge, or perhaps, both, or maybe neither.
$$\begin{align}
...
\end{align}$$
---
## Question 3
Say the potentials throughout space and time are $V(\vec{r},t)=0$ and $\vec{A}(\vec{r},t)=A_0\sin\left(k(z-ct)\right)\hat{x}$, where $A_0$ and $k$ are given constants.
### 3.A


### 3.B

### 3.C

### 3.D


