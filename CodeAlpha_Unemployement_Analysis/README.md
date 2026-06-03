# Unemployment Analysis

## Overview

This project performs an **exploratory data analysis (EDA)** of unemployment rates across regions in India. It focuses on identifying trends over time, analyzing the impact of the **COVID-19 pandemic in 2020**, and uncovering seasonal patterns in unemployment data.

---

## Datasets

| File | Description |
|---|---|
| `Unemployment in India.xls` | General unemployment data across Indian regions |
| `Unemployment_Rate_upto_11_2020.xls` | Unemployment data up to November 2020 (used for COVID analysis) |

- **Key Columns:** `Date`, `Region`, `Estimated Unemployment Rate (%)`

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, and transformation |
| `matplotlib` | Plotting charts |
| `seaborn` | Enhanced statistical visualizations |

---

## Workflow

1. **Load Datasets** — Read both CSV/XLS files into DataFrames
2. **Clean Column Names** — Strip whitespace from column headers
3. **Parse Dates** — Convert `Date` column to `datetime` format (day-first)
4. **Handle Missing Values** — Drop rows with null or invalid entries
5. **Regional Trend Visualization** — Line plot of unemployment rate over time by region
6. **COVID-19 Focus (2020)** — Filter data for 2020 and visualize regional unemployment spikes
7. **Seasonal Analysis** — Compute and plot monthly average unemployment rates
8. **Top 10 COVID Spikes** — Identify the 10 highest unemployment readings during the pandemic

---

## Analyses Performed

### 1. Regional Unemployment Trend
- Line plot showing unemployment rate over time for each region
- Helps identify consistently high or low unemployment areas

### 2. COVID-19 Impact (2020)
- Filtered view of 2020 data only
- Highlights the sharp spike in unemployment during lockdown months (April–June 2020)

### 3. Seasonal Trend
- Average unemployment rate grouped by calendar month
- Bar chart reveals which months historically see higher unemployment

### 4. Top 10 Unemployment Spikes
- Tabular output of the 10 worst unemployment readings during COVID-19
- Columns: `Region`, `Date`, `Estimated Unemployment Rate (%)`

---

## Output

- Line charts for regional unemployment trends
- Bar chart of average monthly unemployment
- Printed table of top 10 highest unemployment spikes during COVID

---

## Key Insight

The analysis reveals a **dramatic surge in unemployment during April–May 2020**, coinciding with India's national lockdown, with some regions seeing extreme spikes compared to the pre-COVID baseline.

---

## How to Run

1. Place both dataset files in your working directory (update paths in the notebook if needed).
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn
   ```
3. Open and run `Unemployment_Analysis.ipynb` cell by cell.
