# LuggaLens - Catalog Operations Analytics
**Amazon IN Luggage | Catalog Analyst Portfolio Project**

![Dashboard](dashboard.png)

## What this project does
End-to-end analytics system simulating the daily workflow of an Amazon 
Catalog Analyst for the IN Luggage category. Covers defect mining, 
listing quality scoring, anomaly detection, and automated reporting.

## Key findings
- **Title too long** is the #1 defect type at 31.6% of all defects
- Anomaly detector flagged 2 spike days (100% above rolling average)
- Quality scoring framework built across 50 luggage ASINs

## SQL queries built
| File | Purpose | Concepts used |
|---|---|---|
| 01_daily_defect_report.sql | Daily defect count by date | SELECT, GROUP BY, WHERE |
| 02_defect_breakdown.sql | Root cause analysis | Subquery, ROUND, ORDER BY |
| 03_quality_score.sql | Listing quality scoring | CASE WHEN, LENGTH, LIKE |
| 04_defect_join.sql | High-risk listing identification | LEFT JOIN, HAVING |
| 05_anomaly_detection.sql | Spike detection | CTE (WITH), Window functions, AVG OVER |

## Tech stack
- MySQL 8.0 — all data mining and reporting queries
- Google Sheets — weekly ops dashboard
- Dataset: Amazon Product Dataset (Kaggle / PromptCloud)

## How to run
1. Run the schema setup in MySQL Workbench
2. Execute queries 01–05 in order
3. Export results as CSV and load into the dashboard sheet
