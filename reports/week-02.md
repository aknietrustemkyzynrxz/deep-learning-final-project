# Weekly Report - Week 2

## Completed This Week

- I loaded the dataset files: train.csv, test.csv, and sample_submission.csv.
- I checked the dataset shape, columns, missing values, and class balance.
- I cleaned the tweet text using simple preprocessing.
- I split the training data into train, validation, and test sets.
- I created TF-IDF features from the cleaned tweet text.
- I trained a baseline model using Logistic Regression.
- I evaluated the model using Accuracy, Precision, Recall, F1-score, and Confusion Matrix.
- I created a baseline submission file.

## Important Files Changed

Files created or updated this week:

- notebooks/week2_baseline.ipynb
- reports/week-02.md
- baseline_submission.csv


## Experiments Run

This week, I trained the first baseline model.

The baseline model was:

- TF-IDF Vectorizer
- Logistic Regression

The text preprocessing included:
- lowercasing
- removing links
- removing mentions
- removing hashtag symbol
- removing special characters
- removing extra spaces

The dataset was split into:
- Train: 5,329 tweets
- Validation: 1,142 tweets
- Test: 1,142 tweets

## Results
The baseline model gave good first results.

### Validation Results
| Metric | Score |
|---|---:|
| Accuracy | 0.7995 |
| Precision | 0.8149 |
| Recall | 0.6904 |
| F1-score | 0.7475 |

### Test Results
| Metric | Score |
|---|---:|
| Accuracy | 0.8170 |
| Precision | 0.8386 |
| Recall | 0.7102 |
| F1-score | 0.7691 |

The model performs better on non-disaster tweets than disaster tweets.  
The recall for disaster tweets is lower, which means the model still misses some real disaster tweets.

## Problems or Blockers

One problem is that some tweets are unclear or use disaster words in a non-real way.
For example, a tweet can use words like “disaster” or “fire” as a joke, not as a real event.
Another problem is that the `location` column has many missing values, so I did not use it in the baseline model.
The baseline model works well, but it does not fully understand word order and context.

## Plan for Next Week
- Prepare text data for deep learning models.
- Convert words into sequences.
- Add padding for equal sequence length.
- Build an LSTM model.
- Build a GRU model.
- Compare LSTM and GRU with the Logistic Regression baseline.
