# Coffee Sales Analytics: Interactive Excel Dashboard

[![Excel](https://img.shields.io/badge/Microsoft_Excel-Pivot_Dashboard-217346?style=flat&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/microsoft-365/excel)

---

## Project Overview

* Tools and Technologies: Microsoft Excel (XLOOKUP, INDEX/MATCH, Excel Tables, PivotTables, PivotCharts, Slicers, Timelines)
* Dataset Scope: 1,000 order lines (957 orders) from 913 customers in the United States, Ireland and the United Kingdom, from 2 January 2019 to 19 August 2022.
* Workbook: `coffee-sales.xlsx` with the sheets `orders`, `customers` and `products` plus the dashboard.

---

## Business Problem

A specialty coffee retailer sells four bean types, three roast levels and four bag sizes to customers in three countries. Management cannot easily see where sales come from, how they move over time, or which customers matter most, because the data sits in three separate sheets. This project joins them into one table and presents sales in an interactive dashboard.

---

## Business Questions

| # | Business question | Dashboard view |
|---|---|---|
| 1 | How do sales change month by month, and by coffee type? | Total Sales (line chart) |
| 2 | Which countries generate the most sales? | Sales by Country (bar chart) |
| 3 | Who are the top 5 customers, and how much do they contribute? | Top 5 Customers (bar chart) |
| 4 | Which coffee types, roasts and bag sizes drive sales? | Slicers: Size and Roast Type Name, applied to all three charts |
| 5 | Do loyalty card holders buy more than other customers? | Slicer: Loyalty Card, applied to all three charts |

---

## Key Insights

All figures come from the dashboard's pivot tables and slicers (total sales of $45,134 across the whole period).

1. **The United States generates most of the sales.** It brings in $35,639 (79.0%), against $6,697 (14.8%) for Ireland and $2,799 (6.2%) for the United Kingdom.
2. **The 2.5 kg bag generates over half of the sales.** Applying the Size slicer shows $23,786 (52.7%) for 2.5 kg, $11,011 for 1.0 kg, $7,030 for 0.5 kg and $3,308 for 0.2 kg. Unit volumes are similar across sizes (841 to 943 units), so the gap comes from price per bag.
3. **Sales are spread evenly across coffee types and roasts.** Excelsa ($12,306), Liberica ($12,054) and Arabica ($11,769) are close together, and Robusta is lowest at $9,005. Light roast leads with $17,355 (38.5%), ahead of Medium ($14,601) and Dark ($13,179).
4. **Sales are flat, with no clear seasonal pattern.** Full-year sales were $12,187 in 2019, $12,118 in 2020 and $13,766 in 2021. The best month is February 2020 ($1,798) and the weakest month is August 2022 ($244). 2022 only runs to 19 August, so its $7,063 is a partial year.
5. **The top 5 customers account for only 3.3% of sales.** The leader is Allis Wilmore ($317), followed by Brenn Dundredge ($307), Terri Farra ($289), Nealson Cuttler ($282) and Don Flintiff ($278). No customer dominates the business.
6. **Loyalty card holders do not spend more per order.** Members account for $20,918 (46.3%) of sales, and average sales per order line are $43.67 for members against $46.48 for non-members. Both groups average 1.05 orders per customer.

---

## Recommendations

1. **Focus on the United States and look at why Ireland and the UK are small.** With 79% of sales from one market, check whether pricing, shipping or marketing explains the gap before investing in the other two.
2. **Keep 2.5 kg bags in stock and promote them.** They give 52.7% of sales from about a quarter of units sold.
3. **Review the loyalty programme before expanding it.** Members spend slightly less per order and do not reorder more often than non-members, so test an offer that targets repeat purchases.

---

## Data Preparation

All preparation was done in Excel on the `orders` sheet:

* Customer lookups: name, email and country brought in with `XLOOKUP` on Customer ID. Loyalty card is looked up the same way.
* Product lookups: coffee type, roast type, size and unit price brought in with `INDEX`/`MATCH` on Product ID.
* Label decoding: codes converted to full names (`Ara` to Arabica, `Rob` to Robusta, `Lib` to Liberica, `Exc` to Excelsa; `L`, `M`, `D` to Light, Medium, Dark).
* Sales: calculated as `Unit Price * Quantity`.

---

## Dashboard Design

| Element | Type | What it does |
|---|---|---|
| Total Sales | Line chart | Monthly sales by coffee type |
| Sales by Country | Bar chart | Sales for each country |
| Top 5 Customers | Bar chart | Five customers with the highest sales |
| Size, Roast Type Name, Loyalty Card | Slicers | Filter all three charts at once |
| Order Date | Timeline | Filters all three charts by period |

---

## Data Notes

* **2022 is a partial year.** Orders stop on 19 August 2022, so yearly comparisons with 2022 are not like for like.
* **Sales means revenue, not profit.** The `products` sheet has a `Profit` column, but the dashboard does not use it, so no profit insight is claimed here.
* **Most customers ordered once.** 888 of 913 customers have a single order, so loyalty and repeat-purchase comparisons rest on very few repeat buyers.
* **206 orders have no email address**, which does not affect the sales figures.
* **Prices are in dollars for all three countries**, and no currency conversion is applied.

---

## How to Open

1. Download `coffee-sales.xlsx` and open it in Microsoft Excel 365 or Excel 2021 (the workbook uses `XLOOKUP`, slicers and timelines).
2. Use the slicers and the timeline on the dashboard sheet to filter the charts. After changing source data, use Data > Refresh All.

---

## Repository Contents

| File | Description |
|---|---|
| `coffee-sales.xlsx` | Workbook with the `orders`, `customers` and `products` sheets, three pivot sheets and the dashboard |
| `README.md` | Project documentation |
