# SuperStore Sales Analysis (Power BI)

A sales and profitability analysis of a retail superstore's order data, built in Power BI. This one's more on the BI/dashboarding side — no SQL or ML here, just digging into the data and turning it into something a business stakeholder could actually use to make decisions.

## Why I built this

Sales data on its own doesn't tell you much until you break it down — which regions are actually profitable, which categories are dragging margins down, which customer segments matter most. I wanted a project that showed I can take a raw transactional dataset and turn it into a dashboard that answers real business questions, not just pretty charts.

## Tools used

- Power BI – data modeling, DAX measures, dashboard/report building
- Excel – source dataset

## The data

Order-level sales data for a superstore, covering **Jan 2019 – Dec 2020**. About **5,900 order line items**, with:

- Order info: order ID, order date, ship date, ship mode, payment mode
- Customer info: customer ID, name, segment (Consumer / Corporate / Home Office)
- Location: country, city, state, region (Central / East / South / West)
- Product info: product ID, category (Furniture / Office Supplies / Technology), sub-category, product name
- Numbers: sales, quantity, profit, and whether the order was returned

Total sales across the dataset come out to a little over **$1.56M**, with about **$175K** in profit — so a blended margin of roughly 11%, though that varies a lot by category (more on that below).

## What I did in Power BI

- Loaded and modeled the SuperStore dataset, set up relationships and a date table for time intelligence
- Built out core DAX measures — total sales, total profit, profit margin %, order count, and a few YoY comparisons
- Built dashboard pages covering:
  - **Sales overview** – overall sales/profit trend over time, by month and by year
  - **Category & sub-category breakdown** – which products are actually profitable vs. which just generate revenue
  - **Regional performance** – sales and profit by region/state, since some regions clearly outperform others
  - **Customer segment view** – how Consumer, Corporate, and Home Office segments compare
  - **Returns** – a look at returned orders and which categories/regions see the most of them

(I'll drop 2-3 screenshots of the actual dashboard pages in here once I export them — `images/overview.png`, `images/category_breakdown.png`, etc. Also going to double check the exact page names/titles I used in the .pbix match what I wrote above before uploading.)

## A few things I noticed

- Furniture (especially Bookcases and Tables) tends to have thin or even negative margins compared to Technology, even though it brings in solid revenue — worth flagging since revenue alone would make it look like a strong category.
- (Add your actual regional/segment findings here once you've gone through the dashboard closely — e.g. which region has the best margin, or how returns cluster by category.)

## Files in this repo

```
SuperStore_Sales.pbix
SuperStore_Sales_DataSet.xlsx
images/                    (dashboard screenshots)
```

## Running it yourself

1. Open `SuperStore_Sales.pbix` in Power BI Desktop.
2. If it prompts for the data source, point it to `SuperStore_Sales_DataSet.xlsx`.
3. Refresh the data if needed and explore the report pages.

---
[Your Name] · [email / LinkedIn]
