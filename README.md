# Customer Retention Prediction

## Project Overview

This project aims to **predict whether a customer will churn** (leave the company) based on their historical data.
Predicting churn helps businesses take proactive steps to **retain valuable customers** and reduce revenue loss.

The workflow includes:

* Exploratory Data Analysis (EDA)
* Data Preprocessing and Feature Engineering
* Model Training: RandomForest, XGBoost, LightGBM, ANN
* Model Evaluation and Comparison
* Summary of key insights and recommendations

---

## Dataset Description

* **Dataset:** Customer churn dataset (CSV)
* **Number of records:** [Insert number of rows]
* **Number of features:** [Insert number of features]
* **Target variable:** `Target_Churn`

  * 1 → Customer churned
  * 0 → Customer retained
* **Key features include:**

  * `Age` – Customer age
  * `Balance` – Account balance
  * `NumOfProducts` – Number of products used
  * `Tenure` – Customer tenure in months
  * `IsActiveMember` – Whether customer is active
  * Additional engineered features like `Balance_per_Product`, `Tenure_per_Age`

---

## Setup Instructions

1. **Clone the repository**

```bash
git clone <repository_url>
cd Customer-Retention-Prediction
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Run the Jupyter Notebook**

```bash
jupyter notebook notebooks/customer_retention_pipeline.ipynb
```

---

## Key Results

| Model        | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ------------ | -------- | --------- | ------ | -------- | ------- |
| RandomForest | 0.528    | 0.551     | 0.568  | 0.560    | 0.531   |
| XGBoost      | 0.511    | 0.535     | 0.558  | 0.546    | 0.522   |
| LightGBM     | 0.511    | 0.543     | 0.463  | 0.500    | 0.522   |
| ANN          | 0.611    | 0.590     | 0.863  | 0.701    | 0.630   |

**Summary:**

* **ANN** is the best-performing model, with the highest recall and F1-score, effectively identifying customers likely to churn.
* Tree-based models (RandomForest, XGBoost, LightGBM) are less effective on this dataset.
* Important features influencing churn include **Tenure, Balance, NumOfProducts, Balance_per_Product**.
* Recommendation: Deploy ANN for churn prediction and enhance features for better performance.

---

## Additional Notes

* Confusion matrices and ROC curves are included in the notebook for model evaluation.
* Future work: Incorporate more behavioral features, increase dataset size, and explore ensemble models.

