# Text Classification using Naive Bayes

This project focuses on **multi-class text classification** using the **20 Newsgroups dataset**. It demonstrates both **scikit-learn’s Multinomial Naive Bayes** and a **custom implementation from scratch** to classify documents into one of 20 categories.

The pipeline involves **vocabulary creation**, **stopword removal**, **feature engineering**, and **model training/evaluation** using accuracy, confusion matrix, and classification report.

---

## Project Overview

This project allows you to:

- Load and parse documents from the 20 Newsgroups dataset
- Create a vocabulary of the most frequent words
- Remove English stopwords
- Convert documents into bag-of-words representations
- Train a Naive Bayes classifier using scikit-learn
- Implement a Multinomial Naive Bayes model from scratch
- Evaluate model performance using standard metrics
- Visualize classification results via confusion matrix and heatmaps

---

## Features

- Vocabulary building from raw text
- Stopword filtering using `ENGLISH_STOP_WORDS`
- Manual one-hot count vector generation using `Counter`
- Classification using:
  - `MultinomialNB` from scikit-learn
  - Custom `MultinomialNaiveBayes` class
- Evaluation:
  - Accuracy score
  - Confusion matrix
  - Classification report with precision, recall, F1-score

---

## Technologies Used

### Core Libraries & Tools

- Python
- NumPy / Pandas
- scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

## Model Architecture

### 1. Scikit-learn MultinomialNB

- Fit on a bag-of-words matrix of shape (20000, 50000)
- Trained on 15,000 samples and tested on 5,000
- Achieved **89.26% accuracy**

### 2. Custom Multinomial Naive Bayes

- Implemented from scratch using probability formulas
- Suffered from numerical instability (due to large vocab size)
- Achieved **35.7% accuracy**

---

## Results

| Metric                  | Value (sklearn) | Value (Scratch) |
|-------------------------|------------------|------------------|
| Accuracy                | 0.8926           | 0.3570           |
| Best Performing Classes | `rec.sport.hockey`, `sci.med` | Lower overall |
| Vocabulary Size         | 50,000           | 50,000           |
| Total Samples           | 20,000           | 20,000           |

---

## Dataset

- **Source**: 20 Newsgroups Text Classification Dataset
- **Format**: Raw text files organized by category folders
- **Total Categories**: 20
- **File Path**: `./twenty+newsgroups/20_newsgroups`

---

## APIs / Integrations

- `sklearn.feature_extraction.text.ENGLISH_STOP_WORDS` – Stopword removal
- `sklearn.naive_bayes.MultinomialNB` – Prebuilt classifier
- `Counter` from `collections` – Bag-of-words modeling
- `sklearn.metrics` – Evaluation and reporting

---

## Author

**Krish Dua**  
[Portfolio Website](https://krishdua.vercel.app) | [LinkedIn Profile](https://www.linkedin.com/in/krish-dua-9202a4272/)

---
