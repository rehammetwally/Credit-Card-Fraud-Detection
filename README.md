# Credit-Card-Fraud-Detection
This repository contains a comprehensive data science project focused on detecting fraudulent credit card transactions. The project tackles the challenges of a highly imbalanced dataset by implementing various techniques for data preprocessing, feature engineering, and advanced machine learning modeling.
  ## Project Overview
This project focuses on building a machine learning model to detect fraudulent credit card transactions. The primary challenge lies in the highly imbalanced nature of the dataset, where fraudulent transactions are extremely rare compared to legitimate ones. The goal is to develop a robust classification model that can effectively identify fraudulent activities with high accuracy, precision, and recall.

  ## Dataset
The dataset used is from a Kaggle competition, containing transactions made by European cardholders in September 2013. The dataset includes:

      Time: The time elapsed since the first transaction in seconds.
      
      Amount: The transaction amount.
      
      V1-V28: Anonymized features resulting from a Principal Component Analysis (PCA) to protect user privacy.
      
      Class: The target variable, where 0 represents a non-fraudulent transaction and 1 represents a fraudulent one.

  ## Methodology
This project followed a structured approach to tackle the challenges of a highly imbalanced dataset.

      ### Exploratory Data Analysis (EDA):

        I performed a thorough analysis to understand the data distribution, correlations, and to identify potential outliers using Box Plots and Violin Plots.
        
        Correlation analysis was used to identify features that have the strongest positive or negative relationships with the Class variable.
        
      ### Feature Engineering:
        
        I created time-based proxies like Hour_from_start_mod24, is_night_proxy, and is_business_hours_proxy to capture temporal patterns.
        
        A logarithmic transformation was applied to the Amount feature to handle its right-skewed distribution.
        
      ### Handling Imbalanced Data:
        
        The dataset was split into training, validation, and test sets to ensure an unbiased evaluation.
        
        I used the imblearn library to implement various over-sampling (SMOTE) and under-sampling (RandomUnderSampler) techniques within a pipeline to balance the training data.
        
      ### Model Training and Evaluation:
        
        I trained several classification models, including Logistic Regression, Random Forest, and XGBoost.
        
        Models were evaluated using metrics crucial for imbalanced classification problems, such as ROC-AUC, Precision, and Recall.

  ## Key Findings
The XGBoost Classifier proved to be the most effective model for this task. It consistently achieved the best performance on the test set, demonstrating a strong ability to distinguish between fraudulent and non-fraudulent transactions. The use of a robust data pipeline and targeted feature engineering significantly contributed to the model's success.

  ## Repository Structure
    Credit_Card_Fraud_Detection.ipynb: The main Jupyter Notebook containing all the code for data cleaning, EDA, feature engineering, modeling, and evaluation.
    
    data/: Directory to store the dataset.
    
    README.md: This file.
    
