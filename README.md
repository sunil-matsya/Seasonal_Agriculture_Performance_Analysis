# Seasonal Agriculture Performance Analysis

A data analytics project exploring how agricultural performance — yield, resource usage,
environmental conditions, and economic outcomes — varies across the three Indian
agricultural seasons: **Kharif**, **Rabi**, and **Zaid**.

## 📌 Description

This project analyzes a farm-level agricultural dataset (4,000 records across 8 Indian
states and 8 crops) to answer a central question: **how and why does agricultural
performance change from one season to another?**

The analysis covers:
- **Data cleaning** — handling missing values (season-wise median imputation), duplicate
  checks, and outlier treatment (IQR-based capping) for yield, water efficiency, and profit.
- **Exploratory Data Analysis (EDA)** — distribution of records by season, state, and crop.
- **Seasonal comparison** of:
  - Environmental conditions (rainfall, temperature, humidity, sunlight, soil moisture)
  - Resource usage (fertilizer, pesticide, water usage, irrigation method mix)
  - Yield and production
  - Economic performance (cost, revenue, profit per hectare, profit margin)
- **Statistical testing** — one-way ANOVA to confirm whether seasonal differences in yield
  and profit are statistically significant.
- **Cross-cutting analysis** — state-wise and crop-wise seasonal heatmaps to check whether
  seasonal patterns are consistent across regions and crops.
- **Correlation analysis** — identifying which environmental/resource variables most
  strongly relate to yield and profit.
- **Insights & recommendations** — evidence-based conclusions to support seasonal
  agricultural planning.

## 🗂️ Repository Structure

```
.
├── Seasonal_Agriculture_Performance_Analysis.ipynb   # Main analysis notebook
├── seasonal_agriculture_performance_dataset.csv      # Dataset (place here before running)
├── requirements.txt                                  # Python dependencies
├── .gitignore
└── README.md
```

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
   ```
2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv .venv
   source .venv/bin/activate      # on Windows: .venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Make sure `seasonal_agriculture_performance_dataset.csv` is in the project root.
5. Open and run the notebook in VS Code (or Jupyter):
   ```bash
   jupyter notebook Seasonal_Agriculture_Performance_Analysis.ipynb
   ```
   or open it directly in VS Code with the Jupyter extension and **Run All**.

## 📊 Dataset

The dataset contains 28 columns per farm record, including:
- **Identifiers:** `Farm_ID`, `State`, `District`, `Crop`, `Season`
- **Environmental conditions:** `Rainfall_mm`, `Avg_Temperature_C`, `Humidity_pct`,
  `Sunlight_Hours_Day`, `Soil_pH`, `Soil_Moisture_pct`
- **Inputs / resource usage:** `Nitrogen_kg_ha`, `Phosphorus_kg_ha`, `Potassium_kg_ha`,
  `Irrigation_Method`, `Fertilizer_kg_ha`, `Pesticide_Litre_ha`, `Seed_Quality_Score`,
  `Water_Used_m3`, `Water_Efficiency_t_per_1000m3`
- **Outcomes:** `Yield_Tonnes_Ha`, `Production_Tonnes`, `Market_Price_INR_Tonne`,
  `Total_Cost_INR`, `Revenue_INR`, `Profit_INR`, `Disease_Pest_Risk_pct`

## 🔎 Key Findings (Summary)

- **Kharif** has the highest average yield (~2.25 t/ha) and profit per hectare (~₹13,800),
  driven mainly by better water availability — despite also having the **highest**
  disease/pest risk of the three seasons.
- **Zaid** is the weakest season economically, with the lowest revenue per hectare and a
  net average loss, even though costs are similar across all seasons.
- **Water efficiency**, not rainfall or fertilizer amount, is the strongest correlate of
  yield and profit in this dataset.
- Seasonal differences in yield and profit per hectare are statistically significant
  (one-way ANOVA, p < 0.001 for both).

Full details, charts, and statistical tests are in the notebook.

## 🛠️ Tools & Libraries

`Python`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `Jupyter Notebook`

## 📄 License

This project is for educational purposes.
