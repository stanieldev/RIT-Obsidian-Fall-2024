**Name:** Stanley Goodwin
## Tasks
For each part of this module, you will work on a set of tasks. After all three tasks are complete, you will write a report about the tasks. During class, you can work in groups. After the class during which we complete Part 3, you will have approximately one week to submit an individual report via MyCourses. Requirements for the report will be provided with each task, and they will all be summarized at the end of the third task.

In this part of the module we will revisit the basic profit model, using key aspects of how the profit is defined. As a reminder, the basic model for profit $P$ (units: dollars per day) is,
$$P=R-C=p\cdot v-C$$
where we have the following variables:
 - P = Daily profit ($ / day),  
 - R = Daily revenue ($ / day),  
 - p = Visitor charge ($ / visitor) to stay at the cooperative,  
 - v = The number of daily visitors (visitors / day),
 - C = the cost to the cooperative ($ / day) to accommodate visitors.

### Section 1
The currency in Nicaragua is the cordoba. *Identify the current conversion between United States dollars and the Nicaraguan cordoba.* 
**Note:** We will now write all the currency units in Nicaraguan cordobas, so knowing this conversion will be helpful to think about your results in a familiar currency.
$$\$1.00\text{ (USD)} = \text{C}\$36.84 \text{ (NIO)} \ \ \ \ \ \text{(As of 10/9/2024)}$$
### Section 2
*With your group, estimate the daily cost to accommodate visitors using the information provided.*
**Note:** Use the Nicaraguan cordoba as the monetary unit. It might be helpful to plan out a typical meal requirement for a given guest and to create an itemized list. Feel free to include items you may think are important but are not listed, and provide a reasonable estimate on the price (with justification!). Justify your reasoning in determining the items that would be important.

| Item           | Cost           | Notes                       |
| -------------- | -------------- | --------------------------- |
| Rice           | C$16 / lb      | 1 lb -> 6 People            |
| Beans          | C$14 / lb      | 1 lb -> 6 People            |
| Oil            | C$30 / 0.25L   | Used for Cooking            |
| Tortillas      | C$3 / 10       |                             |
| Chicken        | C$200 /hen     |                             |
| Eggs           | C$5 / egg      |                             |
| Mango          | C$16           |                             |
| Watermelon     | C$160          |                             |
| Cantelope      | C$70           |                             |
| Bread          | C$50 / loaf    |                             |
| Pasta          | C$15           | 1 lb -> 6 People            |
| Sugar          | C$15 / lb      |                             |
| Cheese         | C$40 / lb      |                             |
| Coffee         |                |                             |
| Purified Water | C$30 / 0.5L    | Used for Cooking & Drinking |
| Toilet Paper   | C$18 / roll    |                             |
| Napkins        | C$60 / package | 60 per Package              |
| Candles        | C$3 / candle   | 1.5 hours / candle of light |
| Body Soap      | C$20 / bar     |                             |
| Laundry Soap   | C$26 / load    |                             |
| Matches        | C$2 / box      |                             |
| Batteries      | C$40 / battery |                             |
**Table 1:** Table of item prices in Rural Nicaragua.

### Section 3
Go back to the itemized list you made. Identify costs that would be:
#### 3.A) Visitor-Dependent
| Item           | Cost           | Notes                       |
| -------------- | -------------- | --------------------------- |
| Rice           | C$16 / lb      | 1 lb -> 6 People            |
| Beans          | C$14 / lb      | 1 lb -> 6 People            |
| Oil            | C$30 / 0.25L   | Used for Cooking            |
| Tortillas      | C$3 / 10       |                             |
| Chicken        | C$200 /hen     |                             |
| Eggs           | C$5 / egg      |                             |
| Mango          | C$16           |                             |
| Watermelon     | C$160          |                             |
| Cantelope      | C$70           |                             |
| Bread          | C$50 / loaf    |                             |
| Pasta          | C$15           | 1 lb -> 6 People            |
| Sugar          | C$15 / lb      |                             |
| Cheese         | C$40 / lb      |                             |
| Purified Water | C$30 / 0.5L    | Used for Cooking & Drinking |
| Toilet Paper   | C$18 / roll    |                             |
| Napkins        | C$60 / package | 60 per Package              |
| Body Soap      | C$20 / bar     |                             |
| Laundry Soap   | C$26 / load    |                             |
**Table 2:** Table of visitor-dependent items.


#### 3.B) Visitor-Independent
| Item         | Cost           | Notes                       |
| ------------ | -------------- | --------------------------- |
| Coffee       | Labor          |                             |
| Candles      | C$3 / candle   | 1.5 hours / candle of light |
**Table 3:** Table of visitor-dependent items.

### Section 4
*Assuming the values of $p$, $k$, and $C$ are known, what is an algebraic expression for the minimum number of visitors needed for the cooperative to be profitable? How does changing the parameters $p$, $k$, and $C$ affect the number of visitors?*

Given $P=p\cdot v-k\cdot v-C$, we can find the minimum number of visitors as:
$$\begin{align}
0&=p\cdot v-k\cdot v-C\\
\Aboxed{v_\text{min}&=\dfrac{C}{p-k}}
\end{align}$$
We can observe the following relationships:
$$\begin{align}
v_\text{min}&\propto C & v_\text{min}&\propto\dfrac{1}{p-k}\\
\end{align}$$
Therefore, the minimum number of visitors to remain profitable is linearly proportional to the operation costs and inversely proportional to the cost *total* per visitor (sum of fixed and variable).

### Section 5
Examine your algebraic expression from the last problem.
*What is a necessary condition for the value of p?*

To make sure the number of visitors is always positive, and doesn't have a singularity:
$$\begin{align}
(p-k\ge0)\wedge(p-k\ne0) \implies \boxed{p\gt k}\\
\end{align}$$
The cost per person must always be larger than the cost per person, which makes sense since we want to make a profit on the collective, not lose profit.

### Section 6
*Based on your itemized lists of fixed and variable costs, estimate $C$.*
**Note:** As you can imagine, the value of the parameter $C$ depends on which items you focused on in the table as visitor-dependent. Provide justification for your reasoning.

For light, electricity, and general power requirements, it would probably only cost about $C\approx\text{C\$}20$, chosen not only from the table but purposely about the cost of 1 visitor so that we can simplify the model easier.

### Section 7
*Based on your itemized lists of fixed and variable costs, estimate $k$ (with justification).* 
**Note:** To determine $k$, it might be useful to take an accounting of the per item cost of goods, estimate the number of items that each visitor would use (for every day or for a visit), and then multiply the two values together. From that work determine if a summative or an average cost per visitor is worthwhile.

Based on this information, we can refine our basic model to the following:  
I used the website [[https://www.numbeo.com/cost-of-living/in/Matagalpa-Nicaragua?displayCurrency=NIO|Numbeo]] to estimate the costs over about a week.

For visitors, it looks to be about ~C$140/week, incorporating food, water, transportation, general amenities (short-time utilities), with this estimate being about middle of the road, so there would be fluctuation over time.

Since visitors are only there for a day:
$k\approx\text{C\$}20/\text{visitor}$.

### Section 8
*Now that you have determined $C$ and $k$, what is a necessary condition for $p$? Would that price $p$ be reasonable for visitors to the cooperative?*
$k\approx\text{C\$}20/\text{visitor}$.
$C\approx\text{C\$}20$.
$$\begin{align}
\boxed{p\gt 20/\text{visitor}}\\
\end{align}$$
This is the bare minimum estimate that avoids the fixed cost per day.
$$\begin{align}
p&\gt\dfrac{C}{v_\text{min}}+k\\
\end{align}$$
This includes the fixed cost, and so is a better metric for the constraint on $p$.

### Section 9
*A recommendation from an external group is to give a daily wage to each family in the cooperative to offset the cost of receiving visitors. The wage should incorporate the fixed cost used to accommodate guests and also any (human) time spent in the receiving of guests. If the cooperative will implement this plan, what type of information would be useful in setting a wage?*

Using a table like numbeo's for Matagalpa to estimate the costs of the families there.
The average amount of people per family would also make a difference, since more children means more mouths to feed and childcare.

*What would be the wage you would recommend? Based on your investigations, determine how this wage will affect $p$, the price they charge to visitors. Would that price $p$ be reasonable for visitors to the cooperative?*

I found that, if you live conservatively and frugally, the cost of living looks to be about C$1500 - C$2000 per month for a family of 4. Given that the costs of operations are about C$20 per day, over 30 days, is an extra C$600.

Also, for the sake of the calculation, we'll assume an average of 4 visitors a day.

Based on this information, I think that a singular family of the cooperative should charge:
$$\begin{align}
p&\ge30\cdot\dfrac{C}{v_\text{month}}+k\\
&\ge\dfrac{30\cdot\text{C\$}20}{30\cdot 4\text{ visitor}}+\text{C\$}20/\text{visitor}\\
\Aboxed{p&\ge\text{C\$}25/\text{visitor}}
\end{align}$$


