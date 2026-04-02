# 🖥️ Laptop Price Prediction Project

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3.0-orange.svg)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-1.7.0-green.svg)](https://xgboost.readthedocs.io/)

> 📊 **Predict laptop prices with machine learning** - A comprehensive end-to-end project for laptop price prediction using various regression algorithms.


## 🎯 Project Overview
This project aims to predict laptop prices based on various technical specifications. Using machine learning algorithms, we analyze features like processor type, RAM, storage, screen resolution, and more to estimate laptop prices accurately.

### Key Highlights ✨
- 📈 Achieved **88.5% R² Score** with Random Forest Regressor
- 🔍 Extensive Exploratory Data Analysis (EDA)
- 🧹 Comprehensive data preprocessing and feature engineering
- 📊 Interactive visualizations for insights

## 📁 Dataset
The dataset contains information about various laptop models including:

| Feature | Description |
|---------|-------------|
| **Company** | Laptop manufacturer |
| **TypeName** | Laptop category (Ultrabook, Notebook, etc.) |
| **Ram** | RAM size in GB |
| **Weight** | Laptop weight in kg |
| **ScreenResolution** | Display resolution |
| **Cpu** | Processor details |
| **Gpu** | Graphics card |
| **Memory** | Storage configuration (HDD/SSD) |
| **OpSys** | Operating System |
| **Price** | Target variable (in USD) |

## 🛠️ Technologies Used
```python
# Core Libraries
- Python 3.8+
- NumPy
- Pandas
- Matplotlib
- Seaborn

# Machine Learning
- Scikit-learn

# Model Evaluation
- R² Score
- Mean Absolute Error (MAE)
```

## 📊 Features
### Original Features
- **Categorical**: Company, TypeName, Cpu_brand, Gpu_brand, OS
- **Numerical**: Ram, Weight, Inches, Price

### Engineered Features
- **Screen Resolution**: Extracted X_res, Y_res, calculated PPI (Pixels Per Inch)
- **Touchscreen & IPS**: Binary features from screen resolution
- **Storage**: Separated HDD and SSD capacities
- **Processor Brand**: Categorized Intel Core i3/i5/i7, Other Intel, AMD
- **Operating System**: Grouped into Windows, Mac, and Others

## ⚙️ Installation & Setup

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Step-by-Step Setup

1️⃣ **Clone the Repository**
```bash
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git
cd MachineLearningProjects/2-Laptop-Price-Prediction-Project
```

2️⃣ **Create Virtual Environment**
```bash
# On Linux
python3 -m venv venv
source venv/bin/activate
```

3️⃣ **Install Dependencies**
```bash
pip install -r requirements.txt
```


## 🚀 Usage

### Quick Start
The notebook is structured to be run sequentially:
1. **Data Loading**: Import and load the dataset
2. **EDA**: Explore data distributions and relationships
3. **Feature Engineering**: Create new meaningful features
4. **Preprocessing**: Handle categorical variables and scaling
5. **Model Training**: Train multiple regression models
6. **Evaluation**: Compare model performance

### Example Code Snippet
```python
# Load and preprocess data
data = pd.read_csv('./laptop_data.csv')
data['Ram'] = data['Ram'].str.replace("GB", "").astype('int32')
data['Weight'] = data['Weight'].str.replace("kg", "").astype('float32')

# Train Random Forest model
rf = RandomForestRegressor(n_estimators=100, random_state=3)
rf.fit(X_train, y_train)

# Predict
predictions = rf.predict(X_test)
```

## 📈 Model Performance

### Best Model: Random Forest Regressor
| Metric | Score |
|--------|-------|
| **R² Score** | **0.885** (88.5%) |
| **MAE** | 0.158 |



## 📝 Project Structure
```
2-Laptop-Price-Prediction-Project/
│
├── project.ipynb          # Main Jupyter notebook
├── laptop_data.csv        # Dataset
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation

```



## 📚 References

- [Laptop_Price_Prediction Repository - Laptop Dataset](https://github.com/Raghavagr/Laptop_Price_Prediction/blob/main/laptop_data.csv)
- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  

---
