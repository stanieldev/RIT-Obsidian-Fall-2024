### Introduction
In Tuesday’s class, we developed a predator-prey model that defined $X(t)$ to be the prey population at time $t$ and $Y(t)$ to be the predator population at time $t$ and relied on the following assumptions:
 - The per capita prey birth rate remains constant;
 - The per capita prey natural death rate remains constant;
 - The per capita prey death rate due to predation depends linearly on the predator population;
 - The per capita predator birth rate depends linearly on the availability of prey; and,
 - The per capita predator death rate is constant.

Once we determined the governing system of equations for the predator-prey model, subject to these assumptions, we determined the equilibrium solution, and then we investigated a particular case where the prey population was characterized by:
1. The production of 4 offspring per capita each 6 months;
2. A life expectancy of 2 years;
3. A preyed-upon death rate per year equals one animal per year for each predator and 100 prey animals; and where the predator population is characterized by:
4. A life expectancy of 5 years; and,
5. The equilibrium population for the prey is approximately 20 times the equilibrium population for the predators.

Our investigation involved plotting both populations versus time, generating phase plots of predator population versus prey population, and generating 3-dimensional plots showing the relationship between both populations and time.

### Instructions
Your task is to write and implement a predator-prey model in which both the predator and prey populations are susceptible to internal competition: Instead of a constant natural death rate, introduce a death rate that increases with the population size. Using the same
particular case described in (1)–(5), investigate the behavior of the populations according to this model, and comment on any similarities/differences you find with respect to the model we developed in class on Tuesday. You will need to choose some values for the new death rate coefficients - a good place to start is to choose values that are much smaller (like 100,000 times smaller) than the “natural” death rates.

By the deadline, you must each submit an individual executive summary (PDF format) of this new model. Your executive summary should include: a compartmental model diagram, list of assumptions, mathematical expressions describing each assumption, the governing system of equations, equilibrium solutions, and investigations of numerical solutions of the model in comparison/contrast with the model presented in class.

Similar to the executive summary you wrote for Module 2, you should create and write your report in a Google Doc using your @g.rit.edu email address. You should download your finalized report in PDF format and upload to MyCourses. Your report should explicitly provide an embedded link to the original Google Doc, so that I can access the Google Doc and view the version history.





### Formulation
Let the vector $\vec{S}(t)$ represent the configuration space of the predator and pray populations.
We can then write the evolution of the configuration state as:
$$\begin{align}
\dfrac{d\vec{S}}{dt}&=M_{2\times2}\cdot\vec{S}\\
\end{align}$$
For now, lets write out the specific components of $\vec{S}$:
$$\begin{align}
\dfrac{dX}{dt}&=AX(t)+kY(t)\\
\dfrac{dY}{dt}&=bX(t)+BY(t)\\
\end{align}$$
With the following parameters:
 - $A$ : The difference in per-capita birth rate and natural death rate of prey.
 - $B$ : The per-capita natural death rate of predators.
 - $k$ : The per-capita prey kill rate due to predation.
 - $b$ : The per-capita birth rate of predators.
Therefore, we can represent this in configuration space as:
$$\begin{align}
\dfrac{d\vec{S}}{dt}&=
\left[\begin{array}{cc}A&k\\b&B\end{array}\right]\vec{S}\\
\vec{S}&=e^{\left[\begin{array}{cc}A&k\\b&B\end{array}\right]t}\\
\end{align}$$






### Introducing Competition
$$\begin{align}
\dfrac{dX}{dt}&=(A-C)X(t)+kY(t)\\
\dfrac{dY}{dt}&=bX(t)+BY(t)\\
\end{align}$$









Investigate the following:
1. The production of 4 offspring per capita each 6 months;
2. A life expectancy of 2 years;
3. A preyed-upon death rate per year equals one animal per year for each predator and 100 prey animals; and where the predator population is characterized by:
4. A life expectancy of 5 years; and,
5. The equilibrium population for the prey is approximately 20 times the equilibrium population for the predators.