https://ieeexplore.ieee.org/abstract/document/5611564
$$\begin{align}
\dfrac{\Delta\rho}{\Delta T}&=\alpha\rho
\end{align}$$
I'm going to extend this to a continuum:
$$\begin{align}
\dfrac{d\rho}{dT}&=\alpha\rho
\end{align}$$
So we can find that:
$$\rho(T)=\rho(T_0)e^{\alpha(T-T_0)}$$
This is a simplified model, but correctly accounts for the exponential behavior instead of just being a linear relationship (which fails at higher temperatures).

### Case 1: Constrained Wires
We'll assume that the wires will not expand in any direction.
$$\rho(T)=\rho(T_0)e^{\alpha(T-T_0)}$$
$$R=\dfrac{\rho(T)\cdot l}{A}=\dfrac{\rho(T_0)\cdot l}{A}e^{\alpha(T-T_0)}=R_0e^{\alpha(T-T_0)}$$

Conservation of energy:
$$P=A\sigma\epsilon(T^4-T_\text{ambient}^4)$$
$$P=VI=I^2R=I^2R_0e^{\alpha(T-T_0)}$$
$$T^4-T_\text{ambient}^4=\dfrac{I^2R_0}{A\sigma\epsilon}e^{-\alpha T_0}e^{\alpha T}$$
$$(T^4-T_\text{ambient}^4)e^{\alpha T}=\dfrac{I^2R_0}{A\sigma\epsilon}e^{-\alpha T_0}$$
Lets assume that the outside is a vacuum:
$$T^4e^{\alpha T}=\left(\dfrac{\rho(T_0)\cdot l}{A_\text{surface}A_\text{cross}\sigma\epsilon}e^{-\alpha T_0}\right)I^2$$
Where $\sigma$ is the steffan-boltzmann constant.


### Case 2: Unrestricted Wires
$$\rho(T)=\rho(T_0)e^{\alpha_T(T-T_0)}$$
$$l(T)=l(T_0)e^{\alpha_M(T-T_0)}$$
$$A(T)=A(T_0)e^{2\alpha_M(T-T_0)}$$
$$R=\dfrac{\rho(T)\cdot l(T)}{A(T)}=\dfrac{\rho(T_0)l(T_0)}{A(T_0)}\dfrac{e^{\alpha_T(T-T_0)}\cdot e^{\alpha_M(T-T_0)}}{e^{2\alpha_M(T-T_0)}}=R_0\dfrac{e^{\alpha_T(T-T_0)}}{e^{\alpha_M(T-T_0)}}$$


Conservation of energy:
$$P=A\sigma\epsilon(T^4-T_\text{ambient}^4)=A(T_0)e^{2\alpha_M(T-T_0)}\sigma\epsilon(T^4-T_\text{ambient}^4)$$
$$P=VI=I^2R=I^2R_0e^{(\alpha_T-\alpha_M)(T-T_0)}$$
$$(T^4-T_\text{ambient}^4)e^{(\alpha_T-3\alpha_M)T}=\dfrac{I^2R_0}{A(T_0)\sigma\epsilon}e^{-(\alpha_T-3\alpha_M)T_0}$$
$$(T^4-T_\text{ambient}^4)e^{(\alpha_T-3\alpha_M)T}=\left(\dfrac{\rho_0l_0}{A_{\text{S}0}A_{\text{C}0}}\dfrac{1}{\sigma\epsilon}e^{-(\alpha_T-3\alpha_M)T_0}\right)I^2$$




### Copper Material

$\rho_0$ at $20^\circ$C : $1.68\cdot10^{−8}$ Ohm meters
https://www.thoughtco.com/table-of-electrical-resistivity-conductivity-608499

