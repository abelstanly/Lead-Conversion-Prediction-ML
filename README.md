# Lead Conversion Prediction using Machine Learning

## 📊 Machine Learning Project | Knovista Technologies Pvt Ltd

A machine learning classification project developed during my **Data Analytics and ML Internship at Knovista Technologies Pvt Ltd** to predict whether a sales lead is likely to be **Converted** or **Lost**.

The project analyzes CRM lead data, performs exploratory data analysis, applies preprocessing and feature engineering, compares multiple machine learning algorithms, and selects a tuned **Random Forest Classifier** as the final model.

---

## 🎯 Project Objective

The primary objective of this project is to build a machine learning model that can predict lead conversion outcomes and identify the factors associated with successful conversions.

The project focuses on:

- Understanding lead conversion patterns
- Analyzing lead sources, campaigns, and assigned agents
- Identifying important factors influencing conversion
- Comparing multiple classification algorithms
- Applying cross-validation for reliable model evaluation
- Hyperparameter tuning using GridSearchCV
- Evaluating the final model using multiple performance metrics

---

## 🗂️ Dataset

The project uses a CRM lead dataset containing **27,375 records and 15 columns**.

### Target Variable

| Target | Meaning |
|---|---|
| `CONVERTED` | Lead successfully converted |
| `LOST` | Lead was not converted |

For machine learning:

```text
CONVERTED → 1
LOST      → 0
