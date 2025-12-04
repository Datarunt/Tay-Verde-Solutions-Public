
# Weekly-Updating Delivery & Routing Analytics Pipeline  
**Python · Data Engineering · APIs · Scheduling · Feature Engineering · ETA Modeling**

A lightweight, automated data pipeline that ingests real, publicly available datasets updated weekly and transforms them into actionable analytics for routing, ETA prediction, congestion analysis, and delivery forecasting.

This pipeline forms the **third pillar** of my analytics platform, alongside:

- **Farm Market Optimizer (FMO)** – route optimization & vehicle planning  
- **ML Studies** – forecasting, regression benchmarks, model selection

Its purpose is to demonstrate **industry-grade data engineering**, aligned with the same domain as my routing and ML work:  
delivery performance, routing efficiency, traffic delays, and ETA modeling.

---

## 🔍 What This Pipeline Does

Each week, the system:

- Pulls fresh transportation-related data from public APIs  
- Stores raw records with timestamps for reproducibility  
- Transforms data into delivery-focused features, such as:  
  - estimated travel speeds  
  - congestion indicators  
  - delay factors  
  - weather severity indexes  
- Produces clean datasets consumed by:  
  - **FMO** (ETA augmentation & routing metrics)  
  - **ML Studies** (real-world forecasting examples)  
- Runs on a scheduled GitHub Actions workflow  
- Publishes simple trend summaries and visuals

The pipeline is intentionally **transparent, modular, and easy to audit**—mirroring best practices used by real logistics analytics teams.

---

## 🗂 Data Sources

Datasets are chosen based on:

1. Public availability  
2. Weekly (or daily → weekly snapshot) updates  
3. Clear relevance to routing and delivery durations  

Examples include:

- **Bay Area Traffic & Congestion Data** – ideal for speed/delay modeling  
- **NOAA Weather Observations** – temperature, rain, storm severity  
- **US DOT Freight & Transit Metrics** – travel-time bottlenecks  
- **USDA Market Trends** – optional demand signals  

These datasets complement the FMO routing engine and support ML-ready feature engineering.

---

## 🏗 Architecture Overview

A classic DE-style workflow:

### **1. Ingestion Layer**
- API calls / scrapers  
- Weekly GitHub Actions schedule  
- Raw data stored in timestamped folders  

### **2. Transformation Layer**
- Normalize fields  
- Compute routing & ETA features  
- Output clean CSV/Parquet files  

### **3. Analytics Consumption**
- **FMO** uses congestion/speed signals for ETA modeling  
- **ML Studies** uses weekly features for forecasting examples  
- Streamlit or Tableau visuals highlight weekly trends  

This modular layout follows real-world logistics analytics architectures.

---

## 🧠 Why This Project Matters

This project demonstrates core skills expected of Data Engineers and ML Engineers:

- API ingestion & scheduled automation  
- Schema design & metadata management  
- Feature engineering for forecasting  
- Integration of real-world data into routing logic  
- Connecting **Data Engineering → ML → Application** layers  
- Operational awareness (scheduling, versioning, reproducibility)

It also grounds the **FMO app** in real data, giving the entire platform credibility for interviews and practical demonstrations.

---

## 📊 Deliverables Included

- Weekly-refreshed raw datasets (`/data/raw/`)  
- Clean feature datasets (`/data/clean/`)  
- Ingestion and transformation scripts  
- GitHub Actions workflow for scheduling  
- Trend visualizations  
- Architecture diagram  
- ML examples using weekly-updated data  

---
