
                                                                               #LINEAR Regression.

#Senario: A company is trying to understand the relationship between the number of years of experience and its employe’s salary. By analysing this relationship,the company hopes to be able to predict the salary of new hires based on their years of experience.


#Process:
## Data Table

The following table contains the raw data, deviations from the mean, product of deviations, and squared deviations for calculating the regression line.

| Mean of (X) | Mean of (Y) | Dev of (X) (xi - x̄) | Dev of (Y) (yi - ȳ) | Product of Deviation ((xi - x̄)(yi - ȳ)) | Sum of Product of Deviation (Σ (xi - x̄)(yi - ȳ)) | Square of Dev (X) ((xi - x̄)²) | Square of Dev (Y) ((yi - ȳ)²) |
|-------------|-------------|---------------------|---------------------|-----------------------------------------|--------------------------------------------------|------------------------------    -|-------------------------------|
| 2.32        | 48,675      | -1.22               | -9,332              | 11,885                                  | 56,063                                             | 1.4884                          | 87,086,724                    |
|             |             | -1.02               | -2,470              | 2,519                                   |                                                  | 1.0404                            | 6,100,900                     |
|             |             | -0.82               | -10,944             | 8,974                                   |                                                  | 0.6724                            | 119,771,936                   |
|             |             | -0.32               | -5,150              | 1,648                                   |                                                  | 0.1024                            | 26,522,500                    |
|             |             | -0.12               | -8,784              | 1,054                                   |                                                  | 0.0144                            | 77,158,656                    |
|             |             | 0.58                | 7,967               | 4,620                                   |                                                  | 0.3364                            | 63,473,089                    |
|             |             | 0.68                | 11,475              | 7,803                                   |                                                  | 0.4624                            | 131,675,625                   |
|             |             | 0.88                | 11,475              | 10,098                                  |                                                  | 0.7744                            | 131,675,625                   |
|             |             | 1.38                | 5,770               | 7,962                                   |                                                  | 1.9044                            | 33,292,900                    |


# Calculation Steps

# 1. Calculate the Slope (M)

The slope (M) represents the change in Y for every one-unit change in X.
The formula for the slope is:
$M = \frac{\text{Sum of Product of Deviation}}{\text{Sum of Square of Dev(X)}}$

Given:
* Sum of Product of Deviation = 56,063
* Sum of Square of Dev(X) = 6.7916

Calculation:
$M = \frac{56,063}{6.7916}$
$M = 8,254.75$

# 2. Calculate the Y-intercept (b)

The Y-intercept (b) is the value of Y when X is 0.
The formula for the Y-intercept is:
$b = \text{mean(Y)} - (M \times \text{mean(X)})$

Given:
* Mean of (Y) = 48,675
* Mean of (X) = 2.32
* Slope (M) = 8,254.75

Calculation:
$b = 48,675 - (8,254.75 \times 2.32)$
$b = 48,675 - 19,151$
$b = 29,524$

# 3. Linear Regression Equation

The simple linear regression equation is given by:
$Y = M \times X + b$

Substituting the calculated values of M and b:
$Y = 8,254.75 \times X + 29,524$

# 4. Predicting Salary for a Given Experience (Example)

# # # Let's predict the salary for an experience of 5.0 years.

Given:
* Experience (X) = 5.0 years

Calculation:
$\text{Salary} = 8,254.75 \times 5.0 + 29,524$
$\text{Salary} = 41,273.75 + 29,524$
$\text{Salary} = 70,797.75$

Therefore, the predicted salary for someone with 5.0 years of experience is $70,797.75.


                                                                           #


 

