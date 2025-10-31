---

## ⚡ Electric Vehicle (EV) Analysis

### 📘 Overview

This project performs a comprehensive **data analysis of Electric Vehicles (EVs)** 
It aims to uncover trends, adoption patterns, and market insights for EV manufacturers, models, and electric range performance.

The analysis helps policymakers, manufacturers, and researchers understand **EV adoption dynamics**, and serves as a practical demonstration of **data cleaning, visualization, and exploratory data analysis (EDA)** in Python.

---

## 🎯 Objectives

* Analyze **EV registration data** and identify trends over years.
* Determine **top EV manufacturers and models**.
* Explore **electric range distribution** and its relation with model year.
* Visualize **geographical distribution** and **CAFV eligibility patterns**.
* Handle missing values and prepare a clean dataset for further ML modeling.

---

## 🧩 Project Pipeline

### **1. Data Collection**

* Source: Washington State Department of Licensing – Electric Vehicle Population Data.
* Format: CSV file containing EV details (VIN, Make, Model, Range, Utility Provider, etc.).

### **2. Data Cleaning & Preprocessing**

* Checked for missing/null values.
* Imputed missing `Electric Range` using the mean value.
* Filled missing `Model Year` using the mode.
* Dropped or imputed other missing categorical fields where necessary.
* Removed redundant or highly missing columns like `Legislative District`.

### **3. Exploratory Data Analysis (EDA)**

* Univariate and bivariate analysis to identify EV trends.
* Visualization using **Matplotlib** and **Seaborn**:

  * Top 10 EV Manufacturers
  * Electric Range vs. Model Year
  * CAFV Eligibility Distribution
  * EV count by County and City

### **4. Insights Extraction**

* Identified the **most popular EV brands** (e.g., Tesla, Nissan, Chevrolet).
* Observed that **newer models** tend to have a **higher electric range**.
* Highlighted that **urban regions** show higher EV concentration.

### **5. Visualization**

* Created clean, modern bar plots and distribution charts.
* Used `viridis` and `coolwarm` palettes for better readability.
* Added meaningful titles, axis labels, and annotations.

---

## 📊 Key Findings

* **Tesla** dominates the EV market share in Washington State.
* **Electric range** has increased significantly over the years.
* Majority of vehicles are **fully electric (BEVs)** rather than plug-in hybrids.
* **CAFV eligibility** correlates strongly with newer EV models.

---

## ⚙️ Tech Stack

| Category          | Tools / Libraries          |
| ----------------- | -------------------------- |
| Language          | Python 3.x                 |
| Data Handling     | pandas, numpy              |
| Visualization     | matplotlib, seaborn        |
| IDE / Environment | Jupyter Notebook / VS Code |

---

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/EV-Analysis.git
   ```
2. Navigate to the project folder:

   ```bash
   cd EV-Analysis
   ```
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
4. Run the notebook:

   ```bash
   jupyter notebook EV_Analysis.ipynb
   ```

---

## 📚 Literature Review Summary

Recent studies highlight the **growing global transition towards EVs**:

* EV adoption is primarily influenced by **government incentives**, **charging infrastructure**, and **technological improvements** (Li et al., 2022).
* Data-driven analysis helps predict **EV demand** and **battery efficiency** trends.
* Similar datasets are used worldwide for **policy-making and forecasting EV growth** (Zhang et al., 2023).

This project contributes by providing a **state-level exploratory analysis**, demonstrating how public datasets can uncover **real-world EV adoption patterns**.

---

## 💡 Future Work

* Integrate **geospatial visualization (Plotly, Folium)** for EV location mapping.
* Build a **machine learning model** to predict electric range based on features.
* Compare EV adoption trends across multiple states.

---

## 👨‍💻 Author

**Chandan**
B.Tech CSE | Guru Nanak Dev Engineering College, Ludhiana
[GitHub](https://github.com/chandan-911) | [LinkedIn](https://www.linkedin.com/in/chandan-m911/)
---
