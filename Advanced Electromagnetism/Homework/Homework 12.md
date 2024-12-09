**Name:** Stanley Goodwin
**Date:** 12/14/2024
**Collaborators:** None
**Time Taken:** XXX Hours

As always, your work will be graded for clarity of explanation as much as for the “correctness” of your final answer. And as always, please include the names of those you collaborated with, as well as the total number of hours spent on this assignment. I’ve decided to treat this as a bonus assignment, both because I’m adding to it in this final week and because a couple of the concepts (specifically, intervals and world lines) are things you’ve seen before but that we skipped reviewing in class (although you can find a good review in Griffiths). That said, don’t blow this off, even if you don’t need the extra credit—one problem on your final exam will be lifted directly from this assignment.

---
## Question 1
Lorentz Transformation in 1D:
$$\begin{align}
\left[\begin{array}{c}ct'\\x'\end{array}\right]&=\gamma\left[\begin{array}{c}1&-\beta\\-\beta&1\end{array}\right]\left[\begin{array}{c}ct\\x\end{array}\right] & \left[\begin{array}{c}ct\\x\end{array}\right]&=\gamma\left[\begin{array}{c}1&\beta\\\beta&1\end{array}\right]\left[\begin{array}{c}ct'\\x'\end{array}\right]
\end{align}$$
### 1.A
Space probe #1 passes very close to earth at a time that both we (on earth) and the onboard computer on Probe1 decide to call $t=t'=0$ in our respective frames. The probe moves at a constant speed of $v=0.6c$ away from earth. When the clock aboard Probe1 reads $t'=60\text{s}$, it sends a light signal straight back to earth.

I made a Lorentz Transform Desmos plot to help my calculations:
https://www.desmos.com/calculator/pzpmfdbeai
**Note:** Earth has $(x,t)$ coordinates, Probe1 has $(x',t')$ coordinates.
#### 1.A.I
At what time was the signal sent, according to Earth’s rest frame?
$$\begin{align}
\left[\begin{array}{c}ct\\x\end{array}\right]
&=\gamma\left[\begin{array}{c}1&\beta\\\beta&1\end{array}\right]\left[\begin{array}{c}ct'\\x'\end{array}\right]\\
&=1.25\left[\begin{array}{c}1&0.6\\0.6&1\end{array}\right]\left[\begin{array}{c}c\cdot60\text{s}\\0\end{array}\right]\\
&=1.25\left[\begin{array}{c}1\cdot c\cdot60\text{s}+0.6\cdot0\\0.6\cdot c\cdot60\text{s}+0\end{array}\right]\\
&=1.25\left[\begin{array}{c}c\cdot60\text{s}\\c\cdot36\text{s}\end{array}\right]\\
\left[\begin{array}{c}ct\\x\end{array}\right]&=\left[\begin{array}{c}c\cdot75\text{s}\\c\cdot45\text{s}\end{array}\right]\\
\Aboxed{\left[\begin{array}{c}t\\x\end{array}\right]&=\left[\begin{array}{c}75\text{s}\\45\text{ l.s.}\end{array}\right]}
\end{align}$$
#### 1.A.II
At what time in Earth’s rest frame do we receive the signal?
$$\begin{align}
\Delta t&=t_0+t_\text{signal}\\
&=t_0+\dfrac{\Delta x}{c}\\
&=75\text{s}+45\text{s}\\
\Aboxed{\Delta t&=120\text{s}}
\end{align}$$
#### 1.A.III
At what time in Probe1’s rest frame does the signal reach Earth?
$$\begin{align}
\left[\begin{array}{c}ct'\\x'\end{array}\right]
&=\gamma\left[\begin{array}{c}1&-\beta\\-\beta&1\end{array}\right]\left[\begin{array}{c}ct\\x\end{array}\right]\\
&=1.25\left[\begin{array}{c}1&-0.6\\-0.6&1\end{array}\right]\left[\begin{array}{c}c\cdot120\text{s}\\0\end{array}\right]\\
&=1.25c\left[\begin{array}{c}120\text{s}\\-0.6\cdot120\text{s}\end{array}\right]\\
\Aboxed{\left[\begin{array}{c}t'\\x'\end{array}\right]
&=\left[\begin{array}{c}150\text{s}\\90\text{ l.s.}\end{array}\right]\\}
\end{align}$$
### 1.B
Space probe #2 passes very close to earth at $t=1\mathrm{s}$ (Earth time), chasing Probe1. Probe2 is moving at $0.3c$ (as viewed by us). Probe2 launches a proton beam (which moves at $v=0.31c$ relative to Probe2) directed at Probe1. Does this proton beam strike Probe1? Please answer twice, once ignoring relativity theory, and then again using Einstein.
https://www.desmos.com/calculator/plagj5lrmc

The equation for the time where the proton beam collides with Probe 1 is:
$$\begin{align}
v(t_c-1\text{s})=0.6ct_c \implies \boxed{t_c=\dfrac{v\cdot1\text{s}}{v-0.6c}}
\end{align}$$
For the non-relativistic case, where $v=0.30c+0.31c=0.61c$, then:
$$\begin{align}
t_c&=\dfrac{0.61c\cdot1\text{s}}{0.61c-0.6c}=61\text{s}
\end{align}$$
As for the relativistic case, we need to find the net speed of the beam:
$$\begin{align}
v_\text{net}&=\dfrac{v_1+v_2}{1+v_1v_2}c=\dfrac{0.30+0.31}{1+0.30\cdot0.31}c=0.558c
\end{align}$$
Plugging it in, we see that:
$$\begin{align}
t_c&=\dfrac{0.558c\cdot1\text{s}}{0.558c-0.6c}<1\text{s}
\end{align}$$
Therefore, it never collides with Probe1 with special relativity's velocity addition.
In the classical velocity addition, Probe1 would have the proton beam collide with it.

---
## Question 2
When I was in undergrad, there was a brief fuss in the media about “faster than light neutrinos”. Let’s investigate those claims. Define the LHC lab in Switzerland to be located at $x_1=0$ in the Earth’s rest frame, and the Italian Gran Sasso neutrino detection facility to be located at $x_2 = 730\text{km}$. (Ignore any motion of the Earth in this problem.).
### 2.A
Suppose a beam of photons travels from LHC (starting at $x_1=t_1=0$) heading to Gran Sasso in a straight line (through vacuum).
#### 2.A.I
At what time $t_2$ will the photons arrive at the detector in Gran Sasso (in the Earth’s rest frame)? (Neglect general relativity)
$$\begin{align}
\Delta\tau&=\dfrac{\Delta x}{c}\\
t_2-0&=\dfrac{730\text{ km}}{3\cdot10^5\text{ km/s}}\\
\Aboxed{t_2&=2.4\bar{3}\text{ ms}}
\end{align}$$
#### 2.A.II
Consider the photon arrival time as measured in a frame that is moving past the LHC towards Gran Sasso at high speed $v$. This frame has been synchronized so $x_1'=t_1'=0$ when the photons leave LHC on their way towards Gran Sasso (i.e. the origins of the two frames ($x_1=x_1'=0$) coincide at $t_1=t_1'=0$). In the limit that $v$ approaches $c$ (from below), what happens to the photon arrival time ($t_2'$) as measured in the moving frame? Show that $t_2'$ is NEVER less than or equal to 0 in a frame that could contain a physical observer (one that is moving at less than $c$). Interpret this result in words (think about “causality”).
$$\begin{align}
ct_2'&=\gamma(v)\left(ct_2-\beta x_2\right)\\
&=\gamma(v)\left(c\dfrac{x_2}{c}-\beta x_2\right)\\
&=\gamma(v)\left(x_2-\beta x_2\right)\\
&=x_2\dfrac{1-\beta}{\sqrt{1-\beta^2}}\\
&=x_2\dfrac{1-\beta}{\sqrt{(1-\beta)(1+\beta)}}\\
ct_2'&=x_2\sqrt{\dfrac{1-\beta}{1+\beta}}\\
\Aboxed{t_2'&=\dfrac{x_2}{c}\sqrt{\dfrac{1-\beta}{1+\beta}}}
\end{align}$$
Taking the bounds as the limits:
$$\begin{align}
\lim_{\beta\rightarrow1^-}\dfrac{x_2}{c}\sqrt{\dfrac{1-\beta}{1+\beta}}<\ &t_2'<\lim_{\beta\rightarrow0}\dfrac{x_2}{c}\sqrt{\dfrac{1-\beta}{1+\beta}}\\
0<\ &t_2'<\dfrac{x_2}{c}\\
\Aboxed{0<\ &t_2'<t_2}
\end{align}$$
The time interval cannot become negative (i.e. go into the past) since all observes are constrained by the speed limit of $c$ from below. Therefore, causality is preserved for *all* frames that travel than less of the speed of light since $t_2'$ must happen after $t_1'$.

### 2.B
Now suppose that a beam of neutrinos could travel from the LHC (starting at $x_1=t_1=0$) heading to Gran Sasso in a straight line with a speed $v=c\left(1+2.5\cdot10^{-5}\right)$. You read that right, let’s suppose for the sake of argument that neutrinos somehow travel faster than $c$ by 25 ppm.
#### 2.B.I
At what time $t_2$ will these neutrinos arrive at the detector in Gran Sasso (in the Earth’s rest frame)? How much sooner do they arrive than the photons of part (a)?
$$\begin{align}
t_2&=\dfrac{\Delta x}{v}\\
&=\dfrac{730\text{ km}}{c\left(1+2.5\cdot10^{-5}\right)}\\
\Aboxed{t_2&=2.433272\text{ ms}}\\
\Aboxed{\Delta t&=60.83\text{ ns}}
\end{align}$$
#### 2.B.II
Now consider the neutrino arrival time, as measured in a frame that is moving past LHC towards Gran Sasso at high speed $v$. (But of course, not $>c$!) Again, synchronized so $x_1'=t_1'=0$ when the neutrinos leave LHC on their way towards Gran Sasso (i.e. the origins of the two frames coincide at $t_1=t_1'=0$). What speed (with respect to the earth frame) does a frame need, in order for a local observer to measure the neutrinos hitting the detector at $t_2'=0$ (i.e., at EXACTLY the same time as they left in that frame?) What is $\gamma$ for this frame? Is it physically possible to have an “observer” with such a $\gamma$?

Using our previous result for $t'$ as a function of $\beta$:
$$\begin{align}
t_2'&=\dfrac{x_2}{c}\sqrt{\dfrac{1-\beta}{1+\beta}}
\end{align}$$
To find when $t'_2=0$, we can substitute and solve:
$$\begin{align}
0&=\dfrac{x_2}{c}\sqrt{\dfrac{1-\beta}{1+\beta}}\\
0&=\sqrt{1-\beta}\\
0&=1-\beta\\
\Aboxed{\beta&=1}
\end{align}$$
For it to appear at the same time as it was emitted, the observer must be traveling at the speed of light $c$. This would result in $|\gamma(c)|=\infty$. For an observer to travel at $c$, it must be massless.
#### 2.B.III (Incorrect)
If this frame were moving just a little FASTER than the above speed (but still less then c, always!) what would be the SIGN of $t_2'$, the time in that frame at which the neutrinos arrive? Is there any physical principle forbidding you from being an observer in this moving inertial frame? (In such an inertial frame, I claim the neutrinos are measured to arrive at the detector before they are emitted from the source. What do you think of this result?)
$$\begin{align}
...
\end{align}$$


### 2.C
Sketch the world line of a neutrino emitted from LHC and ending at Gran Sasso. On the same diagram, with a dashed line, indicate the world line of a photon making the same trip.
![[HW12_Q2C.png]]
I had to exaggerate the neutrino since the speeds were almost identical and overlapping.
#### 2.C.I (Incorrect)
Given such (claimed) data, is the space-time interval between emission and detection for individual neutrinos space-like, time-like, or light-like? 
Above, you considered a frame which flipped the time ordering. In that frame, again tell us about the character of the space-time interval (space-like, time-like, or light-like).


$$\begin{align}
t_2'&=\dfrac{x_2}{c}\sqrt{\dfrac{1-\beta}{1+\beta}}
\end{align}$$







**Note:** For this section, I will be using $\Delta s^2=-(c\Delta t)^2+\Delta x^2$.
$$\begin{align}
\Delta s^2&=-(c\Delta t)^2+\Delta x^2\\
&=-(ct_2')^2+(ct_2)^2\\
\Aboxed{\Delta s^2&<0\ \ \ \text{(Timelike)}}
\end{align}$$
For the flipped time-ordering, we get a similar result since the time interval is squared.





#### 2.C.II (Incorrect)
Suppose, upon detection of a neutrino event at Gran Sasso, the detector sends back a light signal to LHC to indicate they “got it”. Add the world line of that return signal to your diagram. Given the claim that the neutrinos traveled faster than c, some people in the media claimed this meant we had “backwards time travel”. What do you think they mean by that? E.g,. does that mean that this “return signal” arrives before the original signal was sent? (Use your diagram to answer this question unambiguously.)

The time-travel would occur when $t_2'=-2t_2$, and so:
$$\begin{align}
t_2'&=\dfrac{x_2}{c}\sqrt{\dfrac{1-\beta}{1+\beta}}\\
-2\dfrac{x_2}{c}&=\dfrac{x_2}{c}\sqrt{\dfrac{1-\beta}{1+\beta}}\\
-2&=\sqrt{\dfrac{1-\beta}{1+\beta}}\\
4&=\dfrac{1-\beta}{1+\beta}\\
\end{align}$$


---
## Question 3
$$\begin{align}
E'_x&=E_x & E'_y&=\gamma(E_y-vB_z) & E'_z&=\gamma(E_z+vB_y)\\
B'_x&=B_x & B'_y&=\gamma(B_y+vE_z/c^2) & B'_z&=\gamma(B_z-vE_y/c^2)\\
\end{align}$$
### 3.A
Use Griffiths Equation 12.109 (12.108 in 3rd edition) to show that both $\vec{E}\cdot\vec{B}$ and $E^2-c^2B^2$ are Lorentz invariants. We found earlier this semester that $\vec{E}$ and $\vec{B}$ are perpendicular for traveling EM waves. Given that this is true in some frame, can there by any other reference frame in which you would find $\vec{E}$ and $\vec{B}$ not perpendicular for a traveling EM wave?

**Part 1:** Dot Product
$$\begin{align}
E_x'B_x'&=E_xB_x\\
E_y'B_y'&=\gamma(E_y-vB_z)\gamma(B_y+vE_z/c^2)\\
&=\gamma^2(E_yB_y-B_yB_zv+E_yE_zv/c^2-E_zB_zv^2/c^2)\\
E_z'B_z'&=\gamma(E_z+vB_y)\gamma(B_z-vE_y/c^2)\\
&=\gamma^2(E_zB_z+vB_yB_z-E_yE_zv/c^2-E_yB_yv^2/c^2)\\
\end{align}$$
Combining, we get:
$$\begin{align}
\vec{E}'\cdot\vec{B}'
&=E_x'B_x'+E_y'B_y'+E_z'B_z'\\
&=E_xB_x+\gamma^2(E_yB_y-E_zB_zv^2/c^2)+\gamma^2(E_zB_z-E_yB_yv^2/c^2)\\
&=E_xB_x+\gamma^2(E_yB_y-E_yB_yv^2/c^2)+\gamma^2(E_zB_z-E_zB_zv^2/c^2)\\
&=E_xB_x+\dfrac{1-v^2/c^2}{1-v^2/c^2}E_yB_y+\dfrac{1-v^2/c^2}{1-v^2/c^2}E_zB_z\\
&=E_xB_x+E_yB_y+E_zB_z\\
\Aboxed{\vec{E}'\cdot\vec{B}'&=\vec{E}\cdot\vec{B}}
\end{align}$$
**Part 2:** Magnitudes
$$\begin{align}
(E')^2&=(E_x')^2+(E_y')^2+(E_z')^2\\
&=(E_x)^2+(\gamma(E_y-vB_z))^2+(\gamma(E_z+vB_y))^2\\
&=E_x^2+\gamma^2(E_y-vB_z)^2+\gamma^2(E_z+vB_y)^2\\
&=E_x^2+\gamma^2(E_y^2-2vE_yB_z+v^2B_z^2)+\gamma^2(E_z^2+2vE_zB_y+v^2B_y^2)\\
\\
c^2(B')^2&=c^2(B_x')^2+c^2(B_y')^2+c^2(B_z')^2\\
&=c^2B_x^2+c^2(\gamma(B_y+vE_z/c^2))^2+c^2(\gamma(B_z-vE_y/c^2))^2\\
&=c^2B_x^2+c^2\gamma^2(B_y+vE_z/c^2)^2+c^2\gamma^2(B_z-vE_y/c^2)^2\\
&=c^2B_x^2+\gamma^2(c^2B_y^2+2vE_zB_y+v^2E_z^2/c^2)+\gamma^2(c^2B_z^2-2vE_yB_z+v^2E_y^2/c^2)\\
\end{align}$$
Combining, we get:
$$\begin{align}
(E')^2-c^2(B')^2&=E_x^2+\gamma^2(E_y^2-2vE_yB_z+v^2B_z^2)+\gamma^2(E_z^2+2vE_zB_y+v^2B_y^2)\\
&-c^2B_x^2-\gamma^2(c^2B_y^2+2vE_zB_y+v^2E_z^2/c^2)-\gamma^2(c^2B_z^2-2vE_yB_z+v^2E_y^2/c^2)\\
&=E_x^2-c^2B_x^2+\gamma^2(-2vE_yB_z+2vE_zB_y-2vE_zB_y+2vE_yB_z)\\
&+\gamma^2(E_y^2-E_y^2v^2/c^2)-c^2\gamma^2(B_y^2-B_y^2v^2/c^2)\\
&+\gamma^2(E_z^2-E_z^2v^2/c^2)-c^2\gamma^2(B_z^2-B_z^2v^2/c^2)\\
&=E_x^2-c^2B_x^2+E_y^2-c^2B_y+E_z^2-c^2B_z\\
&=E_x^2+E_y^2+E_z^2-c^2(B_x^2+B_y^2+B_z^2)\\
\Aboxed{(E')^2-c^2(B')^2&=E^2-c^2B^2}
\end{align}$$
### 3.B
Use your results from part (a) to answer the following questions:
#### 3.B.I
Suppose $E>cB$ in some frame. Show that there is no possible frame in which $E=0$.

If $E>cB$, then $(E')^2-c^2(B')^2>0$. Suppose $E=0$, then:
$$\begin{align}
(E')^2>c^2(B')^2\implies0>c^2(B')^2\implies0>(B')^2
\end{align}$$
Since $B'$ is a real value, this equation makes a contradiction.
Therefore, there cannot be a frame where $E=0$.
#### 3.B.II
If $E=0$ in some frame, do these relations mean that $E=0$ in every other inertial frame?
$$-c^2B^2=(E')^2-c^2(B')^2$$
The electric field can only be $E=0$ in other inertial frames iff $|B|=|B'|$, otherwise there would have to be an E-field in that frame.

#### 3.B.III
If $B=0$ (but $E$ is nonzero) in some frame, can you always (ever?) find another frame in which $E=0$ but $B$ is nonzero?
$$\begin{align}
E^2-c^2B^2&=(E')^2-c^2(B')^2\\
0^2-c^2B^2=&(E')^2-c^2(0)^2\\
-c^2B^2&=(E')^2\\
\end{align}$$
Is it indeed possible to transform a pure $E$-field into a pure $B$-field. However, it would not be possible for any other electric fields in other frames.

---
## Question 4
It’s common in nuclear and particle physics to talk about the “rapidity” of a particle, defined as $y=\cosh^{-1}\gamma$ (where $\gamma$ is the usual relativistic gamma factor, and that’s an inverse hyperbolic cosine).
### 4.A
Prove that the usual relativistic $\beta$ (that’s $\beta=v/c$) is given by $\beta=\tanh y$, then show that $\beta\gamma=\sinh y$.
$$\begin{align}
...
\end{align}$$
