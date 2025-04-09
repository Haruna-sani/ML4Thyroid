# Thyroid Cancer Recurrence Classifier

## Project Overview

This project aims to develop a robust machine learning model to classify the **recurrence of thyroid cancer** in patients as either **"Yes" (1)** or **"No" (0)**. The classification helps in identifying patients at risk of recurrence and could assist healthcare professionals in making more informed decisions.

## Class Imbalance Handling

The original dataset exhibited a significant class imbalance:

To address this issue, we applied the **SMOTE (Synthetic Minority Oversampling Technique)** to balance the target class and prevent the model from being biased toward the majority class.

## Features and Target

- **Predictor Variables**:
  - `Age`
  - `Gender`
  - `Hx Radiothreapy`
  - `Risk`
  - `T`, `N`, `M`
  - `Stage`
  - `Response`
  - `Pathology`
  - `Focality`
  - `Adenopathy`

- **Target Variable**:
  - `Recurred` (0 = No, 1 = Yes)

## Modeling Techniques

We used a **train-test split of 80:20**, and applied the following models:

- **Random Forest (RF)**
- **LightGBM**
- **XGBoost**
- **Ensemble Learning** (majority vote of the three above)

---

## Model Performance

| Model          | Accuracy | Precision | Recall | Kappa  |
|----------------|----------|-----------|--------|--------|
| XGBoost        | 93.51%   | 91.63%    | 92.73% | 0.8430 |
| Random Forest  | 94.81%   | 92.28%    | 95.00% | 0.8761 |
| LightGBM       | 92.21%   | 89.78%    | 91.82% | 0.8142 |
| Ensemble Model | 94.81%   | 92.28%    | 95.00% | 0.8761 |

---

## Comparative Analysis

- **Random Forest** and **Ensemble models** outperformed the others in terms of **accuracy (94.81%)** and **recall (95%)**, making them highly effective in identifying recurrence cases.

- **XGBoost** achieved slightly lower results but still demonstrated strong performance across all metrics with a kappa statistic of **0.8430**, indicating substantial agreement between predictions and actual outcomes.

- **LightGBM** performed adequately with an accuracy of **92.21%** and a kappa of **0.8142**, showing it can still be a reliable option when computational efficiency is needed.

- **Precision** values were highest for RF and Ensemble at **92.28%**, indicating lower false positives—a critical factor in medical predictions.

- **Kappa statistics**, which account for agreement beyond chance, show that RF and Ensemble are the most consistent and reliable classifiers in this task.

---

## 📌 Conclusion

This analysis demonstrates that ensemble approaches and Random Forest models offer the most promising results for predicting thyroid cancer recurrence. Given their high precision and recall, these models can be valuable tools in clinical settings, aiding in the timely identification of at-risk patients.

---
