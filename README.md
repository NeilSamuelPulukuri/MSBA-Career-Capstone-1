# MSBA-Career-Capstone

## Home Credit Default Risk


### Business Problem

Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders. Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. To address this challenge, Home Credit leverages various sources of alternative data, such as telecom and transactional information, to predict their clients' repayment abilities.

### Groups Solution

In this notebook, we aim to explore the issue of credit default risk at Home Credit, a company that seeks to provide loans to individuals with insufficient or nonexistent credit histories. This underserved population often faces exploitation by unreliable lenders, making it crucial for Home Credit to ensure a positive and safe borrowing experience.

Our analysis begins with data cleaning, where we preprocess and prepare the data for modeling. Subsequently, we develop predictive models using the cleaned data to assess credit default risk. We focus on the target variable and employ different machine learning models, calculating relevant metrics like accuracy and ROC values.The objective is to identify the best-performing model based on Kaggle scores. We used one hot encoder to encode the object variables into dummies so that the modeling can also be done on the factor variables.
We first started with logistic regression model and got around 0.67 kaggle score and understood that it has multicollinearity by examing the VIF scores and used penalized regression model LASSO to fit the data and the kaggle score improved to 0.69. We further examined the data modeling with random forest and did hyper parameter tuning and got kaggle around 0.66 indicating to need further models.So, we used XG Boost model with hyper parameter tuning and secured the 0.71 kaggle score and then we examined the light Gradient boosting which is fast and accurate with kaggle score of 0.723.To conclude, we can say that Light Gradient Boost is the good model fit for the given cleaned dataset with Kaggle score of 0.72387.

### Problems Encountered in the project

There is a significant class imbalance in the dataset, with a small number of defaults compared to non-defaults. Addressing this imbalance is important as it can affect model training and evaluation strategies. So, we used imblearn library and under sampling technique to balance the target variable. We used downsampling for this dataset. 

Since the dataset was huge hyperparameter tuning for advance machine learning algorithms like Random Forest, XG boost and Light Gradient boosting was problematic. So, we had to choose the correct set of parameters in the Grid Search this was achieved by setting one parameter constant and changing the other parameter to get the best ROC-AUC score.

### Important Features

![image](https://github.com/NeilSamuelPulukuri/MSBA-Career-Capstone-1/assets/141296161/f08af6d1-e9ef-4226-b204-40e269b05be5)




### Recomendations

1. The financial institution should be cautious in giving loans to younger people with no credit history as they are more likely to default. Probably the best way to go about this is to ensure whether the individuals has an government id so that they can track the history of the candidate.
2. The Region Population and region rating also seems to impact the default rate, so the institution should also take in account the region while give the loan to the individual.


### Group Contribution

Abhiram Mannam - Abhiram was responsible for implementing Light Gradient Boosting, preparing a notebook write-up, and evaluating the models.

Neil Samuel Pulukuri - Neil's tasks included data cleaning and modeling the Random Forest model to fit the dataset.

Josh Hawley - Josh was in charge of implementing the XG Boost model and conducting hyperparameter tuning.

Kushal Ram Tayi - Kushal's tasks included building the Logistic model, calculating the Variance Inflation Factor (VIF), and using penalized LASSO regression to address multicollinearity.


### Conclusion
Overall, the project was challenging as it had many datasets. It was a good exercise for me to put in all the MSBA skills that I developed accross the three semesters into practice starting from Exploratory Data Analysis, Encoding, Cross Validation, HyperParameter Tuning and applying robust machine learning models. Also I found this home credit dataset to be similiar to real world problem and completing this project has equipped me well enough to handle real world machine learing problems in the near future which aligns to my personal goal that is to become an efficient data scientist.

