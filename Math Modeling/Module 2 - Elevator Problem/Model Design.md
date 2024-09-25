**Date 9/17/2024**

### Model Parameter Space (Email)
Given the set of parameters here:
$$\begin{align}
T_\text{0}&=15\mathrm{s} &\text{The time the elevator is open on the ground floor.}\\
T_\text{F}&=10\mathrm{s}\ &\text{The time the door is open on non-ground floors.} \\
T_\text{t}&=4\ \mathrm{s}/\text{Floor}\ &\text{The time the elevator takes to travel between floors.}\\
N_\text{F}&=6\text{ Floors}\ &\text{The number of floors of the building above the ground floor.}\\
N_\text{E}&=x\text{ Elevators}\ &\text{Number of elevators in the building.}\\
C_\text{E}&=10\text{ People}\ &\text{Max Capacity of a singular Elevator.}
\end{align}$$
We're given that the distribution of workers per floor is:
$$\begin{align}
\text{Floor}&&\text{G}&&\text{1st}&&\text{2nd}&&\text{3rd}&&\text{4th}&&\text{5th}&&\text{6th}\\
\text{Number}&&0&&80&&80&&40&&80&&20&&20
\end{align}$$
### Model Assumptions
In order to keep the mathematics a lot less complicated, I propose a few constraints:
 - An elevator will always be, and will only leave when, filled to capacity $C_\text{E}$.
	 - This has less to do with reality and more to minimize the number of trips.
 - The probability of individual employees going to floors are independent of each-other.
	 - No groups of employees/friends travel together.
	 - This keeps the probability of traveling to different floors independent.
 - Employees always get off at their designated floor.
	 - We assume that employees are paying attention to the floor they're traveling to.
	 - This ensures the door only opens once per floor.
 - Employees do not interfere with the operations of the elevator.
	 - Employees are assumed to be harmless to elevator operations.
	 - This ensures that elevator times are unchanged while operating.
 - Employees arrive to the lobby at equally-spaced interval.
	 - Employees are assumed to have no free will on when they arrive, on average.
	 - This controls for employee arrival times being influenced by other employees and what floor an employee needs to get to.

### Single-Elevator
To model a singular elevator, we can represent the number of employees going to each floor as an ordered list of configurations:
$$E=\left[n_1,n_2,\dots,n_{N_\text{F}}\right],\text{ where } \displaystyle\sum_in_i=C_\text{E}$$
We can also represent the probability of an employee getting off on floor $i$ : 
$$p_i=\dfrac{\text{Employees on floor }i}{\text{Total Employees}}, \text{ where } \displaystyle\sum_i p_i = 1$$
We can express the probability of a configuration $E$ as:
$$\begin{align}
p\left(E\right)&=(C_\text{E})!\cdot\prod_{f=1}^{N_\text{F}}\dfrac{(p_f)^{n_f}}{(n_f)!}
\end{align}$$
To find the time of the configuration, we can write it as:
$$T\left(E\right)= T_0 + F(E)\cdot T_\text{f} + 2M(E)\cdot T_\text{t}$$
Where $F(E)$ is the number of floors that don't have $0$ people going to it and $M(E)$ is the highest floor that doesn't have $0$ people going to it.

#### Sensitivity
Starting with the time of a configuration
$$T\left(E\right)=T_0+F(E)\cdot T_\text{f} + 2M(E)\cdot T_\text{t}$$
we get that the responses of changes to our parameters are:
$$\begin{align}
\dfrac{\partial T(E)}{\partial T_0}&= 1& 
\dfrac{\partial T(E)}{\partial T_\text{f}}&= F(E)&
\dfrac{\partial T(E)}{\partial T_\text{t}}&= M(E)
\end{align}$$




#### Statistical Quantities
We can calculate the expected values of floors, the maximum floor, and total duration:
$$\begin{align}
\langle F\rangle&=\sum_{E} F(E)\cdot p(E)\\
\langle M\rangle&=\sum_{E} F(E)\cdot p(E)\\
\langle T\rangle&=\sum_{E} T(E)\cdot p(E)\\
&=T_0+\langle F\rangle\cdot T_\text{f} + 2\langle M\rangle\cdot T_\text{t}\\
\end{align}$$
As well as the second moments:
$$\begin{align}
\langle F^2\rangle&=\sum_{E} F(E)^2\cdot p(E)\\
\langle M^2\rangle&=\sum_{E} F(E)^2\cdot p(E)\\
\langle T^2\rangle&=\sum_{E} T(E)^2\cdot p(E)\\
&=T_0^2+T_\text{f}^2\langle F^2\rangle + 4T_\text{t}^2\langle M^2\rangle+2T_0T_\text{f}\langle F\rangle+2T_\text{f}T_\text{t}\langle F\cdot M\rangle+2T_\text{t}T_0\langle M\rangle\\
\end{align}$$
Leading to standard deviation:
$$\begin{align}
\sigma_F^2&=\langle F^2\rangle-\langle F\rangle^2\\
\sigma_M^2&=\langle M^2\rangle-\langle M\rangle^2\\
\sigma_{FM}^2&=\langle F\cdot M\rangle-\langle F\rangle\langle M\rangle\\
\sigma_T^2&=\langle T^2\rangle-\langle T\rangle^2\\
&=T_0^2+T_\text{f}^2\langle F^2\rangle + 4T_\text{t}^2\langle M^2\rangle+2T_0T_\text{f}\langle F\rangle+2T_\text{f}T_\text{t}\langle F\cdot M\rangle+2T_\text{t}T_0\langle M\rangle\\
&-T_0^2-T_\text{f}^2\langle F\rangle^2 - 4T_\text{t}^2\langle M\rangle^2-2T_0T_\text{f}\langle F\rangle-2T_\text{f}T_\text{t}\langle F\rangle\langle M\rangle-2T_\text{t}T_0\langle M\rangle\\
\sigma_T^2&=(T_\text{f}^2)\sigma_F^2+(2T_\text{f}T_\text{t})\sigma_{FM}^2+ (4T_\text{t}^2)\sigma_M^2\\
\Aboxed{\sigma_T&=\sqrt{(T_\text{f}^2)\sigma_F^2+(2T_\text{f}T_\text{t})\sigma_{FM}^2+ (4T_\text{t}^2)\sigma_M^2}}
\end{align}$$
Notice: The standard deviation of time depends on both number of floors and the highest floor, but also the cross-correlation between them.


### Calculating by Random Sampling



| Params                    | Trials    | Result    |
| ------------------------- | --------- | --------- |
| $\langle F\rangle$        | 1,000,000 | 4.519028  |
| $\langle M\rangle$        | 1,000,000 | 5.202572  |
| $\langle F^2\rangle$      | 1,000,000 | 21.080626 |
| $\langle M^2\rangle$      | 1,000,000 | 27.79676  |
| $\langle F\cdot M\rangle$ | 1,000,000 | 23.955666 |
**Trial 1 Parameters**

| Params               | Simulated Value<br>(1mil Trials) |
| -------------------- | -------------------------------- |
| $\langle T\rangle$   | 101.810856                       |
| $\langle T^2\rangle$ | 10549.28748                      |
| $\sigma_T^2$         | 183.837081                       |
| $\sigma_T$           | 13.55865335                      |
**Trial 1 Times**
