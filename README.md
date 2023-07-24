# Imbalanced Loan_Tap Dataset - Logistic Regression
##Introduction:

This repository contains code and information related to building a Logistic Regression model for a loan tap dataset with imbalanced classes. The loan tap dataset is a collection of loan application records, where the target variable is "loan_status" indicating whether a loan was approved or not.
#Problem Statement:
The main challenge in this dataset is class imbalance. The "loan_status" classes may have significantly different frequencies, leading to biased model performance. The goal is to develop a Logistic Regression model that can effectively handle the class imbalance and provide accurate predictions for loan approvals.
#Dataset
The dataset consists of various features related to loan applicants, such as loan amount, credit score, employment status, etc. The target variable is "loan_status," which can take one of the following values:

loan_amnt : The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.
term : The number of payments on the loan. Values are in months and can be either 36 or 60.
int_rate : Interest Rate on the loan
installment : The monthly payment owed by the borrower if the loan originates.
grade : LoanTap assigned loan grade
sub_grade : LoanTap assigned loan subgrade
emp_title : The job title supplied by the Borrower when applying for the loan.*
emp_length : Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years.
home_ownership : The home ownership status provided by the borrower during registration or obtained from the credit report.
annual_inc : The self-reported annual income provided by the borrower during registration.
**verification_status : Indicates if income was verified by LoanTap, not verified, or if the income source was verified
issue_d : The month which the loan was funded
loan_status : Current status of the loan - Target Variable
purpose : A category provided by the borrower for the loan request.
title : The loan title provided by the borrower
dti : A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LoanTap loan, divided by the borrower’s self-reported monthly income.
earliest_cr_line : The month the borrower's earliest reported credit line was opened
open_acc : The number of open credit lines in the borrower's credit file.
pub_rec : Number of derogatory public records
revol_bal : Total credit revolving balance
revol_util : Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.
total_acc : The total number of credit lines currently in the borrower's credit file
initial_list_status : The initial listing status of the loan. Possible values are – W, F
application_type : Indicates whether the loan is an individual application or a joint application with two co-borrowers
mort_acc : Number of mortgage accounts.
pub_rec_bankruptcies : Number of public record bankruptcies
Address: Address of the individual
#Approach
To deal with the class imbalance issue, we will apply the Synthetic Minority Over-sampling Technique (SMOTE) to create synthetic samples for the minority class ("Charged Off") and balance the dataset.

The steps involved in building the Logistic Regression model are as follows:

Data Preprocessing:

Handle missing values.
Convert categorical variables into numerical representations.
Scale numerical features if needed.
Data Splitting:

Split the dataset into training and testing sets.
Handling Imbalanced Classes:

Apply SMOTE to oversample the minority class.
Logistic Regression Model:

Build and train the Logistic Regression model on the balanced dataset.
Model Evaluation:

Evaluate the model using various performance metrics, such as accuracy, precision, recall, F1-score, and ROC-AUC.
#Dependencies

Imbalanced Loan Tap Dataset - Logistic Regression
Introduction
This repository contains code and information related to building a Logistic Regression model for a loan tap dataset with imbalanced classes. The loan tap dataset is a collection of loan application records, where the target variable is "loan_status" indicating whether a loan was approved or not.

Problem Statement
The main challenge in this dataset is class imbalance. The "loan_status" classes may have significantly different frequencies, leading to biased model performance. The goal is to develop a Logistic Regression model that can effectively handle the class imbalance and provide accurate predictions for loan approvals.

Dataset
The dataset consists of various features related to loan applicants, such as loan amount, credit score, employment status, etc. The target variable is "loan_status," which can take one of the following values:

Fully Paid: Loan is fully paid off by the borrower.
Charged Off: Loan was not fully paid off, and the borrower has defaulted.
Current: Loan is still in progress, and payments are being made.
Approach
To deal with the class imbalance issue, we will apply the Synthetic Minority Over-sampling Technique (SMOTE) to create synthetic samples for the minority class ("Charged Off") and balance the dataset.

The steps involved in building the Logistic Regression model are as follows:

Data Preprocessing:

Handle missing values.
Convert categorical variables into numerical representations.
Scale numerical features if needed.
Data Splitting:

Split the dataset into training and testing sets.
Handling Imbalanced Classes:

Apply SMOTE to oversample the minority class.
Logistic Regression Model:

Build and train the Logistic Regression model on the balanced dataset.
Model Evaluation:

Evaluate the model using various performance metrics, such as accuracy, precision, recall, F1-score, and ROC-AUC.
Dependencies
Python 3.8 or higher
pandas
numpy
seaborn
matplotlib
scikit-learn
imbalanced-learn
statsmodels
