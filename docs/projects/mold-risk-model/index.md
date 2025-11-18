---
title: Mold Risk Model
layout: default
---

# Mold Risk Model

A machine learning project designed to predict mold risk in microgreens using environmental sensor data collected from IoT devices.

This project lives in my **private development repo** and includes:
- ESP32 + Raspberry Pi sensor pipeline
- Temperature, humidity, and light intensity ingestion
- Logistic regression baseline model
- Rule-based “mold likely tomorrow” indicator
- Iterative grow-cycle learning and retraining

## Problem Statement
Microgreen growers often face mold contamination due to:
- High humidity
- Poor airflow
- Inconsistent light exposure

Early prediction allows growers to:
- Adjust airflow
- Increase light intensity
- Intervene before mold forms

## Data & Features
Features used in early versions include:
- Temperature (°F)
- Humidity (%)
- Light intensity (lux)
- Daily deltas + rolling averages

## Model Overview
- Logistic regression baseline
- Comparison with rule-based triggers
- Future enhancements: random forest, XGBoost, time-series modeling

## Results Summary
*(You can add charts, tables, or images from your private repo later.)*

## Code Availability
Full source code remains private due to active development,  
but I can provide specific components or walkthroughs on request.
