# One-Sample Chi-Square

## The Worked Example



Here is our data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 15 </td>
  </tr>
</tbody>
</table>

And if we add on a column showing the total number of participants, adding all the numbers in the different conditions together, (i.e. 4 + 5 + 8 + 15 = 32),  then we get:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 15 </td>
   <td style="text-align:center;"> 32 </td>
  </tr>
</tbody>
</table>

Now the formula for the chi-square is:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

The Expected values for each condition, in a one-sample chi-square assuming a uniform (equal) distribution is calculated by $N \times \frac{1}{k}$ where $k$ is the number of conditions and $N$ is the total number of participants. This can also be written more straightforward as $N/k$. That means that in our example the expected value in each condition would be:

$$Expected = \frac{N}{k} = \frac{32}{4} = 8$$

Let's now add those Expected values to our table which looks like:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 15 </td>
   <td style="text-align:center;"> 32 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Expected </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 32 </td>
  </tr>
</tbody>
</table>

We now have our data, let's start putting it into the formula, which we said was:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

Which really means:

$$\chi^2 = \frac{(Observed_{A} - Expected_{A})^2}{Expected_{A}} + \frac{(Observed_{B} - Expected_{B})^2}{Expected_{B}} +  \frac{(Observed_{C} - Expected_{C})^2}{Expected_{C}} + \\ \frac{(Observed_{D} - Expected_{D})^2}{Expected_{D}}$$


So

$$\chi^2 = \frac{(4 - 8)^2}{8}+\frac{(5 - 8)^2}{8}+\frac{(8 - 8)^2}{8}+\frac{(15 - 8)^2}{8}$$

Which becomes:

$$\chi^2 = \frac{(-4)^2}{8} + \frac{(-3)^2}{8} + \frac{(0)^2}{8} + \frac{(7)^2}{8}$$

And if we now square the top halves (the numerators):

$$\chi^2 = \frac{16}{8} + \frac{9}{8} + \frac{0}{8} + \frac{49}{8}$$

Then divide the top half by the bottom half for each condition:

$$\chi^2 = {2}+{1.125}+{0}+{6.125}$$
And finally add them altogether

$$\chi^2 = 9.25$$

So we find that $\chi^2 = 9.25$

The degrees of freedom in this test is $k - 1$ and given that we have 4 conditions:

$$df = k - 1$$
$$df = 4 - 1$$
$$df = 3$$


**The effect size**

A common effect size for the one-sample chi-square test is $\phi$ (pronounced "ph-aye" and can be written as "phi"). The formula for $\phi$ is: 

$$\phi = \sqrt\frac{\chi^2}{N}$$

And if we know that $\chi^2 =9.25$ and that $N = 32$, then putting them into the formula we get:

$$\phi = \sqrt\frac{9.25}{32}$$

$$\phi = 0.5376453$$

**The write-up**

If we were to look at a critical value look-up table, we would see that the critical value associated with a $df = 3$ at $\alpha = .05$, to three decimal places, is $\chi^2_{crit} = 7.815$. As the chi-square value of this test (i.e. $\chi^2 = 9.25$) is larger than $\chi^2_{crit}$ then we can say that our test is significant, and as such would be written up as $\chi^2(df = 3, N = 32) = 9.25,p < .05$.

Finally, if our test was significant then all we need to do is state the condition with the highest frequency (i.e. the mode), which in this case is Condition D

## Test Yourself

### DataSet 1



Here is our data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 11 </td>
  </tr>
</tbody>
</table>



<div class='webex-solution'><button>Show me the working and answer</button>

And if we add on a column showing the total number of participants, adding all the numbers in the different conditions together, (i.e. 6 + 0 + 1 + 11 = 18),  then we get:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 18 </td>
  </tr>
</tbody>
</table>

Now the formula for the chi-square is:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

The Expected values for each condition, in a one-sample chi-square assuming a uniform (equal) distribution is calculated by $N \times \frac{1}{k}$ where $k$ is the number of conditions and $N$ is the total number of participants. This can also be written more straightforward as $N/k$. That means that in our example the expected value in each condition would be:

$$Expected = \frac{N}{k} = \frac{18}{4} = 4.5$$

Let's now add those Expected values to our table which looks like:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 6.0 </td>
   <td style="text-align:center;"> 0.0 </td>
   <td style="text-align:center;"> 1.0 </td>
   <td style="text-align:center;"> 11.0 </td>
   <td style="text-align:center;"> 18 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Expected </td>
   <td style="text-align:center;"> 4.5 </td>
   <td style="text-align:center;"> 4.5 </td>
   <td style="text-align:center;"> 4.5 </td>
   <td style="text-align:center;"> 4.5 </td>
   <td style="text-align:center;"> 18 </td>
  </tr>
</tbody>
</table>

We now have our data, let's start putting it into the formula, which we said was:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

So

$$\chi^2 = \frac{(6 - 4.5)^2}{4.5}+\frac{(0 - 4.5)^2}{4.5}+\frac{(1 - 4.5)^2}{4.5}+\frac{(11 - 4.5)^2}{4.5}$$

Which becomes:

$$\chi^2 = \frac{(1.5)^2}{4.5} + \frac{(-4.5)^2}{4.5} + \frac{(-3.5)^2}{4.5} + \frac{(6.5)^2}{4.5}$$

And if we now square the top halves (the numerators):

$$\chi^2 = \frac{2.25}{4.5} + \frac{20.25}{4.5} + \frac{12.25}{4.5} + \frac{42.25}{4.5}$$

Then divide the top half by the bottom half for each condition:

$$\chi^2 = {0.5}+{4.5}+{2.7222222}+{9.3888889}$$
And finally add them altogether

$$\chi^2 = 17.1111111$$

So we find that $\chi^2 = 17.1111111$

The degrees of freedom in this test is $k - 1$ and given that we have 4 conditions:

$$df = k - 1$$
$$df = 4 - 1$$
$$df = 3$$


**The effect size**

A common effect size for the one-sample chi-square test is $\phi$ (pronounced "ph-aye" and can be written as "phi"). The formula for $\phi$ is: 

$$\phi = \sqrt\frac{\chi^2}{N}$$

And if we know that $\chi^2 =17.1111111$ and that $N = 18$, then putting them into the formula we get:

$$\phi = \sqrt\frac{17.1111111}{18}$$

$$\phi = 0.974996$$

**The write-up**

If we were to look at a critical value look-up table, we would see that the critical value associated with a $df = 3$ at $\alpha = .05$, to three decimal places, is $\chi^2_{crit} = 7.815$. As the chi-square value of this test (i.e. $\chi^2 = 17.1111111$) is larger than $\chi^2_{crit}$ then we can say that our test is significant, and as such would be written up as $\chi^2(df = 3, N = 18) = 17.1111111,p < .05$.

Finally, if our test was significant then all we need to do is state the condition with the highest frequency (i.e. the mode), which in this case is Condition D


</div>


### DataSet 2



Here is our data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 12 </td>
   <td style="text-align:center;"> 16 </td>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 14 </td>
  </tr>
</tbody>
</table>



<div class='webex-solution'><button>Show me the working and answer</button>

And if we add on a column showing the total number of participants, adding all the numbers in the different conditions together, (i.e. 12 + 16 + 11 + 14 = 53),  then we get:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 12 </td>
   <td style="text-align:center;"> 16 </td>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 14 </td>
   <td style="text-align:center;"> 53 </td>
  </tr>
</tbody>
</table>

Now the formula for the chi-square is:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

The Expected values for each condition, in a one-sample chi-square assuming a uniform (equal) distribution is calculated by $N \times \frac{1}{k}$ where $k$ is the number of conditions and $N$ is the total number of participants. This can also be written more straightforward as $N/k$. That means that in our example the expected value in each condition would be:

$$Expected = \frac{N}{k} = \frac{53}{4} = 13.25$$

Let's now add those Expected values to our table which looks like:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 12.00 </td>
   <td style="text-align:center;"> 16.00 </td>
   <td style="text-align:center;"> 11.00 </td>
   <td style="text-align:center;"> 14.00 </td>
   <td style="text-align:center;"> 53 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Expected </td>
   <td style="text-align:center;"> 13.25 </td>
   <td style="text-align:center;"> 13.25 </td>
   <td style="text-align:center;"> 13.25 </td>
   <td style="text-align:center;"> 13.25 </td>
   <td style="text-align:center;"> 53 </td>
  </tr>
</tbody>
</table>

We now have our data, let's start putting it into the formula, which we said was:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

So

$$\chi^2 = \frac{(12 - 13.25)^2}{13.25}+\frac{(16 - 13.25)^2}{13.25}+\frac{(11 - 13.25)^2}{13.25}+\frac{(14 - 13.25)^2}{13.25}$$

Which becomes:

$$\chi^2 = \frac{(-1.25)^2}{13.25} + \frac{(2.75)^2}{13.25} + \frac{(-2.25)^2}{13.25} + \frac{(0.75)^2}{13.25}$$

And if we now square the top halves (the numerators):

$$\chi^2 = \frac{1.5625}{13.25} + \frac{7.5625}{13.25} + \frac{5.0625}{13.25} + \frac{0.5625}{13.25}$$

Then divide the top half by the bottom half for each condition:

$$\chi^2 = {0.1179245}+{0.5707547}+{0.3820755}+{0.0424528}$$
And finally add them altogether

$$\chi^2 = 1.1132075$$

So we find that $\chi^2 = 1.1132075$

The degrees of freedom in this test is $k - 1$ and given that we have 4 conditions:

$$df = k - 1$$
$$df = 4 - 1$$
$$df = 3$$


**The effect size**

A common effect size for the one-sample chi-square test is $\phi$ (pronounced "ph-aye" and can be written as "phi"). The formula for $\phi$ is: 

$$\phi = \sqrt\frac{\chi^2}{N}$$

And if we know that $\chi^2 =1.1132075$ and that $N = 53$, then putting them into the formula we get:

$$\phi = \sqrt\frac{1.1132075}{53}$$

$$\phi = 0.1449273$$

**The write-up**

If we were to look at a critical value look-up table, we would see that the critical value associated with a $df = 3$ at $\alpha = .05$, to three decimal places, is $\chi^2_{crit} = 7.815$. As the chi-square value of this test (i.e. $\chi^2 = 1.1132075$) is smaller than $\chi^2_{crit}$ then we can say that our test is non-significant, and as such would be written up as $\chi^2(df = 3, N = 53) = 1.1132075,p > .05$.

Finally, if our test was significant then all we need to do is state the condition with the highest frequency (i.e. the mode), which in this case is Condition B


</div>


### DataSet 3



Here is our data:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 20 </td>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 19 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
</tbody>
</table>



<div class='webex-solution'><button>Show me the working and answer</button>

And if we add on a column showing the total number of participants, adding all the numbers in the different conditions together, (i.e. 20 + 9 + 19 + 1 = 49),  then we get:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 20 </td>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 19 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 49 </td>
  </tr>
</tbody>
</table>

Now the formula for the chi-square is:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

The Expected values for each condition, in a one-sample chi-square assuming a uniform (equal) distribution is calculated by $N \times \frac{1}{k}$ where $k$ is the number of conditions and $N$ is the total number of participants. This can also be written more straightforward as $N/k$. That means that in our example the expected value in each condition would be:

$$Expected = \frac{N}{k} = \frac{49}{4} = 12.25$$

Let's now add those Expected values to our table which looks like:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Values </th>
   <th style="text-align:center;"> A </th>
   <th style="text-align:center;"> B </th>
   <th style="text-align:center;"> C </th>
   <th style="text-align:center;"> D </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> Observed </td>
   <td style="text-align:center;"> 20.00 </td>
   <td style="text-align:center;"> 9.00 </td>
   <td style="text-align:center;"> 19.00 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 49 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Expected </td>
   <td style="text-align:center;"> 12.25 </td>
   <td style="text-align:center;"> 12.25 </td>
   <td style="text-align:center;"> 12.25 </td>
   <td style="text-align:center;"> 12.25 </td>
   <td style="text-align:center;"> 49 </td>
  </tr>
</tbody>
</table>

We now have our data, let's start putting it into the formula, which we said was:

$$\chi^2 = \sum\frac{(Observed - Expected)^2}{Expected}$$

So

$$\chi^2 = \frac{(20 - 12.25)^2}{12.25}+\frac{(9 - 12.25)^2}{12.25}+\frac{(19 - 12.25)^2}{12.25}+\frac{(1 - 12.25)^2}{12.25}$$

Which becomes:

$$\chi^2 = \frac{(7.75)^2}{12.25} + \frac{(-3.25)^2}{12.25} + \frac{(6.75)^2}{12.25} + \frac{(-11.25)^2}{12.25}$$

And if we now square the top halves (the numerators):

$$\chi^2 = \frac{60.0625}{12.25} + \frac{10.5625}{12.25} + \frac{45.5625}{12.25} + \frac{126.5625}{12.25}$$

Then divide the top half by the bottom half for each condition:

$$\chi^2 = {4.9030612}+{0.8622449}+{3.7193878}+{10.3316327}$$
And finally add them altogether

$$\chi^2 = 19.8163265$$

So we find that $\chi^2 = 19.8163265$

The degrees of freedom in this test is $k - 1$ and given that we have 4 conditions:

$$df = k - 1$$
$$df = 4 - 1$$
$$df = 3$$


**The effect size**

A common effect size for the one-sample chi-square test is $\phi$ (pronounced "ph-aye" and can be written as "phi"). The formula for $\phi$ is: 

$$\phi = \sqrt\frac{\chi^2}{N}$$

And if we know that $\chi^2 =19.8163265$ and that $N = 49$, then putting them into the formula we get:

$$\phi = \sqrt\frac{19.8163265}{49}$$

$$\phi = 0.6359362$$

**The write-up**

If we were to look at a critical value look-up table, we would see that the critical value associated with a $df = 3$ at $\alpha = .05$, to three decimal places, is $\chi^2_{crit} = 7.815$. As the chi-square value of this test (i.e. $\chi^2 = 19.8163265$) is larger than $\chi^2_{crit}$ then we can say that our test is significant, and as such would be written up as $\chi^2(df = 3, N = 49) = 19.8163265,p < .05$.

Finally, if our test was significant then all we need to do is state the condition with the highest frequency (i.e. the mode), which in this case is Condition A


</div>


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
