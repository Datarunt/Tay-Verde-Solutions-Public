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

### 1. Delivery Time Predictions
- ETA forecasting (minutes or hours)  
- Probability a delivery will be late  
- Time-of-day congestion patterns  
- Per-route or per-driver travel times  

### 2. Delay Risk Classification
- “Low / Medium / High” delay risk  
- Weather-driven disruptions  
- Traffic bottlenecks  
- Volume surges straining capacity  

### 3. Route & Network Bottleneck Detection
- Roads or regions likely to jam  
- Predicted travel-time spikes  
- Infrastructure strain by day/time  

### 4. Demand & Volume Forecasting
- Expected load per day/week  
- Anticipated surges slowing transport  
- Inbound/outbound freight pressure  

### 5. Capacity & Resource Forecasting
- Required trucks, drivers, or labor  
- Peaks where capacity will fail  
- Warehouse/fulfillment throughput  

### 6. Risk Scoring for Operations
- Weather risk score  
- Market/supply tightness score  
- Road network disruption score  
- Composite delivery-risk score  

### 7. Exception / Event Predictions
- Likelihood of manual intervention  
- Probability of reroutes  
- Spoilage risk for perishables  

---

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

## Code Availability
These studies live in my private repo as ongoing work.  
I can provide walkthroughs or excerpts on request.
