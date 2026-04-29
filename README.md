# 🧹 Sales Data Cleaning — End-to-End Project (Python & Pandas)

> A complete real-world data cleaning project demonstrating structured preprocessing, anomaly detection, and transformation using Python.

---

## 🚀 Project Overview

This project focuses on cleaning a raw sales dataset from a food-service business operating across multiple European cities.  
The goal is to transform messy, inconsistent raw data into a clean, analysis-ready dataset.

---

## 📊 Project Metrics

| Metric | Value |
|--------|------|
| Raw Rows | 262 |
| Clean Rows | 254 |
| Rows Removed | 8 |
| Raw Columns | 10 |
| Final Columns | 9 |
| Cleaning Steps | 9 |

---

## 📂 Dataset Information

- **File Name:** Sales-Data-Analysis.xlsx  
- **Domain:** Food-Service Sales  
- **Cities Covered:** London, Madrid, Lisbon, Berlin, Paris  
- **Time Period:** Nov 7 – Dec 29, 2022  

---

## 🔧 Data Cleaning Workflow

### 1. Import Libraries
- pandas
- matplotlib
- seaborn

---

### 2. Data Inspection
- Dataset loaded with all columns as object type
- Identified:
  - Blank column
  - Incorrect headers
  - Data inconsistencies

---

### 3. Remove Empty Column
- Dropped `Unnamed: 0` (100% null values)

---

### 4. Fix Column Headers
- Promoted first row as header
- Removed redundant row

---

### 5. Normalize Text Data (Manager Column)
- Issue: inconsistent whitespace
- Fixed using string cleaning
- Result: 14 → 5 unique managers

---

### 6. Remove Duplicate Records
- Identified 4 exact duplicates
- Removed using `drop_duplicates()`

---

### 7. Detect & Remove Outliers
- Found duplicate Order IDs with abnormal prices (~10x higher)
- Manually validated and removed 3 incorrect rows

---

### 8. Data Type Conversion
- Order ID → int
- Price → float
- Quantity → int (handled precision)
- Other columns remain categorical

---

### 9. Date Conversion
- Converted Date column to datetime format
- Enabled time-series analysis

---

## 📁 Final Dataset Schema

| Column | Type | Description |
|--------|------|------------|
| Order ID | int64 | Unique identifier |
| Date | datetime | Transaction date |
| Product | object | Product category |
| Price | float | Unit price |
| Quantity | int | Units sold |
| Purchase Type | object | Sales channel |
| Payment Method | object | Payment type |
| Manager | object | Store manager |
| City | object | Location |

---

## 🧠 Key Learnings

- Structural issues must be fixed first
- Text inconsistencies can distort insights
- Duplicate detection requires multiple checks
- Manual validation is critical for anomalies
- Correct data types improve analysis accuracy

---

## 🛠️ Tech Stack

- Python 3
- Pandas
- Matplotlib
- Seaborn
- Google Colab

---

## 📦 Project Structure

```
Sales-Data-Cleaning/
│
├── Data_Cleaning.ipynb
├── Sales-Data-Analysis.xlsx
├── Sales_Data_Cleaning_Report.pdf
├── requirements.txt
└── README.md
```

---

## ▶️ How to Run

1. Open notebook in Google Colab  
2. Upload dataset  
3. Run all cells  

---

## ⭐ Why This Project Matters

This project demonstrates real-world data cleaning skills required for:
- Data Analyst roles
- Business Intelligence
- Market Research

---

## 👤 Author

Portfolio project prepared for Data Analyst / Business Analyst roles.
