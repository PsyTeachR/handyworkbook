# Within-Subjects t-test

**within-subjects t-test:** Compare two conditions where the participants are the same in both conditions (or more rarely are different participants that have been highly matched on a number of demographics such as IQ, reading ability, etc - must be matched on a number of demographics).


## The Worked Example

Let's say that this is our starting data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> PreTest </th>
   <th style="text-align:center;"> PostTest </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 60 </td>
   <td style="text-align:center;"> 68 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 64 </td>
   <td style="text-align:center;"> 75 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 56 </td>
   <td style="text-align:center;"> 62 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 82 </td>
   <td style="text-align:center;"> 85 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 74 </td>
   <td style="text-align:center;"> 73 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 79 </td>
   <td style="text-align:center;"> 85 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 63 </td>
   <td style="text-align:center;"> 64 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 59 </td>
   <td style="text-align:center;"> 59 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> 73 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 66 </td>
   <td style="text-align:center;"> 70 </td>
  </tr>
</tbody>
</table>

The first thing we need to do is calculate the difference between the PostTest and the PreTest for each participant, based on $D = PostTest - PreTest$.  So for example:

* Participant 1 would be: 68 - 60 = 8
* Participant 2 would be: 75 - 64 = 11
* etc

And if we do that for each Participant and added a column of the differences ($D$) then we would see:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> PreTest </th>
   <th style="text-align:center;"> PostTest </th>
   <th style="text-align:center;"> D </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 60 </td>
   <td style="text-align:center;"> 68 </td>
   <td style="text-align:center;"> 8 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 64 </td>
   <td style="text-align:center;"> 75 </td>
   <td style="text-align:center;"> 11 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 56 </td>
   <td style="text-align:center;"> 62 </td>
   <td style="text-align:center;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 82 </td>
   <td style="text-align:center;"> 85 </td>
   <td style="text-align:center;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 74 </td>
   <td style="text-align:center;"> 73 </td>
   <td style="text-align:center;"> -1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 79 </td>
   <td style="text-align:center;"> 85 </td>
   <td style="text-align:center;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 63 </td>
   <td style="text-align:center;"> 64 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 59 </td>
   <td style="text-align:center;"> 59 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> 73 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 66 </td>
   <td style="text-align:center;"> 70 </td>
   <td style="text-align:center;"> 4 </td>
  </tr>
</tbody>
</table>

Now, the within-subjects t-test formula is:  

$$t = \frac{\bar{D}}{\frac{SD_{D}}{\sqrt{N}}}$$

We can see that $N = 10$, but we need to calculate $\bar{D}$ (called D-Bar, the mean of the $D$ column) and $SD_{D}$. 

**Calculating D-bar**

So the $\bar{D}$ formula is the same as the **mean** formula:

$$\bar{D} = \frac{\sum{D}}{N}$$

Where $D$ is $PostTest - PreTest$ for each Participant.

Then:

$$\bar{D} = \frac{(68 - 60) + (75 - 64) + (62 - 56) + (85 - 82) + (73 - 74) + \\ (85- 79) + (64 - 63) + (59 - 59) + (73 - 72) + (70 - 66)}{10}$$

Which if we resolve all the brackets becomes:

$$\bar{D} = \frac{8 + 11 + 6 + 3 + -1 + 6 + 1 + 0 + 1 + 4}{10}$$

And if we sum the top half together

$$\bar{D} = \frac{39}{10}$$

Leaving us with:

$$\bar{D} = 3.9$$

So we find that $\bar{D}$ = 3.9, which is the mean difference between the Post test and Pre test values.

**The Standard Deviation of D**




The standard deviation formula is:

$$SD = \sqrt\frac{\sum(X - \bar{X})^2}{N-1}$$

Which if we translate to using D, becomes:

$$SD_{D} = \sqrt\frac{\sum(D - \bar{D})^2}{N-1}$$

Then:

$$SD_{D} =\sqrt\frac{(8 - 3.9)^2 + (11 - 3.9)^2 + (6 - 3.9)^2 + (3 - 3.9)^2 + (-1 - 3.9)^2 + \\ (6 - 3.9)^2 + (1 - 3.9)^2 + (0 - 3.9)^2 + (1 - 3.9)^2 + (4 - 3.9)^2}{10 - 1}$$

And if we start stepping through this analysis by dealing with the brackets:

$$SD_{D} =\sqrt\frac{(4.1)^2 + (7.1)^2 + (2.1)^2 + (-0.9)^2 + (-4.9)^2 + \\ (2.1)^2 + (-2.9)^2 + (-3.9)^2 + (-2.9)^2 + (0.1)^2}{10 - 1}$$

And then we square those brackets

$$SD_{D} =\sqrt\frac{16.81 + 50.41 + 4.41 + 0.81 + 24.01 + 4.41 + 8.41 + 15.21 + 8.41 + 0.01}{10 - 1}$$

And sum up all the values on the top half:

$$SD_{D} =\sqrt\frac{132.9}{10 - 1}$$

And then we need to sort out the bottom half

$$SD_{D} =\sqrt\frac{132.9}{9}$$

Which by dividing the top half by the bottom half reduces down to:

$$SD_{D} =\sqrt{14.7666667}$$

And then we finally take the square root, which leaves us with:

$$SD_{D} =3.8427421$$



And so we find that the $SD_{D}$ = 3.8427421 which to two decimal places would be, $SD_{D} = 3.84$

**Calculating the t-value**

And finally the t-test formula is:

$$t = \frac{\bar{D}}{\frac{SD_{D}}{\sqrt{N}}}$$

Then if we start filling in the values we know from above we see:

$$t = \frac{3.9}{\frac{3.8427421}{\sqrt{10}}} $$

And if we deal with the square root first:

$$t = \frac{3.9}{\frac{3.8427421}{3.1622777}} $$

And divide $SD_{D}$ by $\sqrt{N}$ - tidying up the bottom of the formula:

$$t = \frac{3.9}{1.2151817} $$

And then solve for $t$ by dividing the top half by the bottom half gives us:

$$t = 3.2093965 $$

And so, rounding to two decimal places, we find that $t = 3.21$

**Degrees of Freedom**

Great! Now we just need the degrees of freedom where the formula is:

$$df = N - 1$$

And we already know that $N= 10$ and putting them into the equation we get:

$$df = 10 - 1$$

Which reduces to:

$$df = 9$$


Meaning that we find a $df = 9$

**Effect Size - Cohen's d**

And finally Cohen's d, the effect size. One of the common formulas based on knowing the t-value and the N is:

$$d = \frac{t}{\sqrt{N}}$$

Which, based on the info above, we know:

* $t = 3.21$
* $N = 10$

And putting those into the formula we get:

$$d = \frac{3.21}{\sqrt{10}}$$

Which gives us:

$$d = \frac{3.21}{3.1622777}$$

And so:

$$d = 1.0150911$$



Meaning that the effect size, to two decimal places, is d = 1.01.

**Determining Significance**

If we were to look at a critical values look-up table for $df = 9$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 2.262$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 3.21$, is equal to or larger than our $t_{crit}$ then we can say our result is significant, and as such would be written up as t(9) = 3.21, p < .05, d = 1.01. 

**Remember:** If you were writing this up as a report, and analysis the data in R, then you would see the p-value was actually p = 0.011, and would be written up as p =  0.011

## Test Yourself

### DataSet 1

Let's say that this is our starting data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> PreTest </th>
   <th style="text-align:center;"> PostTest </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 71 </td>
   <td style="text-align:center;"> 64 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 56 </td>
   <td style="text-align:center;"> 54 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 75 </td>
   <td style="text-align:center;"> 70 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 50 </td>
   <td style="text-align:center;"> 46 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 51 </td>
   <td style="text-align:center;"> 52 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 61 </td>
   <td style="text-align:center;"> 58 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 62 </td>
   <td style="text-align:center;"> 61 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> 74 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 66 </td>
   <td style="text-align:center;"> 60 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 78 </td>
   <td style="text-align:center;"> 78 </td>
  </tr>
</tbody>
</table>


<div class='webex-solution'><button>Show me the working and answer</button>


The first thing we need to do is calculate the difference between the PostTest and the PreTest for each participant, based on $D = PostTest - PreTest$.  So for example:

* Participant 1 would be: 64 - 71 = -7
* Participant 2 would be: 54 - 56 = -2
* etc

And if we do that for each Participant and added a column of the differences ($D$) then we would see:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> PreTest </th>
   <th style="text-align:center;"> PostTest </th>
   <th style="text-align:center;"> D </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 71 </td>
   <td style="text-align:center;"> 64 </td>
   <td style="text-align:center;"> -7 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 56 </td>
   <td style="text-align:center;"> 54 </td>
   <td style="text-align:center;"> -2 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 75 </td>
   <td style="text-align:center;"> 70 </td>
   <td style="text-align:center;"> -5 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 50 </td>
   <td style="text-align:center;"> 46 </td>
   <td style="text-align:center;"> -4 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 51 </td>
   <td style="text-align:center;"> 52 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 61 </td>
   <td style="text-align:center;"> 58 </td>
   <td style="text-align:center;"> -3 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 62 </td>
   <td style="text-align:center;"> 61 </td>
   <td style="text-align:center;"> -1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> 74 </td>
   <td style="text-align:center;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 66 </td>
   <td style="text-align:center;"> 60 </td>
   <td style="text-align:center;"> -6 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 78 </td>
   <td style="text-align:center;"> 78 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
</tbody>
</table>

Now, the within-subjects t-test formula is:  

$$t = \frac{\bar{D}}{\frac{SD_{D}}{\sqrt{N}}}$$

We can see that $N = 10$, but we need to calculate $\bar{D}$ (called D-Bar, the mean of the $D$ column) and $SD_{D}$. 

**Calculating D-bar**

So the $\bar{D}$ formula is the same as the **mean** formula:

$$\bar{D} = \frac{\sum{D}}{N}$$

Where $D$ is $PostTest - PreTest$ for each Participant.

Then:

$$\bar{D} = \frac{(64 - 71) + (54 - 56) + (70 - 75) + (46 - 50) + (52 - 51) + \\ (58- 61) + (61 - 62) + (74 - 72) + (60 - 66) + (78 - 78)}{10}$$

Which if we resolve all the brackets becomes:

$$\bar{D} = \frac{-7 + -2 + -5 + -4 + 1 + -3 + -1 + 2 + -6 + 0}{10}$$

And if we sum the top half together

$$\bar{D} = \frac{-25}{10}$$

Leaving us with:

$$\bar{D} = -2.5$$

So we find that $\bar{D}$ = -2.5, which is the mean difference between the Post test and Pre test values.

**The Standard Deviation of D**




The standard deviation formula is:

$$SD = \sqrt\frac{\sum(X - \bar{X})^2}{N-1}$$

Which if we translate to using D, becomes:

$$SD_{D} = \sqrt\frac{\sum(D - \bar{D})^2}{N-1}$$

Then:

$$SD_{D} =\sqrt\frac{(-7 - -2.5)^2 + (-2 - -2.5)^2 + (-5 - -2.5)^2 + (-4 - -2.5)^2 + \\ (1 - -2.5)^2 + (-3 - -2.5)^2 + (-1 - -2.5)^2 + (2 - -2.5)^2 + \\ (-6 - -2.5)^2 + (0 - -2.5)^2}{10 - 1}$$

And if we start stepping through this analysis by dealing with the brackets:

$$SD_{D} =\sqrt\frac{(-4.5)^2 + (0.5)^2 + (-2.5)^2 + (-1.5)^2 + (3.5)^2 + \\ (-0.5)^2 + (1.5)^2 + (4.5)^2 + (-3.5)^2 + (2.5)^2}{10 - 1}$$

And then we square those brackets

$$SD_{D} =\sqrt\frac{20.25 + 0.25 + 6.25 + 2.25 + 12.25 + \\ 0.25 + 2.25 + 20.25 + 12.25 + 6.25}{10 - 1}$$

And sum up all the values on the top half:

$$SD_{D} =\sqrt\frac{82.5}{10 - 1}$$

And then we need to sort out the bottom half

$$SD_{D} =\sqrt\frac{82.5}{9}$$

Which by dividing the top half by the bottom half reduces down to:

$$SD_{D} =\sqrt{9.1666667}$$

And then we finally take the square root, which leaves us with:

$$SD_{D} =3.0276504$$



And so we find that the $SD_{D}$ = 3.0276504 which to two decimal places would be, $SD_{D} = 3.03$

**Calculating the t-value**

And finally the t-test formula is:

$$t = \frac{\bar{D}}{\frac{SD_{D}}{\sqrt{N}}}$$

Then if we start filling in the values we know from above we see:

$$t = \frac{-2.5}{\frac{3.0276504}{\sqrt{10}}} $$

And if we deal with the square root first:

$$t = \frac{-2.5}{\frac{3.0276504}{3.1622777}} $$

And divide $SD_{D}$ by $\sqrt{N}$ - tidying up the bottom of the formula:

$$t = \frac{-2.5}{0.9574271} $$

And then solve for $t$ by dividing the top half by the bottom half gives us:

$$t = -2.6111648 $$

And so, rounding to two decimal places, we find that $t = -2.61$

**Degrees of Freedom**

Great! Now we just need the degrees of freedom where the formula is:

$$df = N - 1$$

And we already know that $N= 10$ and putting them into the equation we get:

$$df = 10 - 1$$

Which reduces to:

$$df = 9$$


Meaning that we find a $df = 9$

**Effect Size - Cohen's d**

And finally Cohen's d, the effect size. One of the common formulas based on knowing the t-value and the N is:

$$d = \frac{t}{\sqrt{N}}$$

Which, based on the info above, we know:

* $t = -2.61$
* $N = 10$

And putting those into the formula we get:

$$d = \frac{-2.61}{\sqrt{10}}$$

Which gives us:

$$d = \frac{-2.61}{3.1622777}$$

And so:

$$d = -0.8253545$$



Meaning that the effect size, to two decimal places, is d = -0.83.

**Determining Significance**

If we were to look at a critical values look-up table for $df = 9$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 2.262$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 2.61$, is equal to or larger than our $t_{crit}$ then we can say our result is not significant, and as such would be written up as t(9) = 2.61, p < .05, d = 0.83. 

**Remember:** If you were writing this up as a report, and analysis the data in R, then you would see the p-value was actually p = 0.028, and would be written up as p =  0.028





</div>


### DataSet 2

Let's say that this is our starting data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> PreTest </th>
   <th style="text-align:center;"> PostTest </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 73 </td>
   <td style="text-align:center;"> 72 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 60 </td>
   <td style="text-align:center;"> 54 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 53 </td>
   <td style="text-align:center;"> 52 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 74 </td>
   <td style="text-align:center;"> 74 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 58 </td>
   <td style="text-align:center;"> 54 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 55 </td>
   <td style="text-align:center;"> 52 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 54 </td>
   <td style="text-align:center;"> 49 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 57 </td>
   <td style="text-align:center;"> 58 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 59 </td>
   <td style="text-align:center;"> 60 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> 72 </td>
  </tr>
</tbody>
</table>


<div class='webex-solution'><button>Show me the working and answer</button>


The first thing we need to do is calculate the difference between the PostTest and the PreTest for each participant, based on $D = PostTest - PreTest$.  So for example:

* Participant 1 would be: 72 - 73 = -1
* Participant 2 would be: 54 - 60 = -6
* etc

And if we do that for each Participant and added a column of the differences ($D$) then we would see:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> PreTest </th>
   <th style="text-align:center;"> PostTest </th>
   <th style="text-align:center;"> D </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 73 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> -1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 60 </td>
   <td style="text-align:center;"> 54 </td>
   <td style="text-align:center;"> -6 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 53 </td>
   <td style="text-align:center;"> 52 </td>
   <td style="text-align:center;"> -1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 74 </td>
   <td style="text-align:center;"> 74 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 58 </td>
   <td style="text-align:center;"> 54 </td>
   <td style="text-align:center;"> -4 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 55 </td>
   <td style="text-align:center;"> 52 </td>
   <td style="text-align:center;"> -3 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 54 </td>
   <td style="text-align:center;"> 49 </td>
   <td style="text-align:center;"> -5 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 57 </td>
   <td style="text-align:center;"> 58 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 59 </td>
   <td style="text-align:center;"> 60 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
</tbody>
</table>

Now, the within-subjects t-test formula is:  

$$t = \frac{\bar{D}}{\frac{SD_{D}}{\sqrt{N}}}$$

We can see that $N = 10$, but we need to calculate $\bar{D}$ (called D-Bar, the mean of the $D$ column) and $SD_{D}$. 

**Calculating D-bar**

So the $\bar{D}$ formula is the same as the **mean** formula:

$$\bar{D} = \frac{\sum{D}}{N}$$

Where $D$ is $PostTest - PreTest$ for each Participant.

Then:

$$\bar{D} = \frac{(72 - 73) + (54 - 60) + (52 - 53) + (74 - 74) + (54 - 58) + \\ (52- 55) + (49 - 54) + (58 - 57) + (60 - 59) + (72 - 72)}{10}$$

Which if we resolve all the brackets becomes:

$$\bar{D} = \frac{-1 + -6 + -1 + 0 + -4 + -3 + -5 + 1 + 1 + 0}{10}$$

And if we sum the top half together

$$\bar{D} = \frac{-18}{10}$$

Leaving us with:

$$\bar{D} = -1.8$$

So we find that $\bar{D}$ = -1.8, which is the mean difference between the Post test and Pre test values.

**The Standard Deviation of D**




The standard deviation formula is:

$$SD = \sqrt\frac{\sum(X - \bar{X})^2}{N-1}$$

Which if we translate to using D, becomes:

$$SD_{D} = \sqrt\frac{\sum(D - \bar{D})^2}{N-1}$$

Then:

$$SD_{D} =\sqrt\frac{(-1 - -1.8)^2 + (-6 - -1.8)^2 + (-1 - -1.8)^2 + (0 - -1.8)^2 + \\ (-4 - -1.8)^2 + (-3 - -1.8)^2 + (-5 - -1.8)^2 + (1 - -1.8)^2 + \\ (1 - -1.8)^2 + (0 - -1.8)^2}{10 - 1}$$

And if we start stepping through this analysis by dealing with the brackets:

$$SD_{D} =\sqrt\frac{(0.8)^2 + (-4.2)^2 + (0.8)^2 + (1.8)^2 + (-2.2)^2 + \\ (-1.2)^2 + (-3.2)^2 + (2.8)^2 + (2.8)^2 + (1.8)^2}{10 - 1}$$

And then we square those brackets

$$SD_{D} =\sqrt\frac{0.64 + 17.64 + 0.64 + 3.24 + 4.84 + \\ 1.44 + 10.24 + 7.84 + 7.84 + 3.24}{10 - 1}$$

And sum up all the values on the top half:

$$SD_{D} =\sqrt\frac{57.6}{10 - 1}$$

And then we need to sort out the bottom half

$$SD_{D} =\sqrt\frac{57.6}{9}$$

Which by dividing the top half by the bottom half reduces down to:

$$SD_{D} =\sqrt{6.4}$$

And then we finally take the square root, which leaves us with:

$$SD_{D} =2.5298221$$



And so we find that the $SD_{D}$ = 2.5298221 which to two decimal places would be, $SD_{D} = 2.53$

**Calculating the t-value**

And finally the t-test formula is:

$$t = \frac{\bar{D}}{\frac{SD_{D}}{\sqrt{N}}}$$

Then if we start filling in the values we know from above we see:

$$t = \frac{-1.8}{\frac{2.5298221}{\sqrt{10}}} $$

And if we deal with the square root first:

$$t = \frac{-1.8}{\frac{2.5298221}{3.1622777}} $$

And divide $SD_{D}$ by $\sqrt{N}$ - tidying up the bottom of the formula:

$$t = \frac{-1.8}{0.8} $$

And then solve for $t$ by dividing the top half by the bottom half gives us:

$$t = -2.25 $$

And so, rounding to two decimal places, we find that $t = -2.25$

**Degrees of Freedom**

Great! Now we just need the degrees of freedom where the formula is:

$$df = N - 1$$

And we already know that $N= 10$ and putting them into the equation we get:

$$df = 10 - 1$$

Which reduces to:

$$df = 9$$


Meaning that we find a $df = 9$

**Effect Size - Cohen's d**

And finally Cohen's d, the effect size. One of the common formulas based on knowing the t-value and the N is:

$$d = \frac{t}{\sqrt{N}}$$

Which, based on the info above, we know:

* $t = -2.25$
* $N = 10$

And putting those into the formula we get:

$$d = \frac{-2.25}{\sqrt{10}}$$

Which gives us:

$$d = \frac{-2.25}{3.1622777}$$

And so:

$$d = -0.7115125$$



Meaning that the effect size, to two decimal places, is d = -0.71.

**Determining Significance**

If we were to look at a critical values look-up table for $df = 9$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 2.262$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 2.25$, is smaller than our $t_{crit}$ then we can say our result is not significant, and as such would be written up as t(9) = 2.25, p > .05, d = 0.71. 

**Remember:** If you were writing this up as a report, and analysis the data in R, then you would see the p-value was actually p = 0.051, and would be written up as p =  0.051




</div>


### DataSet 3

Let's say that this is our starting data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> PreTest </th>
   <th style="text-align:center;"> PostTest </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 62 </td>
   <td style="text-align:center;"> 56 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 75 </td>
   <td style="text-align:center;"> 72 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 56 </td>
   <td style="text-align:center;"> 55 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 80 </td>
   <td style="text-align:center;"> 79 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 55 </td>
   <td style="text-align:center;"> 55 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 70 </td>
   <td style="text-align:center;"> 69 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 79 </td>
   <td style="text-align:center;"> 79 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 50 </td>
   <td style="text-align:center;"> 52 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 51 </td>
   <td style="text-align:center;"> 49 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 78 </td>
   <td style="text-align:center;"> 77 </td>
  </tr>
</tbody>
</table>


<div class='webex-solution'><button>Show me the working and answer</button>

The first thing we need to do is calculate the difference between the PostTest and the PreTest for each participant, based on $D = PostTest - PreTest$.  So for example:

* Participant 1 would be: 56 - 62 = -6
* Participant 2 would be: 72 - 75 = -3
* etc

And if we do that for each Participant and added a column of the differences ($D$) then we would see:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> PreTest </th>
   <th style="text-align:center;"> PostTest </th>
   <th style="text-align:center;"> D </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 62 </td>
   <td style="text-align:center;"> 56 </td>
   <td style="text-align:center;"> -6 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 75 </td>
   <td style="text-align:center;"> 72 </td>
   <td style="text-align:center;"> -3 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 56 </td>
   <td style="text-align:center;"> 55 </td>
   <td style="text-align:center;"> -1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 80 </td>
   <td style="text-align:center;"> 79 </td>
   <td style="text-align:center;"> -1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 55 </td>
   <td style="text-align:center;"> 55 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 70 </td>
   <td style="text-align:center;"> 69 </td>
   <td style="text-align:center;"> -1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 79 </td>
   <td style="text-align:center;"> 79 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 50 </td>
   <td style="text-align:center;"> 52 </td>
   <td style="text-align:center;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 51 </td>
   <td style="text-align:center;"> 49 </td>
   <td style="text-align:center;"> -2 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 78 </td>
   <td style="text-align:center;"> 77 </td>
   <td style="text-align:center;"> -1 </td>
  </tr>
</tbody>
</table>

Now, the within-subjects t-test formula is:  

$$t = \frac{\bar{D}}{\frac{SD_{D}}{\sqrt{N}}}$$

We can see that $N = 10$, but we need to calculate $\bar{D}$ (called D-Bar, the mean of the $D$ column) and $SD_{D}$. 

**Calculating D-bar**

So the $\bar{D}$ formula is the same as the **mean** formula:

$$\bar{D} = \frac{\sum{D}}{N}$$

Where $D$ is $PostTest - PreTest$ for each Participant.

Then:

$$\bar{D} = \frac{(56 - 62) + (72 - 75) + (55 - 56) + (79 - 80) + (55 - 55) + \\ (69- 70) + (79 - 79) + (52 - 50) + (49 - 51) + (77 - 78)}{10}$$

Which if we resolve all the brackets becomes:

$$\bar{D} = \frac{-6 + -3 + -1 + -1 + 0 + -1 + 0 + 2 + -2 + -1}{10}$$

And if we sum the top half together

$$\bar{D} = \frac{-13}{10}$$

Leaving us with:

$$\bar{D} = -1.3$$

So we find that $\bar{D}$ = -1.3, which is the mean difference between the Post test and Pre test values.

**The Standard Deviation of D**




The standard deviation formula is:

$$SD = \sqrt\frac{\sum(X - \bar{X})^2}{N-1}$$

Which if we translate to using D, becomes:

$$SD_{D} = \sqrt\frac{\sum(D - \bar{D})^2}{N-1}$$

Then:

$$SD_{D} =\sqrt\frac{(-6 - -1.3)^2 + (-3 - -1.3)^2 + (-1 - -1.3)^2 + (-1 - -1.3)^2 + \\ (0 - -1.3)^2 + (-1 - -1.3)^2 + (0 - -1.3)^2 + (2 - -1.3)^2 + \\ (-2 - -1.3)^2 + (-1 - -1.3)^2}{10 - 1}$$

And if we start stepping through this analysis by dealing with the brackets:

$$SD_{D} =\sqrt\frac{(-4.7)^2 + (-1.7)^2 + (0.3)^2 + (0.3)^2 + (1.3)^2 + \\ (0.3)^2 + (1.3)^2 + (3.3)^2 + (-0.7)^2 + (0.3)^2}{10 - 1}$$

And then we square those brackets

$$SD_{D} =\sqrt\frac{22.09 + 2.89 + 0.09 + 0.09 + 1.69 + \\ 0.09 + 1.69 + 10.89 + 0.49 + 0.09}{10 - 1}$$

And sum up all the values on the top half:

$$SD_{D} =\sqrt\frac{40.1}{10 - 1}$$

And then we need to sort out the bottom half

$$SD_{D} =\sqrt\frac{40.1}{9}$$

Which by dividing the top half by the bottom half reduces down to:

$$SD_{D} =\sqrt{4.4555556}$$

And then we finally take the square root, which leaves us with:

$$SD_{D} =2.1108187$$



And so we find that the $SD_{D}$ = 2.1108187 which to two decimal places would be, $SD_{D} = 2.11$

**Calculating the t-value**

And finally the t-test formula is:

$$t = \frac{\bar{D}}{\frac{SD_{D}}{\sqrt{N}}}$$

Then if we start filling in the values we know from above we see:

$$t = \frac{-1.3}{\frac{2.1108187}{\sqrt{10}}} $$

And if we deal with the square root first:

$$t = \frac{-1.3}{\frac{2.1108187}{3.1622777}} $$

And divide $SD_{D}$ by $\sqrt{N}$ - tidying up the bottom of the formula:

$$t = \frac{-1.3}{0.6674995} $$

And then solve for $t$ by dividing the top half by the bottom half gives us:

$$t = -1.9475671 $$

And so, rounding to two decimal places, we find that $t = -1.95$

**Degrees of Freedom**

Great! Now we just need the degrees of freedom where the formula is:

$$df = N - 1$$

And we already know that $N= 10$ and putting them into the equation we get:

$$df = 10 - 1$$

Which reduces to:

$$df = 9$$


Meaning that we find a $df = 9$

**Effect Size - Cohen's d**

And finally Cohen's d, the effect size. One of the common formulas based on knowing the t-value and the N is:

$$d = \frac{t}{\sqrt{N}}$$

Which, based on the info above, we know:

* $t = -1.95$
* $N = 10$

And putting those into the formula we get:

$$d = \frac{-1.95}{\sqrt{10}}$$

Which gives us:

$$d = \frac{-1.95}{3.1622777}$$

And so:

$$d = -0.6166441$$



Meaning that the effect size, to two decimal places, is d = -0.62.

**Determining Significance**

If we were to look at a critical values look-up table for $df = 9$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 2.262$. Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 1.95$, is smaller than our $t_{crit}$ then we can say our result is not significant, and as such would be written up as t(9) = 1.95, p > .05, d = 0.62. 

**Remember:** If you were writing this up as a report, and analysis the data in R, then you would see the p-value was actually p = 0.083, and would be written up as p =  0.083



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
