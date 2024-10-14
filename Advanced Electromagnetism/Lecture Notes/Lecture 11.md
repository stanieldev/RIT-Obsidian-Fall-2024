**Name:** Stanley Goodwin
**Date:** 10/1/2024

---
### Maxwell's Equations
$$\begin{align}
\nabla\cdot \vec{E}&=\dfrac{\rho}{\epsilon_0} & \oint\vec{E}\cdot d\vec{A} &= \dfrac{q_\text{enc}}{\epsilon_0} & \text{(Gauss' Law)}\\
\nabla\cdot \vec{B}&=0 & \oint\vec{B}\cdot d\vec{A} &= 0 & \text{(No Monopoles)}\\
\nabla\times \vec{E}&=-\dfrac{\partial \vec{B}}{\partial t} & \oint\vec{E}\cdot d\vec{l}&=-\dfrac{d}{dt}\int\vec{B}\cdot d\vec{A} & \text{(Faraday's Law)}\\
\nabla\times \vec{B}&=\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial \vec{E}}{\partial t} & \oint\vec{B}\cdot d\vec{l} &= \mu_0I + \epsilon_0\mu_0\dfrac{d}{dt}\int\vec{E}\cdot d\vec{A} & \text{(Ampere's Law)}
\end{align}$$
### Consequences of Maxwell's Equations
#### Electric Continuity Equation
$$\begin{align}
\nabla\cdot\left(\nabla\times\vec{B}\right)&=\nabla\cdot\left(\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial \vec{E}}{\partial t}\right)\\
0&=\mu_0\nabla\cdot\vec{J}+\epsilon_0\mu_0\dfrac{\partial\left(\nabla\cdot\vec{E}\right)}{\partial t}\\
0&=\nabla\cdot\vec{J}+\dfrac{\partial\rho}{\partial t}\\
\end{align}$$
#### Magnetic Continuity Equation
$$\begin{align}
\nabla\cdot\left(\nabla\times\vec{E}\right)&=\nabla\cdot\left(-\dfrac{d\vec{B}}{dt}\right)\\
0&=-\dfrac{d\left(\nabla\cdot\vec{B}\right)}{dt}\\
0&=0
\end{align}$$
#### Magnetic Field Wave Equation
$$\begin{align}
\nabla\times\left(\nabla\times\vec{B}\right)&=\nabla\left(\nabla\cdot\vec{B}\right)-\nabla^2\vec{B}\\
\nabla\times\left(\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial \vec{E}}{\partial t}\right)&=\nabla\left(0\right)-\nabla^2\vec{B}\\
\mu_0\left(\nabla\times\vec{J}\right)+\epsilon_0\mu_0\dfrac{\partial\left(\nabla\times\vec{E}\right)}{\partial t}&=-\nabla^2\vec{B}\\
\mu_0\left(\nabla\times\vec{J}\right)-\epsilon_0\mu_0\dfrac{\partial^2 \vec{B}}{\partial t^2}&=-\nabla^2\vec{B}\\
\Aboxed{\dfrac{1}{c^2}\dfrac{\partial^2 \vec{B}}{\partial t^2}-\nabla^2\vec{B}&=0} \ \ \ \text{(Free Space Solution)}\\
\Aboxed{\dfrac{1}{c^2}\dfrac{\partial^2 \vec{B}}{\partial t^2}-\nabla^2\vec{B}&=\mu_0\left(\nabla\times\vec{J}\right)} \ \ \ \text{(Full Solution)}
\end{align}$$
#### Electric Field Wave Equation
$$\begin{align}
\nabla\times\left(\nabla\times\vec{E}\right)&=\nabla\left(\nabla\cdot\vec{E}\right)-\nabla^2\vec{E}\\
\nabla\times\left(-\dfrac{\partial \vec{B}}{\partial t}\right)&=\nabla\left(\dfrac{\rho}{\epsilon_0}\right)-\nabla^2\vec{E}\\
-\dfrac{\partial\left(\nabla\times\vec{B}\right)}{\partial t}&=\dfrac{1}{\epsilon_0}\nabla\rho-\nabla^2\vec{E}\\
-\mu_0\dfrac{\partial\vec{J}}{\partial t}-\epsilon_0\mu_0\dfrac{\partial^2\vec{E}}{\partial t^2}&=\dfrac{1}{\epsilon_0}\nabla\rho-\nabla^2\vec{E}\\
\Aboxed{\dfrac{1}{c^2}\dfrac{\partial^2\vec{E}}{\partial t^2}-\nabla^2\vec{E}&=0} \ \ \ \text{(Free Space Solution)}\\
\Aboxed{\dfrac{1}{c^2}\dfrac{\partial^2\vec{E}}{\partial t^2}-\nabla^2\vec{E}&=-\dfrac{1}{c\epsilon_0}\left(\dfrac{1}{c}\dfrac{\partial\vec{J}}{\partial t}+c\nabla\rho\right)} \ \ \ \text{(Full Solution)}
\end{align}$$

### Polarization
For electric fields, we can write the following expression:
$$\begin{align}
&&\rho_\text{free}+\rho_\text{bound}&=\rho\\
&&\rho_\text{free}-\vec\nabla\cdot\vec{P}&=\epsilon_0\vec\nabla\cdot\vec{E}\\
&&\rho_\text{free}&=\epsilon_0\vec\nabla\cdot\vec{E}+\vec\nabla\cdot\vec{P}\\
&&\rho_\text{free}&=\vec\nabla\cdot\left(\epsilon_0\vec{E}+\vec{P}\right)\\
&&\vec\nabla\cdot\vec{D}&=\rho_\text{free}\
\end{align}$$
$$\begin{align}
&&J_\text{free}+J_\text{bound}&=J\\
&&J_\text{free}+\vec\nabla\times\vec{M}&=\epsilon_0\vec\nabla\cdot\vec{E}\\
&&\rho_\text{free}&=\epsilon_0\vec\nabla\cdot\vec{E}+\vec\nabla\cdot\vec{P}\\
&&\rho_\text{free}&=\vec\nabla\cdot\left(\epsilon_0\vec{E}+\vec{P}\right)\\
&&\vec\nabla\cdot\vec{D}&=\rho_\text{free}\
\end{align}$$

$$\vec{D}\equiv\epsilon_0\vec{E}+\vec{P}$$
$$\vec{J}_\text{polar}\equiv\dfrac{\partial \vec{P}}{\partial t}$$
$$\vec\nabla\times\vec{H}\equiv J_\text{free}+\dfrac{\partial \vec{D}}{\partial t}$$
