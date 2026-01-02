# Power BI – Energy Cost Analysis steps


This document describes how to build the Power BI report based on the sample invoice data.


---


## 1. Import data



1\. Open \*\*Power BI Desktop\*\*.

2\. Click \*\*Get Data → Text/CSV\*\*.

3\. Select the file: `data/energy\_invoices.csv`.

4\. Check that:

&nbsp;  - Column separators are recognized correctly (comma),

&nbsp;  - Date columns are detected as \*\*Date\*\*,

&nbsp;  - Numeric columns use a dot (`.`) as decimal separator.

5\. Click \*\*Transform Data\*\* to open \*\*Power Query\*\*.



---



## 2. Data cleaning in Power Query



In Power Query:



1\. Verify data types:

&nbsp;  - `InvoiceDate`, `PeriodStart`, `PeriodEnd` → \*\*Date\*\*

&nbsp;  - `kWh`, `TotalCost\_EUR`, `UnitPrice\_EUR\_kWh` → \*\*Decimal Number\*\*

&nbsp;  - `IsEstimated` → \*\*Text\*\* or \*\*Boolean\*\*

2\. Rename the query to: `Invoices`.

3\. Optional: create a \*\*Month\*\* column:

&nbsp;  - Add Column → Date → Month → Start of Month (based on `InvoiceDate`).

&nbsp;  - Rename to `MonthStart`.

4\. Close \& Apply to load data into the model.



---



## 3. Basic measures



In the \*\*Report\*\* view, create the following measures in the `Invoices` table:



1\. \*\*Total kWh\*\*

&nbsp;  ```DAX

&nbsp;  Total kWh = SUM(Invoices\[kWh])



