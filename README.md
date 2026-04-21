# Global Traffic Accidents Analysis

**Authors:** Atharva Bakde & Samarth Naik &nbsp;|&nbsp; **Date:** April 2025

Traffic accidents remain one of the leading causes of preventable death globally. This project analyzes worldwide accident records to uncover patterns in timing, weather, and road conditions — then builds machine learning models to predict whether a reported accident resulted in casualties.

---

## Dataset

The dataset contains global traffic accident records including:

| Feature | Description |
|---|---|
| Date / Time | Timestamp of the accident |
| Location | Geographic coordinates + location name |
| Casualties | Number of people injured or killed |
| Weather Condition | Fog, rain, clear, hail, etc. |
| Road Condition | Wet, dry, icy, etc. |
| Vehicles Involved | Count of vehicles in the accident |
| Cause | Driver error, mechanical failure, drunk driving, etc. |

---

## Workflow

1. **Data Quality Checks** — missing values, duplicates, unique value analysis
2. **Feature Engineering** — time decomposition (hour, day, month, week), one-hot encoding, IQR outlier removal
3. **Preprocessing** — StandardScaler, SMOTE for class imbalance, 70/15/15 stratified split
4. **Modeling** — Random Forest Classifier & Logistic Regression
5. **Evaluation** — Accuracy, Precision, Recall, F1-Score, Confusion Matrix

---

## Results

| Model | Train Accuracy | Validation Accuracy | Test Accuracy |
|---|---|---|---|
| **Random Forest** | **95.0%** | **87.5%** | **86.7%** |
| Logistic Regression | 52.2% | 51.5% | 51.5% |

**Random Forest** is the recommended model. Logistic Regression underperforms due to the non-linear interactions between time, weather, and road features.

> **Note on class imbalance:** ~90% of records involve casualties, so threshold tuning is recommended to improve recall on no-casualty cases.

---

## Key Findings

- **Time-based features dominate** — week of year (18.9%), hour (16.6%), day of week (11.4%), and month (10.3%) are the top four predictors
- **Vehicles involved** is the strongest non-temporal feature (9.4% importance)
- **Weather and cause features** (fog, drunk driving, mechanical failure) each contribute ~2–3%, confirming real-world intuitions about accident severity
- Logistic Regression's near-chance accuracy (51.5%) confirms that linear models are insufficient for this dataset

---

## Setup

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn requests
```

1. Clone the repository
   ```bash
   git clone https://github.com/blacPanthe/Global-Traffic-Acc.git
   cd Global-Traffic-Acc
   ```
2. Open `Global_Traffic_Accidents.ipynb` in Jupyter or Google Colab
3. Run all cells — the dataset loads automatically from Google Drive

---

## Future Work

- Threshold optimization to improve no-casualty recall
- Gradient boosting models (XGBoost, LightGBM) for better imbalance handling
- Geospatial mapping of accident hotspots (Folium)
- Time series forecasting of accident rates by region
- Interactive dashboard (Power BI or Tableau)
