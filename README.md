
# 🌍 Earthquake Magnitude Prediction & High-Risk Region Identification

This project applies **data mining and machine learning techniques** to historical earthquake data to predict earthquake magnitudes and identify **high-risk regions** across the globe. Through exploratory analysis, modeling, and clustering, the goal is to support **disaster preparedness** and **risk assessment** initiatives.

## 📌 Project Objectives

- Predict earthquake magnitudes using classification models.
- Identify high-risk regions using clustering techniques.
- Analyze patterns in seismic data and extract actionable insights.
- Provide visualizations to support interpretation of earthquake behavior.

## 📊 Dataset Overview

- **Source**: [Kaggle - Earthquake Dataset (1995–2023)](https://www.kaggle.com/datasets/warcoder/earthquake-dataset?select=earthquake_1995-2023.csv)
- **Records**: 1001
- **Features**: 19 columns including magnitude, depth, coordinates, tsunami indicator, alert levels, and more.
- **Time Period**: 2001–2023

## 🔍 Research Questions

- Can we predict earthquake magnitudes from past data?
- What regions are most prone to high-magnitude earthquakes?
- How do variables like depth, tsunami alerts, and seismic significance correlate with earthquake severity?

## ⚙️ Methods Used

### 📈 Exploratory Data Analysis (EDA)
- Histograms of magnitude, depth, CDI, MMI, etc.
- Pie charts for alert levels and tsunami occurrence
- Treemap of yearly earthquake counts
- Scatter plots for visual cluster interpretation

### 🧹 Data Preprocessing
- Missing value imputation (mean strategy)
- Z-score normalization for numeric features
- Outlier removal using z-score threshold of 2.5

### 🔮 Predictive Modeling

#### Decision Tree
- Target: Earthquake magnitude
- Accuracy: **63.45%**
- Techniques: Train-test split & cross-validation

#### K-Nearest Neighbors (KNN)
- Target: Discretized magnitude range
- Accuracy: **86.47%**
- K: 3, Distance: Euclidean
- Best performance among models

### 📍 Clustering

#### DBSCAN
- Goal: Identify earthquake-prone regions
- Parameters: `epsilon = 0.8`, `minPoints = 10`
- Result: 5 clusters identifying severity-based risk regions

## 📈 Results Summary

| Model          | Accuracy   | Highlights                          |
|----------------|------------|--------------------------------------|
| Decision Tree  | 63.45%     | Moderate accuracy, high variance     |
| KNN            | 86.47%     | Best performance, strong middle-range predictions |
| DBSCAN Clustering | N/A     | Identified spatially significant risk zones |

## 🧠 Key Insights

- KNN outperforms decision trees in magnitude prediction.
- DBSCAN clustering identifies geographically high-risk regions.
- Features like `depth`, `sig`, `mmi`, and `tsunami` show strong correlation with earthquake impact.

## 🚧 Limitations

- Data inconsistencies and missing values may affect model reliability.
- DBSCAN is sensitive to hyperparameters.
- Real-time prediction was not implemented in this version.

## 📌 Recommendations

- Use the model outputs to aid in early earthquake alerts.
- Strengthen disaster preparedness efforts in clustered high-risk regions.
- Continue improving data quality and explore real-time integrations.

## 🚀 Future Work

- Compare with other clustering techniques (e.g., K-Means, Hierarchical Clustering).
- Add features like tectonic plate data and population density.
- Deploy real-time models using continuous seismic data streams.

## 💻 Tools & Technologies

- Python
- RapidMiner
- Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn
- DBSCAN Clustering
