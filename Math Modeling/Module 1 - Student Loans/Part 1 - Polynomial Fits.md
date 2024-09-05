### Introduction
The problem we will study in this module is presented in Chapter 18: “Student Loans: Fulfilling the American Dream or Surviving a Financial Nightmare?” (1). 
I’ve broken this problem into three parts: 
1. Explores the use of polynomial models to fit data. 
2. Explore models of interest that we will use to construct loan payment “calculators.” 
3. Incorporate aspects of President Biden’s recent Student Loan Relief plan (3, 4) to update our predictions of the cost of college for a fictitious student. 

### Tasks
For Part 1 of this module, we will be referring to the article “Trends in College Pricing and Student Aid 2023” (2) and the corresponding data file that are both available on MyCourses.

All submissions should be typeset (no handwritten answers), and all answers should be written as complete sentences with correct grammar. 
(Answers that are not complete sentences will receive a 50% deduction.)

1. Using the data in Table CP-2 “Average Tuition and Fees and Housing and Food (Enrollment-Weighted) in Current Dollars and in 2023 Dollars, 1971-72 to 2023-24,”
	1. Create three separate graphs that show the tuition and fees for (a) private non-profit four-year colleges, (b) public four-year colleges, and (c) public two-year colleges, starting from the academic year 1973-74 as year 0, and going in five-year intervals. 
	2. Each graph should show tuition and fees in 2023 dollars, and each graph should have a title or caption, as well as labels for the horizontal and vertical axes.

**Figure A:** ![[q1_private.png]]
**Figure B:** ![[q1_public_2.png]]
**Figure C:** ![[q1_public_4.png]]



2. For the data in each of the three graphs, fit the data to a polynomial function. Explore different degrees of polynomials, and choose the degree that you think “best” represents the data. (The degree you choose can be different for each of the three graphs.) Create three additional graphs that show the chosen polynomial models with the data. 



I noticed that Graph A, Private Nonprofit Colleges, look to have increased their tuition closer to linear growth instead of exponential growth. Not sure why this is the case, but perhaps it has to do with how the government started subsidizing universities.

**Figure A:** ![[q2_private.png]]

|          | Linear Fit | Quadratic Fit | Cubic Fit |
| -------- | ---------- | ------------- | --------- |
| $\chi^2$ |            |               |           |
| $r^2$    |            |               |           |




Using least squares, I found a regression: $A(x-1971)^p + C$.
$$T(x)=(274.20)(x-1971)^{1.23} + 11461.88$$
There are a lot of fit statistics that got printed with LMFIT, but I listed some:
$\chi^2 = 2172501.93$, $r^2=98.21\%$.

**Figure B:** ![[q2_public_4.png]]
Using least squares, I found a regression: $A(x-1971)^p + C$.
$$T(x)=(19.03)(x-1971)^{1.61} + 2713.42$$
There are a lot of fit statistics that got printed with LMFIT, but I listed some:
$\chi^2 = 540912.098$, $r^2=95.69\%$.

**Figure C:** ![[q2_public_2.png]]
Using least squares, I found a regression: $A(x-1971)^p + C$.
$$T(x)=(24.33)(x-1971)^{1.25} + 1335.86$$
There are a lot of fit statistics that got printed with LMFIT, but I listed some:
$\chi^2 = 59448.92$, $r^2=94.89\%$.



3. What is the common trend for the three graphs? 

A common trend among the 3 graphs is that tuition increases *super-linearly*, I.e. a power $p>1$.
They all also seem to have a spike around 1973, and a dip at about COVID times.



4. What is the domain and range of each of your chosen polynomial models? 

I chose the domain to be $x\in\left[1971,2023\right]$.
The range tends to overshoot the data, probably because of COVID-19, but it tends to be:
$T(x)\in\left[\$1335.86, \$47000\right]$.
If we wanted the individual ranges, we would find that: $T_n(x)\in\left[T_n(1971), T_n(2023)\right]$.



5. Use your polynomial models to predict the tuition and fees for a student entering each type of institution in the academic year 2028-29. Comment on whether or not you think the predictions are reasonable.

#### Predicted Costs in 2028
Private 4-Year : $\$50869.82$
Public 4-Year : $\$15488.30$
Public 2-Year : $\$5124.94$

I think these predictions would be more valid if COVID-19 didn't occur, since there was a sharp decrease in tuition during that time.
I believe these are overestimates of future tuition costs, but they aren't overly outlandish.



6. List the properties of polynomial functions, and explain the advantages for using them in modeling. 

I misunderstood the statement "Explore different degrees of polynomials, and choose the degree that you think “best” represents the data." to mean that you wanted me to find what degree $p$ best fits the data. I apologize, but since I have already done all the modeling and math with this assumption, I *really* don't want to redo it for higher-degree polynomials.

Polynomials are convenient for finding the different weights for individual degrees of growth, whether it be constant, linear, or quadratic (and above).

The calculation for future values, as well as derivatives, are also much easier to compute, but realistically they're no more useful than most other kinds of regressions.



7. From the graphs you generated, explain the limitations of polynomial fitting. Specify at least three limitations and consider the values of the polynomial as time increases. 

A limitation with polynomials is that truncation of polynomials can lead to larger variances for times much larger than the domain it was defined on, since finances usually grow in some form of exponentials.

IF the true model grows as something that is non-convergent over a larger domain than the source domain, then something like the Taylor series of ln(1+x) occurs, where the function diverges toward infinity differently than a polynomial would.

I've found as well, in my experience, that polynomials have an odd behavior at critical points, or places where a continuous function diverges because of the polynomial arbitrarily at $t_0$, because it wasn't an initial condition that the function has to pass through. This occurred more-so in physics, but I believe it could be a constraint here as well.



8. When do you think that polynomial modeling works best? 

Polynomial modeling works best for when the source model is likely to be a finite-degree polynomial, or that its rate of change is some known polynomial as well.

With finances, it is known that the rate of inflation tends to be exponential, and so a perfect world where tuition increases directly with inflation would also be exponential.
With diminishing returns, it is known that the rate is of some form of logarithmic.

Is it bad to assume a polynomial when there is no external justification for it, especially when the true function is some form of exponential, hyperbolic, or logarithmic.

### References
1. Gizem Karaali and Lily S Khadjavi. Mathematics for Social Justice: Resources for the College Classroom. Vol. 60. American Mathematical Soc., 2019.
2. Jennifer Ma and Matea Pender. Trends in college pricing and student aid 2023. https://research.collegeboard.org/trends/college-pricing. 2023.
3. Biden-Harris Administration Approves Additional $1.2 Billion in Student Debt Relief for 35,000 Public Service Workers. https : / / www . ed . gov / news / press - releases / biden - harris - administration - approves - additional-12-billion-student-debt-relief-35000-public-serviceworkers. Accessed: 2024-08-26.
4. FACT SHEET: President Biden Announces Student Loan Relief for Borrowers Who Need It Most. https : / / www . whitehouse . gov / briefing - room / statements - releases / 2022 / 08 / 24 / fact - sheet - president - biden- announces- student- loan- relief- for- borrowers- who- needit-most/. Accessed: 2022-08-30.









