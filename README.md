# Fuel Efficiency Predictor Machine Learning on Maritime Data
End-to-end ML pipeline for predicting ship fuel usage across Nigerian sea routes. Features data cleaning, label encoding, train-test split, and multi-model evaluation with Decision Tree as best performer.


**Overview**
The Ship Fuel Efficiency dataset is a structured tabular dataset containing 1,440 voyage-level records collected from ships operating across Nigerian maritime routes. It captures real-world operational, environmental, and mechanical data for multiple vessel types across all 12 months of the year. The primary objective of this dataset is to enable predictive modeling of fuel consumption, making it valuable for fleet management optimization, cost reduction analysis, and environmental impact studies.


**Dataset Dimensions**
Rows: 1,440 | Columns: 10 | Missing Values: None | Duplicates: None

**Features Breakdown**
Ship Identifiers

ship_id — A unique alphanumeric code assigned to each vessel (e.g., NG001, NG120). Ranges across 120 ships, each recorded across multiple months and routes.
ship_type — The operational classification of the vessel. Includes types such as Oil Service Boat and Fishing Trawler, each with distinctly different fuel consumption profiles.

Route & Time Information

route_id — The named shipping route for the voyage, covering Nigerian waterways such as Warri-Bonny, Port Harcourt-Lagos, and Lagos-Apapa. Route directly influences distance and sea conditions.
month — The calendar month of the voyage (January through December), capturing seasonal patterns that affect weather and operational decisions.

Operational Metrics

distance — The total distance traveled in kilometers for that voyage. Ranges from 20.08 km to 498.55 km, with a mean of 151.75 km. This is one of the strongest drivers of fuel consumption.
fuel_type — The type of fuel used, either HFO (Heavy Fuel Oil) or Diesel. HFO is cheaper but heavier and more polluting; Diesel is cleaner but more expensive.
engine_efficiency — The percentage efficiency of the ship's engine during the voyage, ranging from 70.01% to 94.98%. Lower efficiency means the engine burns more fuel to produce the same output.
weather_conditions — Categorical description of sea and weather conditions during the voyage: Calm, Moderate, or Stormy. Stormy conditions significantly increase fuel burn due to wave resistance and engine strain.

Target Variable

fuel_consumption — The total fuel consumed during the voyage in liters. This is the prediction target. Values range from 237.88 to 24,648.52 liters, with a mean of 4,844.25 and a high standard deviation of 4,892.35 — reflecting the wide variability driven by ship type, distance, and weather.

Dropped Column

CO2_emissions — Carbon dioxide output calculated directly from fuel consumption using a fixed emission factor. This column was removed during preprocessing to prevent data leakage, as it is mathematically derived from the target variable and would give the model an unfair informational advantage.


Key Statistical Highlights
FeatureMinMeanMaxDistance (km)20.08151.75498.55Fuel Consumption (L)237.884,844.2524,648.52Engine Efficiency (%)70.0182.5894.98

Why This Dataset is Valuable

Real-world domain — Maritime shipping is a major global industry and fuel costs represent up to 60% of operating expenses for ship operators.
Multi-factor complexity — Fuel consumption is influenced by a combination of distance, vessel type, weather, fuel type, and engine health, making it a rich regression problem.
Clean & complete — Zero nulls and zero duplicates make it immediately usable without heavy preprocessing.
Balanced size — At 1,440 records, it is large enough to train generalizable models yet small enough for rapid experimentation.
Practical applications — Predictions from models trained on this data can directly feed into route optimization systems, maintenance scheduling, and carbon footprint tracking tools.
