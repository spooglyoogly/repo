# CQI Coffee Quality Prediction Project

## CRISP-DM Data Science Capstone Submission

---

## Letter of Transmittal

This document presents a data science project designed to support decision-making in coffee quality evaluation. The project follows the CRISP-DM (Cross-Industry Standard Process for Data Mining) framework to ensure a structured approach to developing a predictive data product.

The solution uses Coffee Quality Institute (CQI) data to build machine learning models that estimate Total Cup Score based on measurable coffee attributes. The purpose of this system is to support early-stage prioritization of coffee samples for expert evaluation.

This tool is intended strictly for decision support and does not replace professional cupping processes.

---

## 1. Business Understanding

Coffee quality evaluation is traditionally performed through manual cupping by trained professionals. While accurate, this process is time-consuming and limits scalability when evaluating large volumes of coffee samples.

Organizations involved in coffee sourcing and quality assurance require faster methods to prioritize coffee samples before full sensory evaluation. This project addresses that need using predictive analytics.

---

## 2. Data Understanding

The dataset used in this project is sourced from the Coffee Quality Institute (CQI). It includes sensory, physical, and geographic attributes of coffee samples.

Key variables include:

- Aroma, flavor, acidity, aftertaste, balance, body
- Moisture content and altitude
- Processing method and origin
- Total Cup Score (target variable)

Initial exploration includes summary statistics and visualization of score distributions to understand dataset structure.

---

[INSERT SCREENSHOT: df.head()]

[INSERT SCREENSHOT: df.describe() or df.info()]

---

## 3. Data Preparation

Data preparation includes cleaning missing values, encoding categorical variables, and selecting relevant features for modeling.

Two feature sets are constructed:

- Full feature set (including sensory attributes)
- Reduced feature set (excluding sensory scoring variables to evaluate leakage impact)

The dataset is split into training and testing sets to ensure proper evaluation on unseen data.

---

[INSERT SCREENSHOT: cleaned dataset creation OR dropna step]

---

## 4. Modeling

Two supervised learning models are applied:

- Linear Regression (baseline model)
- Random Forest Regressor (non-linear model)

These models are trained on both feature sets to predict Total Cup Score based on input attributes.

---

## 5. Evaluation

Model performance is evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

A train/test split approach is used to evaluate performance on unseen data.

Results indicate that models including sensory attributes perform better due to their direct relationship with the target variable.

---

[INSERT SCREENSHOT: model evaluation metrics output]

---

## 6. Interpretability and Findings

Feature importance analysis indicates that sensory attributes such as aroma, flavor, and acidity are the strongest predictors of Total Cup Score.

However, several of these attributes are directly involved in the construction of the target variable, introducing partial target leakage. This means the model partially learns the scoring structure rather than fully independent predictive relationships.

Despite this limitation, the model remains useful as a decision-support tool for prioritizing coffee samples.

---

[INSERT SCREENSHOT: feature importance chart]

---

## 7. Decision Support Function

A prediction function is implemented to estimate coffee quality based on input attributes. This allows the model to be used interactively for scenario-based evaluation.

[INSERT SCREENSHOT: prediction function code]

[INSERT SCREENSHOT: sample prediction output]

---

## 8. Hypothesis Testing

- **Null Hypothesis (H0):** Coffee attributes do not significantly predict Total Cup Score.
- **Alternative Hypothesis (H1):** Coffee attributes can significantly predict Total Cup Score.

Model evaluation metrics (MAE, RMSE, R²) and the F-test indicate predictive relationships exist between input features and target score. The results support rejecting the null hypothesis in favor of the alternative hypothesis.

---

## 9. Ethical and Legal Considerations

This model is intended strictly as a decision-support tool and does not replace professional cupping evaluations.

A key limitation is partial target leakage, where certain input features are directly related to the target variable. This inflates predictive performance but does not reduce the model's usefulness for prioritization.

All data used is publicly available and does not contain sensitive personal information.

---

## 10. Deployment (CRISP-DM Final Phase)

The final model is implemented within a Jupyter Notebook environment. It supports interactive prediction through a function that estimates Total Cup Score from input features.

This system is intended for exploratory decision support and prioritization of coffee samples.

---

## 11. Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

All tools used are open-source and require no licensing costs.

---

## 12. Timeline (CRISP-DM Process)

| Phase | Duration |
|---|---|
| Business Understanding | 1 day |
| Data Understanding | 1 day |
| Data Preparation | 1 day |
| Modeling | 1 day |
| Evaluation & Documentation | 1-2 days |

---

## 13. Conclusion

This project demonstrates how machine learning can be applied to structured agricultural quality data to support decision-making processes. While predictive performance is strong, results are influenced by dataset structure and partial target leakage.

The system is best interpreted as a decision-support tool that improves early-stage prioritization rather than replacing expert evaluation.

---

## Appendix A: Dataset Files

- Raw CQI dataset
- Cleaned dataset

## Appendix B: Code (Notebook)

- Full Jupyter Notebook (.ipynb)

## Appendix C: Screenshots

- df.head()
- Dataset summary
- Model metrics
- Feature importance
- Prediction example

## Appendix D: Quick Start Guide

1. Open Jupyter Notebook
2. Run all cells from top to bottom
3. Load dataset (CSV)
4. View EDA outputs
5. Train models
6. Review evaluation metrics
7. Run prediction function with sample input
