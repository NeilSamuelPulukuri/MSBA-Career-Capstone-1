# MSBA-Career-Capstone

## Home Credit Default Risk

<img width="509" alt="image" src="https://github.com/NeilSamuelPulukuri/MSBA-Career-Capstone-1/assets/141296161/c8d4f6ac-ffe3-452d-9237-958c1934fadc">



### Business Problem

Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders. Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. To address this challenge, Home Credit leverages various sources of alternative data, such as telecom and transactional information, to predict their clients' repayment abilities.

The business needs give a clear indication that this is a supervised problem because we have a target variable that predicts whether the customer will repay the loan or not. This is a binary classification problem because we have only two outputs for the target variable '0', which indicates that the client has enough transaction history to repay the loan, and '1', which suggests that the client will face difficulties in repaying the loan. We implement a robust machine learning model which can predict whether the loan will be defaulted or not. 

The success metric for this project is the Area under ROC curve between predicted probability and observed target. The more the Area under the ROC curve, the better the performance of the machine learning model. The project will be successful if the machine learning model is capable enough to predict client’s repayment abilities

### Groups Solution

We started the project by first analysing and cleaning the dataset and preparing the data for modelling. We observed that the class label was imbalanced, so we used downsampling to address this issue. The next step was to deal with the null values. For this we dropped the columns which had percentage null value greater than 45 percent and then imputed null values with median for numerical columns and mode for categorical columns. Then we applied One hot encoding for converting the categorical columns to numerical columns. Finally, we applied the same steps to the test data to ensure it aligns with the training data.

Next we used this cleaned dataset for modelling a machine learning model which predicts loan default. We used metrics like accuracy and ROC values for evaluating the machine learning models. The goal of the project is to select the model which has the highest Kaggle score. We started with a basic stats model that is Logistic Regression and got a Kaggle score of 0.67 and on analysing the VIF values we concluded that the dataset has a problem of multicollinearity. To solve this problem, we used a penalized regression model Lasso and the Kaggle score improved to 0.69. Then we applied a Random Forest model and got a Kaggle score of 0.66 and this made us understand that we need to use a robust machine learning model. Then we applied a XG Boost model with hyperparameter tuning and the Kaggle score increased to 0.71. Finally, we used a Light Gradient Boost model which improved the Kaggle score to 0.723 and this was our winning model for the dataset HomeCredit.


### Problems Encountered in the project

There is a significant class imbalance in the dataset, with a small number of defaults compared to non-defaults. Addressing this imbalance is important as it can affect model training and evaluation strategies. So, we used imblearn library and under sampling technique to balance the target variable. We used downsampling for this dataset. 

The dataset has also many null values and to determine how to impute null values was a challenge. We opted for Median imputation for the numerical variables since this imputation would be less effected by the outliers and used mode imputation for categorical variables. Also we decided to remove the columns which had more than 45 percentage null values.

Since the dataset was huge, hyperparameter tuning for advance machine learning algorithms like Random Forest, XG boost and Light Gradient boosting was problematic. So, we had to choose the correct set of parameters in the Grid Search, this was achieved by setting one parameter constant and varying the other parameters to get the best ROC-AUC score.

Overall cleaning the dataset and hyperparameter tuning were the major hurdles we encountered in the project.


### Important Features

<img width="711" alt="image" src="https://github.com/NeilSamuelPulukuri/MSBA-Career-Capstone-1/assets/141296161/b1789968-3237-4db5-9bc1-3f87b655b14b"> <br/> <br/> <br/>



<img width="486" alt="image" src="https://github.com/NeilSamuelPulukuri/MSBA-Career-Capstone-1/assets/141296161/792b5aa9-dfcf-4b0f-8e33-2a6b4d78774d">  <br/> <br/>




The above plot is a Feature importance plot of Light Gradient Boosting model which was the winning machine learning algorithm in our case. So based upon that plot and correlation values we can make some reccomendations to the financial institution that is Home Credit.


### Recomendations

1. The financial institution should be cautious in giving loans to younger people with no credit history as they are more likely to default. Probably the best way to go about this is to ensure that individual submits a government id  which inturn  helps the financial institution to track the history of the candidate.
2. The Region Population and region rating also seems to impact the default rate, so the institution should also take in account the region while give the loan to the individual.
3. The financial institution can use the prediction model to know whether the customer is going to default or not thereby ensuring a better and accurate procedure of loan processing which would ultimately improve the efficiency of the financial institution in loan making decisions.


### Group Contribution

Abhiram Mannam - Abhiram was responsible for implementing Light Gradient Boosting, preparing a notebook write-up, and evaluating the models.

Neil Samuel Pulukuri - Neil's tasks included data cleaning and modeling the Random Forest model to fit the dataset.

Josh Hawley - Josh was in charge of implementing the XG Boost model and conducting hyperparameter tuning.

Kushal Ram Tayi - Kushal's tasks included building the Logistic model, calculating the Variance Inflation Factor (VIF), and using penalized LASSO regression to address multicollinearity.


### Individual Contribution

I was given the task of data cleaning and modelling the Random Forest model. Since the dataset was huge, the data cleaning took forever. I started off by checking the target variable to inspect for class imbalance and found out that there were more people who were less likely to default compared those who are more likely to default. Then I applied Downsampling to deal with the issue of class imbalance. Next was to remove the columns with high percentage of null values and I removed those columns which had more than 45 % null values. Then came imputation where I used median to impute the null values for numerical columns and mode for categorical columns. Then I used One Hot encoding to convert the categorical columns to numerical columns. Then finally I ensured that the same steps are followed for the test data. Coming to modelling I was given the task for building a Random Forest Model. Well this was easy the only difficult rather time consuming part was hyper parameter tuning which took forever to run. Overall I can say that the data cleaning was tough and I also believe that it is the most time consuming part of a machine learning project.


### Conclusion
Overall, the project was challenging as it had many datasets. It was a good exercise for me to put in all the MSBA skills that I developed accross the three semesters into practice starting from Exploratory Data Analysis, Statistics, Encoding, Cross Validation, HyperParameter Tuning, applying robust machine learning models and finally intepreting the results (Crisp DM Process) . Also I found this home credit dataset quite similiar to real world problem and completing this project has equipped me well enough to handle real world problems by applying machine learning algorithms which in the near future aligns to my personal goal that is to become an efficient data scientist. Apart from the technical aspect the idea of working in a team and collaborating well enough to get an optimized solution for the problem was a learning experience for me and to add up, our team had used google colab that enabled us to be on the same page while developing the machine learning code for the project Home Credit Default.


### References 

Link to the Dataset:
[Home Credit Default Risk Kaggle Competition](https://www.kaggle.com/competitions/home-credit-default-risk/overview)


