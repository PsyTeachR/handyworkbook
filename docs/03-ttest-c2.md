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

$$t = \frac{25.58 - 29.07}{\sqrt{0.28125+0.3556056}}$$
$$t = \frac{25.58 - 29.07}{\sqrt{0.6368556}}$$

$$t = \frac{25.58 - 29.07}{0.7980323}$$

$$t = \frac{-3.49}{0.7980323}$$

$$t = -4.3732566$$


**Degrees of Freedom**

$$df = \frac{\left(\frac{s^2_{x_1}}{n_1}+\frac{s^2_{x_2}}{n_2}\right)^2}{\frac{\left(\frac{s^2_{x_1}}{n_1}\right)^2}{n_1 - 1}+\frac{\left(\frac{s^2_{x_2}}{n_2}\right)^2}{n_2 - 1}}$$
And we know from above that:

* the variance of Group A, $s^2_{x_1} = 5.0625$
* the variance of Group B, $s^2_{x_2} = 6.4009$
* the N of Group A, $n_1 = 18$
* and the N of Group B, $n_1 = 18$

And we can start to fill that in as follows:

$$df = \frac{\left(\frac{5.0625}{18}+\frac{6.4009}{18}\right)^2}{\frac{\left(\frac{5.0625}{18}\right)^2}{18 - 1}+\frac{\left(\frac{6.4009}{18}\right)^2}{18 - 1}}$$

$$df = \frac{\left(\frac{5.0625}{18}+\frac{6.4009}{18}\right)^2}{\frac{\left(0.28125\right)^2}{18 - 1}+\frac{\left(\frac{6.4009}{18}\right)^2}{18 - 1}}$$
$$df = \frac{\left(\frac{5.0625}{18}+\frac{6.4009}{18}\right)^2}{\frac{\left(0.28125\right)^2}{18 - 1}+\frac{\left(0.3556056\right)^2}{18 - 1}}$$

$$df = \frac{\left(\frac{5.0625}{18}+\frac{6.4009}{18}\right)^2}{\frac{\left(0.28125\right)^2}{17}+\frac{\left(0.3556056\right)^2}{17}}$$
$$df = \frac{\left(0.28125+0.3556056\right)^2}{\frac{\left(0.28125\right)^2}{17}+\frac{\left(0.3556056\right)^2}{17}}$$

$$df = \frac{0.6368556^2}{\frac{\left(0.28125\right)^2}{17}+\frac{\left(0.3556056\right)^2}{17}}$$

$$df = \frac{0.405585}{\frac{\left(0.28125\right)^2}{17}+\frac{\left(0.3556056\right)^2}{17}}$$
$$df = \frac{0.405585}{\frac{0.0791016}{17}+\frac{0.1264553}{17}}$$

$$df = \frac{0.405585}{0.004653+0.0074385}$$

$$df = \frac{0.405585}{0.0120916}$$

$$df = 33.5427605$$
