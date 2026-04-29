# Predicting Subscriber Churn in a Music Streaming Platform

## Overview
This project analyzes customer behavior in a music streaming platform to predict subscriber churn and identify the strongest drivers of retention. The analysis combines exploratory data analysis with baseline machine learning models to evaluate which users are most at risk of leaving and what business actions may help reduce churn.

## Business Problem
Subscriber churn is a major challenge for music streaming platforms because losing existing users can directly reduce recurring revenue and long-term growth. The goal of this project is to identify churn patterns and support targeted retention strategies using account-level and behavioral data.

## Dataset
This project uses the **Music Streaming Customer Churn Dataset** from Kaggle.

The dataset contains **41,000 customer records** and includes variables related to:
- subscriber demographics
- subscription structure
- payment behavior
- platform engagement
- churn outcome

The target variable is **`churned`**, where:
- `1` = churned
- `0` = retained

## Tools Used
- Python
- pandas
- matplotlib
- scikit-learn
- Google Colab

## Project Workflow
1. Inspect and prepare the dataset  
2. Explore churn patterns through EDA  
3. Train and compare churn prediction models  
4. Translate findings into business recommendations  

## Key Findings
- churn was more strongly associated with account structure than with simple top-line engagement metrics
- monthly subscribers churned far more often than annual subscribers
- subscription type showed meaningful differences in churn rates
- several simple engagement metrics such as weekly listening hours and playlist creation showed limited separation between churned and retained users
- balanced logistic regression was more useful than random forest for identifying churned users in a retention-focused setting

## Modeling Approach
Two baseline models were trained and compared:
- **Balanced Logistic Regression**
- **Random Forest Classifier**

The random forest achieved slightly stronger overall accuracy and ROC-AUC, but the balanced logistic regression identified a much larger share of churned users. Because recall for churned users is especially important in a retention use case, the balanced logistic regression was treated as the more practical model.

## Business Recommendations
- prioritize retention campaigns for monthly subscribers
- test targeted offers for higher-risk subscription segments such as student users
- monitor churn risk using a combination of account and behavioral features rather than relying only on raw listening volume
- use churn scoring to support re-engagement messaging, renewal offers, or targeted product nudges

## Repository Contents
- `music_streaming_churn_analysis.ipynb` — full notebook containing the analysis
- `README.md` — project summary, methods, findings, and recommendations

## Author
Benjamin Yiu
