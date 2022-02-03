# A full descriptive

To look at a full descriptive example including the mean, standard deviation, standard error, 95% Confidence Intervals, and z-scores, we will use the following data from 10 participants:

<table>
 <thead>
  <tr>
   <th style="text-align:center;"> Participants </th>
   <th style="text-align:center;"> X </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 8 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 11 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 4 </td>
  </tr>
</tbody>
</table>

### The Mean

We know the formula for the mean is:

$$\overline{X} = \frac{\sum_i^n{x_i}}{n}$$

If we start to fill in the information from above we get:

$$\overline{X} = \frac{8 + 11 + 6 +3 +1 +6 +1 +0 +1 +4}{10}$$

And if we sum all the values on the top half together we get:

$$\overline{X} = \frac{41}{10}$$

And finally divide the top half by the bottom half, leaving:

$$\overline{X} = 4.1$$

We find that the mean, rounded to two decimal places, is **$\overline{X} = 4.1$**

### Standard Deviation

Next we want an interval estimate, most commonly the standard deviation. The formula for the standard deviation is:

$$s = \sqrt\frac{\sum_i^n(x_{i} - \overline{x})^2}{n-1}$$
So let's again start by filling in the numbers to the formula:

$$s = \sqrt\frac{(8 - 4.1)^2 + (11 - 4.1)^2 + (6 - 4.1)^2 + (3 - 4.1)^2 + (1 - 4.1)^2 + \\(6 - 4.1)^2 + (1 - 4.1)^2 + (0 - 4.1)^2 + (1 - 4.1)^2 + (4 - 4.1)^2}{10 - 1}$$

And we do the subtractions in all those brackets of the top half and the one on the bottom:

$$s = \sqrt\frac{(3.9)^2 + (6.9)^2 + (1.9)^2 + (-1.1)^2 + (-3.1)^2 + \\(1.9)^2 + (-3.1)^2 + (-4.1)^2 + (-3.1)^2 + (-0.1)^2}{9}$$

Then we square all those values on the top half:

$$s = \sqrt\frac{15.21 + 47.61+ 3.61+ 1.21+ 9.61+ 3.61+ 9.61+ 16.81+ 9.61+ 0.01}{9}$$

Sum those values together:

$$s = \sqrt\frac{116.9}{9}$$
Divide the top half by the bottom half:

$$s = \sqrt{12.9888889}$$

And finally take the square root:

$$s = 3.6040101$$

We find that the standard deviation, rounded to two decimal places, is **$s = 3.6$**

### Standard Error of the Mean

We also want to include a measure of how our sample relates to the population of interest and to do that we can use the Standard Error of the Mean and 95% Confidence Intervals. The formula for the standard error can be written as:

$$SE = \frac{SD}{\sqrt{n}}$$

We know that our $SD = 3.6040101$ and that we have $n = 10$ participants, so:

$$SE = \frac{3.6040101}{\sqrt{10}}$$

And if we do the square root of the bottom half (denominator):

$$SE = \frac{3.6040101}{3.1622777}$$

And divide the top by the bottom:

$$SE = 1.1396881$$

We find that the standard error, rounded to two decimal places, is $SE = 1.14$

### Confidence Intervals

And we can use the standard error not to calculate the Upper and Lower 95% Confidence Intervals using the cut-off value (assuming $\alpha = .05$ and two-tailed) of $z = 1.96$. The key formulas are:

$$Upper \space 95\%CI = \overline{x} + (z \times SE)$$

And

$$Lower \space 95\%CI = \overline{X} - (z \times SE)$$

We know that:

* $\overline{x} = 4.1$
* $SE = 1.1396881$
* $z = 1.96$

**Upper 95% CI**

Dealing with the **Upper 95% CI** we get:

$$Upper \space 95\%CI = 4.1 + (1.96 \times 1.1396881)$$

And if we sort out the bracket first:

$$Upper \space 95\%CI = 4.1 + 2.2337886$$

Which leaves us with:

$$Upper \space 95\%CI = 6.3337886$$

**Lower 95% CI**

And now the **Lower 95% CI** we get:

$$Lower \space 95\%CI = 4.1 - (1.96 \times 1.1396881)$$

And if we sort out the bracket first:

$$Lower \space 95\%CI = 4.1 - 2.2337886$$

Which leaves us with:

$$Lower \space 95\%CI = 1.8662114$$

And if we round both those values to two decimal places, then you get **Lower 95%CI = 1.87** and **Upper 95%CI = 6.33**

### The Write-Up

And if we were to do a decent presentation of this data, including a measure of central tendency (the mean), a measure of spread relating to the sample (the standard deviation), and a measure of spread relating to the population (the 95% CI), then it would start as something like: **"We ran 10 participants (M = 4.1, SD = 3.6, 95%CI = [1.87, 6.33])....."**
