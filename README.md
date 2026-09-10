# online-retail-powerbi-dashboard
End-to-end Power BI dashboard analyzing online retail data to answer CEO/CMO business questions.
# 📊 Online Retail — Executive Dashboard (Power BI)

An end-to-end Power BI project that transforms a raw online retail dataset (500K+ transactions) into an interactive executive dashboard, answering the key business questions a CEO and CMO care about.

## 🖼️ Dashboard Preview
<img width="1318" height="742" alt="dashboard" src="https://github.com/user-attachments/assets/9f63bbae-ce59-4a9c-90dc-ff72900b034f" />
## 🎯 Business Questions Answered

1. **Monthly revenue trend for 2011** — identify seasonal patterns to support forecasting
2. **Top 10 countries by revenue & quantity** (excl. UK) — where the business generates the most value abroad
3. **Top 10 customers by revenue** — the high-value accounts to prioritise for retention
4. **Product demand by country** (excl. UK) — geographic opportunities for expansion

## 🛠️ Process

**Data cleaning (Power Query)**
- Removed returns logged as negative quantities (Quantity ≥ 1)
- Removed pricing errors (UnitPrice ≥ 0)
- Validated and corrected data types

**Data modeling**
- Built a dedicated **Date table** using DAX (`CALENDAR`)
- Created a **star-schema relationship** between the Date table and the sales data
- Marked the Date table for time-intelligence support

**DAX measures**
- `Total Revenue = SUMX(Online Retail, Quantity * UnitPrice)`
- `Total Quantity = SUM(Online Retail[Quantity])`

**Visualisation**
- Line chart — monthly revenue trend
- Line & clustered column chart — revenue vs quantity by country
- Clustered bar chart — top 10 customers by revenue
- Map — product demand by country
- Interactive **Country slicer** to filter the entire dashboard

## 🔍 Key Insights
- **Revenue spikes sharply in Q4** — a classic holiday stock-building pattern for a UK gift retailer, with nearly half the year's revenue concentrated in the final quarter.
- **A small group of customers drives a disproportionate share of revenue** — the top account alone generated ~£258K, highlighting the VIP relationships worth protecting.
- **Outside the UK, the Netherlands, Germany, and France show the strongest demand** — the clearest targets for an expansion strategy.
## 📁 Repository Contents

| File | Description |
|------|-------------|
| `OnlineRetail.pbix` | Power BI report file |
| `dashboard.png` | Dashboard preview image |
| `README.md` | Project documentation |

## 🧰 Tools & Skills

`Power BI Desktop` · `Power Query (M)` · `DAX` · `Data Modeling` · `Data Visualization`
*Built as a hands-on analytics project to practise the full BI workflow: cleaning, modeling, DAX, and dashboard design.*

