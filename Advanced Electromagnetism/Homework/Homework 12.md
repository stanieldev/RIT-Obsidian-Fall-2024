**Name:** Stanley Goodwin
**Date:** XX/XX/2024
**Collaborators:** None
**Time Taken:** XXX Hours

---
## Question 1
### 1.A
Space probe #1 passes very close to earth at a time that both we (on earth) and the onboard computer on Probe1 decide to call $\tau=t=0$ in our respective frames. The probe moves at a constant speed of $0.6c$ away from earth. When the clock aboard Probe1 reads $\tau=60\text{s}$, it sends a light signal straight back to earth.
https://www.desmos.com/calculator/mlefeopscm

Use Lorentz Transform equation instead of direct time-dilation and length-contraction.

#### 1.A.I
At what time was the signal sent, according to Earth’s rest frame?
$$\begin{align}
\Delta t&=\gamma(v)\Delta\tau\\
&=\dfrac{60\text{ s}}{\sqrt{1-0.6^2}}\\
&=\dfrac{60\text{ s}}{\sqrt{1-0.6^2}}\\
\Aboxed{\Delta t&=75\text{ s}}
\end{align}$$
#### 1.A.II
At what time in Earth’s rest frame do we receive the signal?
$$\begin{align}
\Delta t&=t_\text{waiting}+t_\text{signal}\\
&=75\text{ s}+\dfrac{0.6c\cdot75\text{ s}}{c}\\
&=75\text{ s}+45\text{ s}\\
\Aboxed{\Delta t&=120\text{ s}}
\end{align}$$
#### 1.A.III
At what time in Probe1’s rest frame does the signal reach Earth?
$$\begin{align}
\Delta \tau&=\dfrac{\Delta x}{c}+\tau\\
&=\dfrac{0.6c\cdot60\text{ s}}{c}+60\text{s}\\
&=\dfrac{0.6c\cdot60\text{ s}}{c}+60\text{s}\\
&=36\text{s}+60\text{s}\\
\Aboxed{\Delta\tau&=96\text{s}}
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

---
## Question 2
When I was in undergrad, there was a brief fuss in the media about “faster than light neutrinos”. Let’s investigate those claims. Define the LHC lab in Switzerland to be located at $x_1=0$ in the Earth’s rest frame, and the Italian Gran Sasso neutrino detection facility to be located at $x_2 = 730\text{km}$. (Ignore any motion of the Earth in this problem.).
### 2.A
Suppose a beam of photons travels from LHC (starting at $x_1=t_1=0$) heading to Gran Sasso in a straight line (through vacuum).
#### 2.A.I
At what time $t_2$ will the photons arrive at the detector in Gran Sasso (in the Earth’s rest frame)? (Neglect general relativity)
$$\begin{align}
\Delta\tau&=\dfrac{\Delta x}{c}\\
&=\dfrac{730\text{ km}}{3\cdot10^5\text{ km/s}}\\
\Aboxed{t_2&=2.4\bar{3}\text{ ms}}
\end{align}$$
#### 2.A.II
Consider the photon arrival time as measured in a frame that is moving past the LHC towards Gran Sasso at high speed $v$. (But of course, not >c!) This frame has been synchronized so $x_1'=t_1'=0$ when the photons leave LHC on their way towards Gran Sasso (i.e. the origins of the two frames ($x_1'=x_2'=0$) coincide at $t_1'=t_2'=0$). In the limit that $v$ approaches $c$ (from below), what happens to the photon arrival time ($t_2'$) as measured in the moving frame? Show that $t_2'$ is NEVER less than or equal to 0 in a frame that could contain a physical observer (one that is moving at less than $c$). Interpret this result in words (think about “causality”).
$$\begin{align}
\Delta t&=\gamma(v)\Delta\tau\\
\Aboxed{t_2'&=\dfrac{t_2}{\sqrt{1-v^2}}}
\end{align}$$
To constrain $t_2'$, we can see that:
$$\begin{align}
\lim_{v\rightarrow0}\dfrac{t_2}{\sqrt{1-v^2}}<&t_2'<\lim_{v\rightarrow 1^-}\dfrac{t_2}{\sqrt{1-v^2}}\\
\Aboxed{t_2<&t_2'<\infty}
\end{align}$$
Since $t_2>0$ for it to be a valid "interval," then that means that:
$$\begin{align}
\Aboxed{0<&t_2'<\infty}
\end{align}$$
The time interval cannot become negative (i.e. go into the past) since all observes are constrained by the speed limit of $c$ from below. Therefore, causality is preserved for all frames that travel than less of the speed of light.

### 2.B
Now SUPPOSE that a beam of neutrinos could travel from the LHC (starting at $x_1=t_1=0$) heading to Gran Sasso in a straight line with a speed $v=c\left(1+2.5\cdot10^{-5}\right)$. You read that right, let’s suppose for the sake of argument that neutrinos somehow travel FASTER than $c$ by 25 ppm.
#### 2.B.I
At what time $t_2$ will these neutrinos arrive at the detector in Gran Sasso (in the Earth’s rest frame)? How much sooner do they arrive than the photons of part (a)?
$$\begin{align}
t_2&=\dfrac{\Delta x}{v}\\
&=\dfrac{730\text{ km}}{c\left(1+2.5\cdot10^{-5}\right)}\\
\Aboxed{t_2&=2.433272\text{ ms}}\\
\Aboxed{\Delta t&=60.83\text{ ns}}
\end{align}$$
#### 2.B.II
Now consider the neutrino arrival time, as measured in a frame that is moving past LHC towards Gran Sasso at high speed $v$. (But of course, not >c!) Again, synchronized so $x_1'=t_1'=0$ when the neutrinos leave LHC on their way towards Gran Sasso (i.e. the origins of the two frames coincide at $t_1'=t_2'=0$). What speed (with respect to the earth frame) does a frame need, in order for a local observer to measure the neutrinos hitting the detector at $t_2'=0$ (i.e., at EXACTLY the same time as they left in that frame?) What is $\gamma$ for this frame? Is it physically possible to have an “observer” with such a $\gamma$?
#### 2.B.III
If this frame were moving just a little FASTER than the above speed (but still less then c, always!) what would be the SIGN of $t_2'$, the time in that frame at which the neutrinos arrive? Is there any physical principle forbidding you from being an observer in this moving inertial frame? (In such an inertial frame, I claim the neutrinos are measured to arrive at the detector before they are emitted from the source. What do you think of this result?)
### 2.C
Sketch the world line of a neutrino emitted from LHC and ending at Gran Sasso. On the same diagram, with a dashed line, indicate the world line of a photon making the same trip.
#### 2.C.I
Given such (claimed) data, is the space-time interval between emission and detection for individual neutrinos space-like, time-like, or light-like? Above, you considered a frame which flipped the time ordering. In that frame, again tell us about the character of the space-time interval (space-like, time-like, or light-like).
#### 2.C.II
Suppose, upon detection of a neutrino event at Gran Sasso, the detector sends back a light signal to LHC to indicate they “got it”. Add the world line of that return signal to your diagram. Given the claim that the neutrinos traveled faster than c, some people in the media claimed this meant we had “backwards time travel”. What do you think they mean by that? E.g,. does that mean that this “return signal” arrives before the original signal was sent? (Use your diagram to answer this question unambiguously.)

---
## Question 3
### 3.A
Use Griffiths Equation 12.109 (12.108 in 3rd edition) to show that both $\vec{E}\cdot\vec{B}$ and $E^2-c^2B^2$ are Lorentz invariants. We found earlier this semester that $\vec{E}$ and $\vec{B}$ are perpendicular for traveling EM waves. Given that this is true in some frame, can there by any other reference frame in which you would find $\vec{E}$ and $\vec{B}$ not perpendicular for a traveling EM wave?
### 3.B
Use your results from part (a) to answer the following questions:
#### 3.B.I
Suppose $E>cB$ in some frame. Show that there is no possible frame in which $E=0$.
#### 3.B.II
If $E=0$ in some frame, do these relations mean that $E=0$ in every other inertial frame?
#### 3.B.III
If $B=0$ (but $E$ is nonzero) in some frame, can you always (ever?) find another frame in which $E=0$ but $B$ is nonzero?