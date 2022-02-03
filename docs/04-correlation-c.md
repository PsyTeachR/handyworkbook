# Spearman Correlation

**The Spearman correlation** otherwise known as the Spearman rank correlation coefficient measures the relationship between two variables when that relationship is monotonic. It can be used for relationships that are linear or non-linear. 

As in the Pearson Correlation, the Spearman correlation measures the covariance between two variables, or the shared variance, and then standardises that measure between the values of -1 and 1 with -1 being the perfect negative relationship and 1 being the perfect positive relationship.

The key difference between the Spearman Correlation and the Pearson Correlation is that the Spearman Correlation is based on the rank order of data - i.e. the raw data is converted to ordinal ranks.

If all of the ranks within each variable are unique - i.e. there are no <a class='glossary' title='when two or more values/observations within a variable are identical and assume the same rank order value'>tied ranks</a> - then the formula for the Spearman Correlation is as follows:

$$\rho = 1 - \frac{6 \times \sum{d_i^2}}{n(n^2-1)}$$
Let's start with a rather simple dataset of 10 participants measured on two scales, A and B. Here is our data:

<table>
 <thead>
  <tr>
   <th style="text-align:right;"> id </th>
   <th style="text-align:right;"> a </th>
   <th style="text-align:right;"> b </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 20 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 17 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 14 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 13 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 12 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 11 </td>
  </tr>
</tbody>
</table>

And to orientate ourselves a little, the table shows Participant 1 scored 11 for scale A and 20 for scale B, and Participant 2 scored 12 for scale A and 19 for scale B.

**Ranking data**

The first step in this analysis is to convert the data in both scales into their respective rank order starting from the smallest value in each scale. For example, the smallest value would get the rank of 1, the second smallest value would get the rank of 2, and so on and so on. If we do that with our data in scale A, we get the following:

<table>
 <thead>
  <tr>
   <th style="text-align:right;"> id </th>
   <th style="text-align:right;"> a </th>
   <th style="text-align:right;"> a_rank </th>
   <th style="text-align:right;"> b </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 20 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 17 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 14 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 13 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 12 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 11 </td>
  </tr>
</tbody>
</table>

And then do the same for the scores in scale b, again starting from the smallest value and giving it a rank of 1, and so on. This would look like:

<table>
 <thead>
  <tr>
   <th style="text-align:right;"> id </th>
   <th style="text-align:right;"> a </th>
   <th style="text-align:right;"> a_rank </th>
   <th style="text-align:right;"> b </th>
   <th style="text-align:right;"> b_rank </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 10 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 9 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 8 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 7 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 4 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

Now we have both scales in their respective rank orders, we can now calculate $d$, each individual participants difference between their ranks on the two scales. For example, with Participant 1, they have a rank of 1 on scale A, and a rank of 10 on scale B. This would give them a $d$ of 1 - 10 = -9

If we do that for all the participants we then get:

<table>
 <thead>
  <tr>
   <th style="text-align:right;"> id </th>
   <th style="text-align:right;"> a </th>
   <th style="text-align:right;"> a_rank </th>
   <th style="text-align:right;"> b </th>
   <th style="text-align:right;"> b_rank </th>
   <th style="text-align:right;"> d </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> -9 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> -7 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> -5 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> -3 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> -1 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 7 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 9 </td>
  </tr>
</tbody>
</table>

And finally we want to square each of those individual values to give us a $d^2$ for each participant. For example, Participant 1, with a value of d =-9, would have a $d^2$ of -9 $\times$ -9 = 81 

And if we do that for all the participants we then get:

<table>
 <thead>
  <tr>
   <th style="text-align:right;"> id </th>
   <th style="text-align:right;"> a </th>
   <th style="text-align:right;"> b </th>
   <th style="text-align:right;"> a_rank </th>
   <th style="text-align:right;"> b_rank </th>
   <th style="text-align:right;"> d </th>
   <th style="text-align:right;"> d^2 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> -9 </td>
   <td style="text-align:right;"> 81 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> -7 </td>
   <td style="text-align:right;"> 49 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> -5 </td>
   <td style="text-align:right;"> 25 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> -3 </td>
   <td style="text-align:right;"> 9 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> -1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 9 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 25 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 49 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 81 </td>
  </tr>
</tbody>
</table>

Now that we have calculated $d^2$ for each participant we can sum them altogether to give us $\sum{d_i^2}$ as follows:



$$\sum{d_i^2} = 81 + 49 + 25 + 9 + 1 + 1+ 9 + 25 + 49 + 81$$

Which gives us:

$$\sum{d_i^2} = 330$$

**The Correlation**

We can now return to our formula:

$$\rho = 1 - \frac{6 \times \sum{d_i^2}}{n(n^2-1)}$$

And we know that:

* $\sum{d_i^2} = 330$
* and $n = 10$

Which we can then put into our formula giving:

$$\rho = 1 - \frac{6 \times 330}{10(10^2-1)}$$

If we resolve the square in the bottom half of the formula, that gives:

$$\rho = 1 - \frac{6 \times 330}{10(100-1)}$$

And then subtract the 1, giving:

$$\rho = 1 - \frac{6 \times 330}{10(99)}$$
Now the bottom half can really be read as:

$$\rho = 1 - \frac{6 \times 330}{10 \times (99)}$$

Which, when we do the multiplication on the bottom half, gives us:

$$\rho = 1 - \frac{6 \times 330}{990}$$

And if we then do the multiplication on the top half, we get:

$$\rho = 1 - \frac{1980}{990}$$

We then divide the top half by the bottom half to give us:

$$\rho = 1 - 2$$

And we do the final subtraction, leaving us:

$$\rho = -1$$




Meaning that we have a Spearman rho of $\rho = -1$.  Following Cohen's (1988) proposed cut-offs shown below, would be considered to show a strong negative relationship. Remember that these cut-offs are just guides so a value just below a cut-off, e.g. r = .48, would probably be described as, for example, a strong positive relationship.

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

The standard APA format for writing up a Spearman correlation is usually:

<p align = "center">**$\rho$(df) = r-value, p = p-value**</p>

or alternatively

<p align = "center">**$r_s$(df) = r-value, p = p-value**</p>

From above we know the df and we know the r-value and what we need now is the significance.

**Determining Significance**

If we were to look at a critical values look-up table for $df = 8$ and $\alpha = .05$, we would see that the critical value is $r_{crit} = 0.632$. Given that our r-value, ignoring polarity and just looking at the absolute value, so $r = -1$, is equal to or larger than our $r_{crit}$ then we can say our result is significant, and as such would be written up as $r_s$(8) = -1, p < .05. 

**Remember:** If you were writing this up as a report, and analysed the data in R, then you would see the p-value was actually p = 0.00000000000000000000000000000000000000000000000000000000000001063504, and would be written up as p < .001

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
