# Sales Data Cleaning — Python & Pandas

## Project Overview
This project demonstrates an end-to-end data cleaning workflow using Python (Pandas) on a real-world sales dataset. It highlights data preprocessing, anomaly detection, and transformation techniques required for analytics-ready datasets.

## Key Highlights
- Cleaned 262 raw rows into 254 structured records
- Removed duplicates and incorrect entries
- Standardized categorical variables
- Converted all columns to appropriate data types
- Prepared dataset for analysis and visualization

## Tools & Technologies
- Python 3
- Pandas
- Matplotlib
- Seaborn
- Google Colab

## Dataset Details
- File: Sales-Data-Analysis.xlsx
- Rows: 262 → 254 (after cleaning)
- Columns: 10 → 9
- Domain: Food-service sales data

## Data Cleaning Steps
1. Removed empty columns
2. Fixed column headers
3. Cleaned inconsistent text values
4. Removed duplicate records
5. Identified and removed outliers
6. Converted data types
7. Parsed date column

## Final Dataset Schema
- Order ID (int)
- Date (datetime)
- Product (string)
- Price (float)
- Quantity (int)
- Purchase Type (string)
- Payment Method (string)
- Manager (string)
- City (string)

## Key Learnings
- Importance of structured preprocessing
- Handling real-world messy data
- Detecting anomalies manually and programmatically
- Ensuring data consistency before analysis

## Usage
1. Open the notebook in Google Colab
2. Upload dataset
3. Run all cells

## Project Structure
- Data_Cleaning.ipynb
- Sales-Data-Analysis.xlsx
- Sales_Data_Cleaning_Report.pdf
- README.md

## Author
Prepared as a portfolio project for Data Analyst role.
