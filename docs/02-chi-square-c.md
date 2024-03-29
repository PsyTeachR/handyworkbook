# Chi-Square Cross-Tabulation

## The Worked Example



Here is our data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Groups </th>
   <th style="text-align:center;"> Yes </th>
   <th style="text-align:center;"> No </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> A </td>
   <td style="text-align:center;"> 88 </td>
   <td style="text-align:center;"> 93 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> B </td>
   <td style="text-align:center;"> 160 </td>
   <td style="text-align:center;"> 59 </td>
  </tr>
</tbody>
</table>

We are going to need to know the Column Totals and Row Totals and the Total number of participants (N), so lets calculate them add them to our tables:

* **Group A Row Total** = 88 + 93 = 181
* **Group B Row Total** = 160 + 59 = 219
* **Yes Column Total** = 88 + 160 = 248
* **No Column Total** = 93 + 59 = 152
* **N =** 88 + 93 +160 + 59 = 400

And if we add those to our table we see:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Groups </th>
   <th style="text-align:center;"> Yes </th>
   <th style="text-align:center;"> No </th>
   <th style="text-align:center;"> Totals </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> A </td>
   <td style="text-align:center;"> 88 </td>
   <td style="text-align:center;"> 93 </td>
   <td style="text-align:center;"> 181 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> B </td>
   <td style="text-align:center;"> 160 </td>
   <td style="text-align:center;"> 59 </td>
   <td style="text-align:center;"> 219 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Totals </td>
   <td style="text-align:center;"> 248 </td>
   <td style="text-align:center;"> 152 </td>
   <td style="text-align:center;"> 400 </td>
  </tr>
</tbody>
</table>

Now the formula for the chi-square is:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

The Expected values for each condition, in the cross-tabulation in a few ways but the one we will use here is probably the easiest to use and it is:


$$Expected = \frac{Total_{row} \times Total_{column}}{N_{total}}$$

This is the same as other versions you might have seen such as:

$$Expected = \frac{Total_{row}}{N_{total}} \times \frac{Total_{column}}{N_{total}} \times N_{total}$$

The will both give the same result. So using the first approach we would see that the Expected values are:

**For Group A people that said Yes:**

$$Expected_{A-Yes} = \frac{181 \times 248}{400} = \frac{44888}{400} = 112.22$$

**For Group A people that said No:**

$$Expected_{A-No} = \frac{181 \times 152}{400} = \frac{27512}{400} = 68.78$$

**For Group B people that said Yes:**

$$Expected_{B-Yes} = \frac{219 \times 248}{400} = \frac{54312}{400} = 135.78$$

**For Group B people that said No:**

$$Expected_{B-No} = \frac{219 \times 152}{400} = \frac{33288}{400} = 83.22$$

We now have our data, let's start putting it into the formula, which we said was:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

Which really means:

$$\chi^2 = \frac{(Observed_{A-Yes} - Expected_{A-Yes})^2}{Expected_{A-Yes}} + \frac{(Observed_{A-No} - Expected_{A-No})^2}{Expected_{A-No}} + \\ \frac{(Observed_{B-Yes} - Expected_{B-Yes})^2}{Expected_{B-Yes}} +  \frac{(Observed_{B-No} - Expected_{B-No})^2}{Expected_{B-No}}$$



And if we start putting in the values, becomes:

$$\chi^2 = \frac{(88 - 112.22)^2}{112.22}+ \frac{(93 - 68.78)^2}{68.78}+\frac{(160 - 135.78)^2}{135.78}+\frac{(59 - 83.22)^2}{83.22}$$

And if we start to tidy those top halves up a little it becomes:

$$\chi^2 = \frac{(-24.22)^2}{112.22}+ \frac{(24.22)^2}{68.78}+\frac{(24.22)^2}{135.78}+\frac{(-24.22)^2}{83.22}$$

And now we square those top halves to give:

$$\chi^2 = \frac{586.6084}{112.22} + \frac{586.6084}{68.78} + \frac{586.6084}{135.78} + \frac{586.6084}{83.22} $$

And then divide the top halves by the bottom halves

$$\chi^2 = {5.2273071} + {8.5287642} + {4.3202858} + {7.0488873}$$

And then we sum them altogether to find:

$$\chi^2 = 25.1252443 $$

Meaning that, rounded to two decimal places, we find $\chi^2 = 25.13$

**Degrees of Freedom**

The degrees of freedom for the cross-tabulation is calculated as:

$$df = (Rows - 1) \times (Columns - 1)$$

Which is read as **the number of Rows minus 1 times the number of Columns minus 1**. If we look at our original data again:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Groups </th>
   <th style="text-align:center;"> Yes </th>
   <th style="text-align:center;"> No </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> A </td>
   <td style="text-align:center;"> 88 </td>
   <td style="text-align:center;"> 93 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> B </td>
   <td style="text-align:center;"> 160 </td>
   <td style="text-align:center;"> 59 </td>
  </tr>
</tbody>
</table>

Looking at the table we see we have 2 rows and 2 columns of actual observed data (not looking at the titles and group names), so:

$$Rows - 1 = 2 - 1 = 1$$

And

$$Columns - 1 = 2 - 1 = 1$$

Meaning that:

$$df = (Rows - 1) \times (Columns - 1)$$

which becomes:

$$df = (2 - 1) \times (2 - 1)$$

And reduces to:

$$df = (1) \times (1)$$

leaving us with:

$$df = 1$$

so we see that $df = 1$

**The effect size**

One of the common effect sizes for a cross-tabulation chi-square test is Cramer's $V$ and is calculated as:

$$V = \sqrt\frac{\chi^2}{N \times \min(C-1, R-1)}$$

The key thing to note is $\min(C-1, R-1)$ which is read as **the minimum of EITHER the number of Columns (C) minus 1 OR the number of Rows (R) minus 1**; whichever of those two values is smallest. 

And the minimum of Columns minus 1 or Rows minus 1 is:

$$\min(C-1, R-1) = \min( 2 - 1,  2 - 1)$$
$$\min(C-1, R-1) = \min( 1,  1)$$
which gives us:

$$\min(C-1, R-1) = 1$$

And now we can start completing the Cramer's $V$ formula as we know:

* $\chi^2 = 25.13$
* $N = 400$
* $\min(C-1, R-1) = 1$

Giving us:

$$V = \sqrt\frac{25.13}{400 \times 1}$$

And if we deal with the bottom half first we get:

$$V = \sqrt\frac{25.13}{400}$$

Then if we divide the top by the bottom we get

$$V = \sqrt{0.062825}$$

Giving us:

$$V = 0.2506492$$

So we see that, rounded to two decimal places, the effect size is $V = 0.25$

**The write-up**



If we were to look at a critical value look-up table, we would see that the critical value associated with a $df = 1$ at $\alpha = .05$, to three decimal places, is $\chi^2_{crit} = 3.841$. As the chi-square value of this test (i.e. $\chi^2 = 25.13$) is larger than $\chi^2_{crit}$ then we can say that our test is significant, and as such would be written up as $\chi^2(df = 1, N = 400) = 25.13,p < .05, V = 0.25$.

**Following up a significant finding**

If our test was significant then we would go on to carry out the relevant one-sample chi-squares to breakdown how the association manifests itself. The key thing to remember however is that in these one-sample chi-squares, following the cross-tabulation, you **MUST** use the expected values from the cross-tabulation and **do not** calculate new expected values. 

For instance if you were looking at the one-sample chi-square within Group A, then you would use the expected values of $Expected_{A-Yes} = 112.22$ and $Expected_{A-No} = 68.78$ to compare against the observed values of $Observed_{A-Yes} = 88$ and $Observed_{A-No} = 93$ as such:

$$\chi^2 = \frac{(88 - 112.22)^2}{112.22}+ \frac{(93 - 68.78)^2}{68.78}$$

Which if you walk the process through you find:

$$\chi^2 = 13.7560713$$

Meaning that, rounded to two decimal places, we find $\chi^2 = 13.76$. The degrees of freedom, based on $df = k - 1$ (because it is a one-sample chi-square now), and that we have two groups (YES and NO, so $k = 2$), would be:

$$df = k - 1 = 2 - 1 = 1$$

The effect size is $\phi$ again because it is a one-sample chi-square and, to remind us, has the formula:

$$\phi = \sqrt\frac{\chi^2}{N}$$

And we know:

* $\chi^2 = 13.76$
* and N = 88 + 93 = 181

and if we put those into the formula we get:

$$\phi = \sqrt\frac{13.76}{181}$$

Which becomes:

$$\phi = \sqrt{0.0760221} = 0.2757211$$
And rounded to two decimal places would show $\phi = 0.28$

If we were to thinking about writing this one-sample up, and looking at the critical value table, we would see that the critical value associated with a $df = 1$ at $\alpha = .05$, to three decimal places, is $\chi^2_{crit} = 3.841$. As the chi-square value of this test (i.e. $\chi^2 = 13.76$) is larger than $\chi^2_{crit}$ then we can say that our test is significant, and as such would be written up as $\chi^2(df = 1, N = 181) = 13.76,p < .05, \phi = 0.28$.

Likewise, for the one-sample chi-square within Group B you would use the expected values of $Expected_{B-Yes} = 135.78$ and $Expected_{B-No} = 83.22$ to compare against the observed values of $Observed_{B-Yes} = 160$ and $Observed_{B-No} = 59$ as such:

$$\chi^2 = \frac{(160 - 135.78)^2}{135.78}+ \frac{(59 - 83.22)^2}{83.22}$$

Which if you walk the process through you find:

$$\chi^2 = 11.369173$$

Meaning that, rounded to two decimal places, we find $\chi^2 = 11.37$. Again the degrees of freedom, based on $df = k - 1$ (because it is a one-sample chi-square now), and that we have two groups (YES and NO, so $k = 2$), would be:

$$df = k - 1 = 2 - 1 = 1$$

The effect size is $\phi$ again because it is a one-sample chi-square and, to remind us, has the formula:

$$\phi = \sqrt\frac{\chi^2}{N}$$

And we know:

* $\chi^2 = 11.37$
* and N = 160 + 59 = 219

and if we put those into the formula we get:

$$\phi = \sqrt\frac{12.85}{253}$$

Which becomes:

$$\phi = \sqrt{0.0519178} = 0.2278548$$
And rounded to two decimal places would show $\phi = 0.23$

If we were to thinking about writing this one-sample up, and looking at the critical value table, we would see that the critical value associated with a $df = 1$ at $\alpha = .05$, to three decimal places, is $\chi^2_{crit} = 3.841$. As the chi-square value of this test (i.e. $\chi^2 = 11.37$) is larger than $\chi^2_{crit}$ then we can sa that our test is significant, and as such would be written up as $\chi^2(df = 1, N = 219) = 11.37,p < .05, \phi = 0.23$.



And finally we can round everything off by stating that the most common answer for group A was **No** and the most common answer for group B was **Yes**. 

## Chi-Square ($\chi^2$) Look-up Table


|df | $\alpha = .05$|
|:-:|:-------------:|
|1  |3.841|
|2  |5.991|
|3  |7.815|
|4  |9.488|
|5  |11.07|
|6  |12.592|
|7  |14.067|
|8  |15.507|
|9  |16.919|
|10  |18.307|
