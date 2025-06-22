# Improve Credit Scoring with Random Forest

## Introduction

## Introduction

This project was completed as the final assignment for the *Sains Data* course at Universitas Indonesia. Our team (Kelompok 2) implemented and compared several machine learning classification models to improve the accuracy of credit scoring. The focus of the final model was Random Forest, selected due to its strong performance in both training and validation. I contributed mainly to the implementation of the model in Python and was actively involved in writing and organizing the final project report.

## Motivation

Credit scoring plays a critical role in determining whether a borrower is eligible for a loan. Poor accuracy in scoring can lead to either granting credit to high-risk clients or rejecting creditworthy applicants. By applying machine learning—particularly Random Forest—we aim to build a reliable scoring model to support better decision-making for financial institutions.

## Data

- **Source**: [Kaggle – Credit Risk Dataset](https://www.kaggle.com/datasets/laotse/credit-risk-dataset)
- **Size**: 32,581 samples with 12 features
- **Key Features**: Age, income, loan amount, credit history, employment length, home ownership, loan grade, etc.
- **Target Variable**: `loan_status` (0 = creditworthy, 1 = default)

## Methodology

1. **Exploratory Data Analysis (EDA)**
   - Distribution plots, correlation heatmaps
   - Analysis of numerical and categorical features

2. **Preprocessing**
   - Imputation of missing values (mean strategy)
   - Outlier removal using IQR method
   - One-hot encoding for categorical variables
   - Dataset splitting (80% train / 20% test)

3. **Model Selection & Tuning**
   - Compared: Decision Tree, SVM, Random Forest
   - Used GridSearchCV to optimize hyperparameters
   - Best model: Random Forest with 93.33% accuracy (90:10 split)

4. **Feature Engineering**
   - Feature importance analysis using `.feature_importances_`
   - Feature selection with threshold > 0.01
   - Created new interaction feature: `loan_percent_income × person_income`

5. **Evaluation**
   - Confusion Matrix
   - Classification Report (Accuracy, Precision, Recall, F1-score)

## Results

- **Best Accuracy**: 93.33% with Random Forest
- **Best Split**: 90% training / 10% testing
- **Feature Importance**: `loan_percent_income` and `person_income` were most influential
- **Confusion Matrix Summary**:
  - True Positives: 2,516
  - False Positives: 25
  - False Negatives: 187
  - True Negatives: 530

## Conclusion

Random Forest outperformed other models in predicting loan repayment outcomes. The model showed high precision and recall for "creditworthy" predictions, and decent performance for detecting defaults. With a 93.33% accuracy, this model can be a practical tool to help lenders reduce credit risk and improve financial decision-making.

## Team Members

- Haifa Marwa Saniyyah (2206048783)  
- Halimah As-Sajidah (2206048820)  
- Hanny Awlia (2206048751)  
- Rahma Chuzaima (2206048732)  
- Reizka Fathia (2206052755)

