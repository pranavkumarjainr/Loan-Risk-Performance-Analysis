# Bank Loan Risk & Performance Analysis

## Project Overview
This project simulates a **Forward Flow** monitoring process, where a Business Analyst is responsible for tracking the performance, credit risk, and repayment trends of a purchased loan portfolio.

Using **SQL** for data processing and **Power BI** for visualization, this solution provides a 360-degree view of lending operations—from high-level cash flow metrics to granular, loan-level audits. The dashboard is designed to help stakeholders identify "Bad Loan" risks, optimize capital deployment, and perform ad hoc analysis on borrower demographics.

## Tech Stack
* **Database:** SQL (Data extraction, cleaning, and KPI calculation)
* **Visualization:** Power BI (Interactive dashboards, Bookmarks, Navigation)
* **Logic:** DAX (Time-series analysis, sophisticated measures)
* **Data Quality:** Excel (Initial data profiling)

## Business Problem & Solution
**The Challenge:** A financial institution needs to monitor a portfolio of 38,000+ loans to ensure that the "Forward Flow" agreement is profitable. They need to instantly see the ratio of **Funded Amounts** (Outflow) vs. **Received Amounts** (Inflow) and identify segments with high default rates.

**The Solution:** A three-page Power BI report providing:
1.  **Executive Summary:** Real-time visibility into "Good" vs. "Bad" loans.
2.  **Strategic Overview:** Analysis of seasonality, borrower stability, and regional trends.
3.  **Operational Details:** A grid view for auditing specific loan IDs and conducting ad hoc investigations.

---

## Dashboard Features

### 1. Summary Dashboard (Portfolio Health)
*Focus: Immediate Risk & Cash Flow Assessment*
* **Cash Flow Monitoring:** Tracks **$435.8M** in Total Funded Amounts against **$473.1M** in Total Received Amounts to ensure portfolio profitability.
* **Risk Segmentation:** Visualizes the "Good Loan" vs. "Bad Loan" ratio (13.8% Default Rate), enabling the risk team to isolate underperforming assets.
* **Key Metrics:**
    * **Average DTI (13.3%):** Monitors borrower debt load.
    * **Average Interest Rate (12.0%):** Tracks portfolio yield.
    * **MoM (Month-over-Month) Growth:** Indicators for funded amounts and applications.

### 2. Overview Dashboard (Trends & Demographics)
*Focus: Strategic Planning & Capital Deployment*
* **Seasonality Trends:** A line chart analyzing "Total Funded Amount by Month" to predict peak lending periods and manage liquidity.
* **Risk Factors Analysis:**
    * **Home Ownership:** Correlates asset ownership (Rent vs. Mortgage) with loan size.
    * **Loan Purpose:** Breaks down capital usage (e.g., Debt Consolidation vs. Small Business).
    * **Regional Disparities:** A geospatial map identifying high-demand states.

### 3. Details Dashboard (Audit & Ad Hoc Analysis)
*Focus: Operational Validation*
* **Granular Reporting:** A responsive grid view offering row-level data for all 38k+ loans.
* **Ad Hoc Capabilities:** Allows analysts to filter by `Grade`, `Sub-Grade`, and `Verification Status` to investigate specific loan tranches or validate data quality.

---

## SQL Analysis (Data Engineering)
Before visualization, **SQL** was used to clean the data and validate key metrics.
* *Calculated "Bad Loan" Percentage directly in the database to verify Power BI results.*
* *Grouped data by `Loan Status` to ensure `Funded Amount` totals matched the General Ledger.*
* *Standardized date formats for accurate MoM calculation.*

---

## Getting Started

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/pranavkumarjainr/Bank-Loan-Analysis.git](https://github.com/pranavkumarjainr/Bank-Loan-Analysis.git)
    ```
2.  **Data Setup:**
    * Import the raw dataset (`bank_loan_data.csv`) into your SQL Server/Database.
    * Run the queries located in the `/SQL_Queries` folder to verify the KPIs.
3.  **Run the Dashboard:**
    * Open `Bank_Loan_Report.pbix` in Power BI Desktop.
    * (Optional) Update the data source settings to point to your local SQL instance.

## Dashboard Screenshots

### Summary View
![Summary Dashboard](Output/Summary.png)

### Overview View
![Overview Dashboard](Output/Overview.png)

### Details Grid
![Details Dashboard](Output/Details.png)
