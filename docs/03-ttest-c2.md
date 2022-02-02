# Between-Subjects Welch's t-test

**between-subjects Welch's t-test:** Compare two groups or conditions where the participants are different in each group and have not been matched or are only matched on broad demographics, e.g. only age.

## The Worked Example



Here is your data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Group </th>
   <th style="text-align:center;"> N </th>
   <th style="text-align:center;"> Mean </th>
   <th style="text-align:center;"> SD </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> A </td>
   <td style="text-align:center;"> 18 </td>
   <td style="text-align:center;"> 25.58 </td>
   <td style="text-align:center;"> 2.25 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> B </td>
   <td style="text-align:center;"> 18 </td>
   <td style="text-align:center;"> 29.07 </td>
   <td style="text-align:center;"> 2.53 </td>
  </tr>
</tbody>
</table>

Let's look at the main t-test formula for Welch's t-test:

$$t = \frac{\bar{X}_1 - \bar{X}_2}{\sqrt{\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}}}$$

Now, from the table above we know:

* the mean of Group A is $\bar{X_1} = 25.58$, 
* the mean of Group B is $\bar{X_2} = 29.07$, 
* the N of Group A is $N_1 = 18$, 
* and the N of Group B is $N_2 = 18$

From the table above we also know the standard deviation ($s_1$ = 2.25 and $s_2$ = 2.53) of the two groups, but the Welch's t-test formula uses the variance of both groups ($s_1^2$ and $s_2^2$). Fortunately, if you know the standard deviation of a set of values, you can calculate the variance by the formula:

$$variance = SD \times SD$$

Meaning that:

* the variance of Group A, $s_1^2 = 2.25 \times 2.25$ = 5.0625
* and the variance of Group B, $s_2^2 = 2.53 \times 2.53$ = 6.4009

And we can now start to fill in the t-test formula as follows:

$$t = \frac{25.58 - 29.07}{\sqrt{\frac{5.0625}{18}+\frac{6.4009}{18}}}$$

Let's start by resolving the fractions on the bottom half of the formula by dividing the variance of each group by the number of participants in each group:

$$t = \frac{25.58 - 29.07}{\sqrt{0.28125+0.3556056}}$$

And we can then add them together:

$$t = \frac{25.58 - 29.07}{\sqrt{0.6368556}}$$

Then take the square root of that value to give us one value on the bottom half of the formula:

$$t = \frac{25.58 - 29.07}{0.7980323}$$

And we can then resolve the top half of the formula by taking one mean from the other:

$$t = \frac{-3.49}{0.7980323}$$

And finally, dividing the top by the bottom to give us a t-value:

$$t = -4.3732566$$
Meaning that we would have a t-value, rounded to two decimal places, of $t = -4.37$

**Degrees of Freedom**

The degrees of freedom formula for the Welch's between-subjects t-test is actually a little bit complicated as shown below. However, as with anything, once you break it down it is ok and really you only need the variance of both groups and the number of people in both groups. It just requires you to be very careful of the order that you do the different parts.

$$df = \frac{\left(\frac{s^2_{x_1}}{n_1}+\frac{s^2_{x_2}}{n_2}\right)^2}{\frac{\left(\frac{s^2_{x_1}}{n_1}\right)^2}{n_1 - 1}+\frac{\left(\frac{s^2_{x_2}}{n_2}\right)^2}{n_2 - 1}}$$
And we know from above that:

* the variance of Group A, $s^2_{x_1} = 5.0625$
* the variance of Group B, $s^2_{x_2} = 6.4009$
* the N of Group A, $n_1 = 18$
* and the N of Group B, $n_1 = 18$

And we can start to fill that in as follows:

$$df = \frac{\left(\frac{5.0625}{18}+\frac{6.4009}{18}\right)^2}{\frac{\left(\frac{5.0625}{18}\right)^2}{18 - 1}+\frac{\left(\frac{6.4009}{18}\right)^2}{18 - 1}}$$
So let's do this slowly and reduce one of the fractions by dividing the variance of the first group by the number of people in that group.

$$df = \frac{\left(\frac{5.0625}{18}+\frac{6.4009}{18}\right)^2}{\frac{\left(0.28125\right)^2}{18 - 1}+\frac{\left(\frac{6.4009}{18}\right)^2}{18 - 1}}$$
And now we do the same for the second group:

$$df = \frac{\left(\frac{5.0625}{18}+\frac{6.4009}{18}\right)^2}{\frac{\left(0.28125\right)^2}{18 - 1}+\frac{\left(0.3556056\right)^2}{18 - 1}}$$

We could also reduce the formula a little by dealing with both $n-1$ in the bottom half of the formula:

$$df = \frac{\left(\frac{5.0625}{18}+\frac{6.4009}{18}\right)^2}{\frac{\left(0.28125\right)^2}{17}+\frac{\left(0.3556056\right)^2}{17}}$$
And now maybe reduce the top half of the formula by again dividing the variance of the first group by the number of people in that group, and then doing the same for the second group.

$$df = \frac{\left(0.28125+0.3556056\right)^2}{\frac{\left(0.28125\right)^2}{17}+\frac{\left(0.3556056\right)^2}{17}}$$

So now let's stick to the top half and add the two values together:

$$df = \frac{0.6368556^2}{\frac{\left(0.28125\right)^2}{17}+\frac{\left(0.3556056\right)^2}{17}}$$
And then square that value:

$$df = \frac{0.405585}{\frac{\left(0.28125\right)^2}{17}+\frac{\left(0.3556056\right)^2}{17}}$$

Then looking back at the bottom half of the formula we can reduce it a bit by squaring the two values:

$$df = \frac{0.405585}{\frac{0.0791016}{17}+\frac{0.1264553}{17}}$$

And now we resolve the fractions in the bottom half by dividing the top part by the bottom part for each group:

$$df = \frac{0.405585}{0.004653+0.0074385}$$

We then add those two values on the bottom part of the formula together:

$$df = \frac{0.405585}{0.0120916}$$

And finally divide the top half of the formula by the bottom half to get the degrees of freedom:

$$df = 33.5427605$$
Meaning that we would have a df, rounded to two decimal places, of $df = 33.54$

**Effect Size**

And finally Cohen's d, the effect size:

$$d = \frac{2t}{\sqrt{df}}$$

Which, based on the info above, we know:

* the t-value is $t = -4.37$
* and the degrees of freedom is $df = 33.54$

And putting that in the formula we get:

$$d = \frac{2 \times -4.37}{\sqrt{33.54}}$$

So if we resolve the square-root first we get:

$$d = \frac{2 \times -4.37}{5.7913729}$$

And then work through the top half:

$$d = \frac{-8.74}{5.7913729}$$

And divide the top by the bottom:

$$d = -1.5091413$$

Meaning that we have a cohen's d, rounded to two decimal places, of d = -1.51

**Determining Significance**


  
If we were to look at a critical values look-up table for $df = 33.54$ and $\alpha = .05$, we would see that the critical value is $t_{crit} = 2.033$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 4.37$, is equal to or larger than our $t_{crit}$ then we can say our result is significant, and as such could be written up as t(33.54) = -4.37, p < .05, d = -1.51. 

## Look-Up table

Remembering that the $t_{crit}$ value is the smallest t-value you need to find a significant effect, find the $t_{crit}$ for your df, assuming $\alpha = .05$. 

* If the $df$ of your test is not on the look-up table, use the next smallest $df$. For example, if your test has $df = 37$ and your table only has $df = 30$ or $df = 40$, you would use $df = 30$.
* If the $t$ value you calculated is equal to or larger than $t_{crit}$ then your test is significant. 

<table>
 <thead>
  <tr>
   <th style="text-align:right;"> df </th>
   <th style="text-align:right;"> $\alpha = .05$ </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 12.706 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 4.303 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 3.182 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 2.776 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 2.571 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 2.447 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 2.365 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 2.306 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 2.262 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 2.228 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 2.131 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 2.086 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 2.042 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 40 </td>
   <td style="text-align:right;"> 2.021 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 2.009 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 60 </td>
   <td style="text-align:right;"> 2.000 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 70 </td>
   <td style="text-align:right;"> 1.994 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 80 </td>
   <td style="text-align:right;"> 1.990 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 90 </td>
   <td style="text-align:right;"> 1.987 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 100 </td>
   <td style="text-align:right;"> 1.984 </td>
  </tr>
</tbody>
</table>
