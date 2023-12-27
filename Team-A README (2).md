# Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision
we study the borrower-, loan- and social- related determinants of performance predictability in an online P2P lending market by conceptualizing financial and social strength to predict whether the borrowers could be funded with lower interest, and the lenders would be timely paid.

## Table of Contents

- [Introduction](#introduction)
- [LIBRARIES](#libraries)
- [DATA EXPLORATION](#data-EXPLORATION)
- [HANDLING MISSING VALUES](#handling-MISSING-VALUES)
- [PREPROCESSING](#preprocessing)
- [EDA](#eda)
- [FEATURE ENGINEERING](#feature-ENGINEERING)
- [MODELLING & Pipelining](#modelling-pipelining)
- [Deployment](#deployment)
- [CONCLUSION](#conclusion)

# Introduction

## Project Overview

Peer-to-Peer (P2P) lending platforms have become increasingly popular as alternative financial channels that connect borrowers and investors directly, bypassing traditional intermediaries like banks. These platforms facilitate lending by allowing individuals to lend money to others in need, making it crucial to analyze the available data on loan listings. For this project, we have worked with data from a Peer-to-Peer lending platform to gain insights into the dynamics of the lending industry and assess the risk associated with lending.

## Problem Statement
The main objective of this project is to analyze the data from the P2P lending platform and develop predictive models to achieve the following goals:

1) 	Loan Acceptance Prediction: Develop a model that predicts whether a loan application will be accepted or rejected. This will assist investors in making informed decisions and enhance the efficiency of the lending process.
2)	Return on Investment (ROI) Prediction: Create a model to predict the Return on Investment for investors. Accurate ROI predictions will enable investors to make more informed investment decisions, leading to better portfolio management.
3)	Estimated Monthly Installment (EMI) Prediction: Develop a model to estimate the monthly installment amount that borrowers need to pay. This will assist borrowers in planning their finances and managing their debt.


# LIBRARIES
The Libraries we used in our project

![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/70744e7a-6295-4e5e-aae4-12e9322f99cf)

# DATA EXPLORATION
1) Display the first few rows of the dataset.

![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/d006194d-8b7b-4834-a881-b324ceb4e7d3)

2) Check the information and data types of the columns.

![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/5dd50fdc-8c26-4c7f-a62b-c4566b0da730)

3) Describing the dataset.

![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/8db73435-5f5f-4c44-ac52-ebf0db5e4456)

# HANDLING MISSING VALUES
  Handling Missing Values
  Identify columns with a large percentage of missing values.
  Drop columns with a high percentage of missing values.
  Drop rows with missing values in specific columns.
  Handle missing values in the remaining columns.
  
  ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/354ce95d-58f3-48ad-8682-f620b6db1255)


# PREPROCESSING
  Handle outliers using winsorization.
  Fill null values in the DebtToIncomeRatio column.
  Perform data encoding on categorical columns using label encoding and one-hot encoding.
  
  ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/6e3266a5-947b-434f-8521-ae719951f89a)


# EDA
 - Perform various analyses and visualizations to gain insights into the dataset:
 - Analyze credit grades and their distribution.
 - Investigate the relationship between credit grade and loan status.
 - Explore borrower rate and lender yield distributions.
 - Examine the correlation between borrower rate and lender yield.
 - Analyze the relationship between credit grade and monthly loan payment.
 - Visualize the distribution of borrowers by state.
 - Explore income ranges and their distributions.
 - Analyze relationships between income range and other variables.

  ### Some uni-variate graphs
  
  ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/f48b4c23-f79c-4bd3-b000-58597c165e96)



 ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/8605c94c-b1c8-44cd-9fb0-d16f79c75736)



  ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/18008ae5-7ed8-4b31-9b98-7878bde3d2ca)


![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/85cee9bf-2db8-4521-9e04-6a9eea3d52fe)



  ### Some bi-variate graphs

  ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/b249303e-ba4a-4449-bbfb-5e0f327a5428)


  ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/5e2b73c2-0bc8-4c7b-b090-5f328a8c53af)


![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/0bd305c2-d883-40bb-8d79-da7bb9814965)


### some multivariate graphs

![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/1b9415ed-c55c-4898-96e0-6920b566bba0)


![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/b794057c-a0ca-4847-8c84-5bb03f3540d6)

### Data encoding
 - which here exchange every categorical varibles to numeric varibles to prepare it for modeling
   
 ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/a621df17-1ccf-4140-af49-a2153fbd3644)


![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/cf93ca04-7d6c-4b2e-bd52-da06430ec743)


# FEATURE ENGINEERING
 1) what we use in the first target variable (LoanAccepted)
   - Use mutual information score to perform feature selection.
  
     ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/42ec352b-f3d8-4124-96b5-c4284b070407)


   - Select the top features based on mutual information score.

     ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/b3c414f2-308c-4a46-9c70-91775e206279)


2) what we use in the second and third target varibles (ROI & EMI )
  - use mutual information score.
    ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/d72ba51d-6c6c-4b30-a940-ddf2f1599876)

   - perform also PCA to extract the most effected columns
     ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/22fcfa8f-343a-4f20-babf-dfd9c8cba3f4)



# MODELLING & Pipelining
 1)  Loan Acceptance Prediction
Split the data into training and testing sets.
Build a logistic regression model to predict loan acceptance.
Evaluate the model's performance using accuracy, confusion matrix, precision, recall, and F1-score.
Perform cross-validation to check for overfitting.

![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/4d98117c-4c91-4846-9118-c9926b2bcdbe)

![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/b8b53daf-3e23-49be-89f3-0809027eb177)
![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/e4a3d314-7649-46b8-8b49-f619ac53c5ed)


2) ROI & EMI Prediction
 ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/2600decb-efc0-43fe-9122-9d88febc4543)

- after spliting the data to training and testing also perform MI score and PCA then using Pipeline to aggregate the tools we use for reaching the prediction.
- using models Linear Regression , Ridge Regression and Random Forest

  ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/5f7a8714-511c-47f8-ae53-635a8b6830ee)

 - perform cross-validation to check for overfitting.

   ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/3edc80d4-a75d-442a-b56f-63489364a7e7)


   # Deployment
     - Save the trained logistic regression model for loan acceptance prediction.
     - Save the trained linear regression and random forest regressor models for ROI and EMI prediction.
     - Load the saved models for future use.

         ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/f4e373e2-46eb-4ad5-a446-5fad5a147e3d)


     - Using Streamlit Library to make the user interface
      1) for LoanAccepted prediction
       
      ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/2c8fe144-bc66-4d33-b664-10b6db60eeb6)



      2) for Roi & Emi predection

      ![image](https://github.com/Technocolabs100/Predictive-Analysis-Using-Social-Profile-in-Online-P2P-Lending-Decision/assets/105808002/416156ea-dd72-4a9a-beae-d13326840a58)



  # CONCLUSION

  - In this project, we successfully developed predictive models for Loan Acceptance, Return on Investment (ROI), and Estimated Monthly Installment (EMI) prediction. These models can significantly enhance decision-making for both investors and borrowers in the Peer-to-Peer lending platform. The insights gained from data exploration and visualization have provided valuable information about borrowers' credit grades, monthly loan payments, lender yields, and more.
The accurate Loan Acceptance Prediction model can help investors identify potentially high-risk loan applications and make informed lending decisions. The ROI prediction model allows investors to estimate their potential returns, aiding them in better portfolio management. The EMI prediction model provides borrowers with an estimate of their monthly installments, facilitating better financial planning.
Overall, this project demonstrates the effectiveness of data analysis and machine learning techniques in the domain of P2P lending, and the deployed models can provide valuable support to users of the lending platform.

