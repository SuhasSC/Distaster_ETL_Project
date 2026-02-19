# Disaster Affected Region Tracker — ETL & SQL-First Analysis

This project implements an end-to-end ETL pipeline that processes raw disaster datasets and generates analytical insights to support disaster management and planning.

---

## Project Overview

The workflow follows a structured data pipeline:

CSV → Pandas (ETL) → MySQL → SQL Analysis → Visualizations

The analysis focuses on:

- Identifying regions with the highest affected population  
- Finding the most frequent disaster types  
- Understanding disaster trends over time  
- Comparing economic loss with human impact  
- Analyzing region-wise disaster distribution  

---

## Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- MySQL  
- SQLAlchemy  
- Jupyter Notebook  

---

## ETL Pipeline

### Extract
Raw datasets were loaded from CSV files:
- Disaster events  
- Impact assessment  
- Regional information  

### Transform (Business Rules Applied)

- Missing disaster types were replaced with `"Unknown"`  
- Invalid dates were safely converted using `to_datetime(errors="coerce")`  
- Missing population values were filled with the median  
- Missing affected people and economic loss values were replaced with `0`  
- Duplicate records were removed  
- All datasets were merged into a single master table  
- Time-based features were created (`year` and `month`)  

### Load

The cleaned dataset was stored in MySQL, and all analytical queries were performed directly using SQL.

---

## SQL-First Analysis

The analysis was intentionally performed using SQL instead of Pandas groupby operations to reflect a production-style workflow.

Key analyses include:

- Region with the highest affected population  
- Most frequent disaster type  
- Disaster trend over time  
- Economic loss vs affected population  
- Region-wise disaster frequency heatmap  

---

## Key Insights

- One region shows significantly higher affected population and should be prioritized for relief planning  
- Floods are the most frequent disaster type in the dataset  
- Disaster occurrences show an increasing trend after 2020  
- High economic loss does not always correspond to high human impact  

---

## Project Structure

disaster-etl-project/
│
├── data/ → Raw datasets
├── notebooks/ → ETL & SQL analysis notebook
├── sql/ → MySQL DDL script
├── requirements.txt → Project dependencies
└── README.md


---

---

## How to Run the Project

1. Clone the repository

```bash
git clone https://github.com/SuhasSC/Distaster_ETL_Project.git
cd disaster-etl-project


