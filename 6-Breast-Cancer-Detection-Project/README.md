# 🩺 Breast Cancer Detection Project

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-latest-orange.svg)

## 📌 Project Overview

This project implements a **Naive Bayes Classifier** to detect breast cancer using the famous **Wisconsin Breast Cancer Dataset** from scikit-learn. The model classifies tumors as **malignant** or **benign** based on features computed from digitized images of fine needle aspirates (FNA) of breast masses.

The goal is to build a simple yet effective machine learning model that achieves high accuracy in predicting breast cancer, aiding in early detection and diagnosis.

---

## 🎯 Key Features

- ✅ Uses **Gaussian Naive Bayes** algorithm for classification
- 📊 Achieves **~97.4% accuracy** on test data
- 🧪 Trained and tested on real-world medical data
- 📈 Easy to extend with other classifiers (Logistic Regression, SVM, etc.)
- 🔍 Interpretable and fast model suitable for medical screening

---

## 📁 Dataset Information

The dataset is built into `scikit-learn` and contains **569 samples** with **30 features** each.

| Attribute | Details |
|-----------|---------|
| Classes | 2 (Malignant = 0, Benign = 1) |
| Features | Mean radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, fractal dimension (and their standard errors & worst values) |


---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
cd MachineLearningProjects/6-Breast-Cancer-Detection-Project
```

### 2. Create and Activate Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate 
```

### 3. Install Requirements

```bash
pip install -r requirements.txt
```

Run all cells to see the model training and evaluation.

---

## 📊 Model Performance

| Metric       | Score    |
|--------------|----------|
| Accuracy     | 97.37%   |
| Algorithm    | Gaussian Naive Bayes |
| Train/Test Split | 80% / 20% |

```python
# Sample prediction output
[1 0 0 1 1 0 0 0 1 1 1 ...]  # 1 = Benign, 0 = Malignant
```

---

## 🧠 How It Works

1. **Load Dataset** – Load breast cancer data from `sklearn.datasets`
2. **Explore Data** – Print feature names, labels, and sample values
3. **Split Data** – 80% training, 20% testing (random_state=42 for reproducibility)
4. **Train Model** – Fit `GaussianNB()` on training data
5. **Predict & Evaluate** – Predict on test set and calculate accuracy

---

## 📂 Project Structure

```
6-Breast-Cancer-Detection-Project/
│
├── project.ipynb          # Main Jupyter notebook with code
├── requirements.txt       # Python dependencies (to be created)
├── README.md              # Project documentation (this file)
```

---

---

## 📚 References


- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  
