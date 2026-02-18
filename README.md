# 🌍 Disaster Affected Region Tracker — ETL & SQL-First Analysis

An end-to-end **ETL + SQL-first data analytics project** that processes raw disaster datasets and generates actionable insights for disaster management and policy planning.

---

## 📌 Project Overview

This project builds a complete data pipeline:

**CSV → Pandas ETL → MySQL → SQL Analysis → Visualizations**

It identifies:

- Regions with the highest affected population
- Most frequent disaster types
- Disaster trends over time
- Economic loss vs human impact
- Region-wise disaster distribution

---

## 🧰 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- MySQL
- SQLAlchemy
- Jupyter Notebook

---

## ⚙️ ETL Pipeline

### 🔹 Extract
- Loaded raw CSV datasets:
  - Disaster events
  - Impact assessment
  - Regional data

### 🔹 Transform (Business Rules Applied)

- Missing disaster types → replaced with `"Unknown"`
- Invalid dates → safely converted using `to_datetime(errors="coerce")`
- Missing population → filled with median
- Missing affected people & economic loss → replaced with `0`
- Duplicate records removed
- Datasets merged into a master table
- Created time-based features:
  - `year`
  - `month`

### 🔹 Load

- Clean dataset stored in **MySQL**
- All analysis performed using **SQL queries (SQL-first approach)**

---

## 📊 SQL-First Analysis

### 📍 Region with Highest Affected Population
Identifies regions requiring priority disaster response.

### 🌪️ Most Frequent Disaster Type
Helps understand dominant disaster patterns.

### 📈 Disaster Trend Over Time
Tracks how disaster occurrences change across time.

### 💰 Economic Loss vs Affected Population
Compares financial impact with human impact.

### 🔥 Region-wise Disaster Frequency Heatmap
Shows disaster distribution across regions.

---

## 📈 Key Insights

- Region X has the highest affected population → needs priority relief planning
- Floods are the most frequent disaster type
- Disaster frequency increases after 2020
- High economic loss events are not always high population impact

---

## 🗂️ Project Structure

disaster-etl-project/
│
├── data/ → Raw datasets
├── notebooks/ → ETL & SQL analysis notebook
├── sql/ → MySQL DDL script
├── requirements.txt → Project dependencies
└── README.md


---

## 🚀 How to Run This Project

### 1️⃣ Clone the repository

```bash
git clone https://github.com/SuhasSC/Distaster_ETL_Project.git
cd disaster-etl-project


