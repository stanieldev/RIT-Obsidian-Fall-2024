
## Introduction
*For Part 2 of this module, you will work in groups to address the questions below. After class, you will have one week to submit individual solutions to these questions via MyCourses. All submissions should be typeset (no hand-written answers), and all answers should be written as complete sentences with correct grammar. (Answers that are not complete sentences will receive a 50% deduction.)*

## Interest Modeling
*Imagine the following scenario. Nate attended a private four-year college between 1993-1997. Catherine is planning to enroll in a private four-year college from 2025-2029. Nate had to borrow 50% of the tuition, and Catherine will have to borrow 50% of the tuition.*

### Nate and Catherine
|                        | Nate       | Catherine  |
| ---------------------- | ---------- | ---------- |
| Average Annual Tuition | $24,333.00 | $47,713.38 |
| Loan Amount            | $12,161.50 | $23,856.69 |
| Loan Term              | 10 years   | 10 years   |
| Annual Interest Rate   | 7.39%      | 4.99%      |
| Monthly Payment        | $211.72    | $327.11    |
| Total Interest Paid    | $13,278.50 | $15,396.40 |
| Cumulative Payments    | TODO       | TODO       |
**Table 1: The case of Nate and Catherine.**


1. *Fill in Table 1. (A version of this table is in the supplemental spreadsheet “InterestTables.xlsx” for you to use in your typeset homework submission.) Use the data file available on MyCourses that corresponds to the article “Trends in College Pricing and Student Aid 2023” (1) to determine Nate’s tuition, and use the polynomial model you found in Part 1 to estimate Catherine’s tuition.*

For my calculation of the future tuition rates, I ended up using the linear approximation, since it was the median of the 3 models calculations. While is it a little less fitting than the others, I feel that the linear trend has more room to cancel out fluctuations more than x² or x³.

For interest payments, I used a monthly model of compound interest. We had found, in class, the most amount of interest is paid with compound interest, compounding as often as possible.
It's quite common that monthly payments are the main method of college loans, according to my sister who works in Financial Aid for another college.
I also inferred that the table was trying to tell me it was month compound interest.

Equations I used:
$$\begin{align}
R(t_\text{years})&=P_0\left(1+\dfrac{\text{APR}}{12}\right)^{12t} -p\cdot12t &\implies& &R(t_\text{months})&=P_0\left(1+\dfrac{\text{APR}}{12}\right)^{t} -pt\\
T(t_\text{years})&=P_0\left(1+\dfrac{\text{APR}}{12}\right)^{12t} &\implies& &T(t_\text{months})&=P_0\left(1+\dfrac{\text{APR}}{12}\right)^{t}\\
I(t_\text{years})&=P_0\left(1+\dfrac{\text{APR}}{12}\right)^{12t}-P_0 &\implies& &I(t_\text{months})&=P_0\left(1+\dfrac{\text{APR}}{12}\right)^{t}-P_0\\
\end{align}$$
Where $p$ is the payment per month, $P_0$ is the principle, $R(t)$ is remaining balance, $T(t)$ is total balance before payment, and $I(t)$ is the surplus (interest) on top of the principle.


2. *In referring to Nate and Catherine, who pays less in interest and by how much?*

Overall, it seems that Nate paid less in interest than Catherine, over the term of their loan.
Catherine paid a surplus of $2,117.90 in interest relative to Nate.


3. *After repaying their loans, what are the cumulative payments of Nate and Catherine?*

TODO


4. *In reference to the previous question, is this result in line with or contradictory to the interest rate each borrow got?*

With the interest rate of Catherine's loan being smaller than Nate's, it would have been reasonable to assume that Catherine would pay less over time, but instead what we saw is that the larger loan ended up costing Catherine more in interest than Nate.



*Now imagine the following scenario. Catherine and Henry attend a four-year private college concurrently from 2025-2029, and both borrow 50% of tuition. However, Henry receives a lower interest rate on his loan.*

### Catherine & Henry
|                        | Catherine  | Henry      |
| ---------------------- | ---------- | ---------- |
| Average Annual Tuition | $47,713.38 | $47,713.38 |
| Loan Amount            | $23,856.69 | $23,856.69 |
| Loan Term              | 10 years   | 10 years   |
| Annual Interest Rate   | 4.99%      | 2.69%      |
| Monthly Payment        | $327.11    | $260.09    |
| Total Interest Paid    | $15,396.40 | $7,351.11  |
| Cumulative Payments    | TODO       | TODO       |
**Table 2: The case of Catherine and Henry.**


5. *Fill in Table 2. (A version of this table is also in the supplemental spread-*
*sheet “InterestTables.xlsx”.)*

Complete!


6. *How much does Henry save in interest compared with Catherine?* 

During the 10-year payment of the loan, Henry saved about $8,042.30 in interest compared to Catherine.


7. *Is the amount significant?*

I argue that ~$8,000 is significant in this case, since, between Henry's loans and Catherine's loans, the amount that Henry would have to pay in comparison is +109.4% of his interest.
About half the interest cost was saved with a lower interest rate, and so that amount is very much significant.




## References
(1) Jennifer Ma and Matea Pender. Trends in college pricing and student aid 2023. https://research.collegeboard.org/trends/college-pricing. 2023.