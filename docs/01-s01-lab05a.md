# Simple Linear Regression

Simple Linear Regression is analytical method that looks to model the relationship between an outcome variable and **one** explanatory predictor variables. For example, thinking about the data that we used for the Pearson Correlation analysis in this book, say instead of asking is HeadSize and IQ related, we could ask can you reliably predict IQ scores (our outcome or dependent variable) from HeadSize measurements (our predictor or independent variable), with the hypothesis of, "We predict that a linear model based on head size, as measured in cms, will significantly predict IQ scores as measured on a standard IQ test". We are going to look at this example to walk through some of the analysis but lets first remind ourselves of the data.

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> HeadSize </th>
   <th style="text-align:center;"> IQ </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 50.8 </td>
   <td style="text-align:center;"> 107 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 63.5 </td>
   <td style="text-align:center;"> 121 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 45.7 </td>
   <td style="text-align:center;"> 106 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 25.4 </td>
   <td style="text-align:center;"> 72 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 29.2 </td>
   <td style="text-align:center;"> 85 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 49.5 </td>
   <td style="text-align:center;"> 105 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 38.1 </td>
   <td style="text-align:center;"> 93 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 30.5 </td>
   <td style="text-align:center;"> 88 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 35.6 </td>
   <td style="text-align:center;"> 97 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 58.4 </td>
   <td style="text-align:center;"> 123 </td>
  </tr>
</tbody>
</table>

Now in order to determine how well Head Size predicts IQ we need to know the underlying formula for this type of analysis and use that to calculate elements such as the slope of the relationship and the intercept. You might remember from previous years that a line in a two-dimensional coordinate system (i.e. two dimensional space made of variables X and Y) can be described by a linear equation (model) of the form:

$$Y = b_{0} + b_{1}X + error$$
 
Where:

* $Y$ is the value on the outcome variable Y 
* $X$ is the value on the predictor variable X
* $b_{0}$ is the intercept (or regression constant) – pronounced beta-zero - and stated as the value of $Y$ when $X = 0$ when X = 0
* $b_{1}$ is the slope (or regression coefficient) – pronounced beta-one - and stated as the change in $Y$ associated with a one-unit increase in $X$
* $error$ is a measure of your residuals which are the difference between an actual value and a predicted value

Before getting into the full simple linear regression however we will look at making predictions from this linear model formula using the slope and the intercept, based on the following equations.

**the slope:**

$$b_{1} = \frac{cov_{(x, y)}}{s^2_{x}}$$

Or alternatively it can be written as,

$$b_{1} = r_{(x,y)} \times \frac{s_{y}}{s_{x}}$$

**the intercept**

$$b_{0} = \overline{y} - b_{1} \times \overline{x}$$

So lets spend some time looking at those two equations in turn.

## The slope:

As above, the formula for the slope is:

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

## The intercept

Great. So now we know the slope of the regression line between HeadSize and IQ, what we need next is the intercept.  The formula for the intercept, as above, is:

$$b_{0} = \overline{y} - b_{1} \times \overline{x}$$

Which is stated as the mean of y ($\overline{y}$ - in this case IQ, our outcome) minus the slope ($b_{1}$) multiplied by the mean of x ($\overline{x}$ - in this case HeadSize, our predictor).

Looking back at the correlation chapter, and above, we know:

* $b_{1}$ = 1.194
* $\overline{x}$ = 42.67
* $\overline{y}$ = 99.7

And if we substitute those values into the formula we get:

$$b_{0} = 99.7 - 1.194 \times 42.67$$

Remembering BODMAS we need to do the multiplication first, which gives us:

$$b_{0} = 99.7 - 50.94798$$

And we then complete the formula by doing the subtraction giving us:

$$b_{0} = 48.75202$$

Meaning that we have an intercept of $b_{0}$ = 48.75, to two decimal places. And if we remember that the intercept is the value of $y$ when $x$ is zero, then this tells us that when $x$ = 0, the value of $y$ is $y$ = 48.75. Or stated in terms of HeadSize and IQ, when Headsize is 0, then IQ is 48.75.  

## Making a Prediction

Now based on the information we have gained above we can actually use that to make predictions about a person we have not measured based on the formula:

$$\hat{Y} = b_{0} + b_{1}X$$

Well technically it is 

$$\hat{Y} = b_{0} + b_{1}X + error$$

But we will disregard the error for now. Also you might have noticed the small hat about the $Y$ making it $\hat{Y}$ (pronounced Y-hat). This means we are making a prediction of Y ($\hat{Y}$) as opposed to an actually measured (i.e. observed) value ($Y$).

Now let's say we want to make a prediction about someone who has a HeadSize of 60.1. Then, using the information above, we know:

* the slope, $b_{1}$ = 1.194
* the intercept, $b_{0}$ = 48.75
* and the HeadSize, $X$ = 60.1 

If we put all that into the formula we would get:

$$\hat{Y} = 48.75 + 1.194 \times 60.1$$

And if we start to work that through, dealing with the multiplication first, we see:

$$\hat{Y} = 48.75 + 71.7594$$

Which then becomes:

$$\hat{Y} = 120.5094$$

Giving a predicted value of $\hat{Y}$ = 120.51, to two decimal places. Meaning that for a participant with a HeadSize of 60.1 we would predict an IQ of 120.51. And you can use the same approach for any number of predictions with this model. Say you measured someone with a HeadSize of 59.4 cm, then they would be:

$$\hat{Y} = 48.75 + 1.194 \times 59.4 = 119.6736$$

Meaning that for a participant with a HeadSize of 59.4 we would predict an IQ of 119.67.

## The R-squared 

Obviously the question now is how good is our model at making these predictions, and one measure of that is $R^2$ (pronounced R-squared). This relates to the $error$ term that we saw in the original formula, i.e. $\hat{Y} = b_{0} + b_{1}X + error$, and as we said at the start it relates to the residuals. The residuals you might know are the difference between predicted values and observed values. For example, if we look at Participant 1 in our data we see they had a HeadSize of 50.8 and an IQ of 107.  Those are our observed values of $X$ and $Y$ for that participant, but what if we predicted a value for that participant instead ($\hat{Y}$). Using the above formula we would see:

$$\hat{Y} = 48.75 + 1.194 \times 50.8 = 109.4052$$

So we would predict for Participant 1, with a HeadSize of 50.8, to have an IQ of 109.4052. And if we compare that to the actually observed value for that participant ($Y = 107$) we see a difference of 2.4052 IQ points (i.e. $\hat{Y} - Y = 2.4052$). And that difference is our residuals for that person - the left over part between the observed and the predicted. If we were then to check that for all the observed participants we would get an overall value that summarises how big or small our residuals are, and the smaller the residuals are, the better the model is at predicting values of $Y$ from $X$, because there is little difference between our predicted values and our observed values. And that is what our $R^2$ tells us. It is a measure of how good our model is at prediction, and a measure of how small our residuals are. $R^2$ can take values between 0 and 1 and simply put, the closer $R^2$ is to 1, the smaller our residuals and the better our model is at prediction.

Now there is a full approach to calculating the $R^2$ which we will show you in a little bit, but when you are dealing with simple linear regression as we are here, there is a quick approach that gives the same answer, and it is:

$$R^2 = r_{(x,y)} \times r_{(x,y)}$$

where $r_{(x,y)}$ is the correlation between the two variables, in this case Headsize ($x$) and IQ ($y$). And if we look above we see we already know the correlation between HeadSize and IQ, as we calculated it in the correlation chapter. The correlation between HeadSize and IQ is $r_{(HeadSize, IQ)} = 0.967$. And if we put that into our formula for $R^2$ we see:

$$R^2 = 0.967 \times 0.967 = 0.935089$$

Meaning that we have an $R^2$ of $R^2 = 0.935$, to three decimal places. And given that that is quite close to an $R^2$ of 1, it would suggest that our model is very good at predicting IQ from HeadSize (Y from X), that our residuals are small, and that there is a strong positive relationship between the two variables.

## The Write-up

Ok great, so we have now got a lot of information on our model including the slope, the intercept, and the $R^2$. The one thing we don't actually know is where our model is significant. We will go into what that means and how to determine that in a later part, but in the meantime we will just tell you that the model is significant, (F(1, 8) = 115.07, p < .001). So now we have everything we need for the write up:

* The model is significant - F(1, 8) = 115.07, p < .001
* The $R^2$ = 0.935 is very high

The only other element we need is the coefficent - the relationship between the two variables - which can take two versions; unstandardised and standardised.  But, we actually do already know these. We just called them something else:

* what we call **the slope**, above, is the **unstandardised coefficient** and is written as $b$ = 1.194
* what we called **the correlation** between the variables is actually the **standardised coefficient** and is written as $\beta$ = 0.967

And it is totally acceptable to write-up either the standardised coefficient ($\beta$) or the unstandardised coefficient ($b$). The main thing is to make sure you use the right symbol with the right value and don't mix them up as that will mislead a reader.

Now if we take all the information we have, including some information from the correlation chapter, we can put it into a blurb as such:

**A team of researchers were interested in the relationship between Head Size and IQ, and specifically whether they could predict IQ from Head Size. The researchers set out the hypothesis that a linear model based on head size, as measured in cms, will significantly predict IQ scores as measured on a standard IQ test. Descriptive analysis suggested a strong positive relationship between Head Size (M = 42.67, SD = 12.92) and IQ (M = 99.7, SD = 15.95), (r(8) = 0.967). On analysis, a linear regression model revealed that head size (measured in cm) significantly predicted participant scores on an IQ test ($\beta$ = 0.967, F(1, 8) = 115.07, p < .001, $R^2$ = 0.935), with head size explaining 93.5% of the variance in IQ scores. As such the alternative hypothesis was accepted suggesting that...**

But I guess it might look a bit odd as we give the standardised coeffiencient twice, just in different ways, so we could write it with the unstandardised coefficient as:

**A team of researchers were interested in the relationship between Head Size and IQ, and specifically whether they could predict IQ from Head Size. The researchers set out the hypothesis that a linear model based on head size, as measured in cms, will significantly predict IQ scores as measured on a standard IQ test. Descriptive analysis suggested a strong positive relationship between Head Size (M = 42.67, SD = 12.92) and IQ (M = 99.7, SD = 15.95), (r(8) = 0.967), with head size explaining 93.5% of the variance in IQ scores. On analysis, a linear regression model revealed that head size (measured in cm) significantly predicted participant scores on an IQ test ($b$ = 1.194, F(1, 8) = 115.07, p < .001, $R^2$ = 0.935). As such the alternative hypothesis was accepted suggesting that...**
