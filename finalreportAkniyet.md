# Final Report Rustemkyzy Akniyet 
# Disaster Tweet Classification using LSTM and GRU Networks 

# 1. Project Overview
The goal of this project was to classify whether a tweet is about a real disaster or not.
People often use Twitter during earthquakes, floods, fires, accidents, and other emergency situations. But at the same time, people also use words like "disaster" or "dying" in jokes or everyday conversations.

For example:
- "My exam was a disaster"
- "This traffic is killing me"

For humans these examples are easy to understand, but for models it can be confusing because the same words can have different meanings depending on the context.
In this project, I wanted to compare a traditional machine learning approach and deep learning models to see which one works better for this task.

The labels are: 1 = disaster tweet,0 = not disaster tweet

# 2. Dataset Description
For this project I used the dataset: Natural Language Processing with Disaster Tweets
Source:Kaggle Competition Dataset
Link: https://www.kaggle.com/c/nlp-getting-started
Files used:train.csv,test.csv,sample_submission.csv

The training dataset contains 7613 labeled tweets.The test dataset contains 3263 unlabeled tweets.
Main columns:id,keyword,location,text,target
Although the dataset contains keyword and location columns, I mainly used the text column because many values in location were missing.

# 3. Weekly Progress
## Week 1
During the first week I mostly focused on project setup.I selected the topic, chose the dataset, downloaded the files, and created the GitHub repository structure.
I also prepared:
- project proposal
- README
- dataset description
- repository folders

At this stage I mainly tried to understand the dataset and prepare everything for future work.

## Week 2
During Week 2 I started working with the actual data.
First, I checked: dataset size,columns,missing values,class balance. After that I cleaned tweet text.

Preprocessing steps:
- lowercase conversion
- removed links
- removed usernames
- removed hashtags
- removed special characters
- removed extra spaces

Then I split the data and result show that datasets size:
- Train: 5329
- Validation: 1142
- Test: 1142

For the baseline model I used:
TF-IDF + Logistic Regression
Results:
Accuracy: 0.8170
F1-score: 0.7691

Honestly, the baseline worked much better than I expected.

## Week 3
This week I moved to deep learning models.
I prepared text for sequence processing:
- tokenization
- vocabulary creation
- word-to-index conversion
- sequence padding
- Dataset and DataLoader creation

Then I implemented two models:

### LSTM
Model structure:
- Embedding
- Bidirectional LSTM
- Dropout
- Fully connected layer

### GRU
Model structure:
- Embedding
- GRU
- Fully connected layer

Training settings:
- CrossEntropyLoss
- Adam optimizer
- batch size = 32
- epochs = 5

Results:
LSTM:Accuracy: 0.7828 , F1-score: 0.7339
GRU: Accuracy: 0.7592,F1-score: 0.7258

I expected deep learning models to perform better, but the baseline still gave higher results.

## Week 4
The last week was mostly about analysis and project organization.
Completed tasks:
- model comparison
- result tables
- F1-score plot
- confusion matrix
- error analysis
- final project organization

I also checked some incorrect predictions to understand where models make mistakes.

# 4. Final Results
| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression TF-IDF | 0.8170 | 0.8386 | 0.7102 | 0.7691 |
| LSTM | 0.7828 | 0.7738 | 0.6980 | 0.7339 |
| GRU | 0.7592 | 0.7096 | 0.7429 | 0.7258 |

The best model in this project was Logistic Regression.

# 5. Error Analysis
Some tweets were difficult because they contained disaster-related words in different meanings.
Examples:
- "auction shoes retro fire red"
- "was in nyc last week"

The model sometimes focused too much on keywords instead of understanding the full meaning.
Main reasons for mistakes:
- sarcasm
- emotional expressions
- informal language
- short tweets
- unclear context

# 6. Limitations
This project also had some limitations.
The dataset is not very large and tweets are usually short.
Many tweets contain slang, jokes, abbreviations, or emotional expressions.

# 7. Conclusion
In this project I compared traditional machine learning and deep learning approaches for disaster tweet classification.
The best result was achieved by Logistic Regression with TF-IDF features.
Best F1-score: 0.7691
Even though LSTM and GRU learned sequence information, TF-IDF worked better because tweets are short and important keywords are very informative.

# 8. References
Kaggle:  
https://www.kaggle.com/c/nlp-getting-started
