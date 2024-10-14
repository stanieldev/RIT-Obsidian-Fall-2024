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
\langle H\rangle_n &= \int_{-\infty}^{\infty}\psi_n^*H\psi_n\ dx\\
&=\int_{-\infty}^{\infty}\psi_n^*\hbar\omega\left(a^\dagger a+\dfrac{1}{2}\right)\psi_n\ dx+x_0^4\int_{-\infty}^{\infty}\psi_n^*\left(a^\dagger+a\right)^4\psi_n\ dx\\
&=\hbar\omega\left(n+\dfrac{1}{2}\right)+\left(\dfrac{\hbar}{2m\omega}\right)^2\left(\begin{array}{c}4\\2\end{array}\right)\dfrac{(n+1)^{3}-n^{3}}{3}\\
&=\hbar\omega\left(n+\dfrac{1}{2}\right)+\left(\dfrac{\hbar}{2m\omega}\right)^2\left(6n^2+6n+2\right)\\
\end{align}$$


### Question 3
$$\Psi(x,0)=Ae^{-a|x|}$$
$$\begin{align}
\int_{-\infty}^\infty\Psi^*(x,0)\Psi(x,0)\ dx&=\int_{-\infty}^\infty A^*e^{-a|x|}Ae^{-a|x|}\ dx\\
&=2A^2\int_{0}^\infty e^{-2ax}\ dx\\
&=2A^2\dfrac{1}{-2a}\left.e^{-2ax}\right|_{0}^\infty\\
&=-A^2\dfrac{1}{a}\left(0-1\right)\\
1&=A^2\dfrac{1}{a}\\
\Aboxed{A&=\sqrt{a}}
\end{align}$$
$$\begin{align}
\int_{-\infty}^\infty\Psi(x,0)e^{-ikx}\ dx&=\int_{-\infty}^\infty \sqrt{a}e^{-a|x|}e^{-ikx}\ dx\\
&=\sqrt{a}\left(\int_{-\infty}^0 e^{ax}e^{-ikx}\ dx+\int_{0}^\infty e^{-ax}e^{-ikx}\ dx\right)\\
&=\dfrac{\sqrt{a}}{a-ik}\left. e^{ax}e^{-ikx}\right|_{-\infty}^0+\dfrac{\sqrt{a}}{-a-ik}\left. e^{-ax}e^{-ikx}\ dx\right|_{0}^\infty\\
&=\dfrac{\sqrt{a}}{a-ik}\left(1-0\right)+\dfrac{\sqrt{a}}{-a-ik}\left(0-1\right)\\
&=\dfrac{\sqrt{a}}{a-ik}+\dfrac{\sqrt{a}}{a+ik}\\
&=\sqrt{a}\left(\dfrac{(a+ik)}{(a+ik)(a-ik)}+\dfrac{(a-ik)}{(a+ik)(a-ik)}\right)\\
\phi(k,0)&=\dfrac{2a\sqrt{a}}{a^2+k^2}\\
\end{align}$$
$$\begin{align}
\Psi(x,t)&=\left(\int_{-\infty}^\infty\phi(k)\cdot e^{ikx}\ dk\right)e^{-ikx}e^{-iE_kt/\hbar}
\end{align}$$

### Question 4
$$\Psi(x,0)=Ae^{-ax^2}$$
$$\begin{align}
\int_{-\infty}^\infty\Psi^*(x,0)\Psi(x,0)\ dx&=\int_{-\infty}^\infty Ae^{-ax^2}Ae^{-ax^2}\ dx\\
&=A^2\int_{-\infty}^\infty e^{-2ax^2}\ dx\\
&=A^2\int_{-\infty}^\infty e^{-(\sqrt{2a}x)^2}\ dx\\
&=\dfrac{A^2}{\sqrt{2a}}\int_{-\infty}^\infty e^{-u^2}\ du\\
1&=A^2\sqrt{\dfrac{\pi}{2a}}\\
\Aboxed{A&=\left(\dfrac{2a}{\pi}\right)^{1/4}}
\end{align}$$
$$\begin{align}
|\Psi(x,t)|^2\ dx&=\left(\dfrac{2a}{\pi}\right)^{1/2}e^{-ax^2}
\end{align}$$
$$\begin{align}
\langle x(t)\rangle&=\int_{-\infty}^\infty\Psi^*(x,t)\hat{x}\Psi(x,t)\ dx\\
&=\int_{-\infty}^\infty x\Psi^*(x,t)\Psi(x,t)\ dx\\
&=\left(\dfrac{2a}{\pi}\right)^{1/2}\int_{-\infty}^\infty xe^{-ax^2}\ dx\\
&=\dfrac{1}{2a}\left(\dfrac{2a}{\pi}\right)^{1/2}\int_{-\infty}^\infty 2axe^{-ax^2}\ dx\\
&=\dfrac{1}{2a}\left(\dfrac{2a}{\pi}\right)^{1/2}\int_{x=-\infty}^{x=\infty} e^{-u}\ du\\
&=-\dfrac{1}{2a}\left(\dfrac{2a}{\pi}\right)^{1/2}\left.e^{-ax^2}\right|_{-\infty}^{\infty}\\
&=-\dfrac{1}{2a}\left(\dfrac{2a}{\pi}\right)^{1/2}\left(1-1\right)\\
\Aboxed{\langle x(t)\rangle&=0}
\end{align}$$
$$\begin{align}
\langle x^2\rangle&=\int_{-\infty}^\infty\Psi^*(x,t)\hat{x}\Psi(x,t)\ dx\\
&=\int_{-\infty}^\infty x^2\Psi^*(x,t)\Psi(x,t)\ dx\\
&=\left(\dfrac{2a}{\pi}\right)^{1/2}\int_{-\infty}^\infty x^2e^{-2ax^2}\ dx\\
&=\left(\dfrac{2a}{\pi}\right)^{1/2}\sqrt{\dfrac{\pi}{2}}\dfrac{1}{4a^{3/2}}\\
&=\dfrac{1}{4a}\\
\Aboxed{\langle x^2\rangle&=\dfrac{1}{4a}}
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

