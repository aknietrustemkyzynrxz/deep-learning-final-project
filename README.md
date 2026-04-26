# Disaster Tweet Classification using LSTM and GRU Networks

## Project Overview

The goal of this project is to classify whether a tweet is about a real disaster or not.

People use Twitter to post about fires, floods, earthquakes, accidents, and other emergency situations. However, many people also use disaster-related words in jokes or emotional expressions, such as “My exam was a disaster.”

This project uses deep learning models to understand tweet context and predict:

- 1 = real disaster tweet
- 0 = not a real disaster tweet


## Dataset

### Dataset Name

Natural Language Processing with Disaster Tweets

### Source

Kaggle Competition Dataset

### Link

https://www.kaggle.com/c/nlp-getting-started

### Files Used

- train.csv
- test.csv
- sample_submission.csv

The training dataset contains 7,613 labeled tweets.


## Models

### Baseline Model

- Logistic Regression
- TF-IDF Vectorization

### Deep Learning Models

- LSTM (Long Short-Term Memory)
- GRU (Gated Recurrent Unit)

These models are used because tweet classification is a text sequence problem.


## Evaluation Metrics

The project uses:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix


## Repository Structure

## Repository Structure

```
project-repo/
├── README.md
├── project-proposal.md
├── data/
│   └── README.md
├── notebooks/
├── src/
├── reports/
│   ├── week-01.md
│   ├── week-02.md
│   ├── week-03.md
│   └── week-04.md
├── results/
├── requirements.txt
└── final-report.md
```
---

## Final Goal

The final goal is to compare traditional machine learning models and deep learning models and find which method works better for disaster tweet classification.
