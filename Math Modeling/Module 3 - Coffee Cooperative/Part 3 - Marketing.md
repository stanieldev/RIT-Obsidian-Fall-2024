**Name:** Stanley Goodwin
## Tasks
For each part of this module, you will work on a set of tasks. After all three tasks are complete, you will write a report about the tasks. During class, you can work in groups. After the class during which we complete Part 3, you will have approximately one week to submit an individual report via MyCourses. Requirements for the report will be provided with each task, and they will all be summarized at the end of the third task. 

In this final part of the module we will help the cooperative determine how to market themselves to attract about 15-20 visitors per day in order to maximize their profit. In order to do this, we are going to examine reported data from Google. The website that we will be using is Google Trends, a data analytics site that allows you to explore aggregated search data from across the world.

### Section 1-5
 - A plot should be generated highlighting the relative interest (scaled between 0 to 100) in this search term over time. The data are scaled in this way so searches in countries with more active internet users would not dominate the results.
 - You might have to try a few different terms in order to get some data. Record terms that were useful and not as useful.
 - For the purposes of this project, we are going to limit the results to one year. To do that, click on “select time range” and limit it to one complete calendar year.

| Search Term                      | Result        |
| -------------------------------- | ------------- |
| "Vacation to South America"      | Pretty useful |
| "Winter retreat"                 | Pretty useful |
| "Vacation with coffee"           | Meh           |
| "South America vacation"         | Pretty useful |
| "Hiking Trails in South America" | Not useful    |
| "South America travel"           | Pretty useful |
| "South America travel guide"     | Not useful    |
**Table 1:** Search term table over the last 12 months in the United States.

### Section 6
6. Now let’s download the data. At the top right of the webpage, you should see a download icon allowing you to download the data as a comma-separated values (CSV) file. Save this CSV file and open it. When you open up this file in a spreadsheet program, the first few lines provide information about the web search. Starting a few lines later are the “interest” data graphed on the webpage. Notice that in column “A” there is a time stamp corresponding to the weeks. We will rewrite this as weeks of the year. 

### Section 7-8
7. Now create a scatter plot for the Interest data over the course of the year. You will want to select the column of the weeks of the year and the interest. Make a scatter plot of the data.  
8. Title your chart and axes appropriately.  
![[Search Queries since Oct 8th.png]]
I know the question said to use a scatter plot, but it was pretty hard to read with all the points, so I used a smooth-connected line graph instead.
Also I wasn't able to add a y-axis label for some reason, but it's "relative frequency".

### Section 9
9. Let’s try to fit different function families to these data. We will let $I$ represent the interest in your search term and t represent the weeks since January 1, so you are determining a functional form $I(t)$. For each of the function families listed below, fit a curve through the data, and for each one, record how good your model is in representing the data:  
#### 9.A) Linear regression
![[Search Queries since Oct 8th (Linear).png]]
#### 9.B) quadratic regression
![[Search Queries since Oct 8th (Quadratic).png]]
#### 9.C) cubic regression
![[Search Queries since Oct 8th (Cubic).png]]
#### 9.D) exponential regression
![[Search Queries since Oct 8th (Exponential).png]]
#### 9.E) logarithmic regression
![[Search Queries since Oct 8th (Logarithmic).png]]

### Section 10
10. If one was to try to fit a curve that represented the data the best, which function family would you choose and why?  

The best fit is definitely the cubic regression, which makes sense since we'd expect the true distribution to be some form of sinusoidal function. In the Taylor series, this is the next order of the sine wave.

Overall I'd expect that it's periodic, since I believe it would mostly identical every year.

### Section 11
11. With the modeled function that you chose, now use your calculus knowledge to determine the following:
$$\begin{align}
y_1(x)&=+40.5-0.219x+0.0272x^2-0.000575x^3\\
y_2(x)&=+51.8+4.410x-0.3110x^2-0.004400x^3\\
y_3(x)&=-5.86+3.960x-0.2090x^2-0.002940x^3\\
y_4(x)&=+64.5+0.991x-0.0458x^2-0.000516x^3\\
y_5(x)&=+62.2+3.360x-0.1710x^2-0.002120x^3\\
\end{align}$$#### 11.A)
Intervals where I(t) is increasing.
$$\begin{align}
-0.219+0.0544x-0.001725x^2&>0&\implies&&x\in\left(4.74,26.80\right)\\
4.410-0.6220x-0.013200x^2&>0&\implies&&x\in\left[0.00, \ \ 4.41\right)\\
3.960-0.4180x-0.008820x^2&>0&\implies&&x\in\left[0.00, \ \ 8.09\right)\\
0.991-0.0916x-0.001548x^2&>0&\implies&&x\in\left[0.00, \ \ 9.34\right)\\
3.360-0.3420x-0.006360x^2&>0&\implies&&x\in\left[0.00, \ \ 8.49\right)\\
\end{align}$$
#### 11.B)
Intervals where I(t) is decreasing.
$$\begin{align}
-0.219+0.0544x-0.001725x^2&<0&\implies&&x\in\left[0,4.74\right)\cup\left(26.80, 53\right]\\
4.410-0.6220x-0.013200x^2&<0&\implies&&x\in\left(4.41,53\right]\\
3.960-0.4180x-0.008820x^2&<0&\implies&&x\in\left(8.09,53\right]\\
0.991-0.0916x-0.001548x^2&<0&\implies&&x\in\left(9.34,53\right]\\
3.360-0.3420x-0.006360x^2&<0&\implies&&x\in\left(8.49,53\right]\\
\end{align}$$
#### 11.C)
Times of the year when $I'(t)$ is zero ($I(t)$ has a critical point).  
$$\begin{align}
-0.219+0.0544x-0.001725x^2&=0&\implies&&x\in\left\{4.74,26.80\right\}\\
4.410-0.6220x-0.013200x^2&=0&\implies&&x\in\left\{4.41\right\}\\
3.960-0.4180x-0.008820x^2&=0&\implies&&x\in\left\{8.09\right\}\\
0.991-0.0916x-0.001548x^2&=0&\implies&&x\in\left\{9.34\right\}\\
3.360-0.3420x-0.006360x^2&=0&\implies&&x\in\left\{8.49\right\}\\
\end{align}$$
#### 11.D)
Times of the year when I(t) is a maximum or a minimum.
**It looks like the majority of the peaks are during Late November and Early January.**
### Section 12
12. What does $I'(t)$ represent mathematically? How would you describe it contextually?  

It represents when the amount of search queries is maximized and minimized at a certain time.
I didn't do a finite difference, but I used the regression for approximately when there are peaks.

### Section 13
13. Go back to the intervals you identified above. What would they mean in the context of marketing the cooperative?

They should market their services during the winter time in the Northern hemisphere, so that they can attract the most amount of people.

### Section 14
14. Based on your analysis, during what times of the year should the cooperative consider online and social media marketing in order to attract more customers?  

Definitely during the Northern Hemisphere winter. There are other minor peaks, but I would definitely say the largest amount of effort should be put in northern winter.

