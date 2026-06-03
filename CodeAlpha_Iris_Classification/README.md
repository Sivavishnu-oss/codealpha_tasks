# Iris Flower Classification

## Overview

This project classifies **Iris flowers into three species** — *Setosa*, *Versicolor*, and *Virginica* — based on their physical measurements. It uses the classic **K-Nearest Neighbors (KNN)** algorithm and achieves near-perfect accuracy on the dataset.

---

## Dataset

- **File:** `Iris.xls`
- **Target Variable:** `Species` (3 classes: Setosa, Versicolor, Virginica)
- **Features:**
  - `SepalLengthCm`
  - `SepalWidthCm`
  - `PetalLengthCm`
  - `PetalWidthCm`

> Note: The dataset includes an `Id` column which is retained during training to match the feature shape.

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading and exploration |
| `numpy` | Numerical operations |
| `matplotlib` / `seaborn` | Data visualization |
| `scikit-learn` | ML model, splitting, and evaluation |

---

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

---

## Model

- **Algorithm:** K-Nearest Neighbors (KNN)
- **Parameters:** `n_neighbors=3`

---

## Evaluation Metrics

| Metric | Result |
|---|---|
| **Accuracy** | 100% (1.0) on the test set |
| **Confusion Matrix** | Perfect classification across all 3 species |
| **Classification Report** | Precision, Recall, F1-Score per class |

> The model achieves **100% accuracy** on the test set, which is typical for KNN on the well-separated Iris dataset.

---

## Output

- Pairplot of all features colored by species
- Correlation heatmap of numerical features
- Printed predictions, accuracy score, confusion matrix, and classification report
- Prediction for a custom sample flower

---

## Custom Prediction Example

```python
sample = [[0, 5.1, 3.5, 1.4, 0.2]]  # [Id, SepalLength, SepalWidth, PetalLength, PetalWidth]
prediction = model.predict(sample)
print("Predicted Class:", prediction)
```

---

## How to Run

1. Place `Iris.xls` in your working directory (update the path in the notebook if needed).
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Open and run `Iris.ipynb` cell by cell.
