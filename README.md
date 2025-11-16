# Carbon Emission Predictor for Commercial Transport Vehicles

A machine learning model that predicts CO₂ emissions of cargo/goods-carrying vehicles based on key parameters like engine size, fuel type, vehicle weight, and transmission. The Model has an R² score of 0.90970 in predicting CO₂ emissions after cleaning and training on the dataset only for Freight, Cargo carrying commercial vehicles.

---

## What It Does

- Takes vehicle-specific data as input  
- Predicts estimated **CO₂ emissions in grams/km**  
- Helps in assessing environmental impact and fuel efficiency

---

## Key Features

- Data preprocessing and feature engineering  
- Exploratory Data Analysis (EDA)  
- Model training using regression algorithms  
- Exported trained model (`carbon_model.pkl`)  
- Prediction-ready pipeline

---

## Files Included

- `Carbon_Emission_Predictor.ipynb` – Full project notebook  
- `carbon_model.pkl` – Trained model (exported using pickle)  
- `vehicle_data.csv` – Dataset (if included)  
- `README.md` – Project description  
- `requirements.txt` – Dependencies

---

## Setup Instructions

```bash
git clone https://github.com/YourUsername/Carbon-Emission-Predictor.git
cd Carbon-Emission-Predictor
pip install -r requirements.txt
```

---

## Sample Prediction Code

```python
import pickle
import pandas as pd

# Load model
model = pickle.load(open('carbon_model.pkl', 'rb'))

# Sample input
data = {
    'EngineSize': 3.5,
    'FuelType': 'Diesel',
    'VehicleWeight': 2500,
    'Transmission': 'Manual'
}

df = pd.DataFrame([data])
prediction = model.predict(df)[0]
print(f"Estimated CO₂ Emission: {round(prediction)} g/km")
```

---

## Built With

- Python, Pandas, NumPy  
- scikit-learn  
- Matplotlib & Seaborn  
- Pickle
