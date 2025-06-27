

APPROACH 
"# 🌫️ PM2.5 Prediction Using Spatial-Meteorological Correlations

This project predicts PM2.5 levels using local and nearby station data, focusing on **spatial correlation**, **mutual information**, and **machine learning models**.

---

## 📁 Datasets

- `cleaned_data_complete.csv`: Hourly pollutant & meteorological data for 30+ stations (2018–2022)
- `location.csv`: Latitude & longitude of stations

---

## 🎯 Goal

- Predict PM2.5 using:
  - Own station’s features
  - Top 5 geographically nearest stations’ meteorological data
- Analyze trends across **Pre-COVID**, **During-COVID**, and **Post-COVID** periods

---

## ⚙️ Methodology

1. **Preprocessing**: Cleaned data and aligned features
2. **Distance Calculation**: Used Haversine distance for finding nearest stations
3. **Mutual Information**: Selected top features from neighbors based on MI with target station’s PM2.5
4. **Temporal Split**: Pre/During/Post COVID for trend comparison
5. **Visualization**: Used `plotly` to map station trends
6. **ML Models**: Applied Decision Tree, Random Forest, and XGBoost

---

## 📊 Results

- Nearby stations’ weather data (esp. wind, humidity) helped boost accuracy
- COVID lockdown reduced PM2.5 across most clusters
- **Random Forest** showed best overall performance

---

## 🔮 Future Scope

- Try LSTM/CNN-GRU for time-series modeling
- Real-time API integration
- Spatial clustering for dynamic feature selection

---

## 🛠️ Tools

- `pandas`, `sklearn`, `xgboost`, `plotly`, `geopy`
"""
