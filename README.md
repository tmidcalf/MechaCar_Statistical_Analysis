# MechaCar Statistical Analysis

# Overview

For this project we tasked with preforming a statistical analysis for AutosRUs’ newest prototype, the MechaCar. The MechaCar is suffering from production troubles that are blocking the manufacturing team’s progress.

We were asked to complete the following tasks:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

# Analysis

## Linear Regression to Predict MPG

In this section we look at a linear regression model to determine which metrics such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance are related to the vehicle's expected miles per gallon.

**Linear Regression:**

![Linear Regression](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/MechaCar_linear_regression.png?raw=true)

**Linear Regression Summary:**

![Linear Regression Summary](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/MechaCar_summary.png?raw=true)

- Looking at the Linear Regression Summary from the Pr(>|t|) column we can see vehicle length and vehicle ground clearance produced very small values. This means both vehicle length and ground clearance are likely variables that have provided a non-random amount of variance to the mpg values in the dataset.

- We could consider the slope for this linear model to be non zero. This is because the summary returned a p-value of 5.35e-11 which is far below an assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis.

- From the results of the linear regression summary, we notice that this model has an r-squared value of 0.7149. This means that approximately 71% of all mpg predictions can be determined by this model and can effectively predict mpg of MechaCar prototypes to about 71% certainty.

## Summary Statistics on Suspension Coils

In this section we will be preforming summary to look at the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots.

**Total Summary:**

![Total Summary](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/total_summary.png?raw=true)

**Lot Summary:**

![Lot Summary](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/lot_summary.png?raw=true)

- From the total population summary we can notice that, as a whole the variance of the MechaCar suspension coils is approximately 62.29 pounds per square inch(psi). This falls under the design specifications which state that the variance of the suspension coils must not exceed 100 pounds per square inch. Although, when we take a closer look at the summary broken down by each lot, we notice that Lot 3 has a very high variance of approximately 170.29 psi, where Lots 1 and 2 both have variance less than 8 psi. This means Lot 3 that is disproportionately causing a higher variance of the full population of MechaCar prototypes.

## T-Tests on Suspension Coils

In this section we are performing a series of T-test on the total population, as well as each individual lot to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

**Null hypothesis:** The sample mean of the pounds per square inch for the MechaCar suspension coils is equal to 1,500 psi

**Alternative hypothesis:** The sample mean of the pounds per square inch for the MechaCar suspension coils is not equal to 1,500 psi

**All lot T-test:**

![All lot T-test](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/one_sample_t_test.png?raw=true)

- From the results of the all lot T-test we can notice a p-value of approximately 0.0603. Assuming we have a significance level of 0.05, the p-value for the all lot T-test is higher than the significance level, therefore **there is not enough evidence to reject the null hypothesis**.

**Lot 1 T-test:**

![Lot 1 T-test](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/lot_1_t_test.png?raw=true)

- From the results of the Lot 1 T-test we can notice a p-value of approximately 1. Assuming we have a significance level of 0.05, the p-value for the Lot 1 T-test is much higher than the significance level, therefore **there is not enough evidence to reject the null hypothesis**.

**Lot 2 T-test:**

![Lot 2 T-test](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/lot_2_t_test.png?raw=true)

- From the results of the Lot 2 T-test we can notice a p-value of approximately 0.6072. Assuming we have a significance level of 0.05, similarly to the Lot 1 T-test the p-value for the Lot 1 T-test is much higher than the significance level, therefore **there is not enough evidence to reject the null hypothesis**.
  
**Lot 3 T-test:**

![Lot 3 T-test](https://github.com/tmidcalf/MechaCar_Statistical_Analysis/blob/main/Resources/lot_3_t_test.png?raw=true)

- From the results of the Lot 3 T-test we can notice a p-value of approximately 0.04168. Assuming we have a significance level of 0.05, p-value for the Lot 3 T-test is less than the significance level, therefore **there there is enough evidence to reject the null hypothesis**. That is, there is sufficient evidence to support the claim that the mean of the pounds per square inch in Lot 3's suspension coils is statistically different from the population mean of 1,500 pounds per square inch

## Study Design: MechaCar vs Competition

When looking into buying a car, consumers look into many different metrics from cost to city or highway fuel efficiency, horse power, maintenance cost, or safety rating. Although, in this section we will look at MechaCar's carrying capacity, in cubic inches, in comparison to various competitors' vehicles.

**Null hypothesis:** MechaCar prototypes' mean carrying capacity in cubic inches is equal to competitor's vehicles in the same vehicle class

**Alternative hypothesis:** MechaCar prototypes' mean carrying capacity in cubic inches is greater than or less than that of competitor's vehicles in the same vehicle class

- For this analysis the best statistical test to be used would be a two sample T-test, looking at the data of the means for the MechaCar prototypes as well as sample means for competitor's vehicles in the same vehicle class.

- For this test we would need to gather data on the carrying capacity of competitor's vehicles in the same vehicle class
 