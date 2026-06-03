# 🐦 Twitter Sentiment Analysis Using Machine Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![NLP](https://img.shields.io/badge/NLP-NLTK-green)
![sklearn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Best Model](https://img.shields.io/badge/Best%20Model-Logistic%20Regression-brightgreen)

> **AI Mini Project** — NLP-based sentiment classification of tweets using TF-IDF and three machine learning classifiers.

---

## 📌 Overview

This project builds an automated sentiment analysis pipeline for Twitter data. Using the **Sentiment140 dataset** (1.6M tweets), it classifies tweets as **Positive** or **Negative** using Natural Language Processing and three ML classifiers.

**Team:**
- Prashanth Javaji
- Vivek Reddy D
- **Suhas A** *(that's you!)*

---

## 📊 Results

| Model | F1-Score (Class 0) | F1-Score (Class 1) | Winner |
|---|---|---|---|
| Bernoulli Naive Bayes | 0.90 | 0.66 | ❌ |
| Linear SVM | 0.91 | 0.68 | ❌ |
| **Logistic Regression** | **0.92** | **0.69** | ✅ |

> All three models achieved the same ROC-AUC score. **Logistic Regression** was the best overall performer.

---

## 🔄 Pipeline

1. **Data Loading** — Sentiment140 dataset (1.6M tweets, binary: Positive/Negative)
2. **Preprocessing:**
   - Lowercase conversion
   - Stopword removal
   - Punctuation cleaning
   - URL & number removal
   - Tokenization
   - Stemming (Porter Stemmer)
   - Lemmatization (WordNet)
3. **Feature Extraction** — TF-IDF Vectorizer (unigrams + bigrams, 500K features)
4. **Model Training** — Bernoulli NB, Linear SVC, Logistic Regression
5. **Evaluation** — Accuracy, F1-Score, Confusion Matrix, ROC-AUC Curve

---

## 📁 Dataset

- **Name**: Sentiment140
- **Size**: 1.6 million tweets
- **Classes**: Positive (1), Negative (0)
- **Features**: tweet ID, timestamp, user, sentiment, text
- **Link**: [Kaggle - Sentiment140](https://www.kaggle.com/datasets/kazanova/sentiment140)

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| NLP | NLTK (WordNet, PorterStemmer, RegexpTokenizer) |
| ML | scikit-learn (Logistic Regression, LinearSVC, BernoulliNB) |
| Feature Extraction | TF-IDF Vectorizer |
| Visualization | Matplotlib, Seaborn, WordCloud |
| Environment | Google Colab |

---

## 🚀 Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/suhasadidela/twitter-sentiment-analysis.git
cd twitter-sentiment-analysis

# 2. Install dependencies
pip install nltk scikit-learn pandas numpy matplotlib seaborn wordcloud

# 3. Download the dataset
# https://www.kaggle.com/datasets/kazanova/sentiment140
# Place as Project_Data.csv in the same folder

# 4. Open the notebook
jupyter notebook "twitter sentiment.ipynb"
```

---

## 📁 Repository Structure

```
├── twitter sentiment.ipynb               # Full analysis notebook
├── TWITTER SENTIMENT ANALYSIS(...).pptx  # Project presentation
├── AI mini project.pdf                   # Project report
└── README.md
```

---

## 👥 Contributors

| Name | Role |
|---|---|
| **Suhas A** ([@suhasadidela](https://github.com/suhasadidela)) | ML pipeline & model evaluation |
| Prashanth Javaji | Data preprocessing & NLP |
| Vivek Reddy D | Literature survey & visualization |

---

## 🔮 Future Work

- Extend to multi-class sentiment (neutral, mixed)
- Use transformer-based models (BERT, RoBERTa)
- Real-time tweet streaming and classification
- Topic-specific sentiment dashboards
