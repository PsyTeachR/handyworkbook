# Between-Subjects Student's t-test

**between-subjects t-test:** Compare two groups or conditions where the participants are different in each group and have not been matched or are only matched on broad demographics, e.g. only age.

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

Let's look at the main t-test formula:

$$t = \frac{\bar{X}_1 - \bar{X}_2}{s_p \times \sqrt{\frac{1}{N_1} + \frac{1}{N_2}}}$$

Now, from the table above we know:

* the mean of Group A is $\bar{X_1} = 25.58$, 
* the mean of Group B is $\bar{X_2} = 29.07$, 
* the N of Group A is $N_1 = 18$, 
* and the N of Group B is $N_2 = 18$, 

which we can put into the equation right now:

$$t = \frac{25.58 - 29.07}{s_p \times \sqrt{\frac{1}{18} + \frac{1}{18}}}$$

And now we can see that the only thing we don't yet know is the pooled standard deviation ($s_p$). Let's look at that formula:

**Calculating the pooled standard deviation**

$$s_p = \sqrt{\frac{(n_1 -1)  \times s^2_{X_1} + (n_2 -1)\times s^2_{X_2}}{n_1 + n_2 - 2}}$$

And if we start to fill in some details:

$$s_p = \sqrt{\frac{(18 -1)  \times s^2_{X_1} + (18 -1)\times s^2_{X_2}}{18 + 18 - 2}}$$

Now looking at the formula, it is clear we are missing:

* $s^2_{X_1}$ - the variance of Group A (could be written as $s^2_{A}$)
* $s^2_{X_2}$ - the variance of Group B (could be written as $s^2_{B}$) 

What we do know though, from the table, is the standard deviations of both groups ($SD_A$ = 2.25; $SD_B$ = 2.53), and we know that variance of a group is equal to the standard deviation squared. So:

* $s^2_{X_1}$ = $s^2_A$ = $SD_A \times SD_A$ = $2.25 \times 2.25$ = $5.0625$
* $s^2_{X_2}$ = $s^2_B$ = $SD_B \times SD_B$ = $2.53 \times 2.53$ = $6.4009$

And if we now add those values to our formula we get:

$$s_p = \sqrt{\frac{(18 -1)  \times 5.0625 + (18 -1)\times 6.4009}{18 + 18 - 2}}$$

And we can then start working through the formula, taking each stage in turn to make sure we don't make mistakes. Let's get rid of the brackets first:

$$s_p = \sqrt{\frac{(17  \times 5.0625) + (17 \times 6.4009)}{34}}$$

Now we deal with the multiplications:

$$s_p = \sqrt{\frac{86.0625 + 108.8153}{34}}$$

Let's tidy up that top half of the equation (the numerator):

$$s_p = \sqrt{\frac{194.8778}{34}}$$

Which if we then divide the numerator by the denominator (the bottom half), and then take the square root of that we get:

$$s_p = \sqrt{5.7317}$$ 

Giving a pooled standard deviation of:

$$s_p = 2.3940969$$

Meaning that our pooled standard deviation, rounded to three decimal places, is $s_p = 2.394$ and we can now add that to the t-test formula to give us:

**Calculating the t-value**

$$t = \frac{25.58 - 29.07}{2.394 \times \sqrt{\frac{1}{18} + \frac{1}{18}}}$$

And again we just start working through the formula. Let's deal with the fractions relating to sample size first:

$$t = \frac{25.58 - 29.07}{2.394 \times \sqrt{0.0555556 + 0.0555556}}$$

Which we can tidy up a little to give:

$$t = \frac{-3.49}{2.394 \times \sqrt{0.1111111}}$$

And if we sort out the square root on the denominator we are left with:

$$t = \frac{-3.49}{2.394 \times 0.3333333}$$

We can then tidy up the denominator to give us:

$$t = \frac{-3.49}{0.798}$$

Which we can finally solve to give us a t-value, rounded to two decimal places, of $t = -4.37$

**Degrees of Freedom**

Great! Now we just need the degrees of freedom where the formula is:

$$df = (n_1 - 1) + (n_2 - 1)$$

And we already know that:

* the N of Group A is $N_1 = 18$, 
* and the N of Group B is $N_2 = 18$, 

So putting them into the equation we get:

$$df = (18 - 1) + (18 - 1)$$
$$df = 17 + 17$$
$$df = 34$$

**Effect Size: Cohen's d**

And finally Cohen's d, the effect size:

$$d = \frac{2t}{\sqrt{df}}$$

Which, based on the info above, we know:

* $t = -4.37$
* $df = 34$

Putting them into the formula we get:

$$d = \frac{2 \times -4.37}{\sqrt{34}}$$

And if we tidy the nominator and the denominator we get:

$$d = \frac{-8.74}{5.8309519}$$

Which we can then solve to learn that $d = -1.5$

**Determining Significance**

If we were to look at a critical values look-up table for $df = 34$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 2.032$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 4.37$, is equal to or larger than our $t_{crit}$ then we can say our result is significant, and as such would be written up as t(34) = 4.37, p < .05, d = 1.5

**Remember:** If you were writing this up as a report, and analysis the data in R, then you would see the p-value was actually p = 1.1081944\times 10^{-4}, and would be written up as p < .001

## Test Yourself

### DataSet 1



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
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 68.01 </td>
   <td style="text-align:center;"> 0.34 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> B </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 67.80 </td>
   <td style="text-align:center;"> 0.67 </td>
  </tr>
</tbody>
</table>



<div class='webex-solution'><button>Show me the working and answer</button>


Let's look at the main t-test formula:

$$t = \frac{\bar{X}_1 - \bar{X}_2}{s_p \times \sqrt{\frac{1}{N_1} + \frac{1}{N_2}}}$$

Now, from the table above we know:

* the mean of Group A is $\bar{X_1} = 68.01$, 
* the mean of Group B is $\bar{X_2} = 67.8$, 
* the N of Group A is $N_1 = 5$, 
* and the N of Group B is $N_2 = 5$, 

which we can put into the equation right now:

$$t = \frac{68.01 - 67.8}{s_p \times \sqrt{\frac{1}{5} + \frac{1}{5}}}$$

And now we can see that the only thing we don't yet know is the pooled standard deviation ($s_p$). Let's look at that formula:

$$s_p = \sqrt{\frac{(n_1 -1)  \times s^2_{X_1} + (n_2 -1)\times s^2_{X_2}}{n_1 + n_2 - 2}}$$

And if we start to fill in some details:

$$s_p = \sqrt{\frac{(5 -1)  \times s^2_{X_1} + (5 -1)\times s^2_{X_2}}{5 + 5 - 2}}$$

Now looking at the formula, it is clear we are missing:

* $s^2_{X_1}$ - the variance of Group A (could be written as $s^2_{A}$)
* $s^2_{X_2}$ - the variance of Group B (could be written as $s^2_{B}$) 

What we do know though, from the table, is the standard deviations of both groups ($SD_A$ = 0.34; $SD_B$ = 0.67), and we know that variance of a group is equal to the standard deviation squared. So:

* $s^2_{X_1}$ = $s^2_A$ = $SD_A \times SD_A$ = $0.34 \times 0.34$ = $0.1156$
* $s^2_{X_2}$ = $s^2_B$ = $SD_B \times SD_B$ = $0.67 \times 0.67$ = $0.4489$

And if we now add those values to our formula we get:

$$s_p = \sqrt{\frac{(5 -1)  \times 0.1156 + (5 -1)\times 0.4489}{5 + 5 - 2}}$$

And we can then start working through the formula, taking each stage in turn to make sure we don't make mistakes. Let's get rid of the brackets first:

$$s_p = \sqrt{\frac{(4  \times 0.1156) + (4 \times 0.4489)}{8}}$$

Now we deal with the multiplications:

$$s_p = \sqrt{\frac{0.4624 + 1.7956}{8}}$$

Let's tidy up that top half of the equation (the numerator):

$$s_p = \sqrt{\frac{2.258}{8}}$$

Which if we then divide the numerator by the denominator (the bottom half), and then take the square root of that we get:

$$s_p = \sqrt{0.28225}$$ 

Giving a pooled standard deviation of:

$$s_p = 0.5312721$$

Meaning that our pooled standard deviation, rounded to three decimal places, is $s_p = 0.531$ and we can now add that to the t-test formula to give us:

$$t = \frac{68.01 - 67.8}{0.531 \times \sqrt{\frac{1}{5} + \frac{1}{5}}}$$

And again we just start working through the formula. Let's deal with the fractions relating to sample size first:

$$t = \frac{68.01 - 67.8}{0.531 \times \sqrt{0.2 + 0.2}}$$

Which we can tidy up a little to give:

$$t = \frac{0.21}{0.531 \times \sqrt{0.4}}$$

And if we sort out the square root on the denominator we are left with:

$$t = \frac{0.21}{0.531 \times 0.6324555}$$

We can then tidy up the denominator to give us:

$$t = \frac{0.21}{0.3358339}$$

Which we can finally solve to give us a t-value, rounded to two decimal places, of $t = 0.63$

Great! Now we just need the degrees of freedom where the formula is:

$$df = (n_1 - 1) + (n_2 - 1)$$

And we already know that:

* the N of Group A is $N_1 = 5$, 
* and the N of Group B is $N_2 = 5$, 

So putting them into the equation we get:

$$df = (5 - 1) + (5 - 1)$$
$$df = 4 + 4$$
$$df = 8$$

And finally Cohen's d, the effect size:

$$d = \frac{2t}{\sqrt{df}}$$

Which, based on the info above, we know:

* $t = 0.63$
* $df = 8$

Putting them into the formula we get:

$$d = \frac{2 \times 0.63}{\sqrt{8}}$$

And if we tidy the nominator and the denominator we get:

$$d = \frac{1.26}{2.8284271}$$

Which we can then solve to learn that $d = 0.45$

**Determining Significance**

If we were to look at a critical values look-up table for $df = 8$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 2.306$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 0.63$, is smaller than our $t_{crit}$ then we can say our result is non-significant, and as such would be written up as t(8) = 0.63, p > .05, d = 0.45

**Remember:** If you were writing this up as a report, and analysis the data in R, then you would see the p-value was actually p = 0.5462633, and would be written up as p =  0.548


</div>


### DataSet 2



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
   <td style="text-align:center;"> 47 </td>
   <td style="text-align:center;"> 66.18 </td>
   <td style="text-align:center;"> 1.79 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> B </td>
   <td style="text-align:center;"> 47 </td>
   <td style="text-align:center;"> 66.42 </td>
   <td style="text-align:center;"> 1.78 </td>
  </tr>
</tbody>
</table>



<div class='webex-solution'><button>Show me the working and answer</button>


Let's look at the main t-test formula:

$$t = \frac{\bar{X}_1 - \bar{X}_2}{s_p \times \sqrt{\frac{1}{N_1} + \frac{1}{N_2}}}$$

Now, from the table above we know:

* the mean of Group A is $\bar{X_1} = 66.18$, 
* the mean of Group B is $\bar{X_2} = 66.42$, 
* the N of Group A is $N_1 = 47$, 
* and the N of Group B is $N_2 = 47$, 

which we can put into the equation right now:

$$t = \frac{66.18 - 66.42}{s_p \times \sqrt{\frac{1}{47} + \frac{1}{47}}}$$

And now we can see that the only thing we don't yet know is the pooled standard deviation ($s_p$). Let's look at that formula:

$$s_p = \sqrt{\frac{(n_1 -1)  \times s^2_{X_1} + (n_2 -1)\times s^2_{X_2}}{n_1 + n_2 - 2}}$$

And if we start to fill in some details:

$$s_p = \sqrt{\frac{(47 -1)  \times s^2_{X_1} + (47 -1)\times s^2_{X_2}}{47 + 47 - 2}}$$

Now looking at the formula, it is clear we are missing:

* $s^2_{X_1}$ - the variance of Group A (could be written as $s^2_{A}$)
* $s^2_{X_2}$ - the variance of Group B (could be written as $s^2_{B}$) 

What we do know though, from the table, is the standard deviations of both groups ($SD_A$ = 1.79; $SD_B$ = 1.78), and we know that variance of a group is equal to the standard deviation squared. So:

* $s^2_{X_1}$ = $s^2_A$ = $SD_A \times SD_A$ = $1.79 \times 1.79$ = $3.2041$
* $s^2_{X_2}$ = $s^2_B$ = $SD_B \times SD_B$ = $1.78 \times 1.78$ = $3.1684$

And if we now add those values to our formula we get:

$$s_p = \sqrt{\frac{(47 -1)  \times 3.2041 + (47 -1)\times 3.1684}{47 + 47 - 2}}$$

And we can then start working through the formula, taking each stage in turn to make sure we don't make mistakes. Let's get rid of the brackets first:

$$s_p = \sqrt{\frac{(46  \times 3.2041) + (46 \times 3.1684)}{92}}$$

Now we deal with the multiplications:

$$s_p = \sqrt{\frac{147.3886 + 145.7464}{92}}$$

Let's tidy up that top half of the equation (the numerator):

$$s_p = \sqrt{\frac{293.135}{92}}$$

Which if we then divide the numerator by the denominator (the bottom half), and then take the square root of that we get:

$$s_p = \sqrt{3.18625}$$ 

Giving a pooled standard deviation of:

$$s_p = 1.785007$$

Meaning that our pooled standard deviation, rounded to three decimal places, is $s_p = 1.785$ and we can now add that to the t-test formula to give us:

$$t = \frac{66.18 - 66.42}{1.785 \times \sqrt{\frac{1}{47} + \frac{1}{47}}}$$

And again we just start working through the formula. Let's deal with the fractions relating to sample size first:

$$t = \frac{66.18 - 66.42}{1.785 \times \sqrt{0.0212766 + 0.0212766}}$$

Which we can tidy up a little to give:

$$t = \frac{-0.24}{1.785 \times \sqrt{0.0425532}}$$

And if we sort out the square root on the denominator we are left with:

$$t = \frac{-0.24}{1.785 \times 0.2062842}$$

We can then tidy up the denominator to give us:

$$t = \frac{-0.24}{0.3682174}$$

Which we can finally solve to give us a t-value, rounded to two decimal places, of $t = -0.65$

Great! Now we just need the degrees of freedom where the formula is:

$$df = (n_1 - 1) + (n_2 - 1)$$

And we already know that:

* the N of Group A is $N_1 = 47$, 
* and the N of Group B is $N_2 = 47$, 

So putting them into the equation we get:

$$df = (47 - 1) + (47 - 1)$$
$$df = 46 + 46$$
$$df = 92$$

And finally Cohen's d, the effect size:

$$d = \frac{2t}{\sqrt{df}}$$

Which, based on the info above, we know:

* $t = -0.65$
* $df = 92$

Putting them into the formula we get:

$$d = \frac{2 \times -0.65}{\sqrt{92}}$$

And if we tidy the nominator and the denominator we get:

$$d = \frac{-1.3}{9.591663}$$

Which we can then solve to learn that $d = -0.14$

**Determining Significance**

If we were to look at a critical values look-up table for $df = 92$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 1.986$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 0.65$, is smaller than our $t_{crit}$ then we can say our result is non-significant, and as such would be written up as t(92) = 0.65, p > .05, d = 0.14

**Remember:** If you were writing this up as a report, and analysis the data in R, then you would see the p-value was actually p = 0.517312, and would be written up as p =  0.513


</div>


### DataSet 3



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
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 31.80 </td>
   <td style="text-align:center;"> 0.42 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> B </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 32.18 </td>
   <td style="text-align:center;"> 0.57 </td>
  </tr>
</tbody>
</table>



<div class='webex-solution'><button>Show me the working and answer</button>


Let's look at the main t-test formula:

$$t = \frac{\bar{X}_1 - \bar{X}_2}{s_p \times \sqrt{\frac{1}{N_1} + \frac{1}{N_2}}}$$

Now, from the table above we know:

* the mean of Group A is $\bar{X_1} = 31.8$, 
* the mean of Group B is $\bar{X_2} = 32.18$, 
* the N of Group A is $N_1 = 8$, 
* and the N of Group B is $N_2 = 8$, 

which we can put into the equation right now:

$$t = \frac{31.8 - 32.18}{s_p \times \sqrt{\frac{1}{8} + \frac{1}{8}}}$$

And now we can see that the only thing we don't yet know is the pooled standard deviation ($s_p$). Let's look at that formula:

$$s_p = \sqrt{\frac{(n_1 -1)  \times s^2_{X_1} + (n_2 -1)\times s^2_{X_2}}{n_1 + n_2 - 2}}$$

And if we start to fill in some details:

$$s_p = \sqrt{\frac{(8 -1)  \times s^2_{X_1} + (8 -1)\times s^2_{X_2}}{8 + 8 - 2}}$$

Now looking at the formula, it is clear we are missing:

* $s^2_{X_1}$ - the variance of Group A (could be written as $s^2_{A}$)
* $s^2_{X_2}$ - the variance of Group B (could be written as $s^2_{B}$) 

What we do know though, from the table, is the standard deviations of both groups ($SD_A$ = 0.42; $SD_B$ = 0.57), and we know that variance of a group is equal to the standard deviation squared. So:

* $s^2_{X_1}$ = $s^2_A$ = $SD_A \times SD_A$ = $0.42 \times 0.42$ = $0.1764$
* $s^2_{X_2}$ = $s^2_B$ = $SD_B \times SD_B$ = $0.57 \times 0.57$ = $0.3249$

And if we now add those values to our formula we get:

$$s_p = \sqrt{\frac{(8 -1)  \times 0.1764 + (8 -1)\times 0.3249}{8 + 8 - 2}}$$

And we can then start working through the formula, taking each stage in turn to make sure we don't make mistakes. Let's get rid of the brackets first:

$$s_p = \sqrt{\frac{(7  \times 0.1764) + (7 \times 0.3249)}{14}}$$

Now we deal with the multiplications:

$$s_p = \sqrt{\frac{1.2348 + 2.2743}{14}}$$

Let's tidy up that top half of the equation (the numerator):

$$s_p = \sqrt{\frac{3.5091}{14}}$$

Which if we then divide the numerator by the denominator (the bottom half), and then take the square root of that we get:

$$s_p = \sqrt{0.25065}$$ 

Giving a pooled standard deviation of:

$$s_p = 0.5006496$$

Meaning that our pooled standard deviation, rounded to three decimal places, is $s_p = 0.501$ and we can now add that to the t-test formula to give us:

$$t = \frac{31.8 - 32.18}{0.501 \times \sqrt{\frac{1}{8} + \frac{1}{8}}}$$

And again we just start working through the formula. Let's deal with the fractions relating to sample size first:

$$t = \frac{31.8 - 32.18}{0.501 \times \sqrt{0.125 + 0.125}}$$

Which we can tidy up a little to give:

$$t = \frac{-0.38}{0.501 \times \sqrt{0.25}}$$

And if we sort out the square root on the denominator we are left with:

$$t = \frac{-0.38}{0.501 \times 0.5}$$

We can then tidy up the denominator to give us:

$$t = \frac{-0.38}{0.2505}$$

Which we can finally solve to give us a t-value, rounded to two decimal places, of $t = -1.52$

Great! Now we just need the degrees of freedom where the formula is:

$$df = (n_1 - 1) + (n_2 - 1)$$

And we already know that:

* the N of Group A is $N_1 = 8$, 
* and the N of Group B is $N_2 = 8$, 

So putting them into the equation we get:

$$df = (8 - 1) + (8 - 1)$$
$$df = 7 + 7$$
$$df = 14$$

And finally Cohen's d, the effect size:

$$d = \frac{2t}{\sqrt{df}}$$

Which, based on the info above, we know:

* $t = -1.52$
* $df = 14$

Putting them into the formula we get:

$$d = \frac{2 \times -1.52}{\sqrt{14}}$$

And if we tidy the nominator and the denominator we get:

$$d = \frac{-3.04}{3.7416574}$$

Which we can then solve to learn that $d = -0.81$

**Determining Significance**

If we were to look at a critical values look-up table for $df = 14$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 2.145$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 1.52$, is smaller than our $t_{crit}$ then we can say our result is non-significant, and as such would be written up as t(14) = 1.52, p > .05, d = 0.81

**Remember:** If you were writing this up as a report, and analysis the data in R, then you would see the p-value was actually p = 0.1507698, and would be written up as p =  0.144


</div>


## Look-Up table

Remembering that the $t_{crit}$ value is the smallest t-value you need to find a significant effect, find the $t_{crit}$ for your df, assuming $\alpha = .05$. If the $t$ value you calculated is equal to or larger than $t_{crit}$ then your test is significant.

|df | $\alpha = .05$|
|:-:|:-------------:|
|1  |12.706|
|2  |4.303|
|3  |3.182|
|4  |2.776|
|5  |2.571|
|6  |2.447|
|7  |2.365|
|8  |2.306|
|9  |2.262|
|10 |2.228|
|15 |2.131|
|20 |2.086|
|30 |2.042|
|40 |2.021|
|50 |2.009|
|60 |2|
|70 |1.994|
|80 |1.99|
|90 |1.987|
|100|1.984|
