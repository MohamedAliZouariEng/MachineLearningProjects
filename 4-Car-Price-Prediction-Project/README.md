# 🚗 Car Price Prediction Project

![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Latest-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-DataAnalysis-green.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-yellow.svg)

## 📌 Project Overview

This project is part of my **Machine Learning Projects** series. The goal is to build a **Decision Tree Regressor** model to predict car prices based on various technical and physical features of the vehicle.  
The dataset includes attributes such as engine size, horsepower, fuel type, dimensions, and more.

> 🎯 **Objective**: Predict the `price` of a car using a regression model.

---

## 📁 Folder Structure

```
4-Car-Price-Prediction-Project/
│
├── project.ipynb          # Jupyter notebook with full analysis and model training
├── README.md              # Project documentation
└── requirements.txt       # Python dependencies
```

---

## 📊 Dataset Information

- **Source**: [CarPrice.csv](https://raw.githubusercontent.com/amankharwal/Website-data/master/CarPrice.csv)
- **Rows**: 205
- **Columns**: 26
- **Features used for training**:
  - `symboling`, `wheelbase`, `carlength`, `carwidth`, `carheight`
  - `curbweight`, `enginesize`, `boreratio`, `stroke`
  - `compressionratio`, `horsepower`, `peakrpm`, `citympg`, `highwaympg`
  - **Target**: `price`

---

## 🧠 Model Used

- **Algorithm**: `DecisionTreeRegressor` from scikit-learn
- **Train/Test Split**: 80% / 20%
- **Evaluation Metric**: R² Score (coefficient of determination)

---

## 📈 Results

The model achieved a **perfect R² score of 1.0** on the test set.  
⚠️ *This may indicate overfitting due to the small dataset size and the nature of decision trees. Further tuning or cross-validation is recommended for real-world deployment.*

---

## 🚀 Getting Started

Follow these instructions to set up and run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
cd MachineLearningProjects/4-Car-Price-Prediction-Project
```

### 2. Create and Activate Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate        # Linux
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 📦 Dependencies

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

Install all with:

```bash
pip install -r requirements.txt
```

---

## 📷 Sample Visualizations

- Distribution of car prices
- Correlation heatmap of numerical features

---

## 🔗 References

- [Aman Kharwal – Car Price Prediction Dataset](https://thecleverprogrammer.com/)

- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  

---
