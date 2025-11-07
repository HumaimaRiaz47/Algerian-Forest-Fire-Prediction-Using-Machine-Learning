# 🌲 Algerian Forest Fire Prediction – End-to-End Machine Learning Project

This project predicts the **fire risk percentage** for the Algerian forest regions using environmental and meteorological data.  
It’s a complete end-to-end pipeline — from **data preprocessing and model training** to a **Flask web application**.

---

## 🚀 Project Overview

The **Algerian Forest Fire Dataset** contains environmental attributes like temperature, humidity, and wind speed to help predict forest fire occurrences.  
Using regression models, this project estimates the likelihood (in %) of a fire occurring based on the given inputs.

---

## 🧠 Machine Learning Pipeline

### 1️⃣ Data Collection
The dataset was obtained from the **UCI Machine Learning Repository**.  
It includes meteorological data from two regions of Algeria — **Bejaia** and **Sidi Bel-Abbès**.

### 2️⃣ Data Preprocessing
- Handled missing values  
- Cleaned and standardized data  
- Encoded categorical features (`Region`, `Classes`)  
- Applied feature scaling using `StandardScaler`

### 3️⃣ Exploratory Data Analysis (EDA)
- Visualized feature correlations  
- Identified outliers and trends  
- Checked multicollinearity between features  

### 4️⃣ Feature Engineering
- Selected key predictors influencing fire risk:  
  **Temperature, RH, Ws, Rain, FFMC, DMC, ISI, Classes, Region**
- Performed feature scaling (standardization)

### 5️⃣ Model Training
The following models were trained and evaluated:
- 🔹 **Linear Regression**
- 🔹 **Lasso Regression**
- 🔹 **LassoCV**
- 🔹 **Ridge Regression**
- 🔹 **RidgeCV**

 The **Ridge Regression model** gave the best performance and was saved as a `.pkl` file for deployment.

### 6️⃣ Model Serialization
Two pickle files were created:
- `ridge_model.pkl` → Trained Ridge Regression model  
- `scaler.pkl` → StandardScaler object for input scaling

---

## 🌐 Flask Web Application

The Flask web app allows users to input environmental parameters and get the **predicted fire risk percentage** instantly.

### 🖼️ Pages
- `index.html` → <img width="691" height="477" alt="Screenshot 2025-11-07 173822" src="https://github.com/user-attachments/assets/7ac52901-86b6-4fd6-8b72-97f3e6e576ba" />

- `home.html` → <img width="711" height="904" alt="Screenshot 2025-11-07 173744" src="https://github.com/user-attachments/assets/7e400d4c-6e87-446b-afb4-5c3ad83750d5" />
 
- `result.html` → <img width="786" height="492" alt="Screenshot 2025-11-07 173837" src="https://github.com/user-attachments/assets/c023b29d-338c-4be1-8c0f-4a60a145da36" />

### 📊 Input Features
| Feature | Description |
|----------|--------------|
| Temperature | Air temperature (°C) |
| RH | Relative Humidity (%) |
| Ws | Wind Speed (km/h) |
| Rain | Rainfall (mm/m²) |
| FFMC | Fine Fuel Moisture Code |
| DMC | Duff Moisture Code |
| ISI | Initial Spread Index |
| Classes | Fire occurrence class (1 = Fire, 0 = No Fire) |
| Region | Region of Algeria (1 = Bejaia, 2 = Sidi Bel-Abbès) |

---

