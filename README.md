# Stroke Prediction Project

## 🧠 Overview

This repository provides a complete data analysis and predictive modeling pipeline for **Stroke Prediction**, based on the public dataset from Kaggle. The goal of this project is to identify the most influential factors contributing to stroke risk and build a machine learning model capable of predicting potential stroke cases.

## 📂 Project Structure

```
│
├── analysis.py               # Main Python script: data preprocessing, EDA, model training & evaluation
├── REPORT.md                 # Executive summary & analytical findings
├── final_project of stroke prediction.ipynb  # Jupyter notebook version (imported from Colab)
├── Final project.pbix         # Power BI visualization dashboard
└── README.md                 # Project documentation (this file)
```

## 🎯 Objectives

* Perform data cleaning and handle missing values.
* Conduct exploratory data analysis (EDA) to identify correlations and patterns.
* Encode categorical variables and normalize numerical data.
* Build a predictive model using **Random Forest Classifier**.
* Evaluate performance metrics such as accuracy, recall, precision
* Visualize results interactively in Power BI.

## 🧩 Dataset Information

* **Source:** [Kaggle - Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
* **Rows:** 5110
* **Target Variable:** `stroke` (0 = No Stroke, 1 = Stroke)
* **Features:**

  * Demographics: `gender`, `age`, `ever_married`, `Residence_type`
  * Health conditions: `hypertension`, `heart_disease`, `bmi`, `avg_glucose_level`
  * Lifestyle: `work_type`, `smoking_status`

## ⚙️ Setup Instructions

### 1. Environment Setup

```bash
python -m venv venv
source venv/bin/activate   # For macOS/Linux
venv\Scripts\activate      # For Windows
```

### 2. Install Dependencies

Create and install from `requirements.txt`:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib jupyter
```

### 3. Run the Analysis

Run the analysis pipeline directly:

```bash
python analysis.py --data data/stroke_data.csv --output models/rf_model.joblib
```

Or open the Colab/Jupyter notebook:

```bash
jupyter notebook "final_project of stroke prediction.ipynb"
```

### 4. Power BI Dashboard

* Open `Final project.pbix` in Power BI Desktop.
* Refresh data sources if necessary.
* Explore stroke risk patterns visually.

## 📊 Model Summary

| Metric    | Description                         | Example Value |
| --------- | ----------------------------------- | ------------- |
| Accuracy  | Overall correct predictions         | 0.95          |
| Precision | True positives / predicted stroke   | 0.40          |
| Recall    | True positives / actual stroke      | 0.30          |
| F1-score  | Harmonic mean of precision & recall | 0.34          |
| ROC-AUC   | Area under ROC curve                | 0.78          |

> **Note:** Due to class imbalance, recall is prioritized over accuracy.

## 💡 Key Insights

* **Age** and **avg_glucose_level** are the strongest predictors.
* Patients with **hypertension** and **heart disease** show significantly higher risk.
* Lifestyle variables (e.g., smoking) contribute moderately.

## 🚀 Recommendations

1. Apply **SMOTE** or **class-weight balancing** to improve stroke case detection.
2. Use **hyperparameter tuning** for better model optimization.
3. Add **SHAP/LIME** explainability for interpretability.
4. Integrate with Power BI for real-time dashboards.

## 📈 Future Enhancements

* Integrate deep learning models.
* Implement real-time prediction API.
* Automate retraining with new data.
* Add health-based interpretability dashboard.

## 🧾 License

This project is licensed under the **MIT License** — feel free to use and adapt with proper attribution.


👨‍💻 **Authors**

Hà Quang Nam
