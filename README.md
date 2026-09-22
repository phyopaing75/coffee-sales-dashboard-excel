## Coffee Sales Analytics and Interactive Excel Dashboard

An end-to-end data analytics portfolio project transforming raw e-commerce coffee transaction logs into an executive-ready, interactive decision dashboard in Microsoft Excel.

---

## Project Overview

Specialty coffee retail relies heavily on customer retention, timely inventory forecasting, and understanding consumer roast preferences across diverse geographical markets.

This project analyzes transactional order logs across multiple years, customers, and product variants to answer key commercial questions:
* Which bean varieties, roast profiles, and bag sizes generate the greatest revenue and profit?
* How does sales volume trend month-over-month and year-over-year?
* What geographic markets yield the highest conversion and customer lifetime spend?
* Does customer enrollment in the loyalty card program produce measurable uplift in purchasing behavior?

---

## Dataset Overview and Attributes

The source workbook (coffee-sales.xlsx) consists of three dedicated sheets containing raw business records: Orders, Customers, and Products.

1. orders (Transaction Records)
This sheet acts as the core activity log, recording individual sales orders placed by customers:
* Order ID: A unique transaction identifier assigned to each purchase.
* Order Date: The calendar date on which the purchase was finalized (used for time-series trend analysis).
* Customer ID: Reference key mapping the transaction back to the individual customer record.
* Product ID: Reference key specifying the exact coffee product purchased.
* Quantity: Number of coffee units or bags purchased in the transaction.

2. customers (Customer Profiles)
This sheet contains demographic and account information for every registered client:
* Customer ID: Unique identification key for each customer.
* Customer Name: Full name of the client or business contact.
* Email Address: Primary communication channel for billing, confirmations, and marketing.
* Phone Number: Customer contact phone number.
* Address Line / City / Postcode: Granular delivery and residence information.
* Country: Geographic market of the customer (United States, United Kingdom, Ireland).
* Loyalty Card: Status (Yes / No) indicating whether the customer is enrolled in the brand loyalty rewards program.

3. products (Product Catalog)
This sheet defines all available inventory items and their core pricing specifications:
* Product ID: Unique SKU identifying the specific combination of bean variety, roast, and package size.
* Coffee Type: Bean species category, including Arabica (Ara), Robusta (Rob), Liberica (Lib), and Excelsa (Exc).
* Roast Type: The degree of bean roasting: Light (L), Medium (M), and Dark (D).
* Size: Packaged weight per unit (0.25 kg, 0.5 kg, 1.0 kg, 2.5 kg).
* Unit Price ($): Retail selling price per unit.
* Profit Margin ($): Profit generated per unit sold.

---

## Data Preparation and Enrichment

Rather than using complex external pipelines, the data was prepared directly inside Excel to build a unified reporting table ready for analysis:
* Customer Integration: Looked up customer details (name, email, country) into the main orders table using primary customer keys.
* Product Catalog Mapping: Matched product identifiers against the catalog to bring in unit prices, packaging sizes, bean categories, and roast types.
* Data Decoding and Standardization: Converted shorthand codes for coffee varieties (Ara, Rob, etc.) and roasts (L, M, D) into human-readable full names for chart readability.
* Financial Calculations: Derived line-item gross sales by multiplying unit price by quantity ordered.

---

## Interactive Dashboard Highlights

The primary deliverable is an executive dashboard powered by synchronized Pivot Tables and Pivot Charts:
* Sales Trend Over Time: Monthly and quarterly timeline line chart identifying seasonal peaks, dips, and annual growth trajectory.
* Revenue by Country: Ranked bar chart comparing international performance across the United States, United Kingdom, and Ireland.
* Top 5 Customers: Horizontal bar chart tracking key VIP accounts contributing an outsized share of revenue.
* Roast and Variety Share: Composition charts illustrating customer demand across roast levels and bean origins.

---

## Interactive Control Elements

* Timeline Slicer: Interactively filters all connected pivot charts across Year, Quarter, or Month.
* Geographic Slicer: One-click filtering across target sales countries.
* Loyalty Status Filter: Toggle views between loyalty members and non-members.
* Roast Level Slicer: Instant segmentation across Light, Medium, and Dark roasts.

---

## Key Business Findings

* Primary Revenue Driver: The United States constitutes the largest volume of sales, with recurring clusters of high-frequency buyers in the UK and Ireland.
* Preferred Bean Profile: Arabica and Liberica beans across Medium Roast consistently lead both unit volume and overall gross revenue.
* Package Preference: The 0.5 kg and 1.0 kg sizes show the fastest stock rotation. Bulk 2.5 kg units are driven by a concentrated subset of repeat B2B and high-consumption buyers.
* Loyalty Membership Lift: Enrolled loyalty members exhibit higher average order counts per year compared to non-cardholders, confirming the program's value in stabilizing baseline recurring revenue.

---

## Commercial Recommendations

* Loyalty Onboarding Funnels: Target first-time buyers in the US and UK with an immediate sign-up incentive (such as 10% off subsequent orders) to increase the conversion rate of non-loyalty customers.
* Safety Stock Replenishment: Focus warehouse reorder points on 0.5 kg and 1.0 kg Medium Roast Arabica SKUs to avoid lost sales during quarter-end spikes.
* VIP Client Outreach: Institute direct VIP incentives (free sample roasts or seasonal previews) for the top 5 to 10 account holders to protect high-margin volume.

## Technical Competencies Demonstrated

* Data Modeling and Manipulation: Excel Tables, Data Cleaning, Reference Lookups, Categorical Mapping.
* Data Visualization: Pivot Tables, Pivot Charts, Timeline Controls, Interactive Slicers, UI Canvas Design.
