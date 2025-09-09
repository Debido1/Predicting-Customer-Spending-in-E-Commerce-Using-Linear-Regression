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
- Find out whether the company should focus more on the **mobile app** or the **website**.  
- Use a **Linear Regression model** to predict customer yearly spending. 

## Project Structure 
1. Looked at the data and cleaned it.  
2. Explored relationships between features (like app usage vs. website usage).  
3. Built a linear regression model with Scikit-Learn.  
4. Evaluated the model with metrics like R² and error scores.  
5. Shared insights on customer behavior and spending patterns.  


## Dataset Preview  

Below is a preview of the dataset after importing and examining it:  

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/download%20and%20import.png?raw=true)

The necessary libraries (pandas, numpy, matplotlib, seaborn) are imported, and the dataset named Ecommerce Customers is successfully loaded into a DataFrame called df. The dataset contains columns like Email, Address, Avatar, and several numerical features that will be used for analysis and modeling.

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/statistics.png?raw=true)

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/Missing%20values.png?raw=true)

There are no missing values in the dataset. Every column, including numerical and categorical fields such as Email, Address, Avatar, and the numerical predictors, has complete data for all 500 rows. This means no data imputation or cleaning is required for handling null values.

![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/data%20cleaning.png?raw=true)

Non-numeric columns (Email, Address, and Avatar) are dropped to prepare the data for correlation analysis and modeling. The resulting df_copy DataFrame contains only numerical features relevant to predicting Yearly Amount Spent, ensuring that the dataset is ready for statistical and machine learning operations.


![Dataset Preview](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/e2d015d460e27d623744cdb173eaff6aabab80bf/Dataset%20overview.png?raw=true)

The dataset after cleaning contains 500 records and 5 key columns: Average Session Length, Time on App, Time on Website, Length of Membership, and Yearly Amount Spent. These features will serve as predictors for the target variable (Yearly Amount Spent).


## Visualization  

Correlation heatmap showing relationships between features:  

![Correlation Heatmap](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/Correlation.png?raw=true)  

The heatmap shows the correlation matrix between the numerical features. Notably:

- Length of Membership has the strongest positive correlation with Yearly Amount Spent (0.81), suggesting it's a key driver of customer spending.

- Time on App also shows a moderate correlation (0.50) with spending.

- Avg. Session Length has a weaker correlation (0.36).

- Time on Website shows almost no correlation (-0.0026).

These results imply that customers who have been members longer and use the app more tend to spend more, while time on the website is not a strong predictor. This insight supports focusing more on the app experience to boost revenue.

## Explored relationships between features (like app usage vs. website usage).

Time on App

![Time on App](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/time%20on%20app.png?raw=true)


**Time on App vs Yearly Amount Spent:**

- Shows a strong positive linear relationship


**Time on Website**

![Time on Website](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/time%20on%20website.png?raw=true)

**Time on Website vs Yearly Amount Spent:**

- Very weak correlation

- No clear linear trend visible in the scatter plot

#### Insight:

- Time on App is a much better predictor of spending than Time on Website



## Model training and Splitting
![Data splitting](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/splitting.png?raw=true)

**Train/Test Split:**

 The data was Splitted into 400 train and 100 test samples

### Features:

- Avg. Session Length

- Time on App

- Time on Website

- Length of Membership

### Target:
- Yearly Amount Spent

Training and Prediction

![Training and Prediction](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/Training%20and%20prediction.png?raw=true)

## Model Results  

Model Evaluation

![Training and Prediction](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/r2.png?raw=true)

Model Evaluation Results

#### Mean Absolute Error (MAE): 8.56
On average, the model’s predictions are off by about 8.56 units of yearly spending. This shows relatively small errors compared to the scale of the data.

#### Mean Squared Error (MSE): 109.86
The squared errors average around 109, which indicates the overall error magnitude. While larger errors are penalized more, the value is still reasonably low given the target values are in the hundreds.

#### Root Mean Squared Error (RMSE): 10.48
The typical prediction error is about 10.48 units. Since RMSE is in the same units as the target (Yearly Amount Spent), this is an intuitive measure showing that the model predicts quite accurately.

#### R² Score: 0.978
The model explains about 97.8% of the variance in yearly spending. This indicates a very strong fit, meaning the model captures the relationship between features and customer spending effectively.

Regression line fit against actual data:  

![Regression Line](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/Model%20evaluation.png?raw=true)  

**Residual plot showing error distribution:**

- The points closely follow a diagonal line which Indicates the linear regression model fits the data well.

![Residual Plot](https://github.com/Debido1/Predicting-Customer-Spending-in-E-Commerce-Using-Linear-Regression/blob/main/residual.png?raw=true)

The residuals are approximately normally distributed and centered around zero, which indicates that the linear regression model is a good fit. This supports the validity of the model’s assumptions and suggests that predictions are reliable


**Interpretation:**
The linear regression model performs exceptionally well. With a high R² value and low error metrics, the model can reliably predict yearly customer spending. This suggests that features like Time on App and Length of Membership are strong drivers of customer behavior and spending.

## INSIGHT
- **App usage** is a stronger driver of customer spending compared to website usage.  
- **Length of membership** is another strong predictor of yearly spending.  
- The linear regression model provides a good fit and can be used to predict customer spending, helping the company decide where to focus its marketing and development efforts.
