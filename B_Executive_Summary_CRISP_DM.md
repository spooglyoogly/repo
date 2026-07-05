# Executive Summary (CRISP-DM Aligned)

## Business Understanding

This project addresses inefficiencies in coffee quality evaluation by introducing a predictive analytics solution. The current manual cupping process is accurate but does not scale efficiently when large volumes of coffee samples must be assessed.

The opportunity exists to improve early-stage decision-making by estimating coffee quality using historical data.

---

## Customers

Primary users include coffee importers, roasters, and quality assurance professionals. These stakeholders require faster methods to prioritize coffee samples before full sensory evaluation is conducted.

---

## Data Understanding

The project uses the Coffee Quality Institute (CQI) dataset, which contains sensory, physical, and geographic attributes of coffee samples. The target variable is Total Cup Score, representing overall quality determined through cupping evaluations.

Initial exploration includes summary statistics and visualization of score distributions to understand dataset structure.

---

## Data Preparation

Data preparation involves cleaning missing values, encoding categorical variables, and constructing feature sets for modeling. Two feature sets are created to evaluate the impact of sensory attributes on predictive performance.

The dataset is split into training and testing subsets to support model evaluation.

---

## Modeling

The modeling phase applies supervised learning techniques, specifically Linear Regression and Random Forest Regressor. These models are trained to estimate Total Cup Score based on input features.

A comparative approach is used to evaluate the impact of feature selection and model complexity.

---

## Evaluation

Model performance is assessed using MAE, RMSE, and R². A train/test split ensures evaluation is performed on unseen data.

Results indicate that models including sensory attributes achieve higher predictive accuracy, which is consistent with the structure of the dataset and the presence of partial target leakage.

---

## Deployment (Decision Support System)

The final data product is implemented within a Jupyter Notebook environment. A prediction function allows users to estimate coffee quality scores based on input attributes.

The system is intended for exploratory decision support and prioritization of coffee samples rather than automated decision-making.

---

## Tools and Costs

The solution uses Python and standard data science libraries, including Pandas, NumPy, Matplotlib, and Scikit-learn. All tools are open-source, and no additional infrastructure or licensing costs are required.

---

## Timeline (CRISP-DM Aligned)

| Phase | Duration |
|---|---|
| Business Understanding | 1 day |
| Data Understanding | 1 day |
| Data Preparation | 1 day |
| Modeling | 1 day |
| Evaluation and Documentation | 1-2 days |
