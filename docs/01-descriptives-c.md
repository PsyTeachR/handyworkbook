# Interval Estimates

We have so far looked at descriptives that take your whole dataset and summarise the center point of the data - **point estimates** - and whilst that is useful, it does not really tell you that much about your distribution. A more information aspect of your distribution to look at is the spread of the distribution - how wide is your drv3a and what values do most of your data fall between. Here we will look at four measures of spread. They are:

1. The Range
2. The Interquartile Range
3. The Variance
4. The Standard Deviation

In addition, we will look at:

* z-scores
* Standard Error of the Mean
* Confidence Intervals

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

### Test Yourself - Range



* DataSet1: $5, 4, 3, 1, 5, 4, 3, 3, 5, 1, 3, 3, 5, 4, 2$

1. What is the range of Dataset1: <select class='webex-select'><option value='blank'></option><option value=''>3</option><option value=''>5</option><option value='answer'>4</option></select>

---

## Variance

The symbol for the variance is generally written as $s^2$ (pronounced as sigma-squared) but can also be written as $Var$. The formula for the variance is:

$$s^2 = \frac{\sum_i^n(x_{i} - \overline{x})^2}{n-1}$$

And let's use the data from above but keep it a bit more simple by just using the first 10 participants:



$$7, 1, 2, 6, 3, 4, 3, 4, 3, 4$$

So let's again start by filling in the numbers to the formula:

$$s^2 = \frac{(7 - 3.7)^2 + (1 - 3.7)^2 + (2 - 3.7)^2 + (6 - 3.7)^2 + (3 - 3.7)^2 + \\(4 - 3.7)^2 + (3 - 3.7)^2 + (4 - 3.7)^2 + (3 - 3.7)^2 + (4 - 3.7)^2}{10 - 1}$$

And we do the subtractions in all those brackets of the top half and the one on the bottom:

$$s^2 = \frac{(3.3)^2 + (-2.7)^2 + (-1.7)^2 + (2.3)^2 + (-0.7)^2 + \\(0.3)^2 + (-0.7)^2 + (0.3)^2 + (-0.7)^2 + (0.3)^2}{9}$$

Then we square all those values on the top half:

$$s^2 = \frac{10.89 + 7.29+ 2.89+ 5.29+ 0.49+ 0.09+ 0.49+ 0.09+ 0.49+ 0.09}{9}$$

Sum those values together:

$$s^2 = \frac{28.1}{9}$$

And divide the top half by the bottom half:

$$s^2 = 3.1222222$$

Showing that the variance, rounded to two decimal places, is **$s^2 = 3.12$**

### Test Yourself - Variance

---

## Standard Deviation

The symbol for the standard deviation is generally written as $s$ (pronounced as sigma) but can also be written as $SD$. The formula for the standard deviation is:

$$s = \sqrt\frac{\sum_i^n(x_{i} - \overline{x})^2}{n-1}$$

So let's again start by filling in the numbers to the formula:

$$s = \sqrt\frac{(7 - 3.7)^2 + (1 - 3.7)^2 + (2 - 3.7)^2 + (6 - 3.7)^2 + (3 - 3.7)^2 + \\(4 - 3.7)^2 + (3 - 3.7)^2 + (4 - 3.7)^2 + (3 - 3.7)^2 + (4 - 3.7)^2}{10 - 1}$$

And we do the subtractions in all those brackets of the top half and the one on the bottom:

$$s = \sqrt\frac{(3.3)^2 + (-2.7)^2 + (-1.7)^2 + (2.3)^2 + (-0.7)^2 + \\(0.3)^2 + (-0.7)^2 + (0.3)^2 + (-0.7)^2 + (0.3)^2}{9}$$

Then we square all those values on the top half:

$$s = \sqrt\frac{10.89 + 7.29+ 2.89+ 5.29+ 0.49+ 0.09+ 0.49+ 0.09+ 0.49+ 0.09}{9}$$

Sum those values together:

$$s = \sqrt\frac{28.1}{9}$$
Divide the top half by the bottom half:

$$s = \sqrt{3.1222222}$$

And finally take the square root:

$$s = 1.7669811$$

We find that the standard deviation, rounded to two decimal places, is **$s = 1.77$**

### Test Yourself - Standard Deviation



### Var to SD

Remembering that the standard deviation is the square root of the variance, then if you know the variance ($s^2$) and you need the standard deviation ($s$) then you can do:

$$s = \sqrt{s^2}$$

In our example, $s^2 = 3.1222222$ and so

$$s = \sqrt{3.1222222}$$

giving:

$$s = 1.7669811$$

### SD to Var

Sometimes you need to go from the standard deviation to the variance, and remembering that the variance is the standard deviation squared, or the standard deviation multiplied by itself, then you can do:

$$s^2 = s \times s$$

And if we know that the standard deviation in our example is $s = 1.7669811$ then:

$$s^2 = 1.7669811 \times 1.7669811$$

giving us:

$$s^2 = 3.1222222$$
---

## z-scores

Any value on a continuous scale can be converted to a z-score (standard deviation units) through the formula:

$$z = \frac{x - \overline{x}}{s_{x}}$$

which can be read as the value ($x$) minus the mean value of the data ($\overline{x}$), divided by the standard deviation of the data ($s_{X}$).  For example, if we look at Participant 1:

* $x = 7$
* $\overline{x} = 3.7$
* $s_{x} = 1.7669811$

Which if we fill in the formula we get:

$$z = \frac{7 - 3.7}{1.7669811}$$

And if we sort our the top half first:

$$z = \frac{3.3}{1.7669811}$$

Leaving us with:

$$z = 1.8675921$$

So Participant 1, when converted to a z-score and rounded to two decimal places, would have **z = 1.87**

### Test Yourself - z-scores




* What would be 12 expressed as a z-score, assuming a sample with the following values, **M** = 15, **SD** = 1.5: <select class='webex-select'><option value='blank'></option><option value='answer'>-2</option><option value=''>1.24</option><option value=''>-1.67</option></select>
* What would be 8 expressed as a z-score, assuming a sample with the following values, **M** = 10, **SD** = 2: <select class='webex-select'><option value='blank'></option><option value=''>0.94</option><option value='answer'>-1</option><option value=''>-1.67</option></select>
* What would be 31 expressed as a z-score, assuming a sample with the following values, **M** = 28, **SD** = 3.2: <select class='webex-select'><option value='blank'></option><option value=''>1.24</option><option value=''>-2</option><option value='answer'>0.94</option></select>
* What would be 21.2 expressed as a z-score, assuming a sample with the following values, **M** = 19.1, **SD** = 1.7: <select class='webex-select'><option value='blank'></option><option value='answer'>1.24</option><option value=''>-1</option><option value=''>-2</option></select>
* What would be 3.8 expressed as a z-score, assuming a sample with the following values, **M** = 4, **SD** = 0.12: <select class='webex-select'><option value='blank'></option><option value='answer'>-1.67</option><option value=''>-1</option><option value=''>1.24</option></select>

## Standard Error of the Mean

The symbol for the standard error is usually $SE$ but can also be written as $SEM$ when specificaly about the mean - short for standard error of the mean.  The formula for the standard error is the standard deviation ($s$) divided by the square root of the number of observations ($\sqrt{n}$), and is written as:

$$SE = \frac{s}{\sqrt{n}}$$

but can also be written as:

$$SE = \frac{SD}{\sqrt{n}}$$

We know that our $SD = 1.7669811$ and that we have $n = 10$ participants, so:

$$SE = \frac{1.7669811}{\sqrt{10}}$$

And if we do the square root of the bottom half (denominator):

$$SE = \frac{1.7669811}{3.1622777}$$

And divide the top by the bottom:

$$SE = 0.5587685$$

We find that the standard error, rounded to two decimal places, is $SE = 0.56$

### Test Yourself - Standard Error



* Dataset1: **SD** = 10.44, **N** = 10
* Dataset2: **SD** = 5.7, **N** = 10
* Dataset3: **SD** = 9.13, **N** = 10
* Dataset4: **SD** = 8.84, **N** = 10
* Dataset5: **SD** = 8.15, **N** = 10

1. What is the SEM of Dataset1? <select class='webex-select'><option value='blank'></option><option value=''>1.54</option><option value=''>3.23</option><option value='answer'>3.3</option><option value=''>5.09</option></select>
2. What is the SEM of Dataset2? <select class='webex-select'><option value='blank'></option><option value='answer'>1.8</option><option value=''>2.82</option><option value=''>2.39</option><option value=''>4.69</option></select>
3. What is the SEM of Dataset3? <select class='webex-select'><option value='blank'></option><option value='answer'>2.89</option><option value=''>1.76</option><option value=''>1.89</option><option value=''>3.79</option></select>
4. What is the SEM of Dataset4? <select class='webex-select'><option value='blank'></option><option value=''>1.82</option><option value='answer'>2.8</option><option value=''>1.92</option><option value=''>3.51</option></select>
5. What is the SEM of Dataset5? <select class='webex-select'><option value='blank'></option><option value=''>4.17</option><option value='answer'>2.58</option><option value=''>1.98</option><option value=''>2</option></select>

---

## Confidence Intervals

We will specifically focus on the 95% Confidence Interval using the cut-off value (assuming $\alpha = .05$ and two-tailed) of $z = 1.96$. The key formulas are:

$$Upper \space 95\%CI = \overline{x} + (z \times SE)$$

$$Lower \space 95\%CI = \overline{x} - (z \times SE)$$

We know that:

* $\overline{x} = 3.7$
* $SE = 0.5587685$
* $z = 1.96$

**Upper 95% CI**

Dealing with the **Upper 95% CI** we get:

$$Upper \space 95\%CI = 3.7 + (1.96 \times 0.5587685)$$

And if we sort out the bracket first:

$$Upper \space 95\%CI = 3.7 + 1.0951862$$

Which leaves us with:

$$Upper \space 95\%CI = 4.7951862$$

**Lower 95% CI**

And now the **Lower 95% CI** we get:

$$Lower \space 95\%CI = 3.7 - (1.96 \times 0.5587685)$$

And if we sort out the bracket first:

$$Lower \space 95\%CI = 3.7 - 1.0951862$$

Which leaves us with:

$$Lower \space 95\%CI = 2.6048138$$

And if we round both those values to two decimal places, then you get **Lower 95%CI = 2.6** and **$Upper 95%CI = 4.8**. You will often see Confidence Intervals written up as 95%CI = [LowerCI, UpperCI], and so we could summarise our values as, 95%CI = [2.6, 4.8].

### Test Yourself - 95% Confidence Intervals

Below are the Means and Standard Errors of 5 datasets.



* Dataset 1: **M** = 16.1, **SE** = 3.3

1. What is the Upper 95% CI of DataSet 1? <select class='webex-select'><option value='blank'></option><option value=''>9.632</option><option value=''>7.932</option><option value='answer'>22.568</option><option value=''>28.468</option></select>
2. What is the Lower 95% CI of DataSet 1? <select class='webex-select'><option value='blank'></option><option value='answer'>9.632</option><option value=''>22.568</option><option value=''>7.932</option><option value=''>28.468</option></select>

* Dataset 2: **M** = 22, **SE** = 1.8

3. What is the Upper 95% CI of DataSet 2? <select class='webex-select'><option value='blank'></option><option value='answer'>28.468</option><option value=''>9.632</option><option value=''>7.932</option><option value=''>18.768</option></select>
4. What is the Lower 95% CI of DataSet 2? <select class='webex-select'><option value='blank'></option><option value=''>22.568</option><option value='answer'>15.532</option><option value=''>7.932</option><option value=''>18.768</option></select>

* Dataset 3: **M** = 14.4, **SE** = 2.89

5. What is the Upper 95% CI of DataSet 3? <select class='webex-select'><option value='blank'></option><option value=''>28.468</option><option value='answer'>20.868</option><option value=''>9.632</option><option value=''>10.932</option></select>
6. What is the Lower 95% CI of DataSet 3? <select class='webex-select'><option value='blank'></option><option value=''>10.932</option><option value='answer'>7.932</option><option value=''>28.468</option><option value=''>22.568</option></select>

* Dataset 4: **M** = 12.3, **SE** = 2.8

7. What is the Upper 95% CI of DataSet 4? <select class='webex-select'><option value='blank'></option><option value=''>7.932</option><option value=''>28.468</option><option value='answer'>18.768</option><option value=''>10.932</option></select>
8. What is the Lower 95% CI of DataSet 4? <select class='webex-select'><option value='blank'></option><option value='answer'>5.832</option><option value=''>7.932</option><option value=''>23.868</option><option value=''>28.468</option></select>


* Dataset 5: **M** = 17.4, **SE** = 2.58

9. What is the Upper 95% CI of DataSet 5? <select class='webex-select'><option value='blank'></option><option value='answer'>23.868</option><option value=''>22.568</option><option value=''>5.832</option><option value=''>7.932</option></select>
10. What is the Lower 95% CI of DataSet 5? <select class='webex-select'><option value='blank'></option><option value=''>18.768</option><option value=''>22.568</option><option value=''>7.932</option><option value='answer'>10.932</option></select>
