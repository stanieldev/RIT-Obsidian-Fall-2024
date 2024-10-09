**Name:** Stanley Goodwin
**Date:** XX/XX/2024
**Collaborators:** None



### Question 1
$$V(x)=\begin{cases}
&\dfrac{m\omega^2x^2}{2}&,&x\gt 0\\
&\infty&,&x\lt 0\\
\end{cases}$$
$$-\dfrac{\hbar^2}{2m}\dfrac{\partial^2 \psi_n}{\partial x^2}+V(x)\psi_n=E_n\psi_n$$
For $x>0$:
$$\begin{align}
-\dfrac{\hbar^2}{2m}\dfrac{\partial^2 \psi_n}{\partial x^2}+\dfrac{m\omega^2x^2}{2}\psi_n&=E_n\psi_n\\
\dfrac{\partial^2 \psi_n}{\partial x^2}+\dfrac{m^2\omega^2}{\hbar^2}x^2\psi_n&=-\dfrac{2mE_n}{\hbar^2}\psi_n\\
-\left(\dfrac{2mE_n}{\hbar^2}+\dfrac{m^2\omega^2}{\hbar^2}x^2\right)\psi_n&=\dfrac{\partial^2 \psi_n}{\partial x^2}\\
\end{align}$$

### Question 2
Using $H=\hbar\omega\left(a^\dagger a+\dfrac{1}{2}\right)+x_0^4\left(a^\dagger+a\right)^4$.
$$\begin{align}
\left(a^\dagger+a\right)^2\psi_n&=\sqrt{(n+1)(n+2)}\psi_{n+2}+(2n+1)\psi_{n}+\sqrt{n(n-2)}\psi_{n-2}
\end{align}$$


Let's define a certain operator $a$ such that:
$$\begin{align}
a_0\psi_n&=\sqrt{n}\psi_{n-1}\\
a_1\psi_n&=\sqrt{n+1}\psi_{n+1}\\
\end{align}$$
Then we can say that:
$$a_k\psi_n=\sqrt{n+k}\cdot\psi_{n+2k-1}$$


$$\begin{align}
\langle H\rangle_n &= \int_{-\infty}^{\infty}\psi_n^*H\psi_n\ dx\\
&=\int_{-\infty}^{\infty}\psi_n^*\hbar\omega\left(a^\dagger a+\dfrac{1}{2}\right)\psi_n\ dx+x_0^4\int_{-\infty}^{\infty}\psi_n^*\left(a^\dagger+a\right)^4\psi_n\ dx\\
&=\hbar\omega\left(n+\dfrac{1}{2}\right)+\left(\dfrac{\hbar}{2m\omega}\right)^2\left(\begin{array}{c}4\\2\end{array}\right)\dfrac{(n+1)^{3}-n^{3}}{3}\\
&=\hbar\omega\left(n+\dfrac{1}{2}\right)+\left(\dfrac{\hbar}{2m\omega}\right)^2\left(6n^2+6n+2\right)\\
\end{align}$$







# Synthesizing num 2
$$\begin{align}
\sum_{i,j,k,l}a_ia_ja_ka_l\psi_n&=\sum_{i,j,k,l}\left(\sqrt{n+l}\right)a_ia_ja_k\psi_{n+2l-1}\\
&=\sum_{i,j,k,l}\left(\sqrt{n+l}\right)\left(\sqrt{n+2l-1+k}\right)a_ia_j\psi_{n+2l+2k-1-1}\\
&=\sum_{i,j,k,l}\left(\sqrt{n+l}\right)\left(\sqrt{n+2l-1+k}\right)\sqrt{n+2l+2k-1-1+j}\cdot a_i\psi_{n+2l+2k+2j-1-1-1}\\
&=\sum_{i,j,k,l}\left(\sqrt{n+l}\right)\left(\sqrt{n+2l-1+k}\right)\sqrt{n+2l+2k-1-1+j}\sqrt{n+2l+2k+2j+i-1-1-1}\cdot\psi_{n+2l+2k+2j+2i-1-1-1-1}\\
&=\sum_{i,j,k,l}\left(\sqrt{n+l}\right)\left(\sqrt{n+2l-1+k}\right)\sqrt{n+2l+2k-1-1+j}\sqrt{n+2l+2k+2j+i-1-1-1}\cdot\psi_{n-N+2(l+k+j+i)}\\
\end{align}$$


$$\begin{align}
&\sum_{i,j,k,l}\left(\sqrt{n+l}\right)\left(\sqrt{n+k+2(l)-1}\right)\sqrt{n+j+2(l+k)-2}\sqrt{n+i+2(l+k+j)-3}\cdot\psi_{n-N+2(l+k+j+i)}\\
&\sum_{i,j,k,l}\left(\sqrt{n+1-l}\right)\left(\sqrt{n+2-2(l)-k}\right)\sqrt{n+3-2(l+k)-j}\sqrt{n+4-2(l+k+j)-i}\cdot\psi_{n-N+8-2(l+k+j+i)}\\
\end{align}$$


### Looking only 1 Creation
$$\begin{align}
&\sum_{i,j,k,l}\left(\sqrt{n+l}\right)\left(\sqrt{n+k+2(l)-1}\right)\sqrt{n+j+2(l+k)-2}\sqrt{n+i+2(l+k+j)-3}\cdot\psi_{n-2}\\
\end{align}$$
$$\begin{align}
&\sum_{i,j,k,l}\left(\sqrt{n}\right)\left(\sqrt{n-1}\right)\sqrt{n-2}\sqrt{n-2}\cdot\psi_{n-2}\\
&\sum_{i,j,k,l}\left(\sqrt{n}\right)\left(\sqrt{n-1}\right)\sqrt{n-1}\sqrt{n-1}\cdot\psi_{n-2}\\
&\sum_{i,j,k,l}\left(\sqrt{n}\right)\left(\sqrt{n-1}\right)\sqrt{n}\sqrt{n}\cdot\psi_{n-2}\\
&\sum_{i,j,k,l}\left(\sqrt{n}\right)\left(\sqrt{n-1}\right)\sqrt{n+1}\sqrt{n+1}\cdot\psi_{n-2}\\
&=\sqrt{n+0}\sqrt{n+1}\left(4n+4-\dfrac{3\cdot(3+1)}{2}\right)\psi_{n-2}
\end{align}$$
### Looking only 3 Creation
$$\begin{align}
&\sum_{i,j,k,l}\left(\sqrt{n+3}\right)\left(\sqrt{n+3}\right)\sqrt{n+1}\sqrt{n+2}\cdot\psi_{n+2}\\
&\sum_{i,j,k,l}\left(\sqrt{n+2}\right)\left(\sqrt{n+2}\right)\sqrt{n+1}\sqrt{n+2}\cdot\psi_{n+2}\\
&\sum_{i,j,k,l}\left(\sqrt{n+1}\right)\left(\sqrt{n+1}\right)\sqrt{n+1}\sqrt{n+2}\cdot\psi_{n+2}\\
&\sum_{i,j,k,l}\left(\sqrt{n+0}\right)\left(\sqrt{n+0}\right)\sqrt{n+1}\sqrt{n+2}\cdot\psi_{n+2}\\
&=\sqrt{n+1}\sqrt{n+2}\left(4n+\dfrac{3\cdot(3+1)}{2}\right)\psi_{n+2}
\end{align}$$
### Looking only 2 Creation
$$\begin{align}
&\sum_{0,0,1,1}\sqrt{n-1}^2\sqrt{n+0}^2\cdot\psi_{n}\\
&\sum_{0,1,0,1}\sqrt{n+0}^2\sqrt{n+0}^2\cdot\psi_{n}\\
&\sum_{0,1,1,0}\sqrt{n+0}^2\sqrt{n+1}^2\cdot\psi_{n}\\
&\sum_{1,0,0,1}\sqrt{n+0}^2\sqrt{n+1}^2\cdot\psi_{n}\\
&\sum_{1,0,1,0}\sqrt{n+1}^2\sqrt{n+1}^2\cdot\psi_{n}\\
&\sum_{1,1,0,0}\sqrt{n+1}^2\sqrt{n+2}^2\cdot\psi_{n}\\
&=n(n-1)+n^2+n(n+1)+n(n+1)+(n+1)(n+1)+(n+1)(n+2)\\
&=(n^2-n)+n^2+(n^2+n)+(n^2+n)+(n^2+2n+1)+(n^2+3n+2)\\
&=\left(6n^2+6n+3\right)\cdot \psi_{n}\\
\end{align}$$
### Total
$$\begin{align}
\left(a^\dagger+a\right)^4\psi_n&=\sum_{i,j,k,l}a_ia_ja_ka_l\psi_n\\
&=\sqrt{\dfrac{(n+4)!}{n!}}\psi_{n+4}+\sqrt{\dfrac{n!}{(n-4)!}}\psi_{n+4}\\
&+\sqrt{n+0}\sqrt{n+1}\left(4n+4-\dfrac{3\cdot(3+1)}{2}\right)\psi_{n-2}\\
&+\sqrt{n+1}\sqrt{n+2}\left(4n+\dfrac{3\cdot(3+1)}{2}\right)\psi_{n+2}\\
&+\left(6n^2+6n+3\right)\cdot \psi_{n}\\
\end{align}$$

$$\begin{align}
\left(a^\dagger+a\right)^4\psi_n&=\sum_{i,j,k,l}a_ia_ja_ka_l\psi_n\\
&=\sqrt{\dfrac{(n+4)!}{n!}}\psi_{n+4}+\sqrt{\dfrac{n!}{(n-4)!}}\psi_{n+4}\\
&+\sqrt{n+0}\sqrt{n+1}\left(4n-2\right)\psi_{n-2}\\
&+\sqrt{n+1}\sqrt{n+2}\left(4n+6\right)\psi_{n+2}\\
&+\left(6n^2+6n+3\right)\cdot \psi_{n}\\
\end{align}$$

$$\int_{-\infty}^{\infty}\psi_n^*(x)\left(a^\dagger+a\right)^{2p}\psi_n(x)\ dx=\left(\begin{array}{c}2p\\p\end{array}\right)\dfrac{(n+1)^{p+1}-n^{p+1}}{p+1}$$

