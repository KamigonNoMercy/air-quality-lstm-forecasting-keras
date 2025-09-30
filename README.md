# 🌫️ Air Quality Multivariate Forecasting (Keras LSTM)

This project focuses on **hourly air-quality time series forecasting** using deep learning with **Keras LSTM**.  
The goal is to leverage historical multivariate data (pollutants + weather parameters) to predict future air quality and environmental variables.

---

## 🎥 Analysis Video
Watch the analysis walkthrough here:  
👉 https://drive.google.com/file/d/13Ox57iTmJrIrgjGp9O3NhMoGaxe30TSk/view?usp=sharing

---

## 📊 Dataset

The dataset contains **multivariate air-quality measurements** recorded **hourly** at a monitoring station.  

### Features include:
- **Pollutants**: PM2.5, PM10, NO₂, CO, SO₂  
- **Weather**: Temperature (°C), Relative Humidity (RH), Wind Speed (WS)  
- **Datetime**: `From Date` (used to derive sequential input windows)  

Each row corresponds to one hour of measurement. Because of the sequential structure, the dataset is well-suited for **time-series forecasting**.
You can access the dataset here:
https://drive.google.com/file/d/1NMLKgRSjXyuNwt0Rb_lTinx6jSyBdnbB/view?usp=drive_link

---

## ✨ Highlights

- **Exploratory Data Analysis (EDA)**: Trend analysis of pollutants & weather features.
- **Preprocessing**:  
  - Timestamp parsing & sorting.  
  - Scaling with `MinMaxScaler` / `StandardScaler`.  
  - Sliding-window sequence builder (`n_timesteps × n_features`).  
- **Model**:  
  - Baseline **LSTM (Sequential Keras)** with input shape `(timesteps, features)`.  
  - Example: 1 LSTM layer (10 hidden units) + Dense regression output.  
- **Training Setup**:  
  - Optimizer: `Adam`  
  - Loss: `MSE`  
  - Metrics: `MAE`, `R²`  
  - EarlyStopping callback to avoid overfitting.  
- **Evaluation**:  
  - Reported metrics: MAE, MSE, R² score.  
  - Visual comparison of predicted vs actual values.  

---

## 📂 Repository Layout
```
air-quality-lstm-forecasting-keras/
├─ notebook/
│ └─ air-quality-lstm-forecasting.ipynb # main notebook
├─ README.md # project description
├─ requirements.txt # dependencies
├─ LICENSE
└─ .gitignore
```
---

## 🛠 Environment

Install dependencies:
```bash
pip install -r requirements.txt
```
---

## 🚀 Run the Notebook
```
jupyter notebook notebook/air-quality-lstm-forecasting.ipynb
```



