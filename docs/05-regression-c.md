# Multiple Linear Regression

Let's say we want to make a prediction about the following four people who have these scores on the five OCEAN scales:

|    |Openness|Conscientousness|Extraversion|Agreeableness|Neuroticism|
|---|:---:|:---:|:---:|:---:|:---:|
|Participant 1| 9 | 8 | 6 | 6 | 5 |
|Participant 2| 8 | 9 | 5 | 5 | 6 |
|Participant 3| 5 | 6 | 8 | 8 | 9 |
|Participant 4| 5 | 6 | 9 | 9 | 8 |

And let's say we have this output from the multiple linear regression model we created using all of the five OCEAN scales as predictors:




|    |Unstandardised Coefficient|t-value|p-value|
|---|:---:|:---:|:---:|
|Intercept|197.65|22.43|.0001|
|Openness|-5.28|-7.68|.0001|
|Conscientiousness|-5.68|-7.44|.0001|
|Extraversion|-0.4|-0.65|.522|
|Agreeableness|0.64|0.69|.495|
|Neuroticism|1.89|2.56|.014|
|---|---|---|---|
|Multiple R^2^| .7619| Adjusted R^2^|.7348|
|F-statistic|28.16 on 5 and 44 DF| p-value| .001|

## Making a Prediction

Now based on the information we have gained above we can actually use that to make predictions about a person we have not measured based on the formula:

$$\hat{Y} = b_{0} + b_{1}X_{1} + b_{2}X_{2} + b_{3}X_{3} + b_{4}X_{4} + b_{5}X_{5}$$

Well technically it is 

$$\hat{Y} = b_{0} + b_{1}X_{1} + b_{2}X_{2} + b_{3}X_{3} + b_{4}X_{4} + b_{5}X_{5} + error$$

But we will disregard the error for now. Also you might have noticed the small hat about the $Y$ making it $\hat{Y}$ (pronounced Y-hat). This means we are making a prediction of Y ($\hat{Y}$) as opposed to an actually measured (i.e. observed) value ($Y$).

And to break that formula down a bit we can say:

* $b_{0}$ is the intercept of the model
* $b_{1}X_{1}$, for example, is read at the non-standardised coeffecient of the first predictor $b_{1}$ multiplied by the measured value of the first predictor $X_{1}$
* $b_{1}$, $b_{2}$, $b_{3}$, $b_{4}$, $b_{5}$ are the non-standardised coefficient values of the different predictors in the model. There is one non-standardised coefficient for each predictor. For example, let's say Openness is our first predictor and as such $b_{1}$ = -5.28
* $X_{1}$, $X_{2}$, $X_{3}$, $X_{4}$, $X_{5}$ are the measured values of the different predictors for a participant. For example, for Participant 1, again assuming Openness is our first predictor, then $X_{1}$ = 9. If Conscientousness is our second predictor, Extraversion our third predictor, Agreeableness our fourth predictor, and Neuroticism our fifth predictor, then $X_{2}$ = 8, $X_{3}$ = 5 and $X_{4}$ = 5.

Then, using the information above, we know can start to fill in the information for **Participant 1** as follows:

$$\hat{Y} = 197.65 + (-5.28 \times 9) + (-5.68 \times 8) + (-0.4 \times 6) + (0.64 \times 6) + (1.89 \times 5)$$

And if we start to work that through, dealing with the multiplications first, we see:

$$\hat{Y} = 197.65 + (-47.52) + (-45.44) + (-2.4) + (3.84) + (9.45)$$

Which then becomes:

$$\hat{Y} = 115.58$$

Giving a predicted value of $\hat{Y}$ = 115.58, to two decimal places. 

Likewise for **Participant 2** we would have:

$$\hat{Y} = 197.65 + (-5.28 \times 8) + (-5.68 \times 9) + (-0.4 \times 5) + (0.64 \times 5) + (1.89 \times 6)$$

And if we start to work that through, dealing with the multiplications first, we see:

$$\hat{Y} = 197.65 + (-42.24) + (-51.12) + (-2) + (3.2) + (11.34)$$

Which then becomes:

$$\hat{Y} = 116.83$$

Giving a predicted value of $\hat{Y}$ = 116.83, to two decimal places. 

Likewise for **Participant 3** we would have:

$$\hat{Y} = 197.65 + (-5.28 \times 5) + (-5.68 \times 6) + (-0.4 \times 8) + (0.64 \times 8) + (1.89 \times 9)$$

And if we start to work that through, dealing with the multiplications first, we see:

$$\hat{Y} = 197.65 + (-26.4) + (-34.08) + (-3.2) + (5.12) + (17.01)$$

Which then becomes:

$$\hat{Y} = 156.1$$

Giving a predicted value of $\hat{Y}$ = 156.1, to two decimal places. 

And finally for **Participant 4** we would have:

$$\hat{Y} = 197.65 + (-5.28 \times 5) + (-5.68 \times 6) + (-0.4 \times 9) + (0.64 \times 9) + (1.89 \times 8)$$

And if we start to work that through, dealing with the multiplications first, we see:

$$\hat{Y} = 197.65 + (-26.4) + (-34.08) + (-3.6) + (5.76) + (15.12)$$

Which then becomes:

$$\hat{Y} = 154.45$$

Giving a predicted value of $\hat{Y}$ = 154.45, to two decimal places. 

And so in summary, based on our above model, and the above measured values, we would predict the following values:

* Participant 1, $\hat{Y}$ = 115.58  
* Participant 2, $\hat{Y}$ = 116.83
* Participant 3, $\hat{Y}$ = 156.1
* Participant 4, $\hat{Y}$ = 154.45

