# 📧 Spam Message Detection Project

[![Python Version](https://img.shields.io/badge/Python-3.12-blue.svg)](https://python.org)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.8-orange.svg)](https://scikit-learn.org/)

> 🚀 A machine learning project to detect spam messages using **Naive Bayes** classification and **Natural Language Processing (NLP)** techniques.


## 🔍 Overview

This project implements a **Spam Detection System** that classifies messages as either **spam** or **ham** (non-spam). It uses the **Multinomial Naive Bayes** algorithm combined with **CountVectorizer** for text feature extraction. The model is trained on a real-world Email dataset and can be used to filter unwanted messages.

---

## ✨ Features

- ✅ **Text Preprocessing** – Converts raw messages into numerical feature vectors
- ✅ **Naive Bayes Classifier** – Fast and effective for text classification tasks
- ✅ **Interactive Testing** – Enter any message to check if it's spam or ham
- ✅ **High Accuracy** – Well-suited for imbalanced text datasets
- ✅ **Reproducible Results** – Fixed random state for consistent train/test splits

---

## 📊 Dataset

The dataset used is the **SMS Spam Collection** from UCI, containing **5,574** labeled messages:

| Class | Count  | Percentage |
|-------|--------|-------------|
| Ham   | 4,825  | 86.6%       |
| Spam  | 747    | 13.4%       |

**Source**: [SMS Spam Collection on Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| 🐼 `pandas` | Data manipulation & analysis |
| 🔢 `numpy` | Numerical operations |
| 🤖 `scikit-learn` | Machine learning (Naive Bayes, vectorization, train/test split) |
| 📝 `CountVectorizer` | Convert text to token counts |

---

## 💻 Installation

Follow these steps to run the project locally:

### 1️⃣ Clone the repository
```bash
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
cd MachineLearningProjects/5-Spam-Detection-Project
```

### 2️⃣ Create and activate a virtual environment

**On Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```
---

## 🚀 Usage

### 🧠 Training the Model
Run all cells in `project.ipynb`. The script will:
1. Load the dataset from GitHub
2. Clean and prepare the data
3. Split into training (67%) and testing (33%)
4. Train the Naive Bayes model

### 🧪 Testing with Custom Messages
After training, a cell will prompt you to enter a message:
```python
Enter a message: Congratulations! You've won a free iPhone! Click here to claim.
# Output: ['spam']
```

```python
Enter a message: Hey, are we still meeting for coffee tomorrow?
# Output: ['ham']
```

---

## 📁 Project Structure

```
5-Spam-Detection-Project/
│
├── project.ipynb          # Main Jupyter notebook with complete code
├── requirements.txt       # Python dependencies (to be created)
├── README.md              # Project documentation (this file)

```

---

## 📈 Results

| Metric           | Score              |
|------------------|--------------------|
| **Algorithm**    | MultinomialNB      |
| **Vectorizer**   | CountVectorizer    |
| **Test Size**    | 33%                |
| **Random State** | 42                 |

> 💡 *The model achieves high accuracy due to Naive Bayes' strong performance on text classification tasks, especially with sparse word count features.*

---

## 📚 References

- [SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  

---
