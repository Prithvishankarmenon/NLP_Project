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
Precision, Recall, F1 - shown using classification_report()
