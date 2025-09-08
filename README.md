# Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression
The goal of this Analysis is to Know if the E-Commerce store should focus their efforts on their mobile app or website. and also to analyzes e-commerce customer behavior to predict yearly spending using Linear Regression.

# Dataset Overview

In this project, I explored an e-commerce dataset to understand customer behavior and predict their yearly spending. The dataset includes:  
- Average session length  
- Time spent on app  
- Time spent on website  
- Length of membership  

The target variable is **Yearly Amount Spent** (how much each customer spends in a year).

## Goals of the Project  
I. Find out whether the company should focus more on the **mobile app** or the **website**.  
II. Use a **Linear Regression model** to predict customer yearly spending. 

## Project Structure 
1. Looked at the data and cleaned it.  
2. Explored relationships between features (like app usage vs. website usage).  
3. Built a linear regression model with Scikit-Learn.  
4. Evaluated the model with metrics like R² and error scores.  
5. Shared insights on customer behavior and spending patterns.  


## Dataset Preview  

Below is a preview of the dataset after importing and examining it:  

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/download%20and%20import.png?raw=true)

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/statistics.png?raw=true)

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/Missing%20values.png?raw=true)

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/data%20cleaning.png?raw=true)

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/e2d015d460e27d623744cdb173eaff6aabab80bf/Dataset%20overview.png?raw=true)

The dataset after cleaning contains 500 records and 5 key columns: Average Session Length, Time on App, Time on Website, Length of Membership, and Yearly Amount Spent. These features will serve as predictors for the target variable (Yearly Amount Spent).


## Example Visualization  

Correlation heatmap showing relationships between features:  

![Correlation Heatmap](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/Correlation.png?raw=true)  

The heatmap shows that Length of Membership (0.81) and Time on App (0.50) have the strongest positive correlations with Yearly Amount Spent, suggesting they are important predictors. Time on Website shows little to no relationship with spending, indicating that website activity may not significantly drive revenue compared to app usage.

## Model Results  

Regression line fit against actual data:  

![Regression Line](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/Model%20evaluation.png?raw=true)  

Residual plot showing error distribution:  

![Residual Plot](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/residual.png?raw=true)
The residuals are approximately normally distributed and centered around zero, which indicates that the linear regression model is a good fit. This supports the validity of the model’s assumptions and suggests that predictions are reliable

