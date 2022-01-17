# Correlation: Pearson

**The Pearson correlation** otherwise known as the Pearson Product-Moment correlation measures the relationshop between two variables when that relationship is monotonic and linear. To go a step further, in relating it measures the covariance between two variables, or the shared variance, and then standardises that measure between the values of -1 and 1 with -1 being the perfect negative relationship and 1 being the perfect positive relationship.

## The Worked Example

Let's say that this is our starting data:

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

and the formula for the Pearson correlation is:

$$r_{(x,y)} = \frac{cov(x,y)}{\sigma_{x}\sigma_{y}}$$

Meaning that, assuming we consider HeadSize as variable $x$ and IQ as variable $y$, to determine the correlation between HeadSize and IQ ($r_{(HeadSize, IQ)}$) we first need to know the covariance between HeadSize and IQ, ($cov(HeadSize, IQ)$), as well as the standard deviation of HeadSize ($\sigma_{HeadSize}$) and the standard deviation of IQ ($\sigma_{IQ}$). That is what we are going to look at here. We will run it all through from start to finish, assuming all we know are the values. If you know certain aspects like the covariance and the standard deviations then you can skip to just running the correlation but it is good to see the analysis in its entirety.

**Covariance**

The formula for the covariance between two continuous variables is:

$$cov(x,y) = \frac{\sum_i^n(x_i - \overline{x})(y_i - \overline{y})}{n-1}$$

where the $\sum_i^n$ translates as sum (i.e. add up) the values of $(x_i - \overline{x})(y_i - \overline{y})$ for each pair of observations in your data. But to do that we first need to know the mean of x ($\overline{x}$) and the mean of y, ($\overline{y}$). Now we know that the mean of a value is the sum of all the values of that variable divided by the number of values - also written as: 

$$\overline{x} = \frac{\sum_i^n x_i}{n}$$. 

So the mean of x (i.e. HeadSize) is:

$$\overline{x} = \frac{50.8 + 63.5 +  45.7  + 25.4  + 29.2  + 49.5  + 38.1  + 30.5  + 35.6  + 58.4}{10}$$

Which reduces to:

$$\overline{x} = \frac{426.7}{10} = 42.67$$

And if we repeat the same procedure for y (i.e. IQ), we get:

$$\overline{y} = \frac{107 + 121 +  106  + 72  + 85  + 105  + 93  + 88  + 97  + 123}{10}$$

Which reduces to:

$$\overline{y} = \frac{997}{10} = 99.7$$

Ok great so we now have enough information to start filling in the covariance formula. First, however, before looking at it for all participants, let's look at this part, $(x_i - \overline{x})(y_i - \overline{y})$, for one participant just to make sure we understand what we are doing. And one thing to remember is that two sets of parentheses (i.e. brackets) side-by-side like that means to multiply them together. So, if we take Participant 1, then we see that:

* The mean of x is $\overline{x} = 42.67$
* The mean of y is $\overline{y} = 99.7$
* They have a HeadSize (x) of $x_1$ = 50.8
* They have an IQ (y) of $y_1$ = 107
* And note that we are now saying $x_1$ and $y_1$, and no longer $x_i$ and $y_i$, because we know we are specifically dealing with the 1^st^ Participant. If it was the 2^nd^ Participants we would write $x_2$ and $y_2$, and the 8^th^ would be $x_8$ and $y_8$, etc

Putting all that into the formula for Participant 1 (P~1~) would give us:



P~1~ = $(x_1 - \overline{x})(y_1 - \overline{y}) = (50.8 - 42.67)\times(107 - 99.7) = 8.13 \times 7.3 = 59.349$

and we can do that for all participants which would look like:

* P~2~ = $(x_2 - \overline{x})(y_2 - \overline{y}) = (63.5 - 42.67)\times(121 - 99.7) = 20.83\times21.3 = 443.679$
* P~3~ = $(x_3 - \overline{x})(y_3 - \overline{y}) = (45.7 - 42.67)\times(106 - 99.7) = 3.03\times6.3 = 19.089$
* P~4~ = $(x_4 - \overline{x})(y_4 - \overline{y}) = (25.4 - 42.67)\times(72 - 99.7) = -17.27\times-27.7 = 478.379$
* P~5~ = $(x_5 - \overline{x})(y_5 - \overline{y}) = (29.2 - 42.67)\times(85 - 99.7) = -13.47\times-14.7 = 198.009$
* P~6~ = $(x_6 - \overline{x})(y_6 - \overline{y}) = (49.5 - 42.67)\times(105 - 99.7) = 6.83\times5.3 = 36.199$
* P~7~ = $(x_7 - \overline{x})(y_7 - \overline{y}) = (38.1 - 42.67)\times(93 - 99.7) = -4.57\times-6.7 = 30.619$
* P~8~ = $(x_8 - \overline{x})(y_8 - \overline{y}) = (30.5 - 42.67)\times(88 - 99.7) = -12.17\times-11.7 = 142.389$
* P~9~ = $(x_9 - \overline{x})(y_9 - \overline{y}) = (35.6 - 42.67)\times(97 - 99.7) = -7.07\times-2.7 = 19.089$
* P~10~ = $(x_10 - \overline{x})(y_10 - \overline{y}) = (58.4 - 42.67)\times(123 - 99.7) = 15.73\times23.3 = 366.509$

And if we remember that the $\sum_i^n$ part of the formula means that the formula, for this example with 10 participants, is really

$$cov(x,y) = \frac{(x_1 - \overline{x})(y_1 - \overline{y})+(x_2 - \overline{x})(y_2 - \overline{y})+(x_3 - \overline{x})(y_3 - \overline{y})+(x_4 - \overline{x})(y_4 - \overline{y})+\\(x_5 - \overline{x})(y_5 - \overline{y})+(x_6 - \overline{x})(y_6 - \overline{y})+(x_7 - \overline{x})(y_7 - \overline{y})+(x_8 - \overline{x})(y_8 - \overline{y})+\\(x_9 - \overline{x})(y_9 - \overline{y})+(x_{10} - \overline{x})(y_{10} - \overline{y})}{n-1}$$

Then that becomes:

$$cov(x,y) = \frac{((50.8 - 42.67)\times(107 - 99.7)) + ((63.5 - 42.67)\times(121 - 99.7)) +\\ ((45.7 - 42.67)\times(106 - 99.7)) + ((25.4 - 42.67)\times(72 - 99.7)) +\\ ((29.2 - 42.67)\times(85 - 99.7)) + ((49.5 - 42.67)\times(105 - 99.7)) + \\((38.1 - 42.67)\times(93 - 99.7)) + ((30.5 - 42.67)\times(88 - 99.7)) + \\((35.6 - 42.67)\times(97 - 99.7)) + ((58.4 - 42.67)\times(123 - 99.7))}{n-1}$$

and, remembering the rules of BODMAS/PEMDAS, reduces to:

$$cov(x,y) = \frac{59.349 + 443.679 + 19.089 + 478.379 + 198.009\\+ 36.199 + 30.619 + 142.389 + 19.089 + 366.509}{n-1}$$

And all these values match the value we calculated above, so we know that is correct. Then if we know n = 10 as that is the number of participants, and so the bottom of the formula becomes n = 10 - 1 = 9, we can reduce all of the above to:

$$cov(x,y) = \frac{1793.31}{9}$$

Leaving us with a covariance between HeadSize ($x$) and IQ ($y$) of:

$$cov(x,y) = 199.2566667$$

Great! Now if we look back at the formula for the Pearson correlation, we see:

$$r_{(x,y)} = \frac{cov(x,y)}{\sigma_{x}\sigma_{y}}$$

So the covariance of x and y, divided by the product (multiply them together) of the standard deviation of x $\sigma_{x}$ (pronounced sigma-x) and the standard deviation of y $\sigma_{y}$ (pronounced sigma-y). Remember that $\sigma$ can also be written as $S$ or $SD$ and is the symbol for the Standard Deviation and that $\sigma^2$ (pronounced sigma-squared) is the symbol for the variance. So in reality, the pearson correlation between Head Size and IQ is written as:

$$r_{(HeadSize,IQ)} = \frac{cov(HeadSize,IQ)}{\sigma_{HeadSize}\times\sigma_{IQ}}$$

And if we known from above that $cov(HeadSize, IQ)$ = 199.26 (to two decimal places), now all we need is the standard deviation of Headsize ($\sigma_{HeadSize}$) and the standard deviation of IQ ($\sigma_{IQ}$).

We cover standard deviation calculations in the Descriptives chapter, but to briefly recap, the formula is:

$$\sigma = \sqrt\frac{\sum_i^n(x_{i} - \overline{x})^2}{n-1}$$

Which for HeadSize would look like:

$$\sigma_{HeadSize} = \sqrt\frac{(50.8 - 42.67)^2 + (63.5 - 42.67)^2 +(45.7 - 42.67)^2 +(25.4 - 42.67)^2 +\\(29.2 - 42.67)^2 +(49.5 - 42.67)^2 +(38.1 - 42.67)^2 +(30.5 - 42.67)^2 +\\(35.6 - 42.67)^2 +(58.4 - 42.67)^2}{10-1}$$

Which reduces to:

$$\sigma_{HeadSize} = \sqrt\frac{66.0969 + 433.8889 +9.1809 +298.2529 +\\181.4409 +46.6489 +20.8849 +148.1089 +\\49.9849 +247.4329 }{9}$$

Giving us:

$$\sigma_{HeadSize} = \sqrt\frac{1501.921}{9} = \sqrt{166.8801111} = 12.9182085$$

And if we repeat that process for the standard deviation of IQ ($\sigma_{IQ}$) then it would be:

$$\sigma_{IQ} = \sqrt\frac{(107 - 99.7)^2 + (121 - 99.7)^2 +(106 - 99.7)^2 +(72 - 99.7)^2 +(85 - 99.7)^2 +\\(105 - 99.7)^2 +(93 - 99.7)^2 +(88 - 99.7)^2 +(97 - 99.7)^2 +(123 - 99.7)^2}{10-1}$$

Which reduces to:

$$\sigma_{IQ} = \sqrt\frac{53.29 + 453.69 +39.69 +767.29 +216.09 +\\28.09 +44.89 +136.89 +7.29 +542.89 }{9}$$

Giving us:

$$\sigma_{IQ} = \sqrt\frac{2290.1}{9} = \sqrt{254.4555556} = 15.9516631$$

And so if we know the following,

* $cov(x,y)$ = $cov(HeadSpace, IQ)$ = 199.26
* $\sigma_{x}$ = $\sigma_{HeadSpace}$ = 12.92
* $\sigma_{y}$ = $\sigma_{IQ}$ = 15.95

Then our correlation value is:

\begin{align*}
r_{(HeadSize,IQ)} &= \frac{cov(HeadSize,IQ)}{\sigma_{HeadSize}\times\sigma_{IQ}} \\ \\ &= \frac{199.26}{12.92 \times 15.95} \\ \\ &= \frac{199.26}{206.074} \\ \\ &= 0.9669342
\end{align*}




Meaning that we would have a correlation value of, to three decimal places, $r$ = 0.967, which, following Cohen's (1988) proposed cut-offs shown below, would be considered to show a strong positive relationship. Remember that these cut-offs are just guides so a value just below a cut-off, e.g. r = .48, would probably be described as, for example, a strong positive relationship.

|Relationship Description (Cohen, 1988)| r-value |
|---:|:---:|
|Strong positive relationship| r = .5|
|Medium positive relationship| r = .3|
|Weak positive relationship| r = .1|
|No relationship| r = 0| 
|Weak negative relationship| r = -.1|
|Medium negative relationship| r = -.3|
|Strong negative relationship| r = -.5|

**Degrees of Freedom**

Great! Now, finally, to determine significance we first need the degrees of freedom for the test. The degrees of freedom formula is:

$$df = N - 2$$

And we already know that $N= 10$ and putting them into the equation we get:

$$df = 10 - 2$$

Which reduces to:

$$df = 8$$


Meaning that we find a $df = 8$

**Writing up**

The standard APA format for writing up a Pearson correlation is usually:

<p align = "center">**r(df) = r-value, p = p-value**</p>

From above we know the df and we know the r-value and what we need now is the significance.

**Determining Significance**

If we were to look at a critical values look-up table for $df = 8$ and $\alpha = .05$, we would see that the critical value is $r_{crit} = 0.632$. Given that our r-value, ignoring polarity and just looking at the absolute value, so $r = 0.967$, is equal to or larger than our $r_{crit}$ then we can say our result is significant, and as such would be written up as r(8) = 0.967, p < .05. 

**Remember:** If you were writing this up as a report, and analysed the data in R, then you would see the p-value was actually p = 0.000005014954, and would be written up as p < .001

## Look-Up table

Remembering that the $r_{crit}$ value is the smallest r-value you need to find a significant effect, find the $r_{crit}$ value for your df, assuming $\alpha = .05$. If the $r$-value you calculated is equal to or larger than $r_{crit}$ value then your test is significant.

|df | $\alpha = .05$|
|:-:|:-------------:|
|1  |0.997|
|2  |0.95|
|3  |0.878|
|4  |0.811|
|5  |0.754|
|6  |0.707|
|7  |0.666|
|8  |0.632|
|9  |0.602|
|10 |0.576|
|15 |0.482|
|20 |0.423|
|30 |0.349|
|40 |0.304|
|50 |0.273|
|60 |0.25|
|70 |0.232|
|80 |0.217|
|90 |0.205|
|100|0.195|
