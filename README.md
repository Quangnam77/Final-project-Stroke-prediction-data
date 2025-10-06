# 🧠 Stroke Prediction Project

### Swiss Coding Academy — Final Project (October 2025)  
**Author:** Quang Nam 
**Tools used:** Python, Power BI, Jupyter Notebook, Pandas, Scikit-learn  

---

## 📘 Overview
Stroke, or cerebrovascular accident, is one of the leading causes of death and long-term disability worldwide.  
The goal of this project is to analyze stroke-related health data, identify key risk factors, and build a predictive model to help detect patients at high risk of stroke.

This project demonstrates a **complete data analytics workflow** — from data cleaning, exploratory data analysis (EDA), and feature engineering to model building, evaluation, and visualization through Power BI.

---

## 🧩 Project Files
| File | Description |
|------|--------------|
| `final_project of stroke prediction.ipynb` | Jupyter Notebook performing data cleaning, feature grouping, EDA, and predictive modeling. |
| `Final project.pbix` | Power BI dashboard visualizing patterns and correlations among stroke factors. |
| `final_project of stroke prediction.pptx` | Executive presentation summarizing results, insights, and recommendations. |

---

## 🎯 Project Objectives
- Perform data preprocessing and eliminate inconsistencies (null values, outliers, unnecessary columns).
- Group data by health and demographic factors (age, BMI, glucose, hypertension, smoking).
- Develop a regression model to predict stroke likelihood.
- Visualize the results interactively through Power BI.
- Provide actionable insights for healthcare prediction and prevention.

---

## 🧠 Dataset Summary
**Source:** Kaggle — *Stroke Prediction Dataset*  
**Total records:** 5,110  
**Columns:** 11  

| Feature | Description |
|----------|--------------|
| `id` | Unique identifier |
| `gender` | Male / Female / Other |
| `age` | Age of the patient |
| `hypertension` | 1 = has hypertension, 0 = no |
| `heart_disease` | 1 = has heart disease, 0 = no |
| `ever_married` | Yes / No |
| `work_type` | Children / Govt_job / Private / Self-employed / Never_worked |
| `Residence_type` | Urban / Rural |
| `avg_glucose_level` | Average blood glucose level |
| `bmi` | Body Mass Index |
| `smoking_status` | Formerly smoked / Never smoked / Smokes / Unknown |
| `stroke` | 1 = stroke occurred, 0 = no stroke |

---

## 🧹 Data Cleaning and ETL Process
- **Removed unnecessary columns:** `id`, `ever_married`, `work_type`
- **Handled missing BMI values:** Replaced 201 nulls using mean imputation for accuracy preservation.
- **Outlier Detection (IQR method):**  
  - BMI lower bound: 10.3 | upper bound: 46.3  
  - Glucose lower bound: 21.98 | upper bound: 169.36  
  Outliers were retained since they represent meaningful medical extremes.
- **Dropped duplicates:** None detected.
- **Grouped data:**  
  - **Age group:** Young (0–16), Teen (17–24), Adult (25–64), Old (65+)  
  - **BMI group:** Underweight (<18.5), Normal (18.5–21.9), Overweight (21.9–29.9), Obese (>29.9)  
  - **Glucose group:** Underweight (0–70), Normal (70–100), Overweight (100–126), Obese (>126)  
  - **Smoking group:** Smoking, Non-smoking, Unknown  

---

## 📊 Exploratory Data Analysis (EDA)

### 1. **Age**
- Stroke occurs mostly in **adults and elderly**, making up **64.85%** of all stroke cases.
- Most elderly stroke patients are **male** and **live in urban areas**.

### 2. **Hypertension & Heart Disease**
- Hypertension and heart disease are **associated with stroke**, but not all patients with these conditions have strokes.
- Overweight individuals without heart disease/hypertension are still at significant risk.

### 3. **BMI**
- **Overweight BMI (21.9–29.9)** represents **42.57%** of stroke cases.  
- Obesity is most common in **rural areas**, especially among **diabetic and smoking** patients.

### 4. **Glucose Level**
- **Diabetic patients** (avg_glucose_level > 126) represent **41.09%** of stroke cases.  
- Diabetes prevalence aligns strongly with **older**, **obese**, and **smoking** groups.

---

## 📈 Regression Analysis
### Model Formula:
```
Stroke = -0.0529 + 0.0025*Age + 0.0445*Hypertension + 0.0559*HeartDisease 
          + 0.0003*AvgGlucoseLevel - 0.0290*NonSmoke - 0.0239*Smoking 
          - 0.0272*Rural - 0.0255*Urban
```

### Results:
- **R² score:** Weak — model explains a small proportion of the outcome variance.
- **P-value:** `bmi` and `gender (Male)` > 0.05 ⇒ excluded from the model.
- **Accuracy:** ~93% (imbalanced data issue).

> ⚠️ The dataset is **imbalanced** — majority class (non-stroke) dominates, reducing precision for stroke detection.

---

## 📉 Model Evaluation Summary
| Metric | Description | Result |
|---------|--------------|--------|
| Accuracy | Overall model accuracy | 0.93 |
| Precision | Correct stroke predictions among predicted | 0.40 |
| Recall | Correct stroke detections among actual cases | 0.30 |
| F1-score | Balance between precision and recall | 0.34 |
| ROC-AUC | Overall classification quality | 0.78 |

---

## 💡 Key Insights
- **Old age, diabetes, and obesity** are the dominant stroke risk factors.  
- **Higher glucose and BMI** levels consistently correlate with stroke likelihood.  
- **Urban males aged 60+** show a stronger association with stroke in this dataset.  
- **Imbalanced data** reduces model sensitivity — future balancing (e.g., SMOTE) is recommended.

---

## 📊 Power BI Dashboard Highlights
The Power BI dashboard (`Final project.pbix`) visualizes:
- Stroke distribution by **age**, **BMI**, **residence**, and **smoking group**
- Correlation between **heart disease, hypertension, and glucose**
- Overview cards for **key performance metrics**
- Interactive filters for **age group, residence type, and smoking group**

---

## 🧭 Recommendations
1. Apply **data balancing techniques** (SMOTE or cost-sensitive learning).
2. Enhance the model with **ensemble methods** (XGBoost, LightGBM).
3. Add **explainability** (SHAP, LIME) for medical interpretability.
4. Integrate **predictive monitoring dashboard** for hospitals using Power BI.
5. Consider adding **time-series data** (longitudinal health monitoring) for improved accuracy.

---

## 🚀 Technologies Used
| Category | Tools |
|-----------|--------|
| **Data Analysis** | Python (Pandas, NumPy, Scikit-learn) |
| **Visualization** | Power BI, Matplotlib, Seaborn |
| **Modeling** | Random Forest, Linear Regression |
| **Documentation** | Jupyter Notebook, PowerPoint |
| **Version Control** | GitHub |

---

## 🧾 License
This project is released under the **MIT License** — you are free to use, modify, and share with attribution.

---

## 👤 Author
**Hà Quang Nam
---

### ✨ “Data-driven insights save lives — Predicting stroke before it happens.”  
