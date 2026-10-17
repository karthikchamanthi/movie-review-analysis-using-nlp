# IMDB Movie Review Sentiment Classification

## Project Overview

This project uses Natural Language Processing (NLP) and Machine Learning to classify IMDB movie reviews as **positive or negative**. The goal is to transform raw text into numerical features, train a classification model, evaluate its performance, and identify the words and phrases most strongly associated with each sentiment.

## Dataset

- **Dataset:** IMDB Dataset
- **File:** `IMDB Dataset.csv`
- **Input feature:** Movie review text (`review`)
- **Target variable:** Sentiment (`sentiment`)
- **Classes:** Positive and Negative

## Technologies Used

- Python
- Pandas and NumPy
- NLTK
- Scikit-learn
- Matplotlib
- Jupyter Notebook / Google Colab

## Project Workflow

### 1. Data Loading and Exploration
- Load the IMDB dataset using Pandas.
- Examine the dataset structure, column names, and sentiment distribution.
- Check for missing values and duplicate records.

### 2. Text Preprocessing
- Convert text to lowercase.
- Remove HTML tags, punctuation, and numbers.
- Tokenize reviews into individual words.
- Remove English stopwords.
- Apply Porter stemming to reduce words to their root forms.

### 3. Feature Extraction
Use **TF-IDF (Term Frequency–Inverse Document Frequency)** to convert text into numerical features. The vectorizer considers individual words and two-word phrases, helping the model capture useful sentiment-related expressions.

### 4. Model Training
Train a **Logistic Regression** classifier using the processed text features. Split the dataset into training and testing sets using an 80:20 ratio and use stratified sampling to preserve the sentiment distribution.

### 5. Model Evaluation
Evaluate the classifier using:
- **Accuracy:** Measures the proportion of correctly classified reviews.
- **Precision:** Measures the reliability of positive predictions for each class.
- **Recall:** Measures how many actual examples of each class are correctly identified.
- **F1-score:** Balances precision and recall.

### 6. Important Word Analysis
Analyze the learned Logistic Regression coefficients to identify the top 10 features associated with positive sentiment and the top 10 associated with negative sentiment. Visualize these features using horizontal bar charts.

### 7. Prediction on New Reviews
Use the trained model to predict the sentiment of new
