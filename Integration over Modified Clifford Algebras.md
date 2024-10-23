Define the following:
$V$: Vector space
$V^*$: Covector space
$W$: Antivector space
$W^*$: Anticovector space
$\Omega$: Dual space
$\Omega^*$: Antidual space

$$\langle v_i|v_j\rangle=v^iv_j=g_{kj}v^iv^k$$
The bilinear form $g$ has 3 different properties:
1. Axial symmetry: $e^ie_j=e^je_i$
2. Axial antisymmetry: $e^ie_j=-e^je_i$
3. Axial nullability: $e^ie_j=e^je_i=0$
We can define this as a pseudo-metric, since they still follow predictable rules, but don't have the property of transpose symmetry.


### Example
Let the space $A=V\otimes W\otimes\Omega$ and $A^*=V^*\otimes W^*\otimes\Omega^*$. 
Therefore, we can write an element of $A$ as:
$$a=a^0e_0+a^1e_1+a^2e_2$$
Where $e^0e_0=+1$, $e^1e_1=-1$, $e^2e_2=0$.
For all other combinations, we'll assume they're symmetric.
We can define the product of elements in $A$ and $A^*$.
$$\begin{align}
a^*b&=(a_0e^0+a_1e^1+a_2e^2)(b^0e_0+b^1e_1+b^2e_2)\\
&=(a_0e^0b^0e_0+a_0e^0b^1e_1+a_0e^0b^2e_2)\\&+(a_1e^1b^0e_0+a_1e^1b^1e_1+a_1e^1b^2e_2)\\
&+(a_2e^2b^0e_0+a_2e^2b^1e_1+a_2e^2b^2e_2)\\
&=(a_0b^0\mathbb{I}_{00}+a_0b^1\mathbb{I}_{01}+a_0b^2\mathbb{I}_{02})\\&+(a_1b^0\mathbb{I}_{10}+a_1b^1\mathbb{I}_{11}+a_1b^2\mathbb{I}_{12})\\
&+(a_2b^0\mathbb{I}_{20}+a_2b^1\mathbb{I}_{21}+a_2b^2\mathbb{I}_{22})\\
&=(a_0b^0-a_1b^1)+(a_0b^1\mathbb{I}_{01}+a_1b^0\mathbb{I}_{10})\\
&+(a_0b^2\mathbb{I}_{02}+a_2b^0\mathbb{I}_{20})+(a_1b^2\mathbb{I}_{12}+a_2b^1\mathbb{I}_{21})
\end{align}$$



The inspiration is from complex numbers $z=x+iy$, where there's theorems for integration that reduce problems much more, and the idea of *holomorphic* and *residue* are things I want to expand upon for these modified Clifford Algebras.
