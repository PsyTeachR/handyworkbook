# One-Way Between-Subjects tables

This chapter is currently under development but will eventually show how to complete ANOVAs and ANOVA tables by hand.

## The ANOVA table

**One-Way Between-Subjects Scenario:** A research team are investigating the influence of mainstream media on life happiness. They record Life Happiness scores from 0 to 100 with higher scores meaning more happy with life from a large cohort of participants and split the participants into two groups; Group 1 (n = 72) and Group 2 (n = 81). The researchers want to check whether there is a difference between the two groups of participants in terms of Life Happiness. Calculate F from the below one-way ANOVA output table comparing mean Life Happiness scores across the two groups of participants and state whether there is a significant difference between the groups or not. The Sums of Squares ($SS$) have been given to you.



|Conditions|$SS$| $df$ |Mean Square|F-value
|:--------:|:-------------:|:---:|:---:|:---:|
|Between   |44.56||||
|Within    |2126.3||||
|Total     |2170.86||||

In order to complete the above table we need to:

* determine the degrees of freedom ($df$) of the Between and the Within components
* use the $df$ to calculate the Mean Squares ($MS$)
* use the Mean Squares to calculate the F-value

**Degrees of Freedom**

In an ANOVA there are two degrees of freedom. The first is the degrees of freedom related to the number of groups/conditions/models and is usually called $df_{Between}$, $df_{Condition}$, or $df_{Model}$. They all refer to the same idea. Regardless of what you call it, this df is calculated as:

$$df_{between} = k - 1$$

Where $k$ is the number of conditions or groups.

The second degrees of freedom is related to the number of participants/observations/data-points and is usually called $df_{Within}$ or $df_{Model}$; again both referring to the same idea. This df is calculated as:

$$df_{within} = N - k$$

Where $N$ is total number of participants in the whole experiment and $k$ is again the number of conditions or groups. The $df_{within}$ can also be phrased as the:

$$df_{within} = \sum_1^k(n_{k}-1)$$

Which can be read as taking 1 away from the $n$ in each group ($k$) and then summing those values together. For example, if you had a total of 20 participants in your experiment ($N = 20$) and they were split into 2 groups ($k = 2$) of 10 per group ($n = 10$), then you would do:

$$df_{within} = (10-1)+(10-1) = 18$$

But as that is the same as $N-k$ (i.e. 20 - 2 = 18), and $N-k$ is easier to think about, we will use that approach here. 

So, using those two formulas and the information given to us, first we see we have two groups. As such:

$$df_{between} = k - 1 = 2 - 1 = 1$$

Next we see that we have n = 72 in Group 1, and n = 81 in Group 2, meaning that we have a total number of participants of N = 72 + 81 = 153. And if we put that into the formula for the $df_{Within}$ we see:

$$df_{Within} = N-k = 153 - 2 = 151$$

Meaning that we have $df_{Between}$ = 1, and $df_{Within}$ = 151, and we can fill those into our table as such:

|Conditions|$SS$| $df$ |Mean Square|F-value
|:--------:|:-------------:|:---:|:---:|:---:|
|Between   |44.56|1|||
|Within    |2126.3|151|||
|Total     |2170.86||||

**Mean Squares**

Great! Now the next step is to calculate the Mean Square value for both the Between (i.e. Groups) and Within (i.e. Residuals) components. The Mean Square is really an abbreviation of the Mean Sums of Squares and is the Sums of Squares of a component divided by the degrees of freedom. Or in other words:

$$MS = \frac{SS}{df}$$

Looking at the table above we have all the information we need to calculate both the $MS_{Between}$ and the $MS_{Within}$. They would look like:

$$MS_{Between} = \frac{SS_{Between}}{df_{Between}} = \frac{44.56}{1} = 44.56$$

And

$$MS_{Within} = \frac{SS_{Within}}{df_{Within}} = \frac{2126.3}{151} = 14.081457$$

Meaning that we have $MS_{Between}$ = 44.56 and $MS_{Within}$ = 14.081457, which we can add in to our ANOVA table as such:

|Conditions|$SS$| $df$ |Mean Square|F-value|
|:--------:|:-------------:|:---:|:---:|:---:|
|Between   |44.56|1|44.56||
|Within    |2126.3|151|14.081457||
|Total     |2170.86||||

**The F-value**

Awesome. Finally, we need to calculate our F-value which is the ratio between the $MS_{Between}$ and $MS_{Within}$, and can be written as:

$$F = \frac{MS_{Between}}{MS_{Within}}$$

And so if we put our numbers in from above we see:

$$F = \frac{MS_{Between}}{MS_{Within}} = \frac{44.56}{14.081457} = 3.1644453$$

Giving us an F-value of F = 3.16 (to two decimal places), which we can now put into our table to complete our table as such:

|Conditions|$SS$| $df$ |Mean Square|F-value|
|:--------:|:-------------:|:---:|:---:|:---:|
|Between   |44.56|1|44.56|3.16|
|Within    |2126.3|151|14.081457||
|Total     |2170.86||||

**Effect size**

There are a few effect sizes that people use for the ANOVA with one of the more common ones being what is called partial eta-squared with the symbol $\eta_p^2$ (as $\eta$ is the symbol for "eta", and is pronounced "eat-ah", and the $_p^2$ indicating "partial" and "squared"). The formula for partial eta-squared is:

$$\eta_{p^2} = \frac{SS_{Between}}{SS_{Between}+SS_{Within}}$$

From above, we know that:

* $SS_{Between}$ = 44.56 and
* $SS_{Within}$ = 2126.3

And if we start to fill those into the formula we see:

$$\eta_p^2 = \frac{44.56}{44.56 + 2126.3} = \frac{44.56}{2170.86} = 0.0205264$$

Meaning that this analysis has an effect size of $\eta_p^2$ = 0.02 (to two decimal places).

**The Write-UP**

The standard APA format for writing up an ANOVA is usually:

<p align = "center">**F($df_{Between}$, $df_{Within}$) = F-value, p = p-value, $\eta_p^2$ = effectsize-value**</p>

From above we know the two dfs and we know the F-value and the effect size, so what we need now is to determine the significance.

**Determining Significance**

If we were to look at a critical values look-up table for $df_{Between}$ = 1, $df_{Within}$ = 151, and $\alpha = .05$, we would see that the closest we have is for $df_{Between}$ = 1, $df_{Within}$ = 100, which has a critical value of $F_{crit}$ = 3.94. Given that our F-value is smaller than our $F_{crit}$ then we can say our result is not significant, and as such would be written up as F(1, 151) = 3.16, p > .05, $\eta_p^2$ = 0.02. 

**Remember:** If you were writing this up as a report, and analysed the data in R, then you would see the p-value was actually p = 0.07747604, and would be written up as p =  0.077

## Look-Up table

Remembering that the $F_{crit}$ value is the smallest F-value you need to find a significant effect, find the $F_{crit}$ for your dfs, assuming $\alpha = .05$. If the $F$-value you calculated is equal to or larger than $F_{crit}$ then your test is significant. In this table, to fit it on to the page, $df_{Between}$ is written as df1, and $df_{Within}$ is written as df2.

|dfs|df1 = 1|df1 = 2|df1 = 3|df1 = 4|df1 = 5|
|:-:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
|**df2 = 1**|161.448|199.5|215.707|224.583|230.162|
|**df2 = 2**|18.513|19|19.164|19.247|19.296|
|**df2 = 3**|10.128|9.552|9.277|9.117|9.013|
|**df2 = 4**|7.709|6.944|6.591|6.388|6.256|
|**df2 = 5**|6.608|5.786|5.409|5.192|5.05|
|**df2 = 10**|4.965|4.103|3.708|3.478|3.326|
|**df2 = 15**|4.543|3.682|3.287|3.056|2.901|
|**df2 = 20**|4.351|3.493|3.098|2.866|2.711|
|**df2 = 25**|4.242|3.385|2.991|2.759|2.603|
|**df2 = 30**|4.171|3.316|2.922|2.69|2.534|
|**df2 = 40**|4.085|3.232|2.839|2.606|2.449|
|**df2 = 50**|4.034|3.183|2.79|2.557|2.4|
|**df2 = 60**|4.001|3.15|2.758|2.525|2.368|
|**df2 = 70**|3.978|3.128|2.736|2.503|2.346|
|**df2 = 80**|3.96|3.111|2.719|2.486|2.329|
|**df2 = 90**|3.947|3.098|2.706|2.473|2.316|
|**df2 = 100**|3.936|3.087|2.696|2.463|2.305|

