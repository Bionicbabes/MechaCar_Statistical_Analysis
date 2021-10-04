# **MechaCar_Statistical_Analysis**

- **Summary**
  * A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

---------------------------------------------

## **Linear Regression to Predict MPG**

- **Summary** 
  * Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes

![Deliverable1.PNG](https://github.com/Bionicbabes/MechaCar_Statistical_Analysis/blob/main/Deliverable1.PNG)

  * Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    - According to our results, vehicle_length and ground_clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model. In other words the vehicle_length and ground_clearance have a significant impact on mpg values in the dataset.
    - This leads us to the conclusion that the list below will have a non-random amount of variance given their p-value is above the significance level of 0.05
      1. vehicle_weight
      2. spoiler_angle
      3. AWD
      
  * Is the slope of the linear model considered to be zero? Why or why not?
    - The P-value is 5.35e-11 which is less than our standard significance level of 0.05 so the Null hypothesis is rejected.

  * Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
    - The R-squared value is indicative of the accuracy of the regression and the value is 0.7149 or 71.5%.  So this definitely has merrrit but correclation does not mean causation and there is 28.5% of the data that is not correlating to the regression.

---------------------------------------------

## **Summary Statistics on Suspension Coils**

- **Summary**
  * Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots

- **Analysis and Results**
  * The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
   - Using the data set given we are able to run statistics on the data set as a whole and then we are also able to bin the data into lots and run further analysis on each individual lots and compare them all to see if they are meeting specifications.

- **Total Summary**

![Deliverable2_1.PNG](https://github.com/Bionicbabes/MechaCar_Statistical_Analysis/blob/main/Deliverable2_1.PNG)


- **Lot Summary**

![Deliverable2_2.PNG](https://github.com/Bionicbabes/MechaCar_Statistical_Analysis/blob/main/Deliverable2_2.PNG)

  - As we comb through the data and the analysis we can see that the total overall variance for the site (62.29) is under the specification of 100.  As we look deeper and we look at the sample lots we discover that not all the lots are meeting the spec and that lot 3 (170) is over our specification of 100.  We will have to recall these part and make sure they do not make it to the end user.  

---------------------------------------------

## **T-Test on Suspension Coils**

- **Summary**
  * Run t-tests to determine if the manufacturing lots are statistically different from the mean population

## **T-Test Overall**
 
![Deliverable3_1.PNG](https://github.com/Bionicbabes/MechaCar_Statistical_Analysis/blob/main/Deliverable3_1.PNG)

  - Overall P-value .06028 > significance level of 0.05

## **T-Test Lot 1**

![Deliverable3_2.PNG](https://github.com/Bionicbabes/MechaCar_Statistical_Analysis/blob/main/Deliverable3_2.PNG)

  - Lot 1 P-value 1 > significance level of 0.05

## **T-Test Lot 2**

![Deliverable3_3.PNG](https://github.com/Bionicbabes/MechaCar_Statistical_Analysis/blob/main/Deliverable3_3.PNG)

  - Lot 2 P-value .6072 > significance level of 0.05

 ## **T-Test Lot 3**

![Deliverable3_4.PNG](https://github.com/Bionicbabes/MechaCar_Statistical_Analysis/blob/main/Deliverable3_4.PNG)

  - Lot 3 P-value .04168  > significance level of 0.05

---------------------------------------------

## **Study Design: MechaCar vs Competition**

Study considerations:
* Cost
* City vs Highway fuel efficiency
* Horse power
* Maintenance cost
* Safety rating

* What metric or metrics are you going to test?
Comparable performance of gasoline versus electric vehicles in terms of total vehicle range on full tank of gas or full battery charge 

* What is the null hypothesis or alternative hypothesis?

Does an electric powered vehicle have higher range than gasoline powered vehicle?

Null Hypothesis:
Power source (electric vs gasoline) has no effect on total vehicle range assuming similar driving conditions.

Alternative Hypothesis:
Power source (electric vs gasoline) does have a significant effect on total vehicle range assuming similar driving conditions.  

* What statistical test would you use to test the hypothesis? And why?

Two-Sample t-test for a strict comparison of Electric vs Gasoline powered vehicle datasets to determine significant difference exists or not.

* What data is needed to run the statistical test?

Sample Data required:
* Cost of full charge / tank of gas
* Sample set of electric & gasoline powered vehicles (prefer equal distribution on age, make, model)
* Similar driving pattern & weather conditions
* Sample size of 40 vehicles from each group
