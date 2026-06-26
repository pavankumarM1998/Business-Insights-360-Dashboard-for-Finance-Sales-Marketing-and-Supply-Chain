# AtliQ Hardware - Business Insights 360 (Power BI Dashboard)

[![Live Dashboard](https://img.shields.io/badge/Power%20BI-Interactive%20Report-yellow?style=for-the-badge&logo=powerbi)](https://app.powerbi.com/view?r=eyJrIjoiMjY1ODE4MjQtNGQyNS00ZGI4LWIyMjctNGE2MjAxMjUyZDYyIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)
[![Data Stack](https://img.shields.io/badge/Tech-MySQL%20%7C%20PowerQuery%20%7C%20DAX-blue?style=for-the-badge&logo=mysql)](https://github.com/pavankumarM1998/Business-Insights-360-Dashboard-for-Finance-Sales-Marketing-and-Supply-Chain)

An enterprise-grade, multi-page Power BI analytics dashboard designed to replace legacy Excel reporting for AtliQ Hardwares. This project provides a centralized, 360-degree view of business operations, empowering stakeholders across Finance, Sales, Marketing, Supply Chain, and Executive teams to make data-driven, strategic decisions.

---

## 📌 Problem Statement
AtliQ Hardwares, a rapidly growing consumer electronics manufacturer, faced significant operational friction due to its reliance on scattered Excel files. This decentralization caused:
- **Data Silos:** Teams made decisions based on misaligned data.
- **Reporting Latency:** Preparing monthly reports manually took days.
- **Supply Chain Risks:** Poor visibility into forecast errors resulted in inventory stockouts and excess storage costs.
- **Stifled Expansion:** Leadership lacked granular insights into regional markets and customer segments.

---

## 📊 Dashboard Views & Insights

The report is divided into five specialized views, accessible via a user-friendly sidebar navigation menu:

### 1. 💼 Executive View
*Designed for C-suite executives to monitor high-level corporate performance.*
- **KPIs tracked:** Net Sales, Gross Margin %, Net Profit %, and Market Share %.
- **Key Features:** Revenue progression trends, market share breakdown by sub-zone, and top customer/product rankings.

### 2. 📈 Finance View
*Enables finance analysts to monitor Profit & Loss (P&L) performance.*
- **KPIs tracked:** Net Sales, Gross Margin %, Net Profit %, Gross Margin.
- **Key Features:** Granular P&L Statement matrix showing Net Sales, COGS (Cost of Goods Sold), Gross Margin, and Net Profit across regions, markets, and product segments.

### 3. 🤝 Sales View
*Supports sales directors in identifying high-value customers and growth opportunities.*
- **KPIs tracked:** Net Sales, Gross Margin %, COGS.
- **Key Features:** Customer Performance Matrix (comparing Net Sales and Gross Margin contribution), Product Performance lists, and sales breakdowns by channel (Retail, Direct, Distributor).

### 4. 📣 Marketing View
*Enables marketing teams to analyze product segment performances and ROI.*
- **KPIs tracked:** Net Sales, Gross Margin %, Net Profit %.
- **Key Features:** Segment performance trends (Accessories, Notebooks, Desktops), campaign effectiveness, and regional marketing margins.

### 5. 🚚 Supply Chain View
*Empowers operations teams to optimize inventory and reduce storage overhead.*
- **KPIs tracked:** Forecast Accuracy %, Net Error, Absolute Error.
- **Key Features:** Forecast accuracy vs. actual sales metrics, identify products at risk (out-of-stock vs. over-stock), and customer-level forecasting trends.

---

## ⚙️ Technical Architecture & Data Stack

- **Data Sources:** MySQL (relational database containing sales transactions, manufacturing costs, market data, and targets) and Excel spreadsheets (operational inputs).
- **Data Modeling:** Constructed a **Star Schema** involving 10+ tables (combining dimension tables like `dim_customer`, `dim_product`, `dim_market` and fact tables like `fact_sales_monthly`, `fact_forecast_monthly`, `fact_actuals`).
- **ETL & Power Query:** Cleaned data, removed anomalies, adjusted dates, and established dynamic data-types.
- **Advanced DAX:** Authored optimized calculations, including:
  - **Net Sales:** `Net Sales = [Gross Sales] - [Pre-Invoice Deductions] - [Post-Invoice Deductions]`
  - **Forecast Accuracy:** Measures to calculate forecasting deviations and accuracy percentage.
  - **Target Comparisons:** Interactive metrics tracking actuals vs. targets (YTD/YTG).
- **Optimization:** Utilized **DAX Studio** to run model analyzer metrics, reducing the dashboard's memory footprint by **30%** via column indexing and storage tuning.

---

## 🛠️ How to View the Dashboard

### Option A: Interactive Web Link (Recommended)
You can interact with the fully published, responsive dashboard directly in your web browser:
👉 **[Open Live Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMjY1ODE4MjQtNGQyNS00ZGI4LWIyMjctNGE2MjAxMjUyZDYyIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)**

### Option B: Local Execution
To explore the data model, measures, and visual components locally:
1. Ensure you have **Power BI Desktop** installed.
2. Clone this repository:
   ```bash
   git clone https://github.com/pavankumarM1998/Business-Insights-360-Dashboard-for-Finance-Sales-Marketing-and-Supply-Chain.git
   ```
3. Open the `AtliQ.pbix` file.
