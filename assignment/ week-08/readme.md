
# Week 08: NLP Pipeline and Text Classification

**Course:** MBAI 5310G AI Programming
**Institution:** Ontario Tech University
**Instructor:** Zahra Atf
**Student:** Nisha Naresh (101008896)

## Business Problem

SafeShield, an insurance provider, receives a steady stream of customer messages across email, chat, call transcripts, the mobile app, and the claims portal. Each message needs to reach the right team, since a water-damage claim, a request for a policy document, and a billing complaint are handled by completely different departments. Sorting these by hand is slow and inconsistent, and a misrouted urgent claim can sit unanswered for days.

This project builds a Natural Language Processing pipeline that reads the raw message and predicts its `MessageCategory`, so messages can be routed automatically to the correct team. The value is faster, more reliable triage of customer messages, which shortens response times and reduces the chance that an urgent claim is missed.

## Dataset

| Item | Detail |
|------|--------|
| File | `NLP_Dataset_13_Insurance_Customer_Message.xlsx` |
| Rows | 120 customer messages |
| Columns | 9 |
| Missing values | 0 |
| Text column | `CustomerMessage` |
| Target column | `MessageCategory` |
| Classes | Home_Claim, Auto_Claim, Travel_Claim, Document_Request, Payment_Issue, Policy_Question (20 each, balanced) |

Additional context columns: Channel, City, PolicyType, CustomerType, and UrgencyLevel.

## Pipeline (Tasks 1 to 8)

1. **Load and inspect** the dataset: shape, columns, missing values, and target distribution.
2. **Preprocess** the text: lowercase, remove punctuation, tokenize, remove stopwords, and lemmatize into a `clean_message` column.
3. **Exploratory text analysis**: word-frequency counts and a bar chart of the top 20 words, with interpretation.
4. **POS tagging and Named Entity Recognition** on sample messages using spaCy, identifying nouns, verbs, and adjectives, plus locations, dates, and organizations.
5. **Feature extraction** with TF-IDF to convert cleaned text into numerical features.
6. **Model building**: a Multinomial Naive Bayes classifier trained on an 80/20 stratified train/test split.
7. **Evaluation**: accuracy, confusion matrix, and classification report, explained in plain business language.
8. **Business interpretation**: what the model predicts, the insight gained, and the limitations.

## Results Summary

The model classified the test messages with very high accuracy, since each category uses distinctive vocabulary (auto claims say "auto", billing messages say "payment", document requests say "document"). This shows that message text alone is a strong signal for routing. The main limitation is that the dataset is small (120 messages) with very clean, distinctive language, so the near-perfect accuracy is likely optimistic and would drop on a larger, messier set of real-world messages.

## Files

| File | Description |
|------|-------------|
| `Assignment 8_Nisha_Naresh.ipynb` | Full NLP pipeline notebook (Tasks 1 to 8) |
| `NLP_Dataset_13_Insurance_Customer_Message.xlsx` | Dataset |
| `README.md` | This file |

## Tools Used

- Python (Jupyter Notebook / Anaconda)
- pandas and NumPy
- NLTK (stopwords, lemmatization)
- spaCy (POS tagging and Named Entity Recognition)
- scikit-learn (TF-IDF, Multinomial Naive Bayes, evaluation metrics)
- matplotlib for visualisations

## How to Run

1. Open the notebook in Jupyter or Anaconda.
2. Install spaCy and its model if needed: `pip install spacy` then `python -m spacy download en_core_web_sm`.
3. Run the cells from top to bottom in order, since later tasks depend on the `clean_message` column created in Task 2.

## Responsible AI Note

This work is for educational purposes. The dataset is synthetic and contains no real customer information. The model is a decision-support tool for message routing and should be kept under human review, so unusual or ambiguous messages are checked rather than blindly routed.
