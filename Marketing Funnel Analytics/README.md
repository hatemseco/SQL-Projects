# Marketing Funnel Analytics (SQLite)

**Author:** Hatem Elgenedy

---

## Project Overview
This project analyzes a marketing funnel using SQLite to understand how users move through the key stages:

**Visit → Signup → Purchase**

The objective is to measure funnel performance, conversion efficiency, and revenue contribution by marketing channel using clean, reusable SQL logic.

---

## Business Questions
- How many users visit, sign up, and purchase?
- What are the conversion rates between funnel stages?
- Which marketing channels generate the most revenue?
- Which KPIs are ready for dashboards?

---

## Dataset
**Table:** `marketing_events`

Each row represents a user interaction within the marketing funnel.

### Key Columns
- `user_id` – unique user identifier  
- `event_date` – date of the event  
- `event_type` – visit, signup, or purchase  
- `channel` – acquisition channel  
- `revenue` – purchase revenue (0 for non-purchase events)

---

## Data Model (Schema)
- **Table**
  - `marketing_events`
- **Views**
  - `v_funnel_kpis`
  - `v_revenue_by_channel`
- **KPI Table**
  - `kpi_summary`

---

## Key KPIs
- Visitors
- Signups
- Purchasers
- Visit → Signup Conversion Rate
- Visit → Purchase Conversion Rate
- Total Revenue
- Revenue by Channel
- Average Order Value (AOV)

---

## SQL Logic
- Common Table Expressions (CTEs) used for funnel calculations
- Aggregations using `COUNT`, `SUM`, and `AVG`
- `NULLIF` used to prevent divide-by-zero errors
- Views created for reuse in BI tools
- KPI summary table designed for dashboards

---

## Tools Used
- SQLite  
- DB Browser for SQLite

---

## How to Run
1. Open the database in **DB Browser for SQLite**
2. Execute `marketing_funnel_project.sql`
3. Run:
   ```sql
   SELECT * FROM kpi_summary;

## Key Takeaway
This project demonstrates how SQL can be used to design a complete analytics workflow—from raw event data to dashboard-ready KPIs—by applying clean schema design, reusable views, and business-focused SQL logic.

