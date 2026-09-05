# Lead Conversion Prediction using Machine Learning

## 📌 Project Overview

This project uses machine learning to predict whether a sales lead will convert into a paying customer or be lost.

The project was developed using a real-world CRM dataset containing 27,375 lead records.

## 🎯 Objective

The objective is to help sales teams identify high-potential leads and prioritize follow-ups based on predicted conversion probability.

## 📊 Dataset

- Original records: 27,375
- Records used for modeling: 12,543
- Target: Lead Conversion
- CONVERTED = 1
- LOST = 0

The dataset was highly imbalanced, with significantly more lost leads than converted leads.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## 🔧 Machine Learning Workflow

1. Data loading and exploration
2. Missing value analysis
3. Exploratory Data Analysis
4. Data preprocessing
5. Feature engineering
6. Label Encoding
7. Train/Test Split
8. Feature Scaling
9. Model Training
10. Cross Validation
11. Hyperparameter Tuning using GridSearchCV
12. ROC-AUC Evaluation
13. Model Comparison
14. Feature Importance Analysis
15. Lead Conversion Prediction

## 🤖 Models Compared

- K-Nearest Neighbors
- Naive Bayes
- Support Vector Machine
- Decision Tree
- Random Forest

## 🏆 Final Model

Random Forest was selected as the final model.

Although SVM, Decision Tree, and Random Forest achieved the same test accuracy, Random Forest was selected because it provides feature importance, does not rely on distance calculations over encoded categorical variables, and was optimized using GridSearchCV.

### Final Performance

| Metric | Result |
|---|---:|
| Test Accuracy | 95.93% |
| Cross-Validation Accuracy | 95.42% |
| Precision | 0.94 |
| Recall | 0.43 |
| F1 Score | 0.59 |

## 🔍 Key Features

The most important features identified by the Random Forest model were:

1. assigned_to
2. campaign_name
3. had_call_attempt
4. source_type

## 💼 Business Insights

The analysis identified differences in conversion rates across lead sources, campaigns, and salespeople.

The model can also generate conversion probabilities, allowing sales teams to prioritize leads with higher predicted conversion potential.

## ⚠️ Limitations

- The dataset has significant class imbalance.
- Recall for converted leads is relatively low.
- Only four features were used for the final model.
- Label Encoding has limitations for nominal categorical variables.

## 🚀 Future Improvements

Potential improvements include:

- One-Hot Encoding
- SMOTE or class weighting
- Additional time-based feature engineering
- Threshold optimization
- Testing additional ensemble and boosting algorithms

## 📁 Project Files

- `Lead_Conversion_Prediction_RandomForest.ipynb` — Complete machine learning notebook
- `requirements.txt` — Python dependencies

## 👤 Author

Abel Dani Stanly

Data Analytics & Machine Learning
