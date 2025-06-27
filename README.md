# AQI_file

# Define the README content as discussed
PM2.5 Prediction Using Spatial-Meteorological Correlations

This project aims to predict PM2.5 levels for multiple air quality monitoring stations using:
- Local and nearby **meteorological and pollutant features**
- **Mutual Information-based feature selection**
- **Tree-based machine learning models**

---

## 📁 Dataset Overview

- `cleaned_data_complete.csv`: Consolidated hourly data for over **30 stations** from 2018 to 2022.
- Each station includes:
  - **Pollutant levels**: PM2.5, PM10, NO2, SO2, CO, NH3, O3
  - **Meteorological parameters**: Temperature, Humidity, Wind Speed/Direction, Rainfall, Solar Radiation, Barometric Pressure
- `location.csv`: Latitude and Longitude for each station.

---

## 🚦 Objective

- Predict **PM2.5 concentration** at each station using:
  - Its own features
  - Meteorological parameters from **5 geographically closest stations**
- Evaluate **spatial and temporal influence** on air pollution, especially during **COVID** phases.

---

## 🧪 Methodology

### 1. 📌 Preprocessing
- Cleaned missing values and ensured column-wise uniformity across all stations.
- Created a **unified time-indexed dataset** with 270+ features (for 30+ stations).

### 2. 🗺️ Spatial Analysis
- Used `location.csv` to calculate pairwise distances between stations using **Haversine distance**.
- Identified **5 nearest neighbors** for each station.

### 3. 🧠 Mutual Information Analysis
- For each station:
  - Target: Its own **PM2.5 values**
  - Features: Meteorological data from 5 nearest stations
- Calculated **MI scores** to assess dependence and correlation.
- Selected high-MI features to enhance model inputs.

### 4. 🔍 Temporal Segmentation
- Data split into 3 distinct periods:
  - **Pre-COVID**
  - **During COVID**
  - **Post-COVID**
- This allowed analysis of pollution patterns across major socio-economic disruptions.

### 5. 📊 Visualization
- Used `Plotly` to map station locations and visualize spatial PM2.5 trends dynamically.
- Created clustered maps to view hotspots and patterns over time.

### 6. 🤖 Machine Learning Models
Applied supervised ML models to predict PM2.5:
- ✅ Decision Tree Regressor
- ✅ Random Forest Regressor
- ✅ XGBoost Regressor

Evaluation Metrics:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## 🔍 Key Findings

- **Nearby station features** (especially wind speed/direction and humidity) showed strong influence on target PM2.5 levels.
- **COVID lockdown** significantly reduced pollutant levels across multiple clusters.
- Random Forest outperformed others in terms of generalization and accuracy.

---

## 📈 Future Work

- Implement deep learning models (LSTM, CNN-GRU) for time-series forecasting.
- Automate **real-time predictions** using APIs and model deployment.
- Use **spatial clustering** for adaptive feature selection over time.

---

## 🛠️ Libraries Used

- `pandas`, `numpy`
- `sklearn`, `xgboost`
- `plotly`, `seaborn`
- `geopy` for distance calculations
- `mutual_info_regression` from `sklearn.feature_selection`

---

## 📌 Author
