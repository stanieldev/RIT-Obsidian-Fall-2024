**Date 9/17/2024**

### Model Parameter Space
Given the set of parameters here:
$$\begin{align}
T_\text{0}&=15\mathrm{s} &\text{The time the elevator is open on the ground floor.}\\
T_\text{F}&=10\mathrm{s}\ &\text{The time the door is open on non-ground floors.} \\
T_\text{t}&=4\ \mathrm{s}/\text{Floor}\ &\text{The time the elevator takes to travel between floors.}\\
N_\text{F}&=6\text{ Floors}\ &\text{The number of floors of the building above the ground floor.}\\
N_\text{E}&=3\text{ Elevators}\ &\text{Number of elevators in the building.}\\
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


### Equipartition of States
There are 3 characteristics of time we can determine from a bit of thinking:
1. $T_0$ is minimized if the elevator is always full.
2. $T_\mathrm{F}$ is minimized if the elevators have as few different floors as possible.
3. $T_\mathrm{t}$ is minimized if the elevators have adjacent floors.

We also know that the elevator that takes the longest ends up being the total time for everyone, since we're looking at the maximum time of all 3 elevators. This implies that the optimal strategy must be the set of elevators that have identical times between all 3.

Suppose we look at 3 different places in the total list of employees:
 - The first employee, traveling to the first floor.
 - The median employee, traveling to a middle floor.
 - The last employee, traveling to the top floor.

The way to solve this system is to consider the following worst case scenarios:
 - Elevator 1: Takes the first $N_1$ employees, starting from floor 1.
 - Elevator 2: Takes the middle $N_2$ employees.
 - Elevator 3: Takes the last $N_3$ employees, starting from floor 6.
Something of note is that $N_1+N_2+N_3$ must be equal to the total number of employees.

### Elevator 1
We can calculate the expected time travelled with the following approximation:
 - The average number of floors can be written exactly as $\displaystyle\sum_kk\dfrac{n_k}{N_1}$.
 - The average max floor can be written exactly as $\displaystyle\sum_kk\cdot p(k)$.
We can write the average time as the following:
$$\begin{align}
\langle T\rangle&=T_0+\langle F\rangle\cdot T_\text{f} + 2\langle M\rangle\cdot T_\text{t}\\
\sigma_{\langle T\rangle}&=\sqrt{(T_\text{f}^2)\sigma_F^2+(2T_\text{f}T_\text{t})\sigma_{FM}^2+ (4T_\text{t}^2)\sigma_M^2}
\end{align}$$
Which means that we can show the total time is:
$$\begin{align}
T&=\left\lceil\dfrac{N_1}{C_\mathrm{E}}\right\rceil\left(T_0+\langle F\rangle\cdot T_\text{f} + 2\langle M\rangle\cdot T_\text{t}\right)\\
\sigma_T&=\left\lceil\dfrac{N_1}{C_\mathrm{E}}\right\rceil\sqrt{(T_\text{f}^2)\sigma_F^2+(2T_\text{f}T_\text{t})\sigma_{FM}^2+ (4T_\text{t}^2)\sigma_M^2}
\end{align}$$



$$\begin{align}
E_1&=\left[80,80,31,\ 0\ ,\ 0\ ,\ 0\ \right] & N_1&=191\\
E_3&=\left[\ 0\ ,\ 0\ ,\ 9\ ,80,20,20\right] & N_3&=129\\
\end{align}$$
$$T=1308\mathrm{s}=21\mathrm{m},48\mathrm{s}$$

| Trial      | Type | $\langle T\rangle$ | $\dfrac{N_\text{employees}}{N_\text{E}\cdot C_\text{E}}\langle T\rangle$ | Min, Sec                   |
| ---------- | ---- | ------------------ | ------------------------------------------------------------------------ | -------------------------- |
| A (1mil)   | Sim  | 101.810856         | 1,629$\mathrm{s}$                                                        | $27\mathrm{m},9\mathrm{s}$ |
| B (480mil) | Sim  | 101.852417         | 1630$\mathrm{s}$                                                         | $27\mathrm{m},9\mathrm{s}$ |
