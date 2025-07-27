# 🌍 Global Terrorism Trend Analysis (1970–2017)

## 📌 Project Overview

This project analyzes over 180,000 global terrorist incidents from **1970 to 2017** to identify trends, patterns, and changes in the **scale and frequency of attacks** over time. Using data from the **Global Terrorism Database (GTD)**, we examine incident severity, apply **categorical classification**, and build **scatter plots and linear regression models** to understand how terrorism has evolved.

---

## 🧠 Objective

To explore, categorize, and visualize terrorist incidents using historical data in order to:
- Detect trends in **minor**, **small**, and **major** attacks  
- Understand global shifts in terrorism patterns  
- Use **linear regression** to project escalation or decline in attacks over time

---
## 📊 Dataset Description

- **Source:** Kaggle (originally compiled by START, University of Maryland)
- **Rows:** ~181,000 incidents  
- **Time Range:** 1970–2017  
- **Attributes:**  
  - Date, Year, Country, Region, City  
  - Attack Type, Target Type, Weapon Type  
  - Casualties, Coordinates, Motive, Perpetrator group

---

## 🧹 Data Preprocessing

- Created new feature: `attack_type` using `pd.cut()`  
  - **Minor:** 0–2 casualties  
  - **Small:** 3–10 casualties  
  - **Major:** >10 casualties  
- Removed rows with missing values using `dropna()`  
- Selected relevant columns: `iyear`, `attack_type`, `nkill`  
- Cleaned dataset used for grouped visualizations and trend analysis

---

## 📈 Analysis Summary

### ✅ **Scatter Plots by Severity**
- Yearly frequency plotted for **major**, **small**, and **minor** attacks  
- Combined view shows growth in all types, especially **minor** incidents post-2000  
- Notable spikes around early 1980s, 2000s, and early 2010s

### ✅ **Trend Shifts**
- Plotted changes in number of attacks year-to-year using `diff()`  
- Helped highlight **periods of global conflict escalation** or political instability

### ✅ **Linear Regression Modeling**
- Built separate regression models for:
  - **All attacks**
  - **Minor, Small, and Major attacks individually**
- Found consistent upward trend:
  - Minor Attacks: +59.63 per year  
  - Small Attacks: +30.28 per year  
  - Major Attacks: +8.83 per year  
- Total attacks: ~+180/year on average (overall linear coefficient)

---

## 🔍 Key Insights

- **Minor attacks** increased steadily post-2000  
- **Small attacks** peaked mid-90s and early 2010s  
- **Major attacks** showed fluctuation but also trended upward after 2000  
- The dataset reflects how terrorism evolved in tactics, scale, and frequency over 5 decades

---

## 🛠 Tools Used

- Python  
- Pandas  
- Matplotlib  
- Scikit-learn (`LinearRegression`)  
- Jupyter Notebook

---
