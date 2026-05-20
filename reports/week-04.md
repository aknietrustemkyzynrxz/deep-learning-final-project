# Week 4 Report

## Completed This Week
This week I finalized the project and completed the final stage of analysis for disaster tweet classification.
I continued the project from Week 3, where I implemented LSTM and GRU models and compared them with the Logistic Regression baseline.
In Week 4, I focused on:
- comparing all model results
- analyzing model behavior
- preparing final visualizations
- organizing the project structure
- preparing final project materials
- writing conclusions and limitations
- preparing project presentation

## Model Comparison

Three models were compared:
- Logistic Regression (baseline)
- LSTM
- GRU

The comparison included:
- Accuracy
- Precision
- Recall
- F1-score

Final results:
| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression | 0.8170 | 0.8386 | 0.7102 | 0.7691 |
| LSTM | 0.7758 | 0.7566 | 0.7041 | 0.7294 |
| GRU | 0.7653 | 0.7817 | 0.6286 | 0.6968 |


## Analysis
The Logistic Regression baseline achieved the highest overall performance.
The TF-IDF representation worked very well because tweets are short texts and important keywords strongly influence classification.
The LSTM model captured sequence information and contextual patterns but required more training time.
The GRU model trained faster and used fewer parameters than LSTM, but its performance was slightly lower.
Overall observations:
- Logistic Regression achieved best performance
- LSTM performed better than GRU
- Deep learning models required more computational resources
- Sequence models still learned useful semantic information

## Error Analysis
Some tweets remained difficult for all models.
Common sources of errors
- sarcasm
- informal language
- short messages
- emotional expressions
- words used in different contexts

Examples:
- "my exam was a disaster"
- "this traffic is killing me"

These examples contain disaster-related words but do not describe real disaster events.

## Final Conclusions

The project demonstrated that traditional machine learning approaches can outperform deep learning methods on short text classification tasks.
Deep learning models remain useful because they can capture sequence information and may perform better with larger datasets and additional tuning.

---

## Project Status

Project status: Completed

Week 4 successfully finalized the project and prepared all materials for submission and defense.
