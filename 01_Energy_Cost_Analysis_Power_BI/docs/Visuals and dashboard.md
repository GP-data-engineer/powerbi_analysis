## Visuals and dashboard ##
Create a single report page with these visuals:
  - Line chart – Monthly cost and kWh
  - Axis: MonthStart
  - Line 1: [Total Cost EUR]
  - Line 2: [Total kWh] (secondary axis)
  - Purpose: see cost and consumption trends over time.
  - Line chart – Cost per kWh
  - Axis: MonthStart
  - Values: [Avg Unit Price EUR/kWh]
  - Purpose: detect changes in unit price (e.g. contract renegotiations or anomalies).
  - Bar chart – Cost by Site
  - Axis: SiteName
  - Values: [Total Cost EUR]
  - Purpose: compare plants A and B over the full period.
  - Table – Detailed invoice list
  - Columns: InvoiceDate, SiteName, kWh, TotalCost_EUR, UnitPrice_EUR_kWh, IsEstimated, Notes
  - Apply conditional formatting on UnitPrice_EUR_kWh and kWh to highlight unusually high values (e.g. using a red color for the top 10%).
  - Slicers
  - SiteName
  - Supplier
  - Optional: IsEstimated

## Simple anomaly detection logic ##
Use the visualizations and conditional formatting to identify anomalies such as:
  - Sudden spikes in kWh for a given site and month.
  - Significant jumps in Avg Unit Price EUR/kWh.
  - Months where IsEstimated = "Yes" followed by a correction in the next month.

You can also:
  - Add a card visual with [Invoice Count].
  - Add a matrix by Year-Month and SiteName to see aggregated values and spot spikes.

## Optional extensions ##

To make the project richer, you can additionally:
  - Create a Date table and mark it as a date table.
  - Add measures for:
  - Year-to-date cost
  - Year-to-date kWh
  - Add a tooltip page to show detailed information when hovering over a data point.
  - Export selected visuals as PNG and include them in your CV or portfolio.

This project is intentionally minimal but realistic enough to demonstrate your analytical skills in Power BI.
