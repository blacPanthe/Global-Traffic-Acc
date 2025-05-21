# 🌍 Global Traffic Accidents Analysis

This project focuses on analyzing global traffic accident data to uncover patterns, trends, and insights that can help reduce casualties and improve road safety. Using data science techniques such as exploratory data analysis (EDA), feature engineering, and machine learning models like Random Forest, this project aims to predict casualty severity and understand the key factors contributing to accidents globally.

## 📊 Project Goals

* Perform EDA to understand accident distribution, patterns, and severity.
* Preprocess and clean the dataset.
* Engineer meaningful features for modeling.
* Train and evaluate machine learning models to predict **Casualty Severity**.
* Visualize insights using plots and maps for better interpretation.

## 🛠️ Technologies Used

* **Python**
* **Pandas, NumPy** – Data manipulation
* **Matplotlib, Seaborn** – Visualization
* **Scikit-learn** – Machine learning (Random Forest, train-test split, accuracy metrics)
* **Jupyter Notebook** – Interactive analysis and documentation

## 📁 Dataset

The dataset contains global traffic accident records including:

* Date and Time of accident
* Location details
* Number of casualties
* Weather and road conditions
* Vehicle type, driver info
* Severity of the accident

## 🧠 Model

We use a **Random Forest Classifier** to predict the **Casualty Severity** based on multiple features including location, conditions, and involved parties. The model's performance is evaluated using accuracy and classification reports.

## 🔍 Key Findings

* Certain road types and weather conditions are strongly associated with higher accident severity.
* The model shows promising results in predicting accident severity with reasonable accuracy.
* Visualizations highlight accident hotspots and factors contributing to casualty risk.

## 📈 Visuals

Visualizations include:

* Correlation heatmaps
* Bar and pie charts
* Feature importance from Random Forest
* Severity distribution

## 🚀 How to Run

1. Clone the repository

```bash
git clone https://github.com/yourusername/global-traffic-accidents.git
cd global-traffic-accidents
```

2. Install required packages

```bash
pip install -r requirements.txt
```

3. Open the Jupyter Notebook

```bash
jupyter notebook Global_Traffic_Accidents.ipynb
```

## 📌 Future Work

* Include time series forecasting of accident rates
* Integrate geospatial mapping (e.g., Folium)
* Expand model to multi-class severity prediction
* Automate insights using a dashboard (Power BI or Tableau)

## 🙌 Contributors

* Atharva Bakde
* Samarth Naik


