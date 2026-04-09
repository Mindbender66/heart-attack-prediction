# ❤️ Heart Attack Prediction — ML Classification Project

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Dataset](https://img.shields.io/badge/Dataset-303%20Records-red)

A Machine Learning classification project that predicts the **risk of a heart attack** based on patient medical data. Four ML algorithms are trained, evaluated, and compared — Decision Tree, SVM, Logistic Regression, and KNN.

---

## 📌 Project Overview

Using the classic **Heart Disease dataset** (303 patients, 14 features), this project:

1. Loads and explores the data with EDA
2. Checks and handles null/zero values
3. Trains **4 ML classifiers** on an 80/20 train-test split
4. Evaluates each model using Classification Reports, Confusion Matrices, and ROC Curves
5. Compares models to find the best performer

---

## 📁 Project Structure

```
heart-attack-prediction/
│
├── heart_attack_prediction.ipynb     # Main Jupyter / Colab Notebook
├── heart.csv                         # Dataset (303 rows × 14 columns)
├── Explanation.docx                  # Detailed code explanation document
└── README.md
```

---

## 📊 Dataset Features

| Column | Description |
|---|---|
| `age` | Patient age |
| `sex` | Gender (1 = Male, 0 = Female) |
| `cp` | Chest pain type (0–3) |
| `trtbps` | Resting blood pressure (mm Hg) |
| `chol` | Serum cholesterol (mg/dl) |
| `fbs` | Fasting blood sugar > 120 mg/dl |
| `restecg` | Resting ECG results |
| `thalachh` | Maximum heart rate achieved |
| `exng` | Exercise-induced angina |
| `oldpeak` | ST depression from exercise |
| `slp` | Slope of peak exercise ST segment |
| `caa` | Number of major vessels |
| `thall` | Thalassemia type |
| `output` | **Target** — 1 = Heart Attack Risk, 0 = No Risk |

**Target Distribution:** 165 positive (54.5%) vs 138 negative (45.5%) — balanced dataset ✅

---

## 🤖 Models & Results

| Model | Accuracy | Precision (Avg) | Recall (Avg) |
|---|---|---|---|
| Decision Tree | 72.13% | 0.75 | 0.72 |
| **SVM (Linear)** | **75.41%** | **0.78** | **0.75** |
| Logistic Regression | 73.77% | 0.75 | 0.74 |
| KNN | 55.74% | 0.57 | 0.56 |

🏆 **Best Model: SVM with Linear Kernel — 75.41% accuracy**

---

## 📈 Evaluation Methods

- ✅ Classification Report (Precision, Recall, F1-Score)
- ✅ Confusion Matrix (visualized with Seaborn heatmap)
- ✅ ROC Curve + AUC Score for all 4 models

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/Mindbender66/heart-attack-prediction.git
cd heart-attack-prediction
```

### 2. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 3. Run the Notebook
Open `heart_attack_prediction.ipynb` in Jupyter or upload to Google Colab.

> Make sure `heart.csv` is in the same directory (or upload to Colab session).

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| `Pandas` | Data loading & manipulation |
| `NumPy` | Numerical operations |
| `Seaborn / Matplotlib` | EDA plots, heatmaps, ROC curves |
| `Scikit-Learn` | ML models, metrics, train-test split |

---

## 🔍 Key Findings

- **SVM** outperforms other models with 75.41% accuracy on this dataset
- **KNN** performs poorly without feature scaling — applying `StandardScaler` would improve it
- **Logistic Regression** hits a convergence warning — increasing `max_iter=1000` fixes it
- The dataset is well-balanced, so no resampling (SMOTE etc.) was needed

---

## 🚀 Future Improvements

- [ ] Apply `StandardScaler` before KNN and Logistic Regression
- [ ] Tune hyperparameters with `GridSearchCV`
- [ ] Try `RandomForestClassifier` or `XGBoostClassifier`
- [ ] Use k-fold cross-validation for more reliable evaluation
- [ ] Build a simple prediction UI with Streamlit or Gradio

---

## 👤 Author

**Valmiki Sarath**
- GitHub: [@Mindbender66](https://github.com/Mindbender66)
- Email: valmikisarath6666@gmail.com

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
