# Lead Conversion Prediction using Machine Learning

## 📌 Project Overview

This project uses machine learning to predict whether a sales lead will convert into a paying customer or be lost.

The project was developed using a real-world CRM dataset containing 27,375 lead records.

The project compares multiple classification algorithms and uses cross-validation, hyperparameter tuning, ROC-AUC evaluation, and feature importance analysis to identify a suitable final model.

---

## 🎯 Objective

The objective is to help sales teams identify high-potential leads and prioritize follow-ups based on predicted conversion probability.

The model can provide a probability of conversion for a new lead, which can support data-driven lead prioritization.

---

## 📊 Dataset

- Original records: 27,375
- Records used for modeling: 12,543
- Target: Lead Conversion
- CONVERTED = 1
- LOST = 0

The dataset was highly imbalanced, with significantly more lost leads than converted leads.

For privacy and confidentiality reasons, the original CRM dataset is not included in this repository.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

---

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

---

## 🤖 Models Compared

The following classification algorithms were evaluated:

- K-Nearest Neighbors
- Naive Bayes
- Support Vector Machine
- Decision Tree
- Random Forest

---

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

The final Random Forest model achieved strong overall accuracy, while the relatively lower recall for converted leads highlights the impact of the dataset's class imbalance.

---

## 📈 Exploratory Data Analysis

### Conversion Analysis by Source

The analysis identified differences in lead conversion rates across different lead sources.

![Conversion Analysis by Source](Screenshots/eda_by_source.png)

---

### Conversion Analysis by Campaign

Conversion performance was also analyzed across campaigns to identify campaigns associated with higher conversion rates.

![Conversion Analysis by Campaign](Screenshots/eda_by_campaign.png)

---

### Conversion Analysis by Agent

The analysis examined conversion rates across sales agents to identify differences in lead conversion performance.

![Conversion Analysis by Agent](Screenshots/eda_by_agent.png)

---

## 📊 Model Comparison

The five machine learning models were evaluated using test accuracy and 5-fold cross-validation.

![Model Comparison](Screenshots/model_comparison.png)

The top-performing models achieved very similar test accuracy, with Random Forest, Decision Tree, and SVM achieving 95.93% test accuracy.

---

## 📈 ROC-AUC Comparison

ROC-AUC was used as an additional evaluation metric to assess the models' ability to distinguish between converted and lost leads.

![ROC-AUC Comparison](Screenshots/roc_auc_comparison.png)

The tuned Random Forest achieved a ROC-AUC score of approximately 0.845.

---

## 🔍 Feature Importance

The Random Forest model was used to identify the relative importance of the features used for prediction.

![Feature Importance](Screenshots/feature_importance.png)

### Key Features

The most important features identified by the Random Forest model were:

1. `assigned_to`
2. `campaign_name`
3. `had_call_attempt`
4. `source_type`

These results indicate that sales-agent assignment, campaign, and call-attempt information were important predictors within the available modeling data.

---

## 💼 Business Insights

The analysis identified differences in conversion rates across lead sources, campaigns, and salespeople.

The model can also generate conversion probabilities, allowing sales teams to prioritize leads with higher predicted conversion potential.

The analysis also showed differences in conversion rates based on whether a call attempt had been made. This should be interpreted as an observed relationship in the dataset rather than proof of causation.

---

## ⚠️ Limitations

- The dataset has significant class imbalance.
- Recall for converted leads is relatively low.
- Only four features were used for the final model.
- Label Encoding has limitations for nominal categorical variables.
- The dataset is not included in the repository due to privacy and confidentiality considerations.
- Accuracy alone may not fully represent model performance because of the class imbalance.

---

## 🚀 Future Improvements

Potential improvements include:

- One-Hot Encoding
- SMOTE or class weighting
- Additional time-based feature engineering
- Threshold optimization
- Testing additional ensemble and boosting algorithms
- Further tuning of precision and recall based on business requirements
- Evaluation using additional classification metrics

---

## 📁 Project Structure

```text
Lead-Conversion-Prediction-ML/
│
├── ML Notebook/
│   └── Lead_Conversion_Prediction_using_ML_(RF).ipynb
│
├── Screenshots/
│   ├── eda_by_agent.png
│   ├── eda_by_campaign.png
│   ├── eda_by_source.png
│   ├── feature_importance.png
│   ├── model_comparison.png
│   └── roc_auc_comparison.png
│
├── README.md
└── Requirements.txt
