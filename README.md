# Used-Car-Price-Prediction-System 


### Table of Contents
- [Introduction](#introduction)
- [Objective](#objective)
- [Method](#method)
- [Reference](#reference)

## Introduction
  The used car market has become a booming industry in recent years, with India being one of the leading countries in the world in terms of vehicle production. In the financial year 2022, the total production volume of vehicles in India was around 22.9 million units, which was an increase from the previous year[12]. The production of cars has given rise to the used car market, which was valued at USD 32.14 billion in India and is expected to reach USD 74.70 billion, registering a CAGR of 15.1% during the forecast period. However, predicting the prices of used cars accurately can be a daunting task due to the highly competitive and dynamic nature of the market, as well as the vast variety of products available. 

## Objective
  The primary objective of this project is to perform a comparison of supervised machine learning algorithms namely Linear Regression(LR), Random Forest(RF), XGBoost(XGB), Support Vector Machine (SVM), and K-Nearest Neighbour (KNN) for predicting the price of used cars on given dataset from Kaggle. In addition to this, we aim to achieve the following objectives:

  -	Review and synthesize existing literature on the used car market and establish a robust benchmark for efficient machine learning model development.
  -	Collect and pre-process large volumes of data from multiple sources, including historical pricing data, car specifications, and sales details.
  -	Develop and rigorously evaluate the performance of several machine learning models, including classical statistical models and modern deep learning models, to identify the optimal model for used car price prediction.
  
### Research Question: : 
  Which among the selected algorithms Linear Regression(LR), Random Forest(RF), XGBoost(XGB), Support Vector Machine (SVM), and K-Nearest Neighbour (KNN) is efficient in predicting the price of used cars?

### Motivation: 
  The motivation behind this RQ is to find the optimal algorithm among the Linear Regression(LR), Random Forest(RF), XGBoost(XGB), Support Vector Machine (SVM), and K-Nearest Neighbour (KNN) for given dataset. The efficiencies of these models are evaluated using performance metrics such as Mean Absolute Error(MAE) and R^2 score. 

### Data Source:
Sales Data: The primary dataset used for analysis was acquired from Kaggle. The dataset is split into train.csv and test.csv datasets for convenience. 

## Method 
The experimentation procedure can be described as follows:
![image](https://github.com/user-attachments/assets/68a2e137-255e-45c6-a0f3-2eb44e06ec80)

**1. Data Cleaning/Preprocessing and Exploratory Data Analysis(EDA)**

In the initial data preparation phase, we performed the following tasks:
- Data loading and inspection
- Handling missing values
- Data cleaning and formatting

After pre-processing the data, EDA performed to extract following insights:
- What factors strongly influence the price of a used car?
- What impact does a brand of used car has on its price?
- How is the sale of used car effected by transmission type of car?

<img width="562" alt="image" src="https://github.com/user-attachments/assets/ce406a16-7053-4fe0-988e-b914ae11f27b">

**2. Feature Extraction**
The Pearson correlation coefficient is used as the feature selection technique. This coefficient measures the strength of the linear correlation between two variables and ranges between -1 and 1.
- A correlation of 1 indicates a positive correlation, where an increase in one variable corresponds to an increase in the other
- A correlation of -1 indicates a negative correlation, where an increase in one variable corresponds to a decrease in the other.
- A correlation of 0 means there is no linear correlation between the two variables.

  
  ![image](https://github.com/user-attachments/assets/abe35a63-5cc5-453f-a950-57495ede87b5)

**3. Data Segregation**
Using the ‘train-test split’ technique, the cleaned dataset is divided, resulting in 80% of the data being used as the training data and 20% is used as the testing data. 

![image](https://github.com/user-attachments/assets/b51a92e0-1217-4217-82eb-fa9ddaae9dc8)

**4. Model Building**
1. Linear Regression :
   
    ![image](https://github.com/user-attachments/assets/e317ba79-b4b0-4045-8ebb-89d697fc4b03)

2. Random Forest : 

    ![image](https://github.com/user-attachments/assets/c3f46832-7714-412f-87ff-aac3bde9def8)

3. XGBoost: 
 
   ![image](https://github.com/user-attachments/assets/58d83bbb-1c84-43a0-8f83-2448f8292183)

4. Support Vector Machine: 

    ![image](https://github.com/user-attachments/assets/fd5389cd-3519-405f-9ae8-156fa7b42445)

5. K-Nearest Neighbour : 

    ![image](https://github.com/user-attachments/assets/1c2ae9e5-e56b-45e2-a5a6-e65d67ed83f1)

**5. Model Evaluation**
The results of our tests are quantified in terms of the R^2 score, Root Mean Square Error(RMSE) and Mean Absolute Error(MAE) of our predictions. The following tables show the R^2error, the MAE and the RMSE accuracies for both training and testing dataset to evaluate the performance of the individual algorithm. 

<img width="265" alt="image" src="https://github.com/user-attachments/assets/86e5baf4-0b34-48cf-820a-f25d3752bb60">


<img width="248" alt="image" src="https://github.com/user-attachments/assets/9f6755ec-146e-4564-96f4-6980f45df103">


<img width="275" alt="image" src="https://github.com/user-attachments/assets/562a8f78-0f48-4395-a098-ccfbb9bea7ca">

A model with a lower RMSE or MAE and a higher R^2 value is considered to be more accurate than a model with a higher RMSE or MAE and a lower R^2 value. From all the above observations, Random Forest has the highest R^2score in testing dataset while XGBoost has the second highest R^2in the training dataset. But there is a significant difference in the RMSE values of both the algorithms. Finally, Random Forest is considered as an optimal algorithm for the prediction of price of used cars. 


**6. Model Deployment** 

Based on these conclusions, the proposed Random Forest based prediction model has been incorporated into the Flask, a lightweight Python web framework, for the used cars price prediction. Flask gives developers flexibility and is a more accessible framework for new developers since they can build a web application quickly using only a single Python file.

![image](https://github.com/user-attachments/assets/6709d19f-2b1c-4a02-9109-1816fa91ea76)

### Reference: 
1.	https://www.kaggle.com/competitions/1056lab-used-cars-price-prediction/data
2.	vehicle-production-volume-by-segment-india, https://www.statista.com/statistics.
3.	Report: https://www.mordorintelligence.com/industry-reports
