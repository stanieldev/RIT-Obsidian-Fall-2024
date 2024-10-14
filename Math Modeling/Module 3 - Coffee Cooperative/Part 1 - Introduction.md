**Name:** Stanley Goodwin
## Introduction
The problem we will study in this module is presented in Chapter 20: “Sustainability Analysis of a Rural Nicaraguan Coffee Cooperative” of (1). I’ve broken this problem into three parts: the first, which we will work on today, gives an introduction to the problem, asks you to do some fact-finding, and explores a simple model of profit. The second part extends the profit model to consider both fixed and variable costs for accommodating visitors at the coffee cooperative. The third part will focus on the problem of maximizing profit.

## Tasks
For each part of this module, you will work on a set of tasks. After all three tasks are complete, you will write a report about the tasks. During class, you can work in groups. After the class during which we complete Part 3, you will have approximately one week to submit an individual report via MyCourses. Requirements for the report will be provided with each task, and they will all be summarized at the end of the third task.

---
### Section 1
A series of websites about the Penas Blancas region of Nicaragua, and a series of YouTube videos about visits by mathematics students from Augsburg University in Minnesota to the GARBO Coffee Cooperative in Nicaragua, are provided on the MyCourses page for our class (under “Content”). Skim through these websites and videos with your group to do some fact-finding, and discuss the following questions:
#### 1.A)
*What intrigued you about the initial fact-finding?*
I'm not sure if it was mentioned in class or not, but I found how pretty recent the Penas Blancas Massif was founded. The year 1999, while 25 years ago, seems like I would have expected it around the 1980s or older.
I liked the song in The GARBO Coffee Collective. I was able to understand a bit above half of it.
Farmers from the region wanted to improve tourism to help with their economy.
#### 1.B)
*What do you want to know more about?*
I loved the list of animals and trails that were mentioned on the website, but I didn't see all that much about the plant life and ecosystem other than a few mentions of weather.
#### 1.C)
*If you were promoting travel to this region, what would you mention?*
I would probably mention the reasonably warm weather, temperate climate, local wildlife like animals or plants, and the natural beauty of the region. Maybe the kinds of coffee they grow and how they see their crop.
#### 1.D)
*What amenities would you want this region to have?*
I would definitely like food, water, indoor plumbing, and some form of air conditioning.

---
### Section 2
A basic model for profit production P (units: dollars per day) is the following, $P=p\cdot v-C$, where we have the following variables:
 - P = Daily profit ($ / day),  
 - R = Daily revenue ($ / day),  
 - p = Visitor charge ($ / visitor) to stay at the cooperative,  
 - v = The number of daily visitors (visitors / day),  
 - C = The cost to the cooperative ($ / day) to accommodate visitors. 
#### 2.A
Let’s say the daily rate for the cooperative is $20 per person, and it costs $75 per day for upkeep. *What is the profit if the cooperative has five visitors? What about one visitor? How would you interpret these results?*
$$\begin{align}
P(v)&=p\cdot v - C\\
P(5)&=5(\$20) - \$75=\$25\\
P(1)&=(\$20) - \$75=-\$55\\
\end{align}$$
The amount of visitors per day, on average, must be $3.75$ visitors, in order to cover the costs of operation. We can reasonably say that the cooperative should try to get at least 4 visitors a day so that they are, at minimum, net positive.
#### 2.B
Instead of focusing on specific values, examine equation (1) to determine an expression for the basic minimum price for the cooperative to be profitable. *If the number of visitors v and the cost C change in value, what does increasing or decreasing both of them do to the minimum price?*
$$\begin{align}
0&=p\cdot v - C\\
\Aboxed{v_\text{min}&=\dfrac{C}{p}}
\end{align}$$
We can observe the following relationships:
$$\begin{align}
v_\text{min}&\propto C & v_\text{min}&\propto\dfrac{1}{p}\\
\end{align}$$
Therefore, the minimum number of visitors to remain profitable is linearly proportional to the fixed operation costs and inversely proportional to the cost per visitor.
#### 2.C
Related to the last point, examine equation (1) to determine the minimum number of visitors for the cooperative to be profitable. *If both the price p and the cost C change in value, what does increasing or decreasing both of them do to the required minimum number of visitors?*

If both $C$ and $p$ increase in the same order with the same coefficient, then the minimum number of visitors remains unchanged. If they are of the same order, but differing coefficients, then $v_\text{new}=\dfrac{A_c}{A_p}\cdot v_\text{old}$.
#### 2.D
Assuming the price charged to each of the visitors is fixed, discuss with your group some strategies that the cooperative can pursue to potentially boost profit. Make sure to come up with at least three strategies. Evaluate the three strategies on their merit, and determine appropriate data and metrics in your evaluation. With your group, decide on the optimal strategy that you would recommend moving ahead with. Provide justification in your report to the cooperative.

1. More advertising of the cooperative. Having more people know about this opportunity increases the chances of another visitor.
2. Reducing costs per visitor on average, whether it be buying in bulk, decreasing amenities, or by getting better deals on goods.
3. Seeking out financial aid from their local ordinance/government, either by loans or grants.

I didn't discuss with my group since they were busy doing their own work and I didn't want to bother them.

---
### References  
(1) Gizem Karaali and Lily S Khadjavi. Mathematics for Social Justice: Resources for the College Classroom. Vol. 60. American Mathematical Soc., 2019.