# Project Proposal: Disaster Tweet Classification using LSTM and GRU Networks

## 1. Project Title

Disaster Tweet Classification using LSTM and GRU Networks

## 2. Problem Statement

The goal of this project is to classify if a tweet is about a real disaster or not.

People use Twitter to post about fires, floods, earthquakes, accidents, and other emergency situations. But many people also use words like "disaster" or "dying" in a joke or emotional way. For example: "My exam was a disaster" or "I'm dying from homework."

Because of this, it is difficult for a computer to understand if the tweet is about a real disaster or just normal speech.

In this project, I will build a model that reads a tweet and predicts if it is talking about a real disaster.

This project is useful for emergency services, news monitoring, and disaster response because it helps find important tweets faster.

The model will predict:

* 1 = real disaster tweet
* 0 = not a real disaster tweet

## 3. Dataset

### Dataset Name

Natural Language Processing with Disaster Tweets

### Source

Kaggle Competition Dataset

### Link

[https://www.kaggle.com/c/nlp-getting-started](https://www.kaggle.com/c/nlp-getting-started)

### Number of Examples

The training dataset has 7,613 labeled tweets.

The test dataset has unlabeled tweets for final prediction.

### Input Features

Main columns:

* text (main tweet text)
* keyword (important word in the tweet)
* location (tweet location, sometimes empty)

For the main model, I will mainly use the **text** column.

### Target Label

* target = 1 -> real disaster
* target = 0 -> not real disaster

### Data Format

CSV files:

* train.csv
* test.csv
* sample_submission.csv

### Usage Notes

This dataset is public on Kaggle and can be used for academic and non-commercial work.


## 4. Planned Method

### Baseline Model

First, I will use Logistic Regression as a simple baseline model with TF-IDF text vectorization.

This helps compare a simple machine learning model with deep learning models.

### Deep Learning Model

The main deep learning models will be:

* LSTM (Long Short-Term Memory)
* GRU (Gated Recurrent Unit)

These models are good for text classification because tweets are sequences of words, and LSTM/GRU can understand context better.

### Loss Function

CrossEntropyLoss

### Evaluation Metrics

I will use:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

F1-score is important because the classes may not be balanced.

### Train / Validation / Test Split

The data will be split into:

* 70% training
* 15% validation
* 15% testing

The official Kaggle test set will be used only for final prediction.


## 5. Expected Challenges

One problem is that tweets are short and sometimes unclear. People use slang, short words, and informal language.

Another problem is that some tweets use disaster words in a funny or emotional way, not as a real event. This can confuse the model.

Some columns like location and keyword may also have missing values.

Overfitting can also happen when training LSTM and GRU models.

Training and tuning the model may take extra time.


## 6. Weekly Plan

| Week   | Planned Work                                                    | Expected Output                       |
| ------ | --------------------------------------------------------------- | ------------------------------------- |
| Week 1 | Choose dataset, create GitHub repository, and explore the data  | Proposal, README, dataset summary     |
| Week 2 | Data preprocessing, train/validation/test split, baseline model | Baseline results and Week 2 report    |
| Week 3 | Train LSTM and GRU models and compare results                   | Model results, plots, error analysis  |
| Week 4 | Improve model, final evaluation, final report, and presentation | Final code, final report, slides/demo |


## Final Goal

The final goal is to compare a simple machine learning model and deep learning models for disaster tweet classification and find which model works better for this task.
