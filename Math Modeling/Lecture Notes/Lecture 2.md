**Name:** Stanley Goodwin
**Date:** 8/29/2024

---

Interpolation model: Passes through every datapoint.
Regression model: Does a least squares best fit.

Suppose we want to fit an $n^{th}$ degree polynomial to a data set of $m$ points (assume $m\ge n+1$)
To do this, we solve: $$\min_{\vec\alpha\in\mathbb{R}^{n+1}}\dfrac{1}{m}\sum_{i=1}^m\left(f(x_i;\vec{\alpha})-y_i\right)^2$$
Effectively, we're finding the vector $\vec\alpha$ that minimizes the *variance* of the model.


