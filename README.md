# Customer Churn Prediction

## Project overview
This project explores whether customer information can help predict whether a customer will leave a subscription service.

## Dataset
The training dataset contains these fields:

| Field | Description | Role |
|---|---|---|
| `customer_id` | Customer identifier | Identifier only; exclude from model features |
| `tenure_months` | Number of months as a customer | Input feature |
| `support_tickets` | Number of support tickets | Input feature |
| `monthly_spend` | Monthly amount spent | Input feature |
| `last_login_days` | Days since last login | Input feature |
| `plan_type` | Basic, Standard, or Pro plan | Input feature |
| `churned` | 1 = churned, 0 = stayed | Prediction target |

## Problem framing
The goal is to identify customers who may be at risk of leaving so that customer-service staff can review the prediction and decide whether support or a check-in would be useful.

## Responsible use
- Treat predictions as decision support, not as automatic decisions.
- Have a staff member review predictions before taking action.
- Protect customer identifiers and restrict access to the data.
- Check missing values, data leakage, and data quality before training.
- Compare machine learning with a simple non-ML baseline, such as a rule based on recent login activity.
- Monitor model performance and stop using the model if it becomes unreliable.

## Dataset limitation
The screenshot supplied for this project shows 12 customer records. This is too small to support reliable real-world conclusions. Any model trained on this sample should be treated as a demonstration only.

## Files
- `ML_Problem_Framing_Memo.docx` — project problem-framing memo.

## Before real deployment
Confirm the data source, collection method, consent, churn measurement period, and prediction/action window. Evaluate with a held-out dataset and report accuracy, precision, recall, and a confusion matrix.
