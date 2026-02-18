# Retail Cafe Sales Analysis Report

---

## 📋 Project Overview

This project analyzes retail cafe sales transaction data for the year 2023. The objective is to clean raw transactional data, perform exploratory data analysis (EDA), and derive actionable business insights to understand sales patterns, customer preferences, and revenue trends.

### Quick Stats

| Metric | Value |
|--------|-------|
| **Total Transactions** | 10,000 |
| **Total Revenue** | $88,952 |
| **Total Items Sold** | 30,141 |
| **Average Order Value** | $8.90 |
| **Date Range** | January - December 2023 |

### Project Structure

```
retail_dataset/
├── raw_dataset/
│   └── dirty_cafe_sales.csv                              # Original unclean data
├── cleaned_data/
│   └── Retail_dataset - Cleaned_data.csv                 # Processed transaction data
├── pivot_and_calculation/
│   └── Retail_dataset - pivot_tables_and_calculations.csv  # Summary statistics & pivots
├── dasboard/                                              # Dashboard files
├── EDA_Analysis.ipynb                                     # Exploratory Data Analysis notebook
└── README.md
```

---

## 📖 Data Dictionary

| Column Name | Data Type | Description | Example Values |
|-------------|-----------|-------------|----------------|
| **Transaction ID** | Integer | Unique identifier for each transaction | 1, 2, 3, ... |
| **Items** | String | Name of the item purchased | Coffee, Cake, Salad, Sandwich, Smoothie, Juice, Tea, Cookie, Other |
| **Quantity** | Integer | Number of items purchased in the transaction | 1, 2, 3, 4, 5 |
| **Price Per Unit** | Float | Price of a single item in USD | 1.00 - 10.00 |
| **Total Spent** | Float | Total transaction value (Quantity × Price Per Unit) | 1.00 - 50.00 |
| **Payment Method** | String | Method used for payment | Cash, Credit Card, Digital Wallet, UNKNOWN |
| **txn_loc** | String | Location where transaction occurred | In-store, Takeaway, Other |
| **Transaction Date** | String | Date of the transaction (YYYY-MM-DD format) | 2023-01-15, N/A |
| **Items Category** | String | Category classification of the item | Drinks, Food, Bakery |
| **Txn_Month** | Integer | Month extracted from transaction date (1-12, 0 for missing) | 1, 2, ..., 12, 0 |

---

## 🔧 Cleaning Notes

The raw dataset (`dirty_cafe_sales.csv`) contained significant data quality issues that required cleaning:

### Issues Identified & Resolutions

| Issue | Count/Impact | Resolution |
|-------|--------------|------------|
| **ERROR values** in Quantity/Price fields | Multiple records | Replaced with calculated values or flagged for review |
| **Missing Transaction Dates** | ~1,000+ records | Marked as "N/A", Txn_Month set to 0 |
| **Unknown Payment Methods** | 3,178 records | Retained as "UNKNOWN" for transparency |
| **Empty/Blank fields** | Various columns | Filled with appropriate defaults or "Other" |
| **Inconsistent Location values** | Mixed formats | Standardized to: In-store, Takeaway, Other |
| **Non-numeric values in numeric fields** | Quantity, Price | Cleaned and converted to proper data types |

### Data Quality Summary

- **Records with unknown payment:** 31.78% (3,178 transactions)
- **Records with missing dates:** Flagged with Txn_Month = 0
- **Records with zero quantity:** Present in dataset (edge cases)
- **"Other" categorization:** Used for uncategorized items and locations

---

## 💡 Key Insights

### 1. Revenue Performance

| Insight | Detail |
|---------|--------|
| **Top Revenue Item** | Salad ($17,320) - 19.5% of total revenue |
| **Top Category** | Drinks ($39,274) - 45.21% of total revenue |
| **Best Month** | August ($7,428) |
| **Lowest Month** | May ($6,636) |

### 2. Top Selling Items by Revenue

| Rank | Item | Revenue | % of Total |
|------|------|---------|------------|
| 1 | Salad | $17,320 | 19.5% |
| 2 | Sandwich | $13,664 | 15.4% |
| 3 | Smoothie | $13,320 | 15.0% |
| 4 | Juice | $10,509 | 11.8% |
| 5 | Cake | $10,395 | 11.7% |

### 3. Category Distribution

| Category | Revenue | Percentage |
|----------|---------|------------|
| Drinks | $39,274 | 45.21% |
| Food | $28,219 | 32.47% |
| Bakery | $19,385 | 22.31% |

### 4. Payment Method Analysis

| Payment Method | Transactions | Revenue |
|----------------|--------------|---------|
| UNKNOWN | 3,178 (31.78%) | $28,324 |
| Digital Wallet | 2,291 (22.91%) | $20,343 |
| Credit Card | 2,273 (22.73%) | $20,122 |
| Cash | 2,258 (22.58%) | $20,163 |

> **Insight:** Among known payment methods, Digital Wallet leads slightly, indicating growing adoption of contactless payments.

### 5. Location Performance

| Location | Transactions | Revenue |
|----------|--------------|---------|
| Other | 3,961 (39.61%) | $35,238 |
| Takeaway | 3,022 (30.22%) | $27,034 |
| In-store | 3,017 (30.17%) | $26,680 |

### 6. Monthly Trends

| Month | Revenue | Trend |
|-------|---------|-------|
| January | $6,788 | - |
| February | $7,356 | ↑ |
| March | $6,939 | ↓ |
| April | $7,166 | ↑ |
| May | $6,636 | ↓ (Lowest) |
| June | $6,797 | ↑ |
| July | $6,816 | ↑ |
| August | $7,428 | ↑ (Highest) |
| September | $6,814 | ↓ |
| October | $6,851 | ↑ |
| November | $7,064 | ↑ |
| December | $7,164 | ↑ |

> **Insight:** Revenue remains relatively stable throughout the year with slight peaks in February, August, and Q4.

---

## 📊 Dashboard Summaries

### Published Dashboard

🔗 **[View Interactive Dashboard on Google Sheets](https://docs.google.com/spreadsheets/d/e/2PACX-1vRJlBek2VlvYI-PUsfunqqj3kybVrFeOSrdEJCHtSgml3DBNct3s5NPZieUdhXsG_xhOwNbRQac-bB3/pubhtml)**

### Dashboard Contents

The dashboard provides interactive views of:

| Sheet/View | Description |
|------------|-------------|
| **Summary Statistics** | Total revenue, transactions, quantity, and averages |
| **Item Revenue Analysis** | Revenue breakdown by individual items |
| **Category Distribution** | Percentage split across Drinks, Food, Bakery |
| **Payment Method Breakdown** | Transaction and revenue by payment type |
| **Location Analysis** | Performance by In-store, Takeaway, Other |
| **Monthly Trends** | Revenue and transaction patterns across 2023 |
| **Pivot Tables** | Cross-tabulations for deeper analysis |

### EDA Notebook Highlights

The `EDA_Analysis.ipynb` notebook includes:

1. **Univariate Analysis** - Distribution of numerical and categorical features
2. **Bivariate Analysis** - Correlation matrix and cross-tabulations
3. **Monthly Trends** - Transaction counts and revenue patterns with visualizations
4. **Outlier Detection** - Box plots with IQR method analysis
5. **Cross-Analysis** - Items by location and payment method
6. **Heatmaps** - Monthly revenue by payment method and category

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **Python** | Data processing and analysis |
| **Pandas** | Data manipulation and cleaning |
| **Matplotlib & Seaborn** | Data visualization |
| **Jupyter Notebook** | Interactive analysis environment |
| **Google Sheets** | Dashboard publishing |

---

*This analysis was performed on a cafe sales dataset to identify trends, patterns, and areas for business improvement.*