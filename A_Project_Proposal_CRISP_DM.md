# Project Proposal (CRISP-DM Aligned)

## Letter of Transmittal

This proposal presents a data science project designed to support decision-making in coffee quality evaluation. The project follows the CRISP-DM (Cross-Industry Standard Process for Data Mining) framework to ensure a structured and repeatable approach to developing a predictive data product.

The proposed solution uses publicly available Coffee Quality Institute (CQI) data to build a regression-based model that estimates Total Cup Score from measurable coffee attributes. This model is intended to function as a decision-support tool that assists in prioritizing coffee samples for expert evaluation.

The objective is not to replace professional cupping processes, but to improve efficiency in early-stage screening through data-driven estimation.

---

## Business Problem (CRISP-DM: Business Understanding)

Coffee quality evaluation is traditionally performed through manual cupping by trained professionals. While this method is highly accurate, it is also time-intensive and does not scale efficiently when evaluating large volumes of coffee samples.

Organizations involved in coffee sourcing and quality assurance require a faster method to prioritize coffee lots before committing to full sensory evaluation. This project addresses that need by applying predictive modeling techniques to estimate coffee quality using structured data.

---

## Data Product Overview (CRISP-DM: Data + Modeling Understanding)

The data product consists of a regression model developed in Python using the CQI dataset. The dataset includes sensory attributes (such as aroma, flavor, acidity, and balance), physical measurements (such as moisture and altitude), and geographic information.

The target variable is Total Cup Score, which represents overall coffee quality as determined through professional cupping evaluations.

Two feature approaches are used:

- A full feature set including all available attributes
- A reduced feature set excluding sensory scoring variables to evaluate the impact of target leakage

---

## Objectives and Hypothesis

The primary objective of this project is to determine whether coffee attributes can be used to estimate Total Cup Score with reasonable accuracy.

The hypothesis is defined as:

- **Null Hypothesis (H0):** Coffee attributes do not significantly predict Total Cup Score.
- **Alternative Hypothesis (H1):** Coffee attributes can significantly predict Total Cup Score.

---

## Methodology (CRISP-DM: Data Preparation + Modeling + Evaluation)

This project follows the CRISP-DM framework:

1. **Business Understanding:** Define the need for faster coffee quality screening
2. **Data Understanding:** Explore CQI dataset structure and relationships
3. **Data Preparation:** Clean missing values, encode variables, and construct feature sets
4. **Modeling:** Apply Linear Regression and Random Forest models
5. **Evaluation:** Use MAE, RMSE, and R² to assess predictive performance

Train/test splitting is used to evaluate model performance on unseen data.

---

## Funding and Resources

This project requires no external funding. It uses open-source tools including Python, Pandas, NumPy, Matplotlib, and Scikit-learn. The dataset is publicly available and does not require licensing fees or infrastructure costs.

---

## Stakeholders

Primary stakeholders include coffee importers, roasters, and quality assurance teams. These groups benefit from improved efficiency in identifying high-quality coffee samples and prioritizing evaluation resources.

---

## Ethical and Legal Considerations

This system is intended solely as a decision-support tool. It does not replace professional cupping evaluations. A key limitation is partial target leakage, where certain input variables contribute directly to the Total Cup Score. This limitation is acknowledged and does not invalidate the model's usefulness for prioritization purposes.

---

## Expertise

This project is developed using experience in Python programming, data analysis, and machine learning techniques. The implementation demonstrates knowledge of supervised learning workflows, model evaluation, and data visualization.
