# Spatio-Temporal Analysis of Road Traffic Crashes in Kenya (2017–2018)

This repository contains the code, data, and documentation for a comprehensive spatio‑temporal and severity analysis of road traffic accidents in Kenya. The study leverages geo‑referenced crash reports from crowdsourced and open data sources to identify accident hotspots, temporal patterns, and key factors associated with fatal outcomes. The analysis was conducted as part of an undergraduate thesis in Applied Statistics with Computing at Moi University.

---

## 📌 Overview

Road traffic accidents remain a critical public safety issue in Kenya, causing significant fatalities, injuries, and economic losses. This project aims to:

- Map the spatial distribution of crashes and identify high‑risk hotspots.
- Examine temporal trends by hour, day of week, and month.
- Assess the relationship between road user type (pedestrians, motorcyclists, matatus) and crash severity.
- Determine factors that significantly increase the likelihood of fatal crashes using correlation and regression models.
- Provide evidence‑based recommendations for targeted road safety interventions.

---

## 📊 Data Source

The analysis uses secondary crash data obtained from:

- **World Bank Open Data** (Kenya country profile)  
- Crowdsourced reports from **Ma3Route** (2017–2018)

The dataset includes **2,595 geo‑referenced crash records** with variables such as:

- Geographic coordinates (latitude, longitude)
- Date and time of occurrence
- Road user involvement (pedestrian, motorcyclist, matatu)
- Crash severity (fatal / non‑fatal)
- Number of reports per incident

> **Note:** The raw data is not included in this repository due to licensing and privacy considerations. Processed aggregates and code are provided.

---

## 🧠 Methodology

### 1. Descriptive Analysis
- Frequency distributions of crashes by severity, road user category, time, and location.

### 2. Temporal Analysis
- Hourly, daily, and monthly patterns visualised with line and bar charts.

### 3. Spatial Analysis
- **Hotspot mapping** using kernel density estimation and interactive Folium maps.
- Identification of crash clusters in urban areas (Nairobi, Mombasa, Kisumu) and along major highways.

### 4. Statistical Modeling
- **Correlation analysis** (Pearson) to explore relationships among variables.
- **Logistic regression** to model the probability of fatal crashes.
- **Poisson** and **Negative Binomial regression** to analyse crash counts, accounting for overdispersion.

All analyses were performed in **Python** using libraries such as `pandas`, `numpy`, `matplotlib`, `seaborn`, `folium`, `statsmodels`, and `scikit-learn`.

---

## 🔍 Key Findings

- **Non‑fatal crashes** constitute the majority of reported incidents, but **fatal crashes** remain a serious concern.
- **Pedestrians** and **motorcyclists** face significantly higher odds of fatal outcomes (OR ≈ 8.7 and 4.0 respectively) – highlighting their vulnerability.
- **Matatu‑related crashes** are frequent but generally non‑fatal; they are not statistically associated with higher fatality risk after controlling for other factors.
- **Temporal peaks** occur during morning (6–8 AM) and evening (4–7 PM) rush hours, and on Fridays.
- **Spatial hotspots** are concentrated in urban centres and along major transport corridors (e.g., Nairobi–Mombasa highway).
- Negative Binomial regression confirms that pedestrian and matatu involvement significantly increase crash counts, while motorcycle involvement is not significant in the final model.

---

## 🗺️ Interactive Hotspot Map

An interactive HTML map showing accident hotspots across Kenya is included in the repository:  
📁 [`accidents_hotspots.html`](accidents_hotspots.html)  
*Click on the map to explore clusters of crashes.*

---

## 🛠️ Technologies Used

- **Python 3.8+**
- Pandas, NumPy – data manipulation
- Matplotlib, Seaborn – visualisation
- Folium – interactive maps
- Statsmodels, Scikit‑learn – statistical modelling
- Jupyter Notebook – development environment

---

## 📁 Repository Structure
