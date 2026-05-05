# 🚢 Ship Fuel Efficiency Dataset

> A machine learning dataset capturing 1,440 voyage-level records from ships
> operating across Nigerian maritime routes — built for fuel consumption prediction.

---

## 📊 Dataset at a Glance

| Property | Value |
|---|---|
| Total Records | 1,440 |
| Total Features | 10 |
| Missing Values | None |
| Duplicates | None |
| Target Variable | `fuel_consumption` |
| Task Type | Regression |

---

## 📁 Features Breakdown

### 🔹 Identifiers
| Column | Type | Description |
|---|---|---|
| `ship_id` | string | Unique vessel code (e.g., NG001, NG120) |
| `ship_type` | string | Vessel class (Oil Service Boat, Fishing Trawler, etc.) |

### 🔹 Route & Time
| Column | Type | Description |
|---|---|---|
| `route_id` | string | Named shipping route (e.g., Warri-Bonny, Lagos-Apapa) |
| `month` | string | Calendar month of the voyage |

### 🔹 Operational Metrics
| Column | Type | Description |
|---|---|---|
| `distance` | float64 | Distance traveled in kilometers |
| `fuel_type` | string | Fuel used — HFO or Diesel |
| `engine_efficiency` | float64 | Engine efficiency as a percentage |
| `weather_conditions` | string | Sea conditions — Calm, Moderate, or Stormy |

### 🎯 Target Variable
| Column | Type | Description |
|---|---|---|
| `fuel_consumption` | float64 | Total fuel consumed in liters |

### ❌ Dropped Column
| Column | Reason |
|---|---|
| `CO2_emissions` | Removed — mathematically derived from target (data leakage) |

---

## 📈 Key Statistics

| Feature | Min | Mean | Max |
|---|---|---|---|
| Distance (km) | 20.08 | 151.75 | 498.55 |
| Fuel Consumption (L) | 237.88 | 4,844.25 | 24,648.52 |
| Engine Efficiency (%) | 70.01 | 82.58 | 94.98 |

---

## 🤖 Models Evaluated

| Model | Test R² | MAE |
|---|---|---|
| Linear Regression | 0.9134 | 1,159.48 |
| Decision Tree | **0.9271** | **804.33** |
| Lasso Regression | 0.9134 | 1,159.45 |
| Ridge Regression | 0.9134 | 1,159.48 |

> ✅ **Best Model: Decision Tree Regressor** — highest R² and lowest MAE,
> thanks to its ability to capture non-linear relationships between
> distance, weather, ship type, and fuel usage.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

---

## 💡 Why This Dataset?

- 🌍 **Real-world domain** — Fuel costs represent up to 60% of ship operating expenses
- 🔀 **Multi-factor complexity** — Distance, weather, engine health, and vessel type all interact
- ✅ **Clean & complete** — Zero nulls, zero duplicates, ready to use
- 📦 **Balanced size** — Large enough to generalize, small enough to iterate fast
- 🎯 **Practical impact** — Predictions can feed route optimization and carbon tracking systems

---

## 📂 Project Structure

```
ship-fuel-efficiency/
│
├── ship_fuel_efficiency.csv   # Raw dataset
├── ship_fuel.ipynb            # Full analysis notebook
└── README.md                  # This file
```

```python
```



**For a more detailed explanation of this project, please review the accompanying DOCX document.**

[📄 Comparative_ML_Study] -> ship_fuel_analysis.docx)

## ⭐ Give a star if you like this project!
