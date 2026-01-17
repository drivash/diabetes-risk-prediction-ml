# Diabetes Risk Prediction: Optimizing Recall for Medical Screening

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 🏥 About The Project

This project implements a Machine Learning pipeline to predict diabetes risk using the **CDC Health Indicators dataset**. 

In a medical screening context, the cost of missing a positive case (False Negative) is significantly higher than a False Alarm. Therefore, this project prioritizes **Recall (Sensitivity)** over Precision to ensure that the majority of at-risk patients are identified for further testing.

**Key Objective:** Maximize the detection of diabetic patients in a highly imbalanced dataset.

### 🔍 Key Features
* **Imbalanced Data Handling:** extensive use of **SMOTE** and **Undersampling** techniques to balance classes.
* **Metric Optimization:** Model tuning focused on the Precision-Recall trade-off rather than simple Accuracy.
* **Interpretability:** Analysis of key risk factors (BMI, Age, Blood Pressure) to validate medical relevance.

---

## 📊 Methodology & Results

The pipeline includes Exploratory Data Analysis (EDA), feature engineering, and a comparison of multiple models (Logistic Regression, Random Forest, etc.).

### Performance
The final model achieved a **Recall of ~79%** on the test set.

| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **Recall** | **79%** | We successfully identify ~8 out of 10 potential diabetic patients. |
| **Precision** | ~30% | Necessary trade-off to ensure high sensitivity in a screening tool. |

> **Note:** See the full analysis in `docs/project_report.pdf` or in the notebook `notebooks/diabetes_prediction_modeling.ipynb`.

---

## 🛠️ Tech Stack

* **Core:** Python, Pandas, NumPy
* **ML & Stats:** Scikit-Learn, Imbalanced-learn
* **Visualization:** Matplotlib, Seaborn

---

## 📂 Project Structure

```bash
diabetes-risk-prediction-ml/
├── data/                   # Dataset sample or link to source
├── docs/                   # Project documentation (PDF report)
├── images/                 # Plots and confusion matrices
├── notebooks/              # Jupyter Notebooks with the analysis
│   └── diabetes_prediction_modeling.ipynb
├── README.md
└── requirements.txt
