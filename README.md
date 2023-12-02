# MSBA-Career-Capstone-1

## Home Credit Default Risk

Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders. Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience.
In this notebook, we aim to explore the issue of credit default risk at Home Credit, a company that seeks to provide loans to individuals with insufficient or nonexistent credit histories. This underserved population often faces exploitation by unreliable lenders, making it crucial for Home Credit to ensure a positive and safe borrowing experience.
To address this challenge, Home Credit leverages various sources of alternative data, such as telecom and transactional information, to predict their clients' repayment abilities.
Our analysis begins with data cleaning, where we preprocess and prepare the data for modeling. Subsequently, we develop predictive models using the cleaned data to assess credit default risk. We focus on the target variable and employ different machine learning models, calculating relevant metrics like accuracy and ROC values.
The objective is to identify the best-performing model based on Kaggle scores. We start with Logistic regression and then explore penalized regression, specifically LASSO, due to collinearity issues. Additionally, we examine Random Forest, XGBoost, and Light XGBoost to assess their effectiveness in predicting credit default risk.

## Group Contribution

Abhiram Mannam - Abhiram was responsible for implementing Light Gradient Boosting, preparing a notebook write-up, and evaluating the models.

Neil Samuel Pulukuri - Neil's tasks included data cleaning and modeling the Random Forest model to fit the dataset.

Josh Hawley - Josh was in charge of implementing the XG Boost model and conducting hyperparameter tuning.

Kushal Ram Tayi - Kushal's tasks included building the Logistic model, calculating the Variance Inflation Factor (VIF), and using penalized LASSO regression to address multicollinearity.
