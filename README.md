# MechaCar_Statistical_Analysis
## Linear Regression in order to Predict MPG
   * In order to solve the given problemset, "R" was used and a linear regression model was implemented to predict MPG based on the data provided. The data provided was the following:
      * MPG = 6.267(Vehicle Length) + 0.001245(Vehicle Weight) + 0.06877(Spoiler Angle) + 3.546(Ground Clearnace) -3.411(AWD) -0.0104
    
   * The folowing is the R Output:

      ![R Output](Resources/MGP_LIN_regression_output.png)

      * This linear regression model provides the information needed to conduct an inference. The last line provides the "P-value" for the entire model which is 5.35e-11. This represents a value of 0 which signifies the model is statistically accurate. The model also provides the Adj. R-squared value which is ~0.70. This is an adequate R-squared value and demonstrates our model predicts MPG ~70% of the time which is more than acceptable.
      * Additionally, in the Co-Efficients table, we can see that the P-values are at a 95% confidence level which means both vehicle length and ground clearance are critical factors in predicting MPG. 
      
## Summary Statistics determining Suspension Coils
   * According to the design specifications for the MechaCar, variance of the suspension coils must **not** exceed 100 pounds per square inch. In order to adhere to these specifications, below are the summary statistics in total  by lot.
   * 
![Total Summary](Resourcesn/Summary_Table.png)

![Lot Summary](Resources/Lot_Summary.png)

The current manufacturing data meets this design specification for all manufacturing lots in total but not each lot individually. We can see that lots 1 and 2 have a variance that meets that standard but lot 3's variance is not. We should take a look at lot 3 to see what we can do to decrease that variance.

## T-Tests on Suspension Coils
To determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per sq. inch, I performed a t-test.

![Overall T-Test](https://github.com/rmward17/MechaCar_Statistical_Analysis/blob/main/Lot_Summary.png)

The p-value is 0.06028. This means that the overall mean of 14987.8 is not different at a 95% confidence. 

I also performed a t-test on each lot to compare each manufacturing lot mean aganst the population mean.

![Lot 1 T-Test](https://github.com/rmward17/MechaCar_Statistical_Analysis/blob/main/Lot1_test.png)
|:--:|
| <b>Lot 1 T-Test</b>|

For lot 1, we can see that the p-value is 1 which means that the mean of Lot 1 is equal to the population mean at a 95% confidence level.

![Lot 2 T-Test](https://github.com/rmward17/MechaCar_Statistical_Analysis/blob/main/Lot2_test.png)
|:--:|
| <b>Lot 2 T-Test</b>|

Lot 2 has a p-value of 0.607. That is another very high p-value and we can that the Lot 2 mean is equal to the population mean at a 95% confidence level.

![Lot 3 T-Test](https://github.com/rmward17/MechaCar_Statistical_Analysis/blob/main/Lot3_test.png)
|:--:|
| <b>Lot 3 T-Test</b>|

Lot 3 has a p-value of 0.04168. It is lower than 0.05 which means it is not equal to the population mean at a 95% confidence level.

## Study Design: MechaCar vs Competition
A good way to gain insight on how MechaCar performs against comptitors is to run a statistical study. A metric I would consider measuring is fuel efficiency. A high fuel efficiency means that consumers would be spending less on gas and having less anxiety about runing out of gas while driving. 

To do this study, we would need a null hypothesis and an alternative hypothesis. One option is below:
Null: Drivers fill up their tanks at the same rate regardless of car over 30 days
Alternative: Drivers will fill their tanks up at a rate 10% lower than those of their competitors over 30 days

Using these methods, we could use a t-test on the average number of fill ups for each group of car. We would need data on the number of fill ups that drivers make for each car company to compare.

That is just one way to test how well MechaCar fairs against competition, there are many other routes a statistician can take!
