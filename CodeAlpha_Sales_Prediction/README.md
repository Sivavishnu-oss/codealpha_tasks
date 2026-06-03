# Sales Prediction with Machine Learning

## Overview

This project predicts **product sales** based on advertising spend across three channels — TV, Radio, and Newspaper — using a **Linear Regression** model. It explores the relationship between marketing budgets and sales revenue.

---

## Dataset

- **File:** `Advertising.xls`
- **Target Variable:** `Sales`
- **Features:**
  - `TV` — Advertising budget spent on TV
  - `Radio` — Advertising budget spent on Radio
  - `Newspaper` — Advertising budget spent on Newspaper

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical computations |
| `matplotlib` / `seaborn` | Data visualization |
| `scikit-learn` | ML model and evaluation metrics |

---

## Workflow

1. **Load Data** — Read `Advertising.xls` into a DataFrame
2. **Explore Data** — View `.head()`, `.info()`, `.describe()`, and check for missing values
3. **Visualize Relationships** — Pairplot of all features vs. Sales
4. **Correlation Heatmap** — Identify which channels correlate most with Sales
5. **Define Features & Target** — `X` = `[TV, Radio, Newspaper]`; `y` = `Sales`
6. **Train-Test Split** — 80% training / 20% testing (`random_state=42`)
7. **Train Model** — Fit a `LinearRegression` model
8. **Predict & Evaluate** — Compute RMSE and R² Score
9. **Visualize Predictions** — Scatter plot of Actual vs. Predicted Sales
10. **Feature Coefficients** — Display the influence of each advertising channel on sales

---

## Model

- **Algorithm:** Linear Regression
- **Parameters:** Default (no hyperparameter tuning)

---

## Evaluation Metrics

| Metric | Description |
|---|---|
| **RMSE** | Root Mean Squared Error — lower is better |
| **R² Score** | Proportion of variance explained — closer to 1 is better |

---

## Output

- Correlation heatmap
- Pairplot of advertising channels vs. sales
- Scatter plot: Actual vs. Predicted Sales with an ideal reference line
- Coefficient table showing the influence of TV, Radio, and Newspaper

---

## Key Insight

The coefficient table reveals which advertising channel has the **strongest impact on sales**, helping businesses allocate their marketing budget more effectively.

---

## How to Run

1. Place `Advertising.xls` in your working directory (update the path in the notebook if needed).
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Open and run `Sales_Prediction.ipynb` cell by cell.
