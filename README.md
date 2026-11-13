# sms Spam Classifier

A machine learning app that classifies text messages as **spam** or **ham** (legitimate), with a live web demo.

**[Live demo](https://colleymo-spam-ham.streamlit.app)** · Python · scikit-learn · Streamlit

<!-- Add a screenshot or short GIF of the app here: ![Demo](docs/demo.png) -->

## Overview

Spam and phishing messages are a daily nuisance and a real security risk. This project trains a text classifier on labelled messages and serves it through a simple web interface where anyone can paste a message and get an instant prediction.

## How it works

1. **Data:** the [Telegram Spam or Ham](https://www.kaggle.com/datasets/mexwell/telegram-spam-or-ham) dataset from Kaggle.
2. **Preprocessing:** lowercasing, punctuation and stop-word removal, tokenisation (NLTK).
3. **Features:** text converted to numeric vectors with a saved vectorizer (`vectorizer.pkl`).
4. **Model:** Support Vector Machine (SVM) classifier (`svm_classifier.pkl`).
5. **App:** Streamlit interface that loads the saved model and vectorizer and predicts on user input.

## Results

| Metric    | Score |
|-----------|-------|
| Accuracy  | 95%   |
| Precision | XX%   |
| Recall    | XX%   |
| F1-score  | XX%   |

<!-- Fill in from your notebook. Spam data is usually imbalanced, so report precision, recall and F1, not just accuracy. Optionally add a confusion matrix image. -->

## Project structure

```
├── app.py                              # Streamlit app
├── Spam_or_Ham_classification.ipynb    # Exploration, training, evaluation
├── svm_classifier.pkl                  # Trained model
├── vectorizer.pkl                      # Fitted text vectorizer
├── requirements.txt
└── README.md
```

## Tech stack

Python, pandas, NLTK, scikit-learn, Streamlit

## Limitations and next steps

- Trained on a single dataset, so it may not generalise to other message styles or languages.
- Add a confidence score to each prediction.
- Compare against other models (Naive Bayes, Logistic Regression, a fine-tuned transformer).
- Add error analysis of misclassified messages.

## Author

**Muhammed Colley**, MSc Artificial Intelligence
[LinkedIn](https://www.linkedin.com/in/colleymuhammed) · [GitHub](https://github.com/colleymohamed)
