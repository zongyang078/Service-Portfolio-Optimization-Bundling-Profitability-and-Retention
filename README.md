# Service Portfolio Optimization: Bundling, Profitability, and Retention

## Overview
This project analyzes customer churn, lifetime value (LTV), and service bundling strategies for a telecom company using real-world customer data.

By combining churn prediction, customer segmentation, and profitability modeling, the project demonstrates how data-driven insights can support retention-focused business decisions and long-term revenue optimization.

This project was completed as the final project for **DS 5110: Data Science Foundations** at Northeastern University.


## Business Problem
Telecom providers face:
- High customer acquisition costs
- Significant churn among short-tenure and price-sensitive users
- Limited alignment between service bundles and customer lifetime value

The objective is to:
- Predict customer churn risk
- Quantify customer lifetime value
- Segment customers into actionable personas
- Inform service bundling and retention strategies


## Dataset
- **Source**: Telco Customer Churn Dataset (Kaggle)
- **Size**: 7,043 customers
- **Features**:
  - Demographics
  - Contract and service subscriptions
  - Billing and payment behavior
  - Churn indicator

Data preprocessing includes missing-value handling, categorical encoding, and behavioral feature engineering.


## Methodology

### Churn Prediction
- **Logistic Regression**
  - L2 regularization
  - Class balancing for label imbalance
  - Interpretable coefficients for churn drivers
- **XGBoost**
  - Captures nonlinear feature interactions
  - Tuned tree depth, learning rate, and boosting rounds

### Lifetime Value (LTV) Modeling
- Deterministic LTV formulation based on monthly charges and tenure
- Linear regression used to validate profitability estimation

### Customer Segmentation
- K-Means clustering (k = 4)
- Segments customers by:
  - Spending level
  - Tenure
  - Churn risk
  - Estimated LTV


## Key Results
- Logistic Regression and XGBoost achieve comparable churn prediction performance (ROC-AUC ≈ 0.84)
- High-tenure, multi-service customers exhibit significantly higher lifetime value
- Customer segmentation reveals distinct personas with different retention and upsell priorities
- Insights support targeted retention strategies rather than uniform discounting


## Project Structure
├── data/        # Raw and processed datasets
├── notebooks/   # EDA, modeling, and optimization notebooks
├── figure/      # Visualizations
├── report/      # Final project report (PDF)
└── LICENSE


## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib, Seaborn
- Jupyter Notebook


## Contributors
- **Zongyang Li** – LTV modeling, customer segmentation, analysis interpretation
- **Jiani He** – Data preprocessing, EDA, churn modeling, evaluation


## License
MIT License
