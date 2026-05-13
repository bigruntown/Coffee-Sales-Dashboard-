# Coffee Sales Dashboard

An Excel-based sales dashboard analysing 1,000 coffee orders across three countries and four coffee types over a 3.5-year window, with pivot-table aggregations and a top-customers ranking.

## Overview

A foundational Excel analytics project that takes a transactional sales dataset, joins it with reference tables, and builds an interactive dashboard around three core questions:

1. Where are the sales coming from geographically?
2. Which coffee types and roasts are driving revenue?
3. Who are our most valuable customers?

## Tools

- **Microsoft Excel** — pivot tables, XLOOKUP/joins, dashboard layout
- **Power Query** principles for data cleaning
- **Pivot charts** for visualisation

## Dataset

Three normalised sheets joined via Customer ID and Product ID:

- **orders** — 1,000 transactional rows with Order ID, Order Date, Customer ID, Product ID, Quantity, Unit Price, Sales (Jan 2019 — Aug 2022)
- **customers** — 1,001 customers with name, email, phone, address, country, loyalty-card flag
- **products** — 49 product rows mapping each Product ID to Coffee Type (Arabica / Excelsa / Liberica / Robusta), Roast Type (Light / Medium / Dark), Size, Unit Price, Profit

## What the dashboard contains

Built on three supporting pivot sheets that feed the main `Dashboard` view:

- **TotalSales** — monthly sales pivot broken out by coffee type (Arabica, Excelsa, Liberica, Robusta) and year (2019 — 2022)
- **CountryBarChart** — total sales by country, rendered as a horizontal bar
- **Top5Customers** — five highest-spending customers ranked by lifetime sales

## Headline findings

Based on the actual data in this workbook:

| Metric | Value |
|---|---|
| Total orders analysed | 1,000 |
| Unique customers | 913 |
| Total sales | $45,134.26 |
| Date range | Jan 2019 — Aug 2022 |
| **United States share of revenue** | **79%** ($35,638.88) |
| Ireland share of revenue | 15% ($6,696.86) |
| United Kingdom share of revenue | 6% ($2,798.50) |
| Top-selling roast | **Light** ($17,354.46) |
| 2021 sales (best full year) | $13,766.11 |
| Top customer (Allis Wilmore) | $317.07 lifetime |

## Key technical work

- **Cleaned and joined three sheets** — orders, customers, and products — using lookups so the dashboard can slice by attributes that don't live in the transactional table (country, coffee type, roast).
- **Pivot-driven design** — each visual is fed by a dedicated pivot sheet, which keeps the dashboard maintainable; refreshing the orders sheet automatically updates everything.
- **Mix analysis** — separated raw sales totals from share-of-mix to avoid the common mistake of celebrating big absolute numbers without acknowledging concentration risk (79% of revenue from one country is a real concentration risk that this dashboard surfaces).

## Screenshots

![image alt](https://github.com/bigruntown/Coffee-Sales-Dashboard-/blob/main/Screenshot.jpg?raw=true)

## How to view this project

1. Download `Coffe-Sales-Dashboard.xlsx` from this repo.
2. Open it in **Microsoft Excel** (or Excel Online / LibreOffice Calc).
3. The `Dashboard` sheet is the front-end view; the `orders`, `customers`, and `products` sheets carry the underlying data.

---

*Built as part of the Utiva Data Science program (2026).*
