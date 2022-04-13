# MechaCar_Statistical_Analysis

## Purpose:
This analysis was performed to review the prodcution data for insights that will help the manufacturing team. 

The following <ins>analysis</ins> will be done in this activity:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes,
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots,
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population,
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Resources: 
MechaCar CSV file : [MechaCar_mpg.csv](https://github.com/kritika2604/MechaCar_Statistical_Analysis/blob/main/MechaCar_mpg.csv)
Suspension coil file: [Suspension_Coil.csv](https://github.com/kritika2604/MechaCar_Statistical_Analysis/blob/main/Suspension_Coil.csv)
## Tools used: 
Rstudio

## Analysis 1: Linear Regression to Predict MPG
he MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. 

- A multiple linear regression model was developed using R that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file.
- Each independent variable was looked to determine if there is a significant relationship with the dependent variable(mpg) using `lm()` function. 

  <img width="424" alt="image" src="https://user-images.githubusercontent.com/94858846/162874770-a69caee9-598b-476f-9d6a-133ee3a669a2.png">

- Each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model- 
  - Ground clearance, vehicle length (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model. In other words the ground clearance and vehicle length have a significant impact on miles per gallon value.

  - The multi linear model is - 
  
    ```
    mpg = 1.25e-3 * vehicle_weigth + 6.27 * vehicle_length + 6.88e-2 * spoiler_angle + 3.55 * ground_clearance -3.41 * AWD - 1.04e+2
    ```
    or can be written as,
    ```
    mpg = 6.27 * vehicle_length + 3.55 * ground_clearance -3.41 * AWD - 104
    ```
  - The slope value is not zero here as the **r<sup>2</sup> value** is **0.7149** and the higher the correlation is between two variables, the more that one variable can explain/predict the value of the other.

  - This linear model is **fairly efficient to predict** mpg of MechaCar prototypes.
    
 ## Analysis 2: Visualizations for the Trip Analysis
 The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. 
 
  - Statistical summary is for all the lots:
  <img width="270" alt="image" src="https://user-images.githubusercontent.com/94858846/163011497-942b2a7c-bfee-4d49-bd71-38f873d10d22.png">

  - Statistical summary lot wise:
  <img width="386" alt="image" src="https://user-images.githubusercontent.com/94858846/163011904-8c36efe4-cfbc-423d-8b3d-502a62c1de5b.png">

    
