# Diabetes Prediction Project 🩺

> **Predict diabetes using Machine Learning algorithms with high accuracy!**

![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.8-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green.svg)


## 📋 Project Overview

This project applies various machine learning algorithms to predict diabetes based on diagnostic measurements. Using the PIMA Indian Diabetes Dataset, we build and evaluate multiple classifiers to achieve optimal prediction accuracy.

### 🎯 Key Features

- **Multiple ML Algorithms**: K-Nearest Neighbors (KNN), Decision Tree, and Neural Network (MLP) classifiers
- **Data Preprocessing**: Standard scaling and feature importance analysis
- **Performance Visualization**: Accuracy comparisons and feature importance plots
- **Model Optimization**: Hyperparameter tuning for better predictions

## 📊 Dataset

The dataset contains 768 patient records with the following features:

| Feature | Description |
|---------|-------------|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skin fold thickness (mm) |
| Insulin | 2-Hour serum insulin (mu U/ml) |
| BMI | Body mass index (kg/m²) |
| DiabetesPedigreeFunction | Diabetes pedigree function |
| Age | Age (years) |
| **Outcome** | **Target variable (0 = No Diabetes, 1 = Diabetes)** |

## 📈 Results

### Model Performance Comparison

| Model | Training Accuracy | Test Accuracy |
|-------|------------------|---------------|
| KNN (n=10) | 77.43% | 77.08% |
| Decision Tree (max_depth=3) | 77.3% | 74.0% |
| MLP (default) | 73.1% | 72.4% |
| **MLP (Scaled + Optimized)** | **80.6%** | **79.7%** |

### Key Findings

- **Feature Importance**: Glucose and BMI are the most significant predictors
- **Best Model**: MLP with StandardScaler achieved 79.7% test accuracy
- **Neural Network**: 1000 iterations with alpha=1 regularization

## 🚀 Installation & Setup

### Prerequisites

- Python 3.12 or higher
- Git

### Clone & Setup

```bash
# Clone the repository
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git

# Navigate to project directory
cd MachineLearningProjects/10-Predict-Diabetes-Project

# Create virtual environment
python3 -m venv venv

# Activate virtual environment
# On Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```


## 📊 Visualizations

The project includes:
- **Accuracy comparison plots** for KNN with different k-values
- **Feature importance bar charts** for Decision Tree
- **Neural network weight matrix visualization**

## 🧠 Algorithms Explained

### 1. K-Nearest Neighbors (KNN)
- Simple, instance-based learning
- Optimal k-value found through testing (k=10)

### 2. Decision Tree
- Interpretable model with feature importance
- Max depth limited to 3 to prevent overfitting

### 3. Multi-Layer Perceptron (MLP)
- Neural network with one hidden layer
- StandardScaler preprocessing improved accuracy significantly

## 📁 Project Structure

```
10-Predict-Diabetes-Project/
├── project.ipynb          # Main Jupyter notebook with all code
├── diabetes.csv           # Dataset file
├── requirements.txt       # Python dependencies
└── README.md             # Project documentation
```

## 📚 References

- [PIMA Indian Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)

---
