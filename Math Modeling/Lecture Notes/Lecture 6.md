**Name:** Stanley Goodwin
**Date:** 9/12/2024

---
### Building a Simple Model for the Elevator Problem
$$\begin{align}
T_\text{ground} &=25\text{s}&&\text{Time doors are open on Floor 0.}\\
T_\text{floor} &=15\text{s}&&\text{Time doors are open on Floor > 0.} \\
T_\text{travel} &= 5\text{s}&&\text{Time it takes to travel between floors.}\\
N_\text{floors} &= 5&&\text{The number of floors of the building above ground.}\\
C_\text{} &= 10 &&\text{Max Capacity of a singular Elevator.}\\
N_\text{elevators} &= 3 &&\text{Number of elevators in the building.}
\end{align}$$

1) What is the (worst case) time for a single trip?
$$\begin{align}
T_\text{roundtrip}&=T_\text{ground}+N_\text{floors}T_\text{floor}+2N_\text{floors}T_\text{travel}\\
&= \left(25+(5)(15)+2(5)(5)\right)\mathrm{s}\\
&= \left(25+75+50\right)\mathrm{s}\\
\Aboxed{T_\text{roundtrip}&= 150\mathrm{s} = 2.5\mathrm{min}}
\end{align}$$

2) What is the total time required to deliver 300 employees to their floors.

Worst case, every elevator stops at all 5 floors.
$$\begin{align}
N_\text{trips}&=\dfrac{300}{CN_\text{elevator}}=\dfrac{300}{10\cdot3}=10\text{ Trips}\\
T_\text{worst}&=(N_\text{trips}-1)T_\text{roundtrip} + T_\text{halftrip}\\
&=(9)(150\mathrm{s}) + 125\mathrm{s}\\
\Aboxed{T_\text{worst}&= 1475\mathrm{s}=24\mathrm{min}+35\mathrm{s}}
\end{align}$$

3) In the worst case, how much time is being spent delivering employees to their floors after 9:00am?

Given: 60 people arrive late to their office.
$$\begin{align}
N_\text{trips}&=\dfrac{60}{CN_\text{elevator}}=\dfrac{60}{10\cdot3}=2\text{ Trips}\\
T_\text{worst}&=(N_\text{trips}-1)T_\text{roundtrip} + T_\text{halftrip}\\
&=150\mathrm{s} + 125\mathrm{s}\\
\Aboxed{T_\text{worst}&= 275\mathrm{s}=4\mathrm{min}+35\mathrm{s}}
\end{align}$$
This means that they started taking the elevator at 8:40am.


4) Can we propose a solution that will deliver all 300 employees to their floors in under 20min?
   Think of potential strategies for reducing total time of elevator travels to subset of floors.


**Strategy I:**    Let Elevators A & B go to floors 1-3, and Elevator C go to floors 4-5.
$$\begin{align}
N_\text{A\&B}&=\dfrac{60\%\cdot 300}{2\cdot10} = 9\text{ Trips}\\
N_\text{C}&=\dfrac{40\%\cdot 300}{1\cdot10} = 12\text{ Trips}\\
T_\text{A\&B}&= (8)(100\mathrm{s})+85\mathrm{s} = 885\mathrm{s}\\
T_\text{C}&= (11)(105\mathrm{s})+80\mathrm{s} = 1235\mathrm{s}
\end{align}$$
Since $\max(T_\text{A\&B}, T_\text{C}) > 1200\mathrm{s}$, Strategy I would ***not*** be a viable strategy for 0 late employees.


**Strategy II:**   Let Elevator A go to floors 1-2, and Elevators B & C go to floors 3-5.
$$\begin{align}
N_\text{A}&=\dfrac{40\%\cdot 300}{2\cdot10} = 12\text{ Trips}\\
N_\text{B\&C}&=\dfrac{60\%\cdot 300}{2\cdot10} = 9\text{ Trips}\\
T_\text{A}&= (11)(75\mathrm{s})+65\mathrm{s} = 890\mathrm{s}\\
T_\text{B\&C}&= (8)(120\mathrm{s})+95\mathrm{s} = 1055\mathrm{s}
\end{align}$$
Since $\max(T_\text{A\&B}, T_\text{C}) \le 1200\mathrm{s}$, Strategy I ***would*** be a successful strategy for 0 late employees.

