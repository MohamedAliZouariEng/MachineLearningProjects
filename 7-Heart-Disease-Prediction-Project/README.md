# Heart Disease Prediction Project ❤️

> **A Machine Learning project to predict the likelihood of heart disease based on patient medical data**

[![Python Version](https://img.shields.io/badge/python-3.12-blue.svg)](https://python.org)

## 🎯 Overview

This project aims to predict whether a patient has heart disease based on various clinical parameters. Using **Logistic Regression**, we achieve approximately **87% accuracy** in predicting heart disease presence.

Heart disease is one of the leading causes of death worldwide. Early detection and risk assessment can significantly improve patient outcomes. This model provides a tool for healthcare professionals to assess cardiovascular risk based on patient data.

## 📊 Dataset

The dataset used in this project is the **Heart Disease dataset** from the UCI Machine Learning Repository, containing medical records of 303 patients.

| Property | Value |
|----------|-------|
| **Total Samples** | 303 |
| **Features** | 13 clinical features |
| **Target** | 0 = No heart disease, 1 = Heart disease |
| **Missing Values** | None |

## 📈 Features

| Feature | Description | Type |
|---------|-------------|------|
| **age** | Age in years | Continuous |
| **sex** | 1 = male, 0 = female | Binary |
| **cp** | Chest pain type (0-3) | Categorical |
| **trestbps** | Resting blood pressure (mm Hg) | Continuous |
| **chol** | Serum cholesterol (mg/dl) | Continuous |
| **fbs** | Fasting blood sugar > 120 mg/dl (1 = true; 0 = false) | Binary |
| **restecg** | Resting electrocardiographic results (0-2) | Categorical |
| **thalach** | Maximum heart rate achieved | Continuous |
| **exang** | Exercise induced angina (1 = yes; 0 = no) | Binary |
| **oldpeak** | ST depression induced by exercise relative to rest | Continuous |
| **slope** | Slope of the peak exercise ST segment (0-2) | Categorical |
| **ca** | Number of major vessels colored by fluoroscopy (0-4) | Categorical |
| **thal** | Thalassemia (0-3) | Categorical |

## 🚀 Installation

### Prerequisites
- Python 3.12 or higher
- Git

### Step-by-Step Setup

1. **Clone the repository**
```bash
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
cd MachineLearningProjects/7-Heart-Disease-Prediction-Project
```

2. **Create and activate a virtual environment**

**On Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```


3. **Install required packages**
```bash
pip install -r requirements.txt
```



### Key Code Sections

```python
# Import necessary libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

# Load and explore the dataset
df = pd.read_csv("https://raw.githubusercontent.com/amankharwal/Website-data/master/heart.csv")

# Data preprocessing - one-hot encoding for categorical variables
categorical_val = ['sex', 'cp', 'fbs', 'restecg', 'exang', 'slope', 'ca', 'thal']
dataset = pd.get_dummies(df, columns=categorical_val)

# Feature scaling for continuous variables
s_sc = StandardScaler()
col_to_scale = ['age', 'trestbps', 'chol', 'thalach', 'oldpeak']
dataset[col_to_scale] = s_sc.fit_transform(dataset[col_to_scale])

# Split data and train model
X = dataset.drop('target', axis=1)
y = dataset.target
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

lr_clf = LogisticRegression(solver='liblinear')
lr_clf.fit(X_train, y_train)
```

## 📊 Model Performance

### Logistic Regression Results

| Metric | Training Set | Testing Set |
|--------|--------------|-------------|
| **Accuracy** | 86.79% | 86.81% |
| **Precision (Class 0)** | 0.88 | 0.87 |
| **Recall (Class 0)** | 0.82 | 0.83 |
| **F1-Score (Class 0)** | 0.85 | 0.85 |
| **Precision (Class 1)** | 0.86 | 0.87 |
| **Recall (Class 1)** | 0.90 | 0.90 |
| **F1-Score (Class 1)** | 0.88 | 0.88 |

### Confusion Matrix

**Training Set:**
```
[[ 80  17]
 [ 11 104]]
```

**Testing Set:**
```
[[34  7]
 [ 5 45]]
```

## 📈 Visualizations

The project includes several visualizations to understand the data better:

### 1. **Target Distribution**
Bar chart showing the distribution of heart disease cases in the dataset.

### 2. **Categorical Feature Analysis**
Histograms comparing feature distributions between patients with and without heart disease for categorical variables:
- Sex, Chest Pain Type, Fasting Blood Sugar, Resting ECG, Exercise Induced Angina, Slope, Number of Vessels, Thalassemia

### 3. **Continuous Feature Analysis**
Histograms comparing feature distributions for continuous variables:
- Age, Resting Blood Pressure, Cholesterol, Maximum Heart Rate, Oldpeak

### 4. **Correlation Heatmap**
A comprehensive correlation matrix showing relationships between all features and the target variable.

### 5. **Feature Correlation with Target**
Bar plot showing each feature's correlation coefficient with the target variable.

### 6. **Age vs Max Heart Rate Scatter Plot**
Visualization showing the relationship between age, maximum heart rate, and heart disease presence.

## 📈 Results

The Logistic Regression model achieved:

- ✅ **86.81% accuracy** on unseen test data
- ✅ **90% recall** for detecting heart disease (identifying 90% of actual positive cases)
- ✅ **87% precision** for heart disease prediction
- ✅ Consistent performance between training and testing sets (minimal overfitting)

## 🛠️ Technologies Used

| Category | Technologies |
|----------|--------------|
| **Language** | Python 3.12 |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Machine Learning** | Scikit-learn |
| **Development** | Jupyter Notebook |

## 📁 Project Structure

```
7-Heart-Disease-Prediction-Project/
│
├── project.ipynb          # Main Jupyter notebook with complete analysis
├── requirements.txt       # Python package dependencies
├── README.md             # Project documentation
```


## 📚 References

- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  
- [UCI Machine Learning Repository - Heart Disease Dataset](https://archive.ics.uci.edu/ml/datasets/Heart+Disease)
