# Week 3 Report

## Completed This Week
This week I implemented deep learning models for disaster tweet classification using PyTorch.
I continued the project from Week 2, where I already completed data cleaning, preprocessing, TF-IDF vectorization, and the Logistic Regression baseline model.
In Week 3, I added sequence-based deep learning models:
- LSTM model
- GRU model

I also prepared the text data for sequence modeling.

## Data Preparation
I used the cleaned tweet text from Week 2.
The following preprocessing steps were completed:
- tokenization
- vocabulary creation
- converting words into integer IDs
- padding sequences to the same length
- creating PyTorch Dataset and DataLoader objects
The vocabulary size was limited to 10,000 words.
The maximum sequence length was set to 40 tokens.

## Models
### LSTM Model
The LSTM model included:
- Embedding layer
- LSTM layer
- Fully connected output layer

### GRU Model
The GRU model included:
- Embedding layer
- GRU layer
- Fully connected output layer

Both models were implemented using PyTorch.

## Training Setup
For training, I used:
- CrossEntropyLoss
- Adam optimizer
- batch size = 32
- 5 epochs
The models were trained on the training dataset and evaluated on the validation and test datasets.

## Results
### Logistic Regression Baseline
| Metric | Score |
| --- | --- |
| Accuracy | 0.8170 |
| Precision | 0.8386 |
| Recall | 0.7102 |
| F1-score | 0.7691 |

### LSTM Results
| Metric | Score |
| --- | --- |
| Accuracy | 0.7758 |
| Precision | 0.7566 |
| Recall | 0.7041 |
| F1-score | 0.7294 |

### GRU Results
| Metric | Score |
| --- | --- |
| Accuracy | 0.7653 |
| Precision | 0.7817 |
| Recall | 0.6286 |
| F1-score | 0.6968 |

## Analysis
The Logistic Regression baseline achieved the best overall performance in this experiment.
The LSTM and GRU models were still able to learn useful patterns from the tweets, but the traditional TF-IDF approach worked better on this dataset.
One possible reason is that tweets are very short texts, and TF-IDF features are already very informative for this task.
The LSTM model performed slightly better than the GRU model.

## Error Analysis
I also analyzed incorrect predictions from both models.
Some tweets were difficult because:
- they contained sarcasm or jokes,
- they used disaster words in a non-disaster meaning,
- they were very short or unclear.

Examples:
- "my exam was a disaster"
- tweets with emotional language but no real disaster event

## Files Added or Updated
- `notebooks/week3_lstm_gru.ipynb`
- `reports/week-03.md`

## Plan for Next Week
Next week I plan to:
- improve the final project notebook,
- organize the repository,
- prepare the final report,
- prepare presentation slides,
- write the final conclusions and limitations section.
