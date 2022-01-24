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

**Degrees of Freedom**

$$df = \frac{\left(\frac{s^2_{x_1}}{n_1}+\frac{s^2_{x_2}}{n_2}\right)^2}{\frac{\left(\frac{s^2_{x_1}}{n_1}\right)^2}{n_1 - 1}+\frac{\left(\frac{s^2_{x_2}}{n_2}\right)^2}{n_2 - 1}}$$

