# Email Spam Detection Using Machine Learning Classification Techniques

## Introduction

This project was completed for the *Analisis Data Tidak Terstruktur* course at Universitas Indonesia. The aim was to build a machine learning-based email classifier capable of distinguishing between spam and legitimate (ham) emails. I developed and implemented this project individually using Python and various classification models.

## Motivation

With over half of global email traffic potentially consisting of spam, users face both inconvenience and risks such as phishing and malware. Efficient spam detection not only improves user experience but also enhances security. This project explores machine learning as a robust approach to filtering spam emails.

## Data

The dataset used is the **Email Spam Classification Dataset** from Kaggle, containing **83,448 emails** labeled as either *spam* (1) or *ham* (0). A 20% subset was selected for efficient computation, with data split into training, validation, and test sets.

## Methodology

The approach includes:

- **Exploratory Data Analysis (EDA)**: Distribution analysis, duplicate removal, word clouds.
- **Text Preprocessing**: Lowercasing, removing HTML/tags, tokenization, stopword removal, stemming.
- **Feature Extraction**: TF-IDF vectorization with unigram and bigram, max 2,000 features.
- **Model Training**: Evaluated four models — Naive Bayes, SVM, Random Forest, Logistic Regression.
- **Evaluation Metrics**: Accuracy, precision, recall, F1-score, ROC-AUC.

## Results

- **SVM** outperformed all models with **97.4% accuracy** and **0.975 F1-score**.
- Feature importance analysis showed the model learned to recognize patterns of legitimate emails rather than just spam indicators.
- Balanced precision-recall performance on both spam and ham classes.

## Conclusion

This project demonstrates that classical machine learning models, especially SVM combined with solid text preprocessing and TF-IDF, can perform exceptionally well in spam classification tasks. Future improvements could include metadata features or deep learning-based models for even higher adaptability.

