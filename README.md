# Indian Companies — Financial Performance & Risk Analytics

An interactive financial analytics project analyzing the **financial performance, profitability, growth, leverage, cash flow, and risk profile of 979 Indian companies**.

The project combines **Python, SQL, Tableau, and an interactive HTML dashboard** to transform raw financial data into decision-ready business insights.

---

## Project Overview

Financial statements contain a large amount of information, but the real challenge is turning that information into insights that can support better business decisions.

This project analyzes Indian companies across key financial dimensions:

* Profitability
* Revenue and profit growth
* Return on Equity (ROE)
* Return on Assets (ROA)
* Debt-to-Equity
* Borrowings
* Operating cash flow
* Cash conversion
* Financial risk
* Growth quality

The final output is an interactive financial intelligence dashboard designed to help users quickly identify **high-performing companies, financially stressed companies, strong growth businesses, and companies requiring further investigation.**

---

## Objectives

The project was built to answer questions such as:

* Which companies generated the highest profits?
* Which companies have strong returns on equity and assets?
* Which companies have high leverage?
* Which companies combine strong growth with healthy profitability?
* Which companies show signs of financial stress?
* How effectively are companies converting accounting performance into operating cash flow?
* How do profitability and leverage vary across companies?

---

## Dataset

**Source:** Indian Company Financial Dataset

The original dataset contains approximately **8,991 company-year observations** covering **999 companies** across multiple financial years.

The final dashboard focuses on the **2026 financial snapshot**, containing:

**979 companies × 23 analytical fields**

Key fields include:

* Company
* Year
* Sales
* Net Profit
* Operating Profit
* ROE
* ROA
* Debt-to-Equity
* Borrowings
* Total Assets
* Cash from Operating Activity
* Operating CF Ratio
* Cash Margin
* Cash-to-Debt
* Revenue Growth
* Profit Growth
* Asset Growth
* Borrowing Growth
* Risk Category
* Growth Category

---

## Data Preparation & Validation

The raw dataset was cleaned and validated using Python in Google Colab.

The process included:

* Missing-value checks
* Duplicate detection
* Company-Year uniqueness validation
* Financial statement consistency checks
* Outlier and anomaly identification
* Ratio validation
* Growth metric validation
* Cash-flow validation
* Financial risk flagging

### Validation highlights

* **8,991** original observations
* **0** missing values after cleaning
* **0** exact duplicate records
* **0** duplicate Company-Year combinations
* Total Assets reconciled against Total Liabilities
* Financial ratios independently validated against underlying financial statement values
* Negative/zero sales observations retained and flagged rather than silently removed

Source-provided metrics that were not independently overwritten were retained for analysis.

---

## Risk Classification

Companies were categorized using predefined financial conditions.

### High Risk

Companies meeting all three conditions:

* Negative Net Profit
* Negative ROE
* Debt-to-Equity greater than 5

### Moderate Risk

Companies meeting at least one of:

* Negative Net Profit
* Negative ROE
* Debt-to-Equity greater than 5

### Healthy

Companies not meeting the above conditions.

### 2026 Distribution

| Risk Category | Companies |
| ------------- | --------: |
| Healthy       |       872 |
| Moderate Risk |       103 |
| High Risk     |         4 |
| **Total**     |   **979** |

> High leverage should be interpreted in context. Financial institutions such as banks naturally operate with higher leverage than many non-financial companies.

---

## Growth Classification

Growth was classified using revenue growth, profit growth, ROE, and ROA.

### Quality Growth

Companies with:

* Revenue Growth > 20%
* Positive Profit Growth
* ROE > 10%
* ROA > 5%

### Revenue Growth Only

Companies with:

* Revenue Growth > 20%

but not meeting the Quality Growth criteria.

### Stable / Low Growth

Companies with:

* Positive Revenue Growth

but below the high-growth threshold.

### Declining

Companies with:

* Revenue Growth ≤ 0%

### 2026 Distribution

| Growth Category     | Companies |
| ------------------- | --------: |
| Quality Growth      |       169 |
| Revenue Growth Only |       146 |
| Stable / Low Growth |       525 |
| Declining           |       139 |
| **Total**           |   **979** |

---

## Key 2026 Insights

### Top companies by Net Profit

| Rank | Company                             | Net Profit |
| ---: | ----------------------------------- | ---------: |
|    1 | State Bank of India                 |  83,298.78 |
|    2 | Tata Motors Passenger Vehicles Ltd  |  82,390.00 |
|    3 | Reliance Industries Ltd             |  80,775.00 |
|    4 | HDFC Bank Ltd                       |  76,025.97 |
|    5 | Life Insurance Corporation of India |  57,453.15 |

### Executive Snapshot

| Metric                      |      2026 |
| --------------------------- | --------: |
| Companies                   |       979 |
| Average Sales               | 18,763.60 |
| Average Net Profit          |  1,966.46 |
| Average ROE                 |    13.16% |
| Average ROA                 |     6.74% |
| Average Debt-to-Equity      |      0.95 |
| Average Operating Cash Flow |  1,848.14 |

---

## Technology Stack

**Data Analysis**

* Python
* Pandas
* NumPy
* Google Colab

**Database & Analysis**

* SQLite
* SQL

**Visualization**

* Tableau
* HTML
* JavaScript
* Interactive charts

**Version Control & Deployment**

* Git
* GitHub
* GitHub Pages

---

## Dashboard

The project includes an interactive dashboard covering four analytical areas:

### 01 — Executive Overview

A high-level view of:

* Financial KPIs
* Top companies
* Risk distribution
* Growth distribution
* ROE vs Debt-to-Equity

### 02 — Company Explorer

Explore an individual company's:

* Revenue
* Profitability
* ROE
* ROA
* Leverage
* Borrowings
* Operating cash flow
* Revenue growth
* Profit growth
* Risk classification
* Growth classification

### 03 — Risk & Financial Health

Analyze:

* Financial risk
* Leverage
* Profitability
* Cash generation
* High-risk companies

### 04 — Growth & Performance

Explore:

* Growth categories
* Revenue vs profit growth
* Quality Growth companies
* Profitability and leverage

---

## Financial Metrics

The project uses several core financial metrics, including:

**Profit Margin**

`Net Profit / Sales`

**ROE**

`Net Profit / (Equity Share Capital + Reserves)`

**ROA**

`Net Profit / Total Assets`

**Debt-to-Equity**

`Borrowings / (Equity Share Capital + Reserves)`

Growth metrics and selected financial ratios were validated against the underlying financial statement data.

---

## Project Structure

```text
indian-company-financial-analytics/
│
├── dashboard/
│   └── index.html
│
├── data/
│   ├── raw/
│   └── cleaned/
│
├── notebooks/
│   └── financial_analysis.ipynb
│
├── sql/
│   └── analysis.sql
│
├── README.md
└── LICENSE
```

---

## Analytical Workflow

```text
Raw Financial Dataset
        ↓
Data Cleaning & Validation
        ↓
Financial Ratio Validation
        ↓
SQL Analysis
        ↓
Risk & Growth Classification
        ↓
Dashboard Dataset
        ↓
Interactive Visualization
        ↓
Financial Insights
```

---

## Important Analytical Notes

* The dashboard uses the **2026 company snapshot** for the primary executive analysis.
* Negative profits are treated as legitimate financial observations rather than automatically classified as data errors.
* Negative and zero sales observations were retained and explicitly flagged.
* High Debt-to-Equity does not automatically imply financial distress, particularly for banks and other highly leveraged financial institutions.
* Risk and Growth categories were defined before dashboard visualization and are not dynamically redefined by the dashboard.

---

## Author

**Iqra Koradia**

Data Analytics | Business Intelligence | Financial Analytics

Interested in building data products that connect **technology, analytics, and business decision-making**.

---

## Project Purpose

This project was created as a portfolio demonstration of:

**Data Cleaning → Financial Analysis → SQL → Business Intelligence → Interactive Visualization**

The goal is not simply to display financial data, but to turn a large financial dataset into a structured analytical product that can support faster and more informed decision-making.

