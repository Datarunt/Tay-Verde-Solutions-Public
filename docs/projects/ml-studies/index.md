---
title: ML Studies
layout: default
---

# ML Studies

This section highlights my machine learning research, experiments, and exploratory notebooks that support my applied projects (Delivery Forecasting, Mold Risk Prediction, Farm Route Optimization, and more).

These studies live in my **private development repo** and include:
- Regression benchmarking (Linear Regression, etc)
- Error metric comparisons (RMSE vs MAE vs MBE)
- Feature engineering prototypes
- Time-series forecasting experiments
- Data cleaning and EDA workflows

## Topics Included

### 1. Regression Models
- Naive
- Moving Average
- Basic Linear Regression  
- Exponential Smoothing
- ARIMA
- Prophet
- Error analysis: RMSE, MAE, MBE 

### 2. Time Series Experiments
- Rolling averages  
- Lag features  
- Simple forecasting baselines  

### 3. EDA Notebook Patterns
- Data cleaning
- Correlation mapping
- Outlier detection
- Trend and seasonality inspection
- Quick prototype visualizations

# Machine Learning Use Cases in Logistics

- **Smarter Demand Forecasting**  
  Machine learning models can predict order volumes, inventory needs, and labor requirements with greater accuracy, reducing shortages and excess inventory.

- **Optimized Routing and Network Planning**  
  Algorithms can generate efficient delivery routes and load plans in real time, lowering transportation costs and improving delivery reliability.

- **Predictive Asset Maintenance**  
  Machine learning can unconver early indicators of equipment or fleet failure, minimizing downtime and increasing overall operational resilience.

- **Intelligent Warehouse Automation**  
  Machine learning optimizes picking strategies, predicts optimal slotting, flags anomalies in order flow, and coordinates automated systems to improve accuracy and accelerate fulfillment.

# Delivery Risk Forecasting — What ML Predicts in Logistics

Modern delivery logistics uses machine learning to anticipate **when**, **where**, and **why** delays happen. Models blend weather, traffic, market conditions, and operational history to produce forward-looking risk signals.

## What ML Commonly Predicts

### 1. **Delivery Delay Risk Classification**
Predict whether the coming week is **Low / Medium / High** risk for delivery disruption, based on:

- Weather severity (rain, wind, storms)  
- Market pressure (AMS volume, volatility)  
- Road incidents & closures (Bay Area open data)  

This is the **primary output** of your V1 delivery-risk model.

---

### 2. **Probability of Delivery Delay (Numeric Score)**
A numeric **0–1 probability** that conditions will cause a delay.

Useful for:

- Dashboards  
- Ranking weekly delivery windows  
- Future ML models (regression or classification)

---

### 3. **Weather-Driven Disruption Risk**
A sub-score derived entirely from **NOAA weather data**, including:

- Expected precipitation  
- Wind speeds  
- Severe weather events  

This matters especially for **small farmers transporting perishables**.

---

### 4. **Market & Network Pressure Forecasting**
Uses **USDA AMS** + **regional incident data** to estimate:

- Expected volume surges  
- Demand/supply tightness  
- Congestion likelihood  
- Infrastructure or market-driven strain  

This captures the **macro-pressure environment** that raises delivery risk even when the weather is clear.

## Why This Matters for Small Farmers
Machine-learning forecasting helps small farms:

- Anticipate weather-driven delays  
- Adjust harvest/packaging windows  
- Plan routes around closures/incidents  
- Identify pricing or volume pressure weeks  
- Improve coordination with buyers and markets  

Even **simple, weekly risk models** deliver meaningful ROI without expensive infrastructure.

---

## What This Project supports

This repository implements a **beginner-friendly, weekly delivery-risk predictor** using:

- **NOAA weather data**  
- **USDA AMS market signals**  
- **Bay Area open-data incidents**

With:

- A **Postgres schema**  
- **Weekly ingestion scripts**  
- A **simple rule-based risk scoring model**  
- **Prediction vs. actual validation**

This serves as the foundation for adding real ML forecasting later (regression, classification, time-series models).

---

## Top 3 Prediction Targets

To keep the delivery-risk project simple, interpretable, and aligned with a weekly ingestion pipeline, the model focuses on three core prediction targets:

### 1. **Delivery Risk Level (Low / Medium / High)**
- A categorical signal summarizing expected delivery difficulty for the upcoming week.
- **Examples:**
  - **Low:**  
    Sunny week, normal market volume, no planned road closures → deliveries run smoothly.
  - **Medium:**  
    Light rain and moderate wind, plus a minor construction closure on a key route → some delays possible.
  - **High:**  
    Heavy storms forecast + high AMS market pressure + multiple Bay Area incident reports → high likelihood of late or rerouted deliveries.
    
- This is easy for farmers and buyers to understand and works well for dashboards and alerts.

### 2. **Probability of Delivery Delay (numeric)**
- A quantitative estimate (0–1 or 0–100%) representing the likelihood of a late or disrupted delivery.
- **Examples:**
  - **0.15(15%)** – Mostly clear weather; only minor congestion expected.
  - **0.42(42%)** – Rain predicted mid-week + increased shipment volume → moderate chance of delays.
  - **0.78(78%)** – Severe weather incoming + low supply elasticity + multiple Bay Area incidents → strong risk of late deliveries.

- This enables thresholding, benchmarking, and future ML model calibration.

### 3. **Weather-Driven Disruption Risk Score**
- A continuous score derived from NOAA forecasts (precipitation, wind, severe weather counts).
- - **Examples:**
  - **0.10** – Light clouds, minimal wind, no precipitation.
  - **0.55** – 0.5–1 inch of rain expected + 20–30 mph winds.
  - **0.90** – Multi-day storm system with >2 inches of rainfall, high winds, and NOAA severe weather advisories.
    
- Weather is the strongest driver of small-farm delivery disruption, making this a critical feature.

### Why These Three?
- **Interpretability** — Farmers and buyers can make fast decisions.  
- **Quantitative insights** — Numeric scores support automation and monitoring.  
- **ML-ready foundation** — These map cleanly to regression/classification models later.  
- **Natural weekly cadence** — Perfect alignment with NOAA, USDA AMS, and Bay Area open-data refresh cycles.

These three targets strike the right balance between **simplicity**, **actionability**, and **technical depth**, forming the backbone of the delivery-risk forecasting system.


---

## Code Availability
These studies live in my private repo as ongoing work.  
I can provide walkthroughs or excerpts on request.
