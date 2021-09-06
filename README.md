# Module 12 Challenge

## Overview of the Analysis

 ***PURPOSE:***
 This analysis assesses the creditworthiness of borrowers using various supervised learning methodologies.
 
 ***DATA:***
 This analysis utilizes lending data from a peer-to-peer lending company.
 
 The data consist of various loan statistics (the features) and a loan assessment (the target):
 
 ***FEATURES***
- loan_size
- interest_rate
- borrower_income
- debt_to_income
- num_of_accounts
- derogatory_marks
- total_debt
      
 ***TARGET***
- loan_status

The loan dataset contains info on over 77,000 loans. Here's a look at the vitals stats of the data (**lending_df.describe()**)

![image](https://user-images.githubusercontent.com/35455504/132131006-2ae7a160-e21b-46d7-98c8-e3c218cc58ab.png)

 Given the information contained in features, we look to be able to predict the loan_status and assess loan risk.
 
 ***VARIABLES***
- y = dataframe to hold target column
- X = dataframe to hold feature columns
- y.value_counts() = assess the balance of the **loan_status** values

***RESULTS***

* Machine Learning Model 1:
![image](https://user-images.githubusercontent.com/35455504/132216411-21e0b486-1fdd-405a-a42b-903bb2f77cae.png)

* Machine Learning Model 2:
![image](https://user-images.githubusercontent.com/35455504/132216433-7a4fb5ca-71af-4272-82a9-6f6904ae93ad.png)

***SUMMARY***
**[MODEL 1]**
The precision and recall for the 0 class ("healthy loan") is a bit better than for the 1 class ("high risk loan"). For healthy loans, all of the predictions were correct (precision = 1.00). For high-risk loans, 85% of those predictions were correct (precision = 0.85). The recall value for healthy loans was slightly lower than the precision, but still great (recall = 0.99). For high-risk-loans, the recall was an improvement over the precision by 6 percentage points.

**[MODEL 2]**
The precision and recall for the 0 class ("healthy loan") is a bit better than for the 1 class ("high risk loan"). For healthy loans, all of the predictions were correct (precision = 1.00). For high-risk loans, 84% of those predictions were correct (precision = 0.84). This represents a slight degradation from the original model. The recall value for healthy loans was slightly lower than the precision, but still great (recall = 0.99). For high-risk-loans, the recall was an improvement over the precision by 15 percentage points, and represents a significant improvement over the original model (0.91 to 0.99)

Based upon the improvement in Model 2 recall for high-risk loans, it is recommended that we use Model 2 over Model 1
