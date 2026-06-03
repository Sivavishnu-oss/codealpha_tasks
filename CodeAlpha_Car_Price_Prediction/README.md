# Car Price Prediction with Machine Learning

## Overview

This project predicts the **selling price of used cars** using a Random Forest Regressor. It covers the full ML pipeline — from data loading and preprocessing to model training, evaluation, and feature importance visualization.

---

## Dataset

- **File:** `car data.csv`
- **Target Variable:** `Selling_Price`
- **Features Used:**
  - `Year`, `Present_Price`, `Kms_Driven`
  - `Fuel_Type`, `Selling_type`, `Transmission`, `Owner`

> The `Car_Name` column is dropped as it is not useful for regression modeling.

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical computations |
| `matplotlib` / `seaborn` | Data visualization |
| `scikit-learn` | ML model, preprocessing, and evaluation |

---

## Workflow

1. **Load Dataset** — Read CSV and inspect with `.head()`, `.info()`, `.describe()`
2. **Drop Irrelevant Column** — Remove `Car_Name`
3. **Encode Categorical Features** — Apply `LabelEncoder` to `Fuel_Type`, `Selling_type`, `Transmission`
4. **Define Features & Target** — `X` = all columns except `Selling_Price`; `y` = `Selling_Price`
5. **Train-Test Split** — 80% training / 20% testing (`random_state=42`)
6. **Train Model** — `RandomForestRegressor` with 100 estimators
7. **Predict** — Generate predictions on the test set
8. **Evaluate** — Compute RMSE and R² Score
9. **Feature Importance** — Horizontal bar chart of feature importance scores

---

## Model

- **Algorithm:** Random Forest Regressor
- **Parameters:** `n_estimators=100`, `random_state=42`

---

## Evaluation Metrics

| Metric | Description |
|---|---|
| **RMSE** | Root Mean Squared Error — lower is better |
| **R² Score** | Proportion of variance explained — closer to 1 is better |

---

## Output

- Printed RMSE and R² Score
- Feature importance bar chart (horizontal, teal-colored)

---

## How to Run

1. Place `car data.csv` in your working directory (update the path in the notebook if needed).
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Open and run `Car_Price_Prediction.ipynb` cell by cell.
