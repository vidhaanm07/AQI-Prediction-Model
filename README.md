# AQI Prediction Model · Group 14 (BASF)

A static, single-page website presenting our supervised machine-learning project that predicts the Air Quality Index (AQI) from pollutant and weather data.

- **Dataset:** [UrbanAirNet: Urban Air Quality and Weather Dataset (Kaggle)](https://www.kaggle.com/datasets/ziya07/urbanairnet-urban-air-quality-and-weather-dataset), 175,205 hourly samples, 12 input features, target `AQI_Target`
- **Models:** Linear Regression, Random Forest Regressor (n_estimators=100, random_state=42), 80/20 train-test split
- **Results:** Linear Regression RMSE 0.1713, R² 0.9997 (best); Random Forest RMSE 0.2466, R² 0.9995
- **Key finding:** PM2.5 is the dominant driver of AQI (~88% feature importance)

## Project structure
```
index.html    # the whole site (HTML + CSS + JS, no dependencies)
favicon.svg
vercel.json   # Vercel config
README.md
```

## Run locally
No build step. Open `index.html` in a browser, or run a local server:
```
python3 -m http.server 8000
```
then visit http://localhost:8000

## Deploy
**GitHub Pages:** repo Settings → Pages → Deploy from branch → `main` / root.
**Vercel:** import the GitHub repo at vercel.com/new, Framework Preset "Other", leave build settings empty, then Deploy.
