
# 🌸 Iris Flower Classification Project

[![Python Version](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
[![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?logo=Jupyter)](https://jupyter.org/try)

A classic machine learning project that classifies Iris flowers into three species (**Setosa**, **Versicolor**, **Virginica**) based on the length and width of their sepals and petals. This project serves as a perfect introduction to the world of data science and machine learning, utilizing the famous Iris dataset.

*The Iris dataset consists of three species: Setosa, Versicolor, and Virginica.*




## 🧠 Project Overview

This project aims to build a machine learning model that can accurately classify Iris flowers. We use the classic Iris dataset, which is often considered the "Hello World" of machine learning. The main steps involved are:

1.  **Data Exploration**: Understanding the data through statistical summaries and visualizations.
2.  **Data Preprocessing**: Splitting the dataset into training and testing sets.
3.  **Model Building**: Training a **Support Vector Machine (SVM)** classifier.
4.  **Model Evaluation**: Assessing the model's performance using metrics like accuracy and a classification report.

## 🌿 Dataset Description

The dataset used is the **Iris dataset**, which contains 150 samples of Iris flowers. There are 50 samples from each of the three species:

- **Setosa** (Iris setosa)
- **Versicolor** (Iris versicolor)
- **Virginica** (Iris virginica)

Each sample has **four features** (in centimeters):
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

The goal is to predict the **species (Class_labels)** based on these four measurements.

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

- **Python 3.12** (or later)
- `pip` (Python package installer)

### Installation

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
    cd MachineLearningProjects/1-Iris-Flower-Classification-Project
    ```

2.  **Create a virtual environment** (recommended):
    ```bash
    python3 -m venv venv
    ```

3.  **Activate the virtual environment**:
    - **On Linux**:
        ```bash
        source venv/bin/activate
        ```

4.  **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```


## 📁 Project Structure

```
1-Iris-Flower-Classification-Project/
│
├── project.ipynb          # The main Jupyter Notebook with all the code and analysis
├── iris.csv               # The dataset file
├── requirements.txt       # A list of required Python packages
└── README.md              # This file
```

## 📈 Analysis and Model Building

The project walks through a standard data science workflow.

### Data Visualization

We use `seaborn` and `matplotlib` to visualize the data. A pair plot of all features, colored by species, shows clear separations, especially for the Setosa species.


A bar chart comparing the average measurements for each species helps to highlight the differences in their physical characteristics.

### Model Training

We train a **Support Vector Machine (SVM)** classifier using the training data. SVM is a powerful and versatile model that works well on small datasets like this one.

```python
from sklearn.svm import SVC
svn = SVC()
svn.fit(X_train, y_train)
```

## 🎯 Results

The model demonstrates excellent performance on the test set.

- **Accuracy**: **96.67%**
- **Classification Report**:

```
              precision    recall  f1-score   support

      Setosa       1.00      1.00      1.00        11
  Versicolor       1.00      0.90      0.95        10
   Virginica       0.90      1.00      0.95         9

    accuracy                           0.97        30
   macro avg       0.97      0.97      0.96        30
weighted avg       0.97      0.97      0.97        30
```

The model successfully predicts all three species, with only a few minor misclassifications between the more similar Versicolor and Virginica species.

## 🔮 How to Use

You can use the trained model to predict the species of a new Iris flower. Provide the sepal and petal measurements in the same order.

```python
# Example: Predicting for three new flowers
X_new = np.array([[3, 2, 1, 0.2],
                  [4.9, 2.2, 3.8, 1.1],
                  [5.3, 2.5, 4.6, 1.9]])

prediction = svn.predict(X_new)
print("Prediction of Species: {}".format(prediction))
```

**Output**:
```
Prediction of Species: ['Setosa' 'Versicolor' 'Virginica']
```


## 📚 References

- [UCI Machine Learning Repository - Iris Dataset](https://archive.ics.uci.edu/ml/datasets/iris)
- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  
