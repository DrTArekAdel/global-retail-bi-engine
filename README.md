# Global Retail Business Intelligence Dashboard (Maven Market)

An end-to-end Power BI dashboard built on the Maven Market retail dataset (multi-year transactions across the US, Canada, and Mexico), covering data modeling, DAX measures, and executive-level reporting.

## Objective
Build a star-schema data model and interactive dashboard to track regional sales performance, product/supplier profitability, and customer loyalty tiers for a multinational grocery retailer.

## Tech Stack
Power BI · DAX · Power Query (M) · Python / pandas (data cleaning & duplicate checks) · star-schema data modeling

## Approach
1. **Data modeling** — built a star schema linking transactions, returns, customers, products, stores, regions, and a calendar dimension table.
2. **Python / pandas** — used for an initial pass on the source CSVs to check for duplicate records and inconsistencies before loading into Power Query.
3. **Power Query** — cleaned and shaped seven source CSVs (customers, products, regions, stores, calendar, transactions, returns) before loading.
4. **DAX** — wrote calculated measures for revenue, profit margin, return rate, and year-over-year comparisons.
5. **Dashboard design** — built executive-facing pages for regional performance, supplier/product profitability, and customer loyalty segmentation.

## Key Findings
- The **US market** generated the large majority of total revenue in the dataset; Canada and Mexico (added in 1998) are early-stage by comparison.
- Some high-volume suppliers (e.g. Hermanos) generate large transaction counts and total profit but carry **lower margins and higher return rates** than smaller suppliers like Plato, which post the highest margin in the dataset.
- **Product returns spiked in the final two months of 1998**, warranting a supply-chain/quality investigation.
- **Bronze-tier loyalty customers** drive the highest transaction volume but the lowest average basket size, compared to Golden-tier customers.

## Business Recommendations
- Continue prioritizing the US market for near-term marketing spend while treating Canada/Mexico as growth markets to monitor.
- Evaluate whether high-volume, low-margin suppliers are worth the return-rate trade-off, or whether volume should shift toward higher-margin suppliers.
- Investigate the late-1998 returns spike for a seasonal or logistics root cause.
- Test upgrade incentives to migrate Bronze customers toward higher-tier spending behavior.

## Dashboard Preview
<!-- Add screenshots of your actual dashboard pages here, e.g.:
![Regional Overview](screenshots/overview.png)
![Supplier & Product Analysis](screenshots/suppliers.png)
![Customer Segmentation](screenshots/loyalty.png)
Replace the filenames above with your real screenshot files, or delete this section if you don't have any yet. -->

## Files
- `global-retail-bi-engine.pbix` — Power BI file (model + dashboard)
- `global-retail-bi-engine.ipynb` — Python data-cleaning/duplicate-check notebook
- `MavenMarket_*.csv` — source data ([Maven Analytics: Maven Market dataset](https://mavenanalytics.io/))

## How to Run
Open `global-retail-bi-engine.pbix` in Power BI Desktop (free download from Microsoft). All source CSVs are included for the Power Query steps to refresh.
