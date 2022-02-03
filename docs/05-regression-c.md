# Slopes

The slope in a simple linear regression can be defined as the change in predicted values of Y (the dependent variable) for every one unit change in X (the predictor variable). In the simple linear regression model shown below, the slope is written as $b_1$ (pronounced beta-one) . 

$$Y = b_{0} + b_{1}X + error$$

To put the slope into a physical context, say, for example, when measuring headsize to predict IQ, you find a slope of $b_1$ = 1.5, that would mean that for every increase of 1 in headsize, you would predict an increase of 1.5 in IQ.  



**the slope:**

The formula for the slope is:

$$b_{1} = \frac{cov_{(x, y)}}{s^2_{x}}$$
which is stated as the covariance of x and y ($cov_{(x,y)}$) divided by the variance of x ($s^2_{x}$). If we translate that into outcome and predictors then, given our Head Size is the predictor ($x$) and the IQ is the outcome ($y$), that becomes:

$$b_{1} = \frac{cov_{(HeadSize, IQ)}}{s^2_{HeadSize}}$$

But this can also be written in terms of the correlation between the two variables as opposed to the covariance, and this would look like:

$$b_{1} = r_{(x,y)} \times \frac{s_{y}}{s_{x}}$$

Which is stated as the correlation between x and y ($r_{(x,y)}$) multiplied by the standard deviation of y ($s_{y}$) divided by the standard deviation of x ($s_{x}$). [Remember that $s$ is the standard deviation of a variable, and $s^2$ is the variance of the variable.]

And again we can translate that back into terms of HeadSize ($x$) and IQ ($y$) as:

$$b_{1} = r \times \frac{s_{IQ}}{s_{HeadSize}}$$

Now if we think back to the correlation chapter we actually do know all the values we need, or at least can calculate them. Here is what we know from the correlation chapter:

* $cov_{(x,y)}$ = 199.26
* $s_{HeadSize}$ = 12.92
* $s_{IQ}$ = 15.95
* $r_{(x,y)}$ = 0.967

And from that we can calculate the variance of HeadSize ($s^2_{HeadSize}$) and IQ ($s^2_{IQ}$), based on $s^2 = s \times s$, meaning:

* $s^2_{HeadSize}$ = $12.92 \times 12.92$ = 166.9264
* $s^2_{IQ}$ = $15.95 \times 15.95$ = 254.4025

So we could really use either formula for the slope as we have all the information, but for now let's use:

$$b_{1} = r \times \frac{s_{IQ}}{s_{HeadSize}}$$

And if we start to feed in the values, remembering that the IQ is ($y$ - the outcome) and HeadSize is ($x$ - the predictor) we get:

$$b_{1} = 0.967 \times \frac{15.95}{12.92}$$

And then if we sort out the fraction first, that becomes:

$$b_{1} = 0.967 \times 1.2345201$$

Which leads down to:

$$b_{1} = 1.193781$$

Giving a slope of $b_{1}$ = 1.194, to three decimal places, meaning that for a 1 unit change in $x$ we get a 1.194 unit change in $y$. Or in other words, for a 1 unit change in HeadSize we get a 1.194 unit change in IQ.

