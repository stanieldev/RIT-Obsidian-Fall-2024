**Name:** Stanley Goodwin
**Date:** 9/9/2024

---

Example:
$$\begin{align}
y''+\lambda y&=0 & y(0)&=0 & y(1)&=0
\end{align}$$
$$\begin{align}
y(x)&=Ae^{i\sqrt{\lambda}x}+Be^{-i\sqrt{\lambda}x}\\
y(0)&=A+B\\
y(1)&=A\sin\left(\sqrt{\lambda}x\right)=0\\
\Aboxed{\lambda&=\pm\left(2\pi n\right)^2}\\
\Aboxed{y(x)&=Ae^{2\pi ni\sqrt{\text{sign}(\lambda)}x}+Ae^{-2\pi ni\sqrt{\text{sign}(\lambda)}x}}
\end{align}$$

Example:
$$\begin{align}
y''+\lambda y&=0 & y(0)&=0 & y(\pi)&=0
\end{align}$$
$$\begin{align}
y(x)&=Ae^{i\sqrt{\lambda}x}+Be^{-i\sqrt{\lambda}x}\\
y(0)&=A+B\\
y(1)&=A\sin\left(\pi\sqrt{\lambda}x\right)=0\\
\Aboxed{\lambda&=\pm n^2}\\
\Aboxed{y(x)&=A\sin\left(n\sqrt{-\text{sign}(\lambda)}x\right)}
\end{align}$$


Example:
$$\begin{align}
y''+2y'+\lambda y&=0 & y(0)&=0 & y(\pi)&=0
\end{align}$$
$$\begin{align}
y(x)&=Ae^{-y}e^{(\sqrt{1-\lambda})y}+Be^{-y}e^{-(\sqrt{1-\lambda})y}\\
y(0)&=A+B=0\\
y(\pi)&=Ae^{-\pi}\left(e^{(\sqrt{1-\lambda})\pi}-e^{-(\sqrt{1-\lambda})\pi}\right)\\
y(x)&=\begin{cases}
A\sinh\left(\sqrt{1-\lambda}\cdot x\right) & \lambda=1\\
A\sin\left(\sqrt{1-\lambda}\cdot x\right) & \lambda\gt1, (1-\lambda)^2\in\mathbb{Z}\\
\end{cases}
\end{align}$$
