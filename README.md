# MechaCar_Statistical_Analysis

# Overview

# Analysis

## Linear Regression to Predict MPG

*Summary Here*

Linear Regression:

![Linear Regression](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/MechaCar_linear_regression.png?raw=true)

Linear Regression Summary:

![Linear Regression Summary](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/MechaCar_summary.png?raw=true)

- Looking at the Linear Regression Summary from the Pr(>|t|) column we can see vehicle length and vehicle ground clearance produced very small values. This means both vehicle length and ground clearance are likely variables that have provided a non-random amount of variance to the mpg values in the dataset.

- We could consider the slope for this linear model to be non zero. This is because the summary returned a p-value of 5.35e-11 which is far below an assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis.

- From the results of the linear regression summary, we notice that this model has an r-squared value of 0.7149. This means that approximately 71% of all mpg predictions can be determined by this model and can effectively predict mpg of MechaCar prototypes to about 71% certainty.

## Summary Statistics on Suspension Coils

In this section we will be preforming 

Null hypothesis: The sample mean of the pounds per square inch for the MechaCar suspension coils is equal to 1,500 psi

Alternative hypothesis: The sample mean of the pounds per square inch for the MechaCar suspension coils is not equal to 1,500 psi

Total Summary:

![Total Summary](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/total_summary.png?raw=true)

Lot Summary:

![Lot Summary](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/lot_summary.png?raw=true)

- From the total population summary we can notice that, as a whole the variance of the MechaCar suspension coils is approximately 62.29 pounds per square inch(psi). This falls under the design specifications which state that the variance of the suspension coils must not exceed 100 pounds per square inch. Although, when we take a closer look at the summary broken down by each lot, we notice that Lot 3 has a very high variance of approximately 170.29 psi, where Lots 1 and 2 both have variance less than 8 psi. This means Lot 3 that is disproportionately causing a higher variance of the full population of MechaCar prototypes.

## T-Tests on Suspension Coils

In this section we are performing a series of T-test on the total population, as well as each individual lot to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

Null hypothesis: The sample mean of the pounds per square inch for the MechaCar suspension coils is equal to 1,500 psi

Alternative hypothesis: The sample mean of the pounds per square inch for the MechaCar suspension coils is not equal to 1,500 psi

All lot T-test:

![All lot T-test](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/one_sample_t_test.png?raw=true)

- From the results of the all lot T-test we can notice a p-value of approximately 0.0603. Assuming we have a significance level of 0.05, the p-value for the all lot T-test is higher than the significance level, therefore there is not enough evidence to reject the null hypothesis.

Lot 1 T-test:

![Lot 1 T-test](Dragster.jpg)

- From the results of the Lot 1 T-test we can notice a p-value of approximately 1. Assuming we have a significance level of 0.05, the p-value for the Lot 1 T-test is much higher than the significance level, therefore there is not enough evidence to reject the null hypothesis.

Lot 2 T-test:

![Lot 2 T-test](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/lot_2_t_test.png?raw=true)

- From the results of the Lot 2 T-test we can notice a p-value of approximately 0.6072. Assuming we have a significance level of 0.05, similarly to the Lot 1 T-test the p-value for the Lot 1 T-test is much higher than the significance level, therefore there is not enough evidence to reject the null hypothesis.
  
Lot 3 T-test:

![Lot 3 T-test](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/lot_3_t_test.png?raw=true)

- From the results of the Lot 3 T-test we can notice a p-value of approximately 0.04168. Assuming we have a significance level of 0.05, p-value for the Lot 3 T-test is less than the significance level, therefore there there is enough evidence to reject the null hypothesis. That is, there is sufficient evidence to support the claim that the mean of the pounds per square inch in Lot 3's suspension coils is statistically different from the population mean of 1,500 pounds per square inch