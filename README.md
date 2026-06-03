# Machine Learning Projects — Overview

This repository contains four machine learning and data analysis projects. Each section below documents one project independently.

---

# Table of Contents

1. [Car Price Prediction](#1-car-price-prediction)
2. [Sales Prediction](#2-sales-prediction)
3. [Unemployment Analysis](#3-unemployment-analysis)
4. [Iris Flower Classification](#4-iris-flower-classification)

---

# 1. Car Price Prediction with Machine Learning

## Overview

This project predicts the **selling price of used cars** using a Random Forest Regressor. It covers the full ML pipeline — from data loading and preprocessing to model training, evaluation, and feature importance visualization.

## Dataset

- **File:** `car data.csv`
- **Target Variable:** `Selling_Price`
- **Features Used:**
  - `Year`, `Present_Price`, `Kms_Driven`
  - `Fuel_Type`, `Selling_type`, `Transmission`, `Owner`

> The `Car_Name` column is dropped as it is not useful for regression modeling.

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical computations |
| `matplotlib` / `seaborn` | Data visualization |
| `scikit-learn` | ML model, preprocessing, and evaluation |

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

## Model

- **Algorithm:** Random Forest Regressor
- **Parameters:** `n_estimators=100`, `random_state=42`

## Evaluation Metrics

| Metric | Description |
|---|---|
| **RMSE** | Root Mean Squared Error — lower is better |
| **R² Score** | Proportion of variance explained — closer to 1 is better |

## Output

- Printed RMSE and R² Score
- Feature importance bar chart (horizontal, teal-colored)

## How to Run

1. Place `car data.csv` in your working directory (update the path in the notebook if needed).
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Open and run `Car_Price_Prediction.ipynb` cell by cell.

---

# 2. Sales Prediction

## Overview

This project predicts **product sales** based on advertising spend across three channels — TV, Radio, and Newspaper — using a **Linear Regression** model. It explores the relationship between marketing budgets and sales revenue.

## Dataset

- **File:** `Advertising.xls`
- **Target Variable:** `Sales`
- **Features:**
  - `TV` — Advertising budget spent on TV
  - `Radio` — Advertising budget spent on Radio
  - `Newspaper` — Advertising budget spent on Newspaper

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical computations |
| `matplotlib` / `seaborn` | Data visualization |
| `scikit-learn` | ML model and evaluation metrics |

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

## Model

- **Algorithm:** Linear Regression
- **Parameters:** Default (no hyperparameter tuning)

## Evaluation Metrics

| Metric | Description |
|---|---|
| **RMSE** | Root Mean Squared Error — lower is better |
| **R² Score** | Proportion of variance explained — closer to 1 is better |

## Output

- Correlation heatmap
- Pairplot of advertising channels vs. sales
- Scatter plot: Actual vs. Predicted Sales with an ideal reference line
- Coefficient table showing the influence of TV, Radio, and Newspaper

## Key Insight

The coefficient table reveals which advertising channel has the **strongest impact on sales**, helping businesses allocate their marketing budget more effectively.

## How to Run

1. Place `Advertising.xls` in your working directory (update the path in the notebook if needed).
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Open and run `Sales_Prediction.ipynb` cell by cell.

---

# 3. Unemployment Analysis

## Overview

This project performs an **exploratory data analysis (EDA)** of unemployment rates across regions in India. It focuses on identifying trends over time, analyzing the impact of the **COVID-19 pandemic in 2020**, and uncovering seasonal patterns in unemployment data.

## Datasets

| File | Description |
|---|---|
| `Unemployment in India.xls` | General unemployment data across Indian regions |
| `Unemployment_Rate_upto_11_2020.xls` | Unemployment data up to November 2020 (used for COVID analysis) |

- **Key Columns:** `Date`, `Region`, `Estimated Unemployment Rate (%)`

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, and transformation |
| `matplotlib` | Plotting charts |
| `seaborn` | Enhanced statistical visualizations |

## Workflow

1. **Load Datasets** — Read both XLS files into DataFrames
2. **Clean Column Names** — Strip whitespace from column headers
3. **Parse Dates** — Convert `Date` column to `datetime` format (day-first)
4. **Handle Missing Values** — Drop rows with null or invalid entries
5. **Regional Trend Visualization** — Line plot of unemployment rate over time by region
6. **COVID-19 Focus (2020)** — Filter data for 2020 and visualize regional unemployment spikes
7. **Seasonal Analysis** — Compute and plot monthly average unemployment rates
8. **Top 10 COVID Spikes** — Identify the 10 highest unemployment readings during the pandemic

## Analyses Performed

### Regional Unemployment Trend
Line plot showing unemployment rate over time for each region, helping identify consistently high or low unemployment areas.

### COVID-19 Impact (2020)
Filtered view of 2020 data only, highlighting the sharp spike in unemployment during lockdown months (April–June 2020).

### Seasonal Trend
Average unemployment rate grouped by calendar month — a bar chart reveals which months historically see higher unemployment.

### Top 10 Unemployment Spikes
Tabular output of the 10 worst unemployment readings during COVID-19, with columns: `Region`, `Date`, `Estimated Unemployment Rate (%)`.

## Output

- Line charts for regional unemployment trends
- Bar chart of average monthly unemployment
- Printed table of top 10 highest unemployment spikes during COVID

## Key Insight

The analysis reveals a **dramatic surge in unemployment during April–May 2020**, coinciding with India's national lockdown, with some regions seeing extreme spikes compared to the pre-COVID baseline.

## How to Run

1. Place both dataset files in your working directory (update paths in the notebook if needed).
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn
   ```
3. Open and run `Unemployment_Analysis.ipynb` cell by cell.

---

# 4. Iris Flower Classification

## Overview

This project classifies **Iris flowers into three species** — *Setosa*, *Versicolor*, and *Virginica* — based on their physical measurements. It uses the classic **K-Nearest Neighbors (KNN)** algorithm and achieves near-perfect accuracy on the dataset.

## Dataset

- **File:** `Iris.xls`
- **Target Variable:** `Species` (3 classes: Setosa, Versicolor, Virginica)
- **Features:**
  - `SepalLengthCm`
  - `SepalWidthCm`
  - `PetalLengthCm`
  - `PetalWidthCm`

> Note: The dataset includes an `Id` column which is retained during training to match the feature shape.

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading and exploration |
| `numpy` | Numerical operations |
| `matplotlib` / `seaborn` | Data visualization |
| `scikit-learn` | ML model, splitting, and evaluation |

## Workflow

1. **Load Dataset** — Read `Iris.xls` and preview with `.head()`
2. **Explore Data** — Check shape, columns, descriptive stats, and null values
3. **Visualize Data** — Pairplot (colored by species) and correlation heatmap
4. **Prepare Features & Labels** — `X` = all columns except last; `y` = `Species`
5. **Train-Test Split** — 80% training / 20% testing (`random_state=42`)
6. **Train Model** — Fit a `KNeighborsClassifier` with `n_neighbors=3`
7. **Make Predictions** — Predict species on the test set
8. **Evaluate** — Accuracy score, confusion matrix, and classification report
9. **Test with New Data** — Predict the species of a custom flower sample

## Model

- **Algorithm:** K-Nearest Neighbors (KNN)
- **Parameters:** `n_neighbors=3`

## Evaluation Metrics

| Metric | Result |
|---|---|
| **Accuracy** | 100% (1.0) on the test set |
| **Confusion Matrix** | Perfect classification across all 3 species |
| **Classification Report** | Precision, Recall, F1-Score per class |

> The model achieves **100% accuracy** on the test set, which is typical for KNN on the well-separated Iris dataset.

## Output

- Pairplot of all features colored by species
- Correlation heatmap of numerical features
- Printed predictions, accuracy score, confusion matrix, and classification report
- Prediction for a custom sample flower

## Custom Prediction Example

```python
sample = [[0, 5.1, 3.5, 1.4, 0.2]]  # [Id, SepalLength, SepalWidth, PetalLength, PetalWidth]
prediction = model.predict(sample)
print("Predicted Class:", prediction)
```

## How to Run

1. Place `Iris.xls` in your working directory (update the path in the notebook if needed).
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Open and run `Iris.ipynb` cell by cell.

---

## Projects Summary

| Project | Algorithm | Type | Key Metric |
|---|---|---|---|
| Car Price Prediction | Random Forest Regressor | Regression | RMSE, R² Score |
| Sales Prediction | Linear Regression | Regression | RMSE, R² Score |
| Unemployment Analysis | EDA (No ML Model) | Analysis | Visual Trends |
| Iris Classification | K-Nearest Neighbors | Classification | Accuracy (100%) |
