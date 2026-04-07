
# 🙃 Sarcasm Detection

[![Python Version](https://img.shields.io/badge/python-3.12-blue.svg)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4.0-orange.svg)](https://scikit-learn.org/)


## 📌 Overview

This project implements a **sarcasm detection model** using **Natural Language Processing (NLP)** and **Machine Learning**. The model is trained on a dataset of news headlines labeled as sarcastic or not sarcastic, and it uses a **Bernoulli Naïve Bayes** classifier combined with a **CountVectorizer** for feature extraction.

> 🎯 **Goal**: Predict whether a given text input is sarcastic or non-sarcastic.

---

## 📁 Project Structure

```
9-Sarcasm-Detection-Project/
│
├── project.ipynb          # Jupyter Notebook with full implementation
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
```

---

## 🚀 Getting Started

Follow these instructions to set up and run the project on your local machine.

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
cd MachineLearningProjects/9-Sarcasm-Detection-Project
```

### 2️⃣ Create and Activate Virtual Environment

**On Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```


### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```


---

## 🧪 How It Works

1. **Data Loading**  
   The dataset is loaded directly from a JSON file hosted on GitHub. It contains `headline` and `is_sarcastic` (0/1) columns.

2. **Preprocessing**  
   - The target labels are mapped to `"Sarcasm"` and `"Not Sarcasm"` for readability.
   - Only the `headline` and `is_sarcastic` columns are kept.

3. **Feature Extraction**  
   - `CountVectorizer` converts text headlines into a bag-of-words matrix.

4. **Model Training**  
   - A **Bernoulli Naïve Bayes** classifier is trained on 80% of the data.

5. **Evaluation**  
   - The model achieves ~84.5% accuracy on the test set.

6. **Prediction**  
   - Users can input any text to check if it's sarcastic or not.

---

## 📊 Example

```python
Enter a Text: "Oh great, another Monday morning."
Output: ['Sarcasm']
```

---

## 📈 Model Performance

| Metric    | Score     |
|-----------|-----------|
| Accuracy  | 84.48%    |

---
## 🔗 References

- [Aman Kharwal – Sarcasm Dataset](https://raw.githubusercontent.com/amankharwal/Website-data/master/Sarcasm.json)

- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  
---
