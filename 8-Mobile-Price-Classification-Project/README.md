## 📱 Mobile Price Classification Project

[![Python Version](https://img.shields.io/badge/python-3.12-blue.svg)](https://www.python.org/downloads/)


A machine learning project to classify mobile phones into **4 price ranges** (0-3) based on their specifications. The model achieves **95.5% accuracy** using Logistic Regression.

---

## 📊 Project Overview

This project uses a dataset of mobile phone specifications to predict the price range of a device. The goal is to help manufacturers and consumers understand how hardware features influence pricing tiers.

### Key Features
- **4 Price Ranges:**
  - `0` → Low cost
  - `1` → Medium cost
  - `2` → High cost
  - `3` → Very high cost
- **20+ Features:** battery power, RAM, internal memory, screen size, camera resolution, and more.
- **High Accuracy:** 95.5% using Logistic Regression.

---

## 📂 Repository Structure

```
8-Mobile-Price-Classification-Project/
│
├── project.ipynb                # Jupyter notebook with full EDA & modeling
├── requirements.txt             # Python dependencies
├── README.md                    # Project documentation
```

---

## 🛠️ Installation & Setup

Follow these steps to run the project locally:

```bash
# 1. Clone the repository
git clone https://github.com/MohamedAliZouariEng/MachineLearningProjects.git

# 2. Navigate to the project folder
cd MachineLearningProjects/8-Mobile-Price-Classification-Project

# 3. Create a virtual environment
python3 -m venv venv

# 4. Activate the virtual environment
# On Linux:
source venv/bin/activate

# 5. Install dependencies
pip install -r requirements.txt


---
```
## 🧠 Model & Performance

- **Algorithm:** Logistic Regression
- **Train/Test Split:** 80/20
- **Data Standardization:** StandardScaler
- **Accuracy:** **95.5%**

### Confusion Matrix Summary
| Price Range | Predicted Count |
|-------------|----------------|
| 0           | 95              |
| 1           | 90              |
| 2           | 97              |
| 3           | 118             |

---

## 📈 Dataset Features

| Feature        | Description |
|----------------|-------------|
| battery_power  | Total battery energy (mAh) |
| blue           | Has Bluetooth or not |
| clock_speed    | Processor speed (GHz) |
| dual_sim       | Supports dual SIM |
| fc             | Front camera megapixels |
| four_g         | Has 4G or not |
| int_memory     | Internal memory (GB) |
| m_dep          | Mobile depth (cm) |
| mobile_wt      | Weight (g) |
| n_cores        | Number of processor cores |
| pc             | Primary camera megapixels |
| px_height      | Pixel resolution height |
| px_width       | Pixel resolution width |
| ram            | RAM (MB) |
| sc_h           | Screen height (cm) |
| sc_w           | Screen width (cm) |
| talk_time      | Talk time (hours) |
| three_g        | Has 3G or not |
| touch_screen   | Has touch screen or not |
| wifi           | Has wifi or not |
| **price_range**| Target: 0, 1, 2, 3 |

---

---

## 📚 References

- Dataset: [Mobile Price Classification](https://raw.githubusercontent.com/amankharwal/Website-data/master/mobile_prices.csv)

- [موقع التعلم العميق بالعربي || الدكتور علاء طعيمة](https://dlarabic.com/)
  
