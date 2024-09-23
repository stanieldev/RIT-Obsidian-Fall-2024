**Name:** Stanley Goodwin
**Date:** 9/17/2024

---
### Sensitivity Analysis
When constructing a model, it's useful to explore how sensitive the outputs of the model are to perturbations in one or more of the assumptions.

### Elevator Problem Analysis
Given the set of parameters here:
$$\begin{align}
T_0:\ &\text{The time the door is open on the ground floor.}\\
T_\text{f}:\ &\text{The time the door is open on non-ground floors.} \\
T_\text{t}:\ &\text{The time the elevator takes to travel between floors.}\\
n:\ &\text{The number of floors of the building above the ground floor.}\\
C:\ &\text{Max Capacity of a singular Elevator.}\\
N:\ &\text{Number of elevators in the building.}
\end{align}$$
Worst Case Period : $T_\text{W} = T_0 + nT_\text{f} + 2nT_\text{t}$
$$\begin{align}
\dfrac{\partial T_\text{W}}{\partial T_0}&= 1& 
\dfrac{\partial T_\text{W}}{\partial T_\text{f}}&= n&
\dfrac{\partial T_\text{W}}{\partial T_\text{t}}&= 2n&
\dfrac{\partial T_\text{W}}{\partial n}&= T_\text{f}+2T_\text{t}
\end{align}$$

### Incorporating Randomness


### Combinatorics
Given the probability $p_i$, representing the probability of a worker going to floor $i$ :
$$p\in\left\{p_i|1\le i\le n, i\in\mathbb{N}\right\} \text{ where } \displaystyle\sum_i p_i = 1$$
We can represent the probability of certain configurations of elevator stops :
$$\begin{align}
p\left(\left\{n_1,n_2,\dots,n_n\right\}\right)&=\left(\begin{array}!C\\n_1\end{array}\right)\left(\begin{array}!C-n_1\\n_2\end{array}\right)\left(\begin{array}!C-n_1-n_2\\n_3\end{array}\right)\dots p_1^{n_1}p_2^{n_2}p_3^{n_3}\dots\\
&=\dfrac{(C)!}{(n_1)!}\dfrac{1}{(n_2)!}\dots\dfrac{1}{(n_{n-1})!}\dfrac{1}{(n_n)!}\dots p_1^{n_1}p_2^{n_2}p_3^{n_3}\dots\\
\Aboxed{p\left(\left\{n_1,n_2,\dots,n_n\right\}\right)&=C!\cdot\prod_{i=1}^n\dfrac{p_i^{n_i}}{n_i!}}
\end{align}$$
We can also represent the time for each configuration.
$$T\left(S\right)= T_0 + |S|T_\text{f} + 2\max(S)\cdot T_\text{t}$$
This means we can calculate the expected value of $T$.
$$\begin{align}
\langle T\rangle&=\sum_{S} T(S)\cdot p(S)\\
&=T_0+T_\text{f}\langle|S|\rangle+2T_\text{t}\langle\max{S}\rangle
\end{align}$$
And the second moment of $T$.
$$\begin{align}
\langle T^2\rangle&=\sum_{S} T(S)^2\cdot p(S)\\
&=\sum_{S} (T_0+T_\text{f}|S|+2T_\text{t}\max{S})^2\cdot p(S)\\
&= T_0^2+T_\text{f}^2\langle|S|^2\rangle+4T_\text{t}^2\langle(\max{S})^2\rangle+2T_0T_\text{f}\langle|S|\rangle+4T_\text{f}T_\text{t}\langle|S|\cdot\max{S}\rangle+4T_0T_\text{t}\langle\max{S}\rangle
\end{align}$$
As well as the variance of $T$.
$$\begin{align}
\sigma_T^2&= T_0^2+T_\text{f}^2\langle|S|^2\rangle+4T_\text{t}^2\langle(\max{S})^2\rangle+2T_0T_\text{f}\langle|S|\rangle+4T_\text{f}T_\text{t}\langle|S|\cdot\max{S}\rangle+4T_0T_\text{t}\langle\max{S}\rangle\\
&-T_0^2-T_\text{f}^2\langle|S|\rangle^2-4T_\text{t}^2\langle\max{S}\rangle^2-2T_0T_\text{f}\langle|S|\rangle-4T_\text{f}T_\text{t}\langle|S|\rangle\langle\max{S}\rangle-4T_0T_\text{t}\langle\max{S}\rangle\\
\Aboxed{\sigma_T^2&=T_\text{f}^2\sigma_{|S|}^2+4T_\text{t}^2\sigma_{\max S}^2+4T_\text{f}T_\text{t}\left(\langle|S|\cdot\max{S}\rangle-\langle|S|\rangle\langle\max{S}\rangle\right)}\\
\end{align}$$


### Summary of Combinatorics
*Singular Elevator Period*
$$\begin{align}
\langle T\rangle&=T_0+T_\text{f}\langle|S|\rangle+2T_\text{t}\langle\max{S}\rangle\\
\langle T^2\rangle&=T_0^2+T_\text{f}^2\langle|S|^2\rangle+4T_\text{t}^2\langle(\max{S})^2\rangle+2T_0T_\text{f}\langle|S|\rangle+4T_\text{f}T_\text{t}\langle|S|\cdot\max{S}\rangle+4T_0T_\text{t}\langle\max{S}\rangle\\
\sigma_T^2&=T_\text{f}^2\sigma_{|S|}^2+4T_\text{t}^2\sigma_{\max S}^2+4T_\text{f}T_\text{t}\left(\langle|S|\cdot\max{S}\rangle-\langle|S|\rangle\langle\max{S}\rangle\right)
\end{align}$$
*Number of Stops*
$$\begin{align}
\langle |S|\rangle&=\sum_{S} |S|\cdot p(S)\\
\langle |S^2|\rangle&=\sum_{S} |S|^2\cdot p(S)\\
\sigma_{|S|}^2&=\langle |S^2|\rangle-\langle |S|\rangle^2
\end{align}$$
*Number of Floors*
$$\begin{align}
\langle \max S\rangle&=\sum_{S} (\max{S})\cdot p(S)\\
\langle (\max{S})^2\rangle&=\sum_{S} (\max{S})^2\cdot p(S)\\
\sigma_{\max{S}}^2&=\langle(\max{S})^2\rangle-\langle\max{S}\rangle^2
\end{align}$$

