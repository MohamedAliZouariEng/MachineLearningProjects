# 𝕩 X Sentiment Analysis Project

[![Python](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
[![NLTK](https://img.shields.io/badge/NLTK-Sentiment-green.svg)](https://www.nltk.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-DecisionTree-orange.svg)](https://scikit-learn.org/)

## 📌 Project Overview

This project performs **sentiment analysis** on X data using **VADER (Valence Aware Dictionary and sEntiment Reasoner)** from NLTK. It processes raw tweets, cleans them, and classifies the overall sentiment as **Positive 😊**, **Negative 😩**, or **Neutral 😐** based on aggregated polarity scores.

The dataset contains labeled tweets with hate speech, offensive language, and neutral categories. However, the analysis focuses on extracting sentiment scores (Positive, Negative, Neutral) from the tweet text itself.

---

## 📂 Repository Structure

```
3-X-Sentiment-Analysis-Project/
│
├── project.ipynb          # Main Jupyter Notebook with all code
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation (this file)
```

---

## 🚀 Features

- ✅ Text cleaning (removes URLs, punctuation, numbers, stopwords)
- ✅ Stemming using SnowballStemmer
- ✅ Sentiment scoring with VADER (Positive, Negative, Neutral)
- ✅ Aggregate sentiment classification
- ✅ Easy-to-read emoji output 😊😩😐

---

## 🛠️ Technologies Used

| Library | Purpose |
|---------|---------|
| `pandas` | Data manipulation |
| `numpy` | Numerical operations |
| `nltk` | Stopwords, stemming, VADER sentiment |
| `scikit-learn` | CountVectorizer |
| `re` | Regular expressions for text cleaning |

---

## 📊 Dataset

The dataset is loaded directly from a raw GitHub URL:
```
https://raw.githubusercontent.com/amankharwal/Website-data/master/twitter.csv
```

Columns:
- `tweet` — raw tweet text
- `class` — 0: hate speech, 1: offensive language, 2: neutral
- `count`, `hate_speech`, `offensive_language`, `neither` — annotation details

---

## 🔧 Setup Instructions

Follow these steps to run the project on your local machine:

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
cd MachineLearningProjects/3-X-Sentiment-Analysis-Project
```

### 2️⃣ Create and Activate Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate      # On Linux
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```


> 🧠 **Note:** NLTK will automatically download required data (`stopwords`, `vader_lexicon`) when you run the notebook.

---

## 📈 Output Example

After processing all tweets, the script outputs:

```
Positive:  2880.086
Negative:  7201.021
Neutral:   14696.888
Neutral 😐
```

> The overall dataset sentiment is **Neutral** based on aggregate scores.

---

## 📝 Code Walkthrough

1. **Load Data** — Read CSV from GitHub
2. **Clean Tweets** — Remove noise (URLs, punctuation, stopwords, numbers)
3. **Stemming** — Reduce words to root form
4. **Sentiment Scoring** — Apply VADER to each cleaned tweet
5. **Aggregate** — Sum Positive, Negative, Neutral scores
6. **Classify** — Compare totals and print sentiment with emoji

---

## 📚 References

- [NLTK VADER Sentiment Analysis](https://www.nltk.org/howto/sentiment.html)
- [Dataset Source](https://github.com/amankharwal/Website-data/blob/master/twitter.csv)
- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  
---
