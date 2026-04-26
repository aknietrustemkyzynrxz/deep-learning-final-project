# Weekly Report - Week 1 Rustemkyzy Akniyet

## Completed This Week

- I chose the project topic: Disaster Tweet Classification
- I chose the dataset: Natural Language Processing with Disaster Tweets from Kaggle
- I downloaded the dataset files (train.csv, test.csv, sample_submission.csv)
- I created the GitHub repository structure
- I wrote the project proposal
- I created the main README file
- I added dataset information in data/README.md


## Important Commits and Files Changed

Files created this week:

- project-proposal.md
- README.md
- data/README.md
- reports/week-01.md

Important commits:

- Add project proposal for disaster tweet classification
- Create README for final project
- Add dataset README and dataset information

## Experiments Run
I did not train the model this week.
This week was for project setup, dataset understanding, and GitHub organization.


## Results So Far
I checked the dataset successfully.

Main columns are:
- text
- keyword
- location
- target

The task is binary text classification:

- 1 = real disaster tweet
- 0 = not real disaster tweet

The training dataset has 7,613 labeled tweets.

## Problems or Blockers
One problem is that tweets are short and sometimes not clear.
Some people use disaster words as a joke, for example:
“My exam was a disaster.”

This can make prediction harder.
Some missing values may also exist in keyword and location columns.

## Plan for Next Week

- Clean and preprocess the dataset
- Handle missing values
- Split data into train, validation, and test sets
- Build the baseline model using Logistic Regression and TF-IDF
- Check baseline model results
