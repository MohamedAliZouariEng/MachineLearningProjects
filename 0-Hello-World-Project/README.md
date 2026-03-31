# Iris Flower Classification

A machine learning project that classifies iris flowers into three species (Setosa, Versicolor, and Virginica) based on their sepal and petal measurements.

## 📋 Overview

This project implements and compares multiple classification algorithms on the classic Iris dataset. The goal is to predict the species of an iris flower given its sepal length, sepal width, petal length, and petal width measurements.

## 🎯 Dataset

The dataset contains 150 samples of iris flowers with the following features:
- **Sepal length** (cm)
- **Sepal width** (cm)  
- **Petal length** (cm)
- **Petal width** (cm)

### Target Classes:
- **Iris-setosa** (50 samples)
- **Iris-versicolor** (50 samples)
- **Iris-virginica** (50 samples)

## 🚀 Algorithms Tested

The following classification algorithms were evaluated:

1. **Linear Discriminant Analysis (LDA)**
2. **K-Nearest Neighbors (KNN)**
3. **Classification and Regression Trees (CART)**
4. **Naive Bayes (NB)**
5. **Support Vector Machine (SVM)**

## 📊 Results

### Cross-Validation Performance (10-fold)

| Algorithm | Mean Accuracy | Standard Deviation |
|-----------|--------------|-------------------|
| SVM | 0.9833 | 0.0333 |
| LDA | 0.9750 | 0.0382 |
| KNN | 0.9583 | 0.0417 |
| CART | 0.9500 | 0.0408 |
| NB | 0.9500 | 0.0553 |

### Best Model Performance (SVM on Test Set)

- **Accuracy**: 96.67%
- **Confusion Matrix**:
```
[[11  0  0]
 [ 0 12  1]
 [ 0  0  6]]
```

### Classification Report (SVM)

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| Iris-setosa | 1.00 | 1.00 | 1.00 | 11 |
| Iris-versicolor | 1.00 | 0.92 | 0.96 | 13 |
| Iris-virginica | 0.86 | 1.00 | 0.92 | 6 |

## 📈 Visualizations

The project includes several visualizations to understand the data:
- **Box and Whisker plots**: Shows feature distributions across classes
- **Histograms**: Displays the frequency distribution of each feature
- **Scatter Plot Matrix**: Reveals relationships between different features

## 🛠️ Technologies Used

- Python 3.x
- Pandas - Data manipulation and analysis
- NumPy - Numerical computing
- Matplotlib - Data visualization
- Scikit-learn - Machine learning algorithms

## 📁 Project Structure

```
iris-classification/
├── project.ipynb          # Jupyter notebook with complete analysis
├── README.md             # Project documentation
└── requirements.txt      # Python dependencies
```

## 🔧 Installation & Usage

1. **Clone the repository**
```bash
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
cd MachineLearningProjects/0-Hello-World-Project
```

2. **Create and activate a virtual environment**
```bash
# Create virtual environment
python3 -m venv venv

# Activate virtual environment
# On Linux:
source venv/bin/activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

## 📊 Model Comparison

The SVM algorithm performed best with 98.33% cross-validation accuracy. The analysis shows that:

- **SVM** and **LDA** achieved the highest accuracy scores
- All algorithms performed well due to the dataset's clear class separability
- Petal measurements proved to be more discriminative than sepal measurements

## 🎓 Key Insights

1. **Feature Importance**: Petal length and width are the most discriminative features for classification
2. **Class Separability**: Iris-setosa is perfectly separable from the other two species
3. **Model Selection**: SVM is recommended for this problem due to its superior performance

## 📝 Future Improvements

- Implement deep learning approaches
- Add feature engineering techniques
- Include more evaluation metrics
- Cross-validate with different test sizes
- Implement ensemble methods

## 📚 References

- [UCI Machine Learning Repository - Iris Dataset](https://archive.ics.uci.edu/ml/datasets/iris)
- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  
