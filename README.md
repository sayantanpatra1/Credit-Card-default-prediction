# Credit-Card-default-prediction

Problem Description
Taiwan's credit card issuers faced a debt crisis in recent years, with delinquency expected to peak in Q3 2006 (Chou, 2006). To increase market share, banks over-issued credit cards to unqualified applicants, leading to excessive credit usage and heavy debts. This crisis impacted consumer finance confidence and presented challenges for both banks and cardholders.

Dataset
We used the Credit Card Default Payment in Taiwan dataset to predict whether credit card holders are defaulters or non-defaulters. The dataset includes the following features:

ID: Client ID
LIMIT_BAL: Amount of given credit in NT dollars
SEX: Gender (1=male, 2=female)
EDUCATION: Education level (1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown)
MARRIAGE: Marital status (1=married, 2=single, 3=others)
AGE: Age in years
PAY_0 to PAY_6: Repayment status from April 2005 to September 2005
BILL_AMT1 to BILL_AMT6: Bill statement amounts from April 2005 to September 2005
PAY_AMT1 to PAY_AMT6: Previous payments from April 2005 to September 2005
default.payment.next.month: Default payment next month (1=yes, 0=no)
# Steps Involved
1. Exploratory Data Analysis (EDA)
2. Load and read the dataset.
3. Identify variables impacting payment default and their correlations.
4. Use graphical analysis to visualize data.
5. Null Values and Outliers
6. Confirm the dataset contains no null values.
# Feature Analysis
1. Analyze categorical and numerical features.
2. Correlation Analysis
3. Plot a heatmap to find correlations between dependent and independent variables.
4. Train-Test Split
5. Split data into dependent (X) and independent (y) variables.
6. Train the model using an 80-20 split for training and testing data.
# Models
1. Train data using Logistic Regression, Random Forest, SVC, and XGBoost.
# Feature Selection
1. Drop 'ID' and target variable, keep 23 predictor features.
2. Imbalanced Data Handling
3. Use train-test split to balance data.
4. Apply SMOTE (Synthetic Minority Over-Sampling Technique) to handle imbalance.
# Performance Metrics
1. Use accuracy, precision, recall, confusion matrix, ROC_AUC, and precision-recall curve to evaluate models.
2. SMOTE Oversampling
   
Purpose: Compensate for rare classes in the dataset.
Effectiveness: SMOTE duplicates examples from the minority class, ensuring balanced training data.
Model Performance with and without SMOTE
Model	Training AUC Without SMOTE	Training AUC With SMOTE
Logistic Regression	0.726	0.797
Random Forest	0.764	0.916
XGBoost	0.762	0.899

# Conclusion
Higher default rates are observed for lower credit limits (around 10,000 NT dollars).
Lower default rates are observed among highly educated cardholders.
Default rates are higher for clients over 60 years old compared to younger clients.
The best algorithms for predicting default payments next month include classification trees and bagging approaches.
