# Interval Estimates

We have so far looked at descriptives that take your whole dataset and summarise the center point of the data - **point estimates** - and whilst that is useful, it does not really tell you that much about your distribution. A more information aspect of your distribution to look at is the spread of the distribution - how wide is your data and what values do most of your data fall between. Here we will look at four measures of spread. They are:

1. The Range
2. The Interquartile Range
3. The Variance
4. The Standard Deviation

## The Range




The Range is the most basic and least informative measure of the spread of your data as really it only tells you the distance between the largest value and the smallest value in your data set. You never really see the formula for the range but it can be written as:

$$Range(X) = max(X) - min(X)$$
And is read as the maximum value in your dataset ($max(X)$) minus the minimum value in your dataset ($min(X)$). So if we look at our driving data again:

$$7, 1, 2, 6, 3, 4, 3, 4, 3, 4, 5, 4, 7, 5, 6, 5, 5, 4, 5, 6, 5, 6, 3, 2, 5$$
Then we can see that our largest value here is 7 and the smallest value is 1, so if we put those into our formula we get:

$$Range(X) = max(X) - min(X) = 7 - 1 = 6$$
Meaning that this dataset has a range of **Range = 6**.  It is worth pointing out that it doesn't matter how many people have the largest value or the smallest value for that matter, just that those are the smallest and largest values.

The range however can be deceptive as it is heavily influenced by <a class='glossary' target='_blank' title='A data point that is extremely distant from most of the other data points' href='https://psyteachr.github.io/glossary/o#outlier'>outliers</a>. Look at this data for example:



$$7, 1, 2, 6, 3, 4, 3, 4, 3, 4, 5, 4, 30, 5, 6, 5, 5, 4, 5, 6, 5, 6, 3, 2, 5$$
Here we can see that our largest value here is 30 and the smallest value is 1, so if we put those into our formula we get:

$$Range(X) = max(X) - min(X) = 30 - 1 = 29$$

Meaning that this dataset has a range of **Range = 29** which probably doesn't really reflect the spread of the data that well as only one data point is really large. That is why the range is informative to state but not that great for doing analyses on.






## Section glossary

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> term </th>
   <th style="text-align:left;"> definition </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> [outlier](https://psyteachr.github.io/glossary/o.html#outlier){class="glossary" target="_blank"} </td>
   <td style="text-align:left;"> A data point that is extremely distant from most of the other data points </td>
  </tr>
</tbody>
</table>

