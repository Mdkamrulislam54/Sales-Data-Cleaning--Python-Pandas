# 🧹 Sales Data Cleaning — Python & Pandas

> A complete, step-by-step data wrangling project on a real-world food-service sales dataset — built with Python, Pandas, and Google Colab.

<br/>

## 🔗 Project Files

<table>
  <tr>
    <td align="center" width="50%">
      <a href="https://github.com/Mdkamrulislam54/Sales-Data-Cleaning-in-Python/blob/e18cf7b76cb2906e0d7810ad7aec312a7d33059e/Data_Cleaning.ipynb">
        <img src="https://img.shields.io/badge/📓%20View%20Notebook-Data__Cleaning.ipynb-blue?style=for-the-badge&logo=jupyter&logoColor=white" alt="View Notebook"/>
      </a>
      <br/><sub>Full cleaning code — 9 steps, syntax-highlighted</sub>
    </td>
    <td align="center" width="50%">
      <a href="https://github.com/Mdkamrulislam54/Sales-Data-Cleaning-in-Python/blob/6ade69dbc914e449a3710b12add806ef10245afe/Sales-Data-Analysis.xlsx">
        <img src="https://img.shields.io/badge/📊%20View%20Dataset-Sales--Data--Analysis.xlsx-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white" alt="View Dataset"/>
      </a>
      <br/><sub>Raw Excel file — 262 rows × 10 columns</sub>
    </td>
  </tr>
</table>

<br/>

## 🚀 Open Directly in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Mdkamrulislam54/Sales-Data-Cleaning-in-Python/blob/e18cf7b76cb2906e0d7810ad7aec312a7d33059e/Data_Cleaning.ipynb)

> **How to run:**
> 1. Click the badge above → opens in Google Colab instantly
> 2. Upload [`Sales-Data-Analysis.xlsx`](https://github.com/Mdkamrulislam54/Sales-Data-Cleaning-in-Python/blob/6ade69dbc914e449a3710b12add806ef10245afe/Sales-Data-Analysis.xlsx) to your Colab session
> 3. `Runtime → Run all` — done ✅

---

## 📊 Dataset Overview

| Property | Detail |
|----------|--------|
| **File** | [`Sales-Data-Analysis.xlsx`](https://github.com/Mdkamrulislam54/Sales-Data-Cleaning-in-Python/blob/6ade69dbc914e449a3710b12add806ef10245afe/Sales-Data-Analysis.xlsx) |
| **Period** | November 7 – December 29, 2022 |
| **Business** | Food-service chain — 5 European cities |
| **Cities** | London · Madrid · Lisbon · Berlin · Paris |
| **Raw rows** | 262 |
| **Clean rows** | **254** |
| **Columns** | 10 raw → 9 clean |

---

## 🔧 What Was Cleaned

> Full code walkthrough → [`Data_Cleaning.ipynb`](https://github.com/Mdkamrulislam54/Sales-Data-Cleaning-in-Python/blob/e18cf7b76cb2906e0d7810ad7aec312a7d33059e/Data_Cleaning.ipynb)

| # | Issue Found | Fix Applied |
|:-:|-------------|-------------|
| 1 | Blank column `Unnamed: 0` — 100% null | `df.drop(columns='Unnamed: 0')` |
| 2 | Real headers buried in row 0 | `df.columns = df.loc[0]` → drop row 0 |
| 3 | Manager names with irregular whitespace (14 apparent → 5 real) | `.str.strip().str.replace(r'\s+', ' ', regex=True)` |
| 4 | 4 fully identical duplicate rows | `df.drop_duplicates()` |
| 5 | 3 rows with prices inflated ~10× (data-entry errors) | Manual inspection + `df.drop([65, 66, 69])` |
| 6 | All columns stored as `object` dtype | Cast → `int64` / `float64` / `datetime64[ns]` |

---

## 📁 Project Structure

```
Sales-Data-Cleaning-in-Python/
│
├── 📓 Data_Cleaning.ipynb        ← Main notebook (open in Colab)
├── 📊 Sales-Data-Analysis.xlsx   ← Raw dataset
├── requirements.txt              ← Python dependencies
└── README.md
```

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-≥1.5-150458?style=flat-square&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-≥3.5-11557c?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-≥0.12-4c72b0?style=flat-square)
![Colab](https://img.shields.io/badge/Google%20Colab-notebook-F9AB00?style=flat-square&logo=google-colab&logoColor=white)

```bash
pip install -r requirements.txt
```

---

## 📋 Final Clean Schema

```
Column           dtype              Notes
─────────────────────────────────────────────────────────────────
Order ID         int64              Unique per order
Date             datetime64[ns]     Nov 7 – Dec 29, 2022
Product          object             5 categories
Price            float64            USD, 7 distinct price points
Quantity         int64              Units sold
Purchase Type    object             Online / In-store / Drive-thru
Payment Method   object             Gift Card / Credit Card / Cash
Manager          object             5 managers (1 per city)
City             object             London, Madrid, Lisbon, Berlin, Paris
```

---

## 💡 Key Learnings

- **Structural issues first** — shifted headers and blank columns must be fixed before anything else
- **Whitespace is invisible and dangerous** — the same manager appeared as 14 unique values
- **Two-pass duplicate detection** — exact row duplicates, then same-key / different-value duplicates
- **Type conversion order matters** — `object → float → round → int` avoids floating-point remnants

---

## 🔗 Connect & Contribute

Found an improvement? Feel free to **fork**, open a **PR**, or drop a ⭐ if this helped you!

---

<p align="center">
  <i>Cleaned with ❤️ using Python 3 · Pandas · Google Colab</i><br/>
  <a href="https://github.com/Mdkamrulislam54/Sales-Data-Cleaning-in-Python/blob/e18cf7b76cb2906e0d7810ad7aec312a7d33059e/Data_Cleaning.ipynb">📓 Notebook</a> &nbsp;•&nbsp;
  <a href="https://github.com/Mdkamrulislam54/Sales-Data-Cleaning-in-Python/blob/6ade69dbc914e449a3710b12add806ef10245afe/Sales-Data-Analysis.xlsx">📊 Dataset</a>
</p>
