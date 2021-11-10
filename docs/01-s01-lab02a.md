# One-Sample t-test

**one-sample t-test:** Compare your sample mean to a known test value. For example, to compare your sample IQ to the population norm of 100.

## The Worked Example



The formula is as follows:

$$t = \frac{\bar{x} - \mu}{\frac{s}{\sqrt{n}}}$$
And you can translate the symbols as:

* $\bar{x}$ is the mean value of your sample of interest
* $\mu$ is the test value to compare against (also called the **criterion value**)
* $s$ is the standard deviation of your sample of interest
* $n$ is the number of observations (e.g. participants) in your sample of interest

So for example, if we had a sample of 25 people, and we knew that the mean and standard deviation of the IQ of was M = 110, SD = 7.5, and that we wanted to compare that sample to a criterion value of $\mu$ = 100, then we would do the following:

$$t = \frac{110  - 100}{\frac{7.5}{\sqrt{25}}}$$

And if we do the top half of the formula first, that becomes:

$$t = \frac{10}{\frac{7.5}{\sqrt{25}}}$$

And then start to complete the bottom half by taking the sqaure root of n first, (i.e. $\sqrt{n}$), we get:

$$t = \frac{10}{\frac{7.5}{5}}$$
And so if we then complete the bottom half by dividing the standard deviation of the sample ($s$) by the square root of n ($\sqrt{n}$), we get:

$$t = \frac{10}{1.5}$$

And finally, if we divide the top half of the formula by the bottom half we get:

$$t = \frac{10}{1.5} = 6.6666667$$

Giving us a t-value of t = 6.6666667 which we can round to two decimal places, giving us t = 6.67

## Degrees of Freedom

The degrees of freedom in a one-sample t-test is calculated as:

$$df = N - 1$$

And if we know that we have 25 participants in our sample then we get:

$$df = N - 1 = 25 - 1 = 24$$

Giving us $df$ = 24

## Effect Size

A common effect size used for t-test is Cohen's d. The formula for the effect size, in of a one-sample t-test, if you only know the t-value and the number of participants is:

$$d = \frac{t}{\sqrt{N}}$$

And here we know that:

* $t$ = 6.67
* $N$ = 25

Which if we put those into the formula we get:

$$d = \frac{6.67}{\sqrt{25}}$$
And if we resolve the bottom half first:

$$d = \frac{6.67}{5}$$

And then divide the top by the bottom we get:

$$d = \frac{6.67}{5} = 1.334$$

Giving us an effect size of $d$ = 1.33, rounded to two decimal places.

## Write-up

If we were to look at a critical values look-up table for $df = 24$ and $\alpha = .05$ (two-tailed), we would see that the critical value is $t_{crit} = 2.064$. 

Given that our t-value, ignoring polarity and just looking at the absolute value, so $t = 6.67$, is equal to or larger than our $t_{crit}$ then we can say our result is significant, and as such would be written up as t(24) = 6.67, p < .05, d = 1.33

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
