# Daily News Digest - Model Training

This repo contains the machine learning pipeline for training a category-wise news classifier and a summarizer.

## Project Overview

**Goal:**  
Automatically summarize daily news articles into short bullet points grouped by category like **Politics, Sports, Technology**, etc.

**Problem Statement:**  
People don’t have time to read full articles. This project solves that by giving bite-sized summaries from live news.

## Dataset

We used the [GNews Dataset](https://www.kaggle.com/datasets) which contains:

- News class labels (`World`, `Sports`, `Business`, `Sci/Tech`)
- Headlines + descriptions
- CSV format used: `train.csv`

## Model

- **Classifier**: TF-IDF + Naive Bayes
- **Summarizer**: TF-IDF + PageRank (Extractive)

Model output:
```plaintext
              precision    recall  f1-score   support

    Business       0.85      0.86      0.85      5911
    Sci/Tech       0.88      0.86      0.87      6075
      Sports       0.94      0.97      0.96      6058
       World       0.91      0.88      0.90      5956

    accuracy                           0.89     24000
   macro avg       0.89      0.89      0.89     24000
weighted avg       0.89      0.89      0.89     24000
