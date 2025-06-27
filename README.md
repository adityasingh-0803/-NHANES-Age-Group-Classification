# 🧠 NHANES Age Group Classification

This project is a binary classification task built on a subset of the NHANES dataset provided during the **Summer Analytics 2025 Hackathon**, organized by the **Consulting & Analytics Club, IIT Guwahati**. The goal is to predict whether a respondent is a **Senior (65+)** or an **Adult (<65)** using health and lifestyle data.

---

## 🗂️ Dataset Overview

- **Train Data:** `2016` rows with target labels (`age_group`)
- **Test Data:** `312` rows without labels
- **Target Variable:**  
  - `Adult` → `0`  
  - `Senior` → `1`

### 📊 Features Used
| Column       | Description |
|--------------|-------------|
| `SEQN`       | Sequence ID |
| `RIAGENDR`   | Gender (1 = Male, 2 = Female) |
| `PAQ605`     | Weekly physical activity response |
| `BMXBMI`     | Body Mass Index |
| `LBXGLU`     | Glucose level |
| `DIQ010`     | Diabetes diagnosis indicator |
| `LBXGLT`     | Oral glucose tolerance |
| `LBXIN`      | Insulin level |

---

## ✅ Problem Statement

> **Objective:** Predict the `age_group` (0 or 1) using lifestyle and medical lab features.

---

## 🧪 Approach

1. **Exploratory Data Analysis (EDA)**
   - Distribution plots for BMI, glucose, insulin
   - Correlation heatmap to analyze feature-target relationships

2. **Preprocessing**
   - Handling missing values using median imputation
   - Label encoding for categorical fields (`RIAGENDR`, `PAQ605`, `DIQ010`)

3. **Model Building**
   - Logistic Regression (baseline)
   - Random Forest Classifier
   - XGBoost Classifier (final model used)
   - Ensemble Voting Classifier (experimental)

4. **Evaluation**
   - Accuracy and cross-validation on train set
   - Final test set predictions saved to `submission.xlsx`

---

## 📈 Final Model Performance

- ✅ Format: `submission.csv` (1 column: `age_group`, values: 0 or 1)
- ✅ Validation Score: **65.584% accuracy** (Leaderboard Score: **34.416**)
- ✅ File: [submission.xlsx](./submission.xlsx)

---

## 📁 Files in This Repository

| File | Description |
|------|-------------|
| `Train_Data.csv` | Training dataset |
| `Test_Data.csv` | Test dataset (without target) |
| `submission.csv` | Final model predictions |
| `NHANES_Age_Classification.ipynb` | Full Jupyter notebook |
| `README.md` | Project overview and documentation |

---

## 🛠️ Tools & Libraries

- Python (Pandas, NumPy)
- Scikit-learn (Logistic Regression, Random Forest)
- XGBoost
- Matplotlib, Seaborn (EDA & plotting)

---

## 📌 How to Run

```bash
# Install dependencies
pip install -r requirements.txt

# Open notebook
jupyter notebook NHANES_Age_Classification.ipynb
```
## 📌 Submission Format
```bash
age_group
0
1
0
...
```
Must contain 312 rows

Only 0 and 1 values

## 📚 Learnings
Hands-on with real-world health data

Applied classification algorithms and ensemble learning

Feature engineering and EDA for insight-driven modeling

Submission preparation and validation for ML competitions

## 📍 Future Improvements
Hyperparameter tuning using GridSearchCV or Optuna

Feature interaction terms (e.g., BMI * Glucose)

Deep Learning models (if dataset is expanded)

SHAP/LIME-based interpretability
