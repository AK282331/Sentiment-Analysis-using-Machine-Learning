
This project focuses on building a sentiment analysis model using real-time user reviews. The goal was to classify sentiments (positive/negative) from 200 user-submitted reviews collected via Google Forms, covering both product and movie opinions.

---

## Overview

- **Type of Task**: Sentiment Classification  
- **Data Source**: Collected via Google Form  
- **Domain**: Product and Movie Reviews  
- **Reviews Count**: 200 real user reviews  
- **Target Variable**: Sentiment (Text format - Positive/Negative/Neutral)  

---

## Tools and Libraries Used

- **Python**
- **Numpy & Pandas** – Data manipulation and EDA  
- **NLTK** – Text preprocessing (stopword removal, stemming, etc.)  
- **scikit-learn** – Model building, evaluation, and pipeline  
- **Imbalanced-learn** – SMOTE for class imbalance  
- **Optuna** – Hyperparameter tuning  
- **XGBoost** – Final model selection  

---

## Data Preprocessing

- **Text Cleaning**: Lowercasing, removing punctuation, and stopwords
- **Label Encoding**: Converted sentiment labels (Positive/Negative/Neutral) into binary (2/1/0)
- **Imbalance Handling**: Applied SMOTE to balance class distribution

---

## Feature Engineering

- **N-gram Vectorization**: Used CountVectorizer with n-gram range (1,4) to convert text into numerical vectors
- **Dimensionality Reduction**: Applied PCA to reduce dimensionality while preserving key patterns

---

##  Models Tested

A pilot test was done using multiple models:
- DecisionTreeClassifier  
- SVC (Support Vector Classifier)  
- RandomForestClassifier  
- GradientBoostingClassifier  
- XGBRFClassifier

After comparing their performance, **XGBRFClassifier** gave the best results.

---

## Hyperparameter Tuning

- Used **Optuna** for efficient and automated hyperparameter tuning of the selected XGBRF model.

---

## Model Pipeline

- Created a **pipeline** to automate preprocessing, vectorization, dimensionality reduction, and prediction.
- This made the process scalable and consistent across different data samples.

---

##Final Outcome

- A sentiment classifier that can predict whether a review (product or movie) is **positive** or **negative** or **neutral**.
- All steps from preprocessing to prediction are integrated in a single pipeline for ease of deployment or further experimentation.

---
