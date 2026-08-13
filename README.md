# Payment Processing Data Engineering Pipeline

**An End-to-End AWS Data Lake for Fraud, Dispute, and Compliance Analytics**

A cloud data engineering project that takes raw, multi-source payment data through
an AWS **Medallion (Landing → Clean → Curated)** data lake to governed,
analytics-ready datasets and interactive dashboards — supporting fraud detection,
dispute and refund resolution, and regulatory compliance reporting.

*Course: INSS 661 — Data Engineering, Morgan State University (December 2025)*

---

## Architecture

Built end-to-end on Amazon Web Services:

- **Amazon S3** — three-zone Medallion data lake (Landing / Clean / Curated).
- **AWS Glue** — Glue Studio for ETL and the Glue Data Catalog for cataloging.
- **AWS Lambda** — event-driven triggers that auto-update the Data Catalog as new data lands.
- **Amazon Athena** — serverless SQL querying directly over the curated Parquet tables.
- **Tableau** — visualizations and a consolidated interactive dashboard.

Data flows from raw XLS/CSV sources → converted to Parquet → cleaned and standardized
in Glue → modeled into a star schema → queried in Athena → visualized in Tableau.

## Data Sources

- **PaySim** transaction data (165,577 records with fraud flags)
- **CFPB** consumer complaints (support tickets, disputes, satisfaction)
- Quarterly **financial reports** (revenue, volume, chargeback losses)
- Industry benchmarks (**Federal Reserve**, **Visa PERC**, **Mastercard**)

## Key Findings

- **Fraud:** DEBIT had the highest fraud rate (0.75%); TRANSFER carried the greatest financial exposure ($15,295.91 in losses).
- **Disputes:** Billing disputes were highest-risk for Money Transfer products (13.64%); Credit Cards showed elevated duplicate-charge disputes (12.70%).
- **Compliance:** Visa PERC trends showed enumeration attacks up 25% and account takeover up 20% in 2024, with $760M in fraud prevented in Q4.

## Skills Demonstrated

Cloud data engineering (AWS S3, Glue, Lambda, Athena) · Medallion data-lake architecture ·
ETL and data quality · OLTP (3NF) and OLAP (star schema) data modeling · SQL ·
data governance and lineage (AML / PCI-DSS context) · Tableau dashboards.

## Files

| File | Description |
|------|-------------|
| `INSS661_Project_Portfolio.pdf` | Consolidated project write-up with architecture, findings, and screenshots |
| `INSS661_Final_Report.pdf` | Full detailed project report |

## Team

Group 1 project. All three members contributed across the pipeline:

- **Ayomide Ajibola** 
- **Rofiah Akanni**
- **Ingrid Djoman**

*Course project for INSS 661 — Data Engineering, Morgan State University.*
