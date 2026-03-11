# Amazon Alexa Reviews Sentiment Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![NLP](https://img.shields.io/badge/NLP-Text%20Processing-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

# Project Overview

This project performs **Sentiment Analysis on Amazon Alexa product reviews** using Natural Language Processing (NLP) and Machine Learning techniques.

The goal is to classify customer reviews as **Positive or Negative** based on the review text.

The project includes:

- Text preprocessing
- Feature extraction using TF-IDF
- Machine learning models
- Model evaluation
- Visualization of results
- Sentiment prediction for new reviews

---

# Dataset

Dataset used: **Amazon Alexa Reviews Dataset**

The dataset contains **3,150 customer reviews** with the following columns:

| Column | Description |
|------|-------------|
| rating | Product rating (1–5) |
| date | Date of review |
| variation | Product variation |
| verified_reviews | Review text |
| feedback | Sentiment label (1 = Positive, 0 = Negative) |

Dataset shape:

```
3150 rows × 5 columns
```

Class distribution:

```
Positive Reviews : 2893
Negative Reviews : 257
```

---

# Project Workflow

The pipeline of the project follows these steps:

```
Data Loading
      ↓
Exploratory Data Analysis
      ↓
Text Preprocessing
      ↓
Feature Extraction (TF-IDF)
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Visualization
      ↓
Sentiment Prediction
```

---

# Text Preprocessing

To prepare the review text for machine learning, several NLP preprocessing steps were applied.

### Steps Included

1. Convert text to lowercase  
2. Remove URLs  
3. Remove special characters and digits  
4. Tokenization  
5. Stopword removal  
6. Lemmatization  

Example:

```
Original Review:
Love my Echo!

Cleaned Text:
love echo
```

Libraries used:

- **NLTK**
- **Regex**

---

# Feature Extraction

Text data was converted into numerical features using **TF-IDF (Term Frequency – Inverse Document Frequency)**.

Parameters used:

```
max_features = 5000
ngram_range = (1,2)
```

TF-IDF shapes:

```
Training Data : (2449, 5000)
Testing Data  : (613, 5000)
```

---

# Machine Learning Models

Two classification models were implemented:

### 1️⃣ Multinomial Naive Bayes

Commonly used for text classification problems.

Accuracy:

```
0.9233
```

---

### 2️⃣ Logistic Regression

A strong baseline model for binary classification.

Accuracy:

```
0.9233
```

---

# Model Evaluation

Metrics used:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Example classification report:

```
Accuracy: 0.92

Positive Reviews Precision: 0.92
Positive Reviews Recall:    1.00
F1 Score:                   0.96
```

---

# Visualizations

The following visualizations were generated:

### Confusion Matrices
Comparison between:

- Naive Bayes
- Logistic Regression

Saved as:

```
confusion_matrices.png
```

---

### Rating Distribution

Shows distribution of product ratings from customers.

Saved as:

```
rating_distribution.png
```

---

### Sentiment Distribution

Pie chart showing proportion of positive and negative reviews.

Saved as:

```
sentiment_distribution.png
```

---

# Predicting Sentiment for New Reviews

The project includes a function to predict sentiment for new user input.

Example:

```
Review:
This Alexa is amazing! It works perfectly.

Prediction:
Positive (Confidence: 95.79%)
```

Example output:

```
Review:
Terrible product. It doesn't work half the time.

Prediction:
Positive (Confidence: 50.71%)
```

---

# Technologies Used

Programming Language

```
Python
```

Libraries

```
NumPy
Pandas
Matplotlib
Seaborn
Scikit-learn
NLTK
Regex
```

Environment

```
Jupyter Notebook / Kaggle Notebook
```

---

# Project Structure

```
amazon-alexa-sentiment-analysis/
│
├── amazon_alexa.tsv
├── sentiment_analysis.ipynb
│
├── confusion_matrices.png
├── rating_distribution.png
├── sentiment_distribution.png
│
└── README.md
```

---

# Key Learnings

Through this project:

- Applied **Natural Language Processing techniques**
- Implemented **text preprocessing pipelines**
- Used **TF-IDF for feature extraction**
- Trained **multiple machine learning classifiers**
- Evaluated models using classification metrics
- Built a **sentiment prediction system**

---

# Future Improvements

Possible improvements include:

- Handling **class imbalance**
- Using **Deep Learning models (LSTM, BERT)**
- Hyperparameter tuning
- Deploying the model as a **web app**
- Creating a **real-time sentiment dashboard**

---

# Conclusion

This project demonstrates how **Natural Language Processing and Machine Learning can be used to analyze customer feedback**.

Such systems can help companies understand **customer satisfaction and product performance** by automatically analyzing large volumes of reviews.
